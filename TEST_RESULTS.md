# Verification results — 2026-10-11 KST

Environment: Apple Silicon / macOS 15.8.1 / Apple Swift 6.1.2 / macOS SDK 15.5 / one display. Xcode.app is not installed; project/plist syntax was validated and direct Swift builds were executed.

- CoreChecks: **83 passed**, covering geometry, bounds/finite values, focus pause/resume/serialization/once-only completion, queue cooldown/priority/capacity, clock rollback, schedules/midnight/DST, corruption recovery and custom colors. Commerce checks cover trial expiry/rollback, paid offline cache, old-schema migration, valid/product-mismatched/refunded/chargebacked/disputed responses and transient API failure.
- Free/Pro AppKit integration: **PASS**. Free rejects Pro selection and imported Pro themes; explicit trial unlocks Pro and exact app-profile matching works.
- Actual AppKit integration: **PASS**. Clear non-key click-through windows, status icon, breathing, duplicate merging, full animation cancellation, Reduce Motion and Low Power substitutes, transient cleanup, timer completion once, disabled display suppression, menu popover.
- Raster integration: **PASS**, center alpha = 0, maximum alpha = 152/255 at configured maximum intensity. Interior remains transparent and final opacity stays below 0.6.
- Universal compilation: arm64 + x86_64, both Mach-O minimum OS = 13.0, SDK = 15.5. Final rebuild is required after any source change.
- Native UI: onboarding, Afterglow selection, start/pause/reset focus, normal quit, reopening settings using Command+, paused focus preserved at 23:38, Korean/English switches checked with actual UI automation. Finder file selection worked while the M0 overlay was active.
- Gumroad seller test purchase: **PASS** (no charge). Issued key activated Pro in the actual app, allowed a Pro theme, survived quit/relaunch in Keychain, and local deactivation returned to Free. License recheck also completed. The test key was removed from this Mac afterward; no key was written to source or documentation.
- Delivery: **PASS**. The Gumroad buyer download matches the packaged DMG SHA-256, and GitHub reports the same asset digest: `03c13c8d8f2786cb9b058c7fe00918cd590e14cf92ad3b3ae22f1b29f4ee6813`.
- Code signing: local ad-hoc signature only. No Developer ID identities are available on this Mac. Notarization/Gatekeeper clean-Mac acceptance was not performed.

The expanded animation-counter integration check initially caught implicit animations while transient layers were being removed. Shutdown/cancellation now disable implicit actions and recursively remove all animation keys; the expanded check passes.

Pending: Xcode project build in full Xcode; physical multi-monitor/hotplug/rotation and mixed-density validation; Safari/Finder drag matrix; macOS 13/Intel and other OS runtime tests; sleep/lock/Spaces/Stage Manager matrix; SMAppService registration/approval test; sustained CPU/GPU/energy/memory measurements; clean-Mac signed/notarized install; battery cable transition; Sparkle.

M0/M1/M2 implementation checks do not certify every manual acceptance gate. Public artifacts are labelled Early Access, with ad-hoc signing and pending checks disclosed. Gumroad activation was verified using a seller test-purchase key; no real-money buyer transaction was performed.
