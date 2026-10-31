# SCP:SL CE12 Lighting
Public standalone reversible lighting mod for CE12.0.2/Unity6000.3/Built-in. Canonical patch-only source; never add full game, DLL, local secrets or user projects. Manager namespace/state/backups are separate from character mods. Only ProjectSettings/QualitySettings.asset is allowed outside Assets/Translations.

## Status
2026-10-31: extracted accepted .35/.50 ambient, shadow defaults/native menu/pixel count and AO fixes. Source main and protected clean are read-only. Actual clean-copy Unity QA and publication pending; full project backups only PRIVATE and separate.

2026-10-31 QA passed:47engine checks,27nativeAPI+12preset/undo gates, actual4component selections/manualedit/nativewindow controller/restoration/reinstall,0CSharp. QualitySettings cache synchronized; only that YAML tolerates BOM/EOL normalization, realvalue edits blocked. Source main/clean unchanged. Public Preview publication next; no new EXE/FPS/fullFacility run.

2026-10-31 published:public https://github.com/Havermeng/scpsl-ce12-lighting/releases/tag/lighting-v1.0.0-preview.1, source2e231d1, package21733bytes/SHA0a19f4c94688195a9b6093629e293a4d0cdae557334852c6dd84e2b0a4bf67cf. Anonymous package/checksum downloads exact; LinuxCI41156939204+41156874462SUCCESS and byte-identical build. Actual47engine/27nativeAPI/12cache-roundtrip/4selection checksPASS. All ownQAinstallerAssets removed; source3bytes+qualityvalues restored, ownQA29964closed, then only ownedQA preset EOLlayout restored from original archive. Main4sourceSHAexact; clean untouched. Fullprojectuploads are separate PRIVATE-only snapshot task, never this public repo.
