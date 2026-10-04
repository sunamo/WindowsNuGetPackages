---
schema_version: 7
type: my-library
file_count: 36
avg_lines_per_file: 21
move_to_legacy_percent: 3
generated_date: 2026-10-01
generated_time: 16:40:24
github_source_url: 
last_build_ok: yes
last_build_date: 2026-10-02
last_tests_run_date: 2026-10-02
covered_lines: 0
total_lines: 5989
---

## Description

Sbírkové repo NuGet balíčků pro vývoj Windows aplikací (WPF, WinForms, UWP) — 25 submodulů typu SunamoWpf.*, SunamoWf.*, SunamoLogMessage, SunamoBitLockerManager a SunamoYouTube.Uwp. Samotné repo obsahuje jen ukazatele na submoduly, slnx, Taskfile a dokumentaci (REPOS.md).

## Původ zdrojáků

Staženo z GitHubu: **ne** — vlastní sbírka balíčků, sama je publikovaná v účtu sunamo.

- Ověřeno: origin je github.com/sunamo/WindowsNuGetPackages, historie od 2025-03-16, autoři smutekutek, Radek Jančík a sunamo.cz (vlastní účty), obsah tvoří submoduly z účtu sunamo; gh search neprováděn, původ je zjevně vlastní.

## Doporučení přesunu do legacy

Doporučení přesunu do sunamocz-legacy.visualstudio.com: **3 %** — sbírka všech Windows balíčků, aktivně udržovaná (poslední commit 2026-09-30).

- Rodič drží ukazatele na 25 submodulů, které se publikují na NuGet.
- Smazáním by se ztratila vazba na všechny submoduly.

## Vazby na moje repa

- Submoduly: `SunamoBitLockerManager`, `SunamoLogMessage`, `SunamoWf.Controls`, `SunamoWf.Converters`, `SunamoWf.Extensions`, `SunamoWf.Helpers`, `SunamoWf.Tray`, `SunamoWpf.AwesomeFont`, `SunamoWpf.Cef`, `SunamoWpf.Controls`, `SunamoWpf.Converters`, `SunamoWpf.Core`, `SunamoWpf.Data`, `SunamoWpf.Extensions`, `SunamoWpf.Helpers`, `SunamoWpf.Logging`, `SunamoWpf.Mvvm`, `SunamoWpf.RegistryWin`, `SunamoWpf.Storage`, `SunamoWpf.SunamoUtils`, `SunamoWpf.ToggleSwitch`, `SunamoWpf.TreeView`, `SunamoWpf.Web3`, `SunamoWpf.Windows`, `SunamoYouTube.Uwp`
- ProjectReference / PackageReference: žádné
