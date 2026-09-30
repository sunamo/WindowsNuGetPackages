# P instrukce — WindowsNuGetPackages

## Balíčky jsou FLAT a všechny se jmenují `Sunamo*` (uživatel 2026-09-30, ABSOLUTNÍ)

- Žádný balíček (submodul) v tomhle repu nesmí referencovat jiný balíček z pinp/wnp — ani `ProjectReference`, ani `PackageReference` (včetně `.Net48` variant a napříč pinp↔wnp). Povolené jsou jen cizí balíčky z nuget.org.
- Výjimka: `Runner*` balíčky a `*.Tests` projekty smějí referencovat ostatní pinp/wnp balíčky.
- Název každého balíčku/repa/projektu/`PackageId` musí začínat `Sunamo` (výjimka `Runner*`). Bez prefixu = přejmenovat (včetně remote a `.gitmodules`).
- Potřebný kód z jiného balíčku se zkopíruje do balíčku (preferovaně `internal`), případně se příbuzné balíčky sloučí — nikdy nová reference mezi balíčky.
- Před commitem/`ptgan` zkontroluj `.csproj` na reference na jiné pinp/wnp balíčky a na chybějící prefix `Sunamo`.
- Plné znění: G (`C:\Users\aktiv\.claude\CLAUDE.md`), sekce „pinp/wnp balíčky jsou FLAT".
