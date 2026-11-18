# Changelog

## 2.1.0 - 2026-11-18

### Changed
- `semi` range `^0.24.0` -> `">=0.26.0 <1.0.0"`: the kit covers @semi/ui v0.26 and every later 0.x minor, so `/semi-sync` can install v0.26.1, v0.27.0 and later in apps of this brand (hoanghuynh296/semi-brand#1). Plugins older than v0.27.0 do not parse this form and read it as uncapped; that is safe because no 1.x tag exists.
- Dev dependency on @semi/ui is now v0.27.0 (its validator accepts the wide range); generated files rebuilt (only the @semi/ui version stamp and `semi` change).
- `next` (site preview dev dependency) 16.4.3 -> 16.4.6, fixing the Next.js security advisories that failed the site build.
- No colour, font, logo or voice change. @semi/ui 0.25.0 to 0.26.1 changes (BootLoader, shell lint rules, FileDrop, fixes) need nothing in a brand kit.
