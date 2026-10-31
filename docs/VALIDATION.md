# Validation — 2026-10-31

## Current package acceptance

**Preview, verified in an isolated CE12.0.2 copy / Windows / Unity6000.3.3f1 / Built-in.** The original main project and the user's clean project were not modified.

- 47 transactional-engine checks passed: BOM/CRLF exact restoration, composition, independent selection, rollback/recovery, manual-edit protection, GUID handling, payload tampering, strict target paths and safe mod IDs. Outside Assets/Translations, only ProjectSettings/QualitySettings.asset is allowed; internal state and other project settings are rejected.
- Actual Unity import and compilation passed with zero C# errors. First import installed the package. All four component selections (core, +shadows, +AO, both) produced the expected normalized hashes for all four targets. Actual hidden editor-window selection controller, manual-edit conflict guard, four-file uninstall and reinstall passed. C# restores byte-exactly; Unity may normalize only line endings/BOM in its own QualitySettings YAML. Original bytes remain in backups.
- 27 native API checks passed in the editor: LCZ/HCZ/EZ/surface/fallback fill, native unlit option, AO0/1/2 and unchanged radius/intensity, saved/default shadow policy, actual menu shadow application and five pixel-light boundary cases. Native preset cache synchronization and a quality-only line-ending normalization guard were added: actual quality value edits still block removal, while Unity formatting does not. Preference modifications were memory-only in an isolated QA registry; memory, registry file and preset file were restored exactly.
- 12 additional native preset/undo gates passed across real Unity recompilation: line normalization accepted, value edits blocked, all cached presets disabled/restored, active shadow value restored, original targets restored, automatic reinstall and subsequent uninstall valid.
- Package boundaries: sparse patches only; no whole vanilla file, game DLL/EXE, scene, texture, voice or network/authentication payload. Publication lint passed without failures/warnings. Target paths do not overlap the published character packages, and installer namespace/state/backups are separate.

## Scope and limitations

This extracts the accepted 2026-10-25/26 Built-in lighting changes. Earlier integrated-project acceptance covered actual native blackouts/relight, settings controls and same-map room surveys across LCZ/HCZ/EZ/surface. The image in README is from that earlier run. Those historical checks are not a new full gameplay run of this package. The fresh package checks above are native API/installer checks in Edit Mode; no new standalone player, independent peer, full fresh Facility route or FPS/power result is claimed.

Exact HDRP parity is not claimed. Existing saved preferences take priority; the package does not rewrite the user's shared registry. Graphics-preset refresh can require an editor restart. Scene profiles, fog, emission, material brightness and brightness slider behavior remain unchanged.

During package development Unity temporarily retained an older compiled installer despite changed source; a clean C# recompilation resolved this and actual loaded code was verified before the passing tests. This was fixed and verified before release; the published installer accepts the lighting manifest.
