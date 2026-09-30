# P instrukce — WindowsNuGetPackages

## Balíčky jsou FLAT a všechny se jmenují `Sunamo*` (uživatel 2026-09-30, ABSOLUTNÍ)

- Žádný balíček (submodul) v tomhle repu nesmí referencovat jiný balíček z pinp/wnp — ani `ProjectReference`, ani `PackageReference` (včetně `.Net48` variant a napříč pinp↔wnp). Povolené jsou jen cizí balíčky z nuget.org.
- Výjimka: `Runner*` balíčky a `*.Tests` projekty smějí referencovat ostatní pinp/wnp balíčky.
- Název každého balíčku/repa/projektu/`PackageId` musí začínat `Sunamo` (výjimka `Runner*`). Bez prefixu = přejmenovat (včetně remote a `.gitmodules`).
- Potřebný kód z jiného balíčku se zkopíruje do balíčku (preferovaně `internal`), případně se příbuzné balíčky sloučí — nikdy nová reference mezi balíčky.
- Před commitem/`ptgan` zkontroluj `.csproj` na reference na jiné pinp/wnp balíčky a na chybějící prefix `Sunamo`.
- Plné znění: G (`C:\Users\aktiv\.claude\CLAUDE.md`), sekce „pinp/wnp balíčky jsou FLAT".

- **Kam se kopíruje chybějící kód (uživatel 2026-09-30, ABSOLUTNÍ):** místo reference na jiný balíček se to, co chybí, dává do složky `_sunamo\<NázevDárce>\` v balíčku (jako už je v mnoha balíčcích, např. `SunamoPS\_sunamo\SHJoin.cs`). Ne do `Internal\`, ne celé balíčky.
  - **S citem, bez zbytečného kódu:** kopíruj jen členy (metody/třídy), které balíček skutečně používá, ne celé soubory ani celé pomocné třídy (`SH`, `CA`, `FS`, `TF` apod.) kvůli jedné metodě. Nepoužitý kód smaž.
  - Třídy jsou `internal`, namespace `<Balíček>._sunamo` (případně `._sunamo.<Dárce>`), každá metoda má dokumentaci (`///`).
  - Typ vystavený veřejným API balíčku nejde `internal` — tam je výjimka: sloučení příbuzných balíčků (např. `SunamoWpf.*` do `SunamoWpf.Core`) nebo veřejný typ v `_sunamo`, podle konkrétního případu.
  - Balíček nesmí záviset na externím balíčku `Sunamo*` mimo pinp/wnp (např. `SunamoImageSharp`) — i ten se nahrazuje kódem v `_sunamo` nebo přímo nuget.org balíčkem.

## Verze po `ptgan` se zapisuje do gitu přes `Sync-PublishedVersions.ps1` (uživatel 2026-09-30, ABSOLUTNÍ)

`ptgan` spuštěný v čistém non-worktree checkoutu (mass mode) přeskočí git kroky (`noChanges`), takže bump `<Version>` zůstane necommitnutý a zahodí se. `master` je navíc chráněný PR, přímý push by stejně selhal.

- Po každé publikaci přes `ptgan` spusť: `pwsh -NoProfile -File E:\vs\Scripts_Projects\PowershellScripts-claude\Sync-PublishedVersions.ps1 -Parent <pinp|wnp> [-Only <Balíček>] -Apply`.
- Skript v `-claude` submodulu (větev `claude`) porovná `<Version>` v csproj s NuGetem, zapíše publikovanou verzi, commitne, pushne a otevře PR `claude`→`master` (squash).
- Bez `-Apply` jen vypíše rozdíly (dry-run).
- Poté v `-claude` rodiči posuň ukazatele submodulů na `origin/master` submodulu (PR `claude`→`master`) a fast-forwardni hlavní checkout.
- `ptgan` se kvůli tomu neupravuje.
