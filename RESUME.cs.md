---
schema_version: 11
type: real-app
category_override: none
file_count: 36
file_extensions: noext:5, md:4, controls:2, converters:2, extensions:2, helpers:2, awesomefont:1, cef:1, core:1, data:1, logging:1, mvvm:1, registrywin:1, slnx:1, storage:1, sunamoutils:1, toggleswitch:1, tray:1, treeview:1, uwp:1, web3:1, windows:1, yml:1
file_extensions_updated: 2026-10-04
avg_lines_per_file: 21
total_lines: 5989
metrics_lm: 2026-10-01 16:40:24
move_to_legacy_percent: 3
description_updated: 2026-10-01
links_updated: 2026-10-01
github_source_url: not found
origin_status: found
origin_checked: 2026-10-01
article_source_url: not run
article_status: pending
article_checked: not run
last_build_ok: yes
last_build_date: 2026-10-02
last_tests_run_date: 2026-10-02
covered_lines: 0
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
