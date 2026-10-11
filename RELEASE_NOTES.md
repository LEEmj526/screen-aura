# Screen Aura 0.3.0 — Development Preview

Initial native macOS MVP with two free presets, customizable edge lighting, focus timer, per-display preferences, scheduling and Korean/English settings.

The Universal binary contains arm64 and x86_64 slices targeting macOS 13. Built using Apple Swift 6.1.2 and the macOS 15.5 SDK. The 60 core checks and AppKit integration checks passed on macOS 15.8.1 Apple Silicon. Raster verification confirmed a fully transparent center and maximum alpha 152/255. Animation cleanup, timer completion deduplication and paused-timer restart restoration were verified.

This is an ad-hoc signed development build. Developer ID signing, notarization and clean-Mac installation verification are not complete. Physical multi-display, Intel runtime and the broader manual compatibility matrix remain pending. Pro commerce/license/trial, battery signals, automatic app profiles and automatic updates are not included. Gumroad sales are on hold pending the paid Pro release.

Assets: Universal DMG and its SHA-256 checksum. Source is kept in the private source repository.
