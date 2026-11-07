# Apollon Comic Reader 1.0

First release under the Apollon Comic Reader name, adapted from the supplied Inkframe 1.3 preview build.

## Changes

- New launcher label, About text, export folder branding, version name `1.0`, version code `1`, and application ID `com.apollon.comicreader`.
- Total-page-count sorting in both directions for library groups/folders and individual comics.
- Panel-view background rendering supports page-edge color, blurred art, black, white, and custom color.
- New **Join speech-bubble panels** sensitivity option, between **Eager** and **Find every panel**; works with adjoining side-by-side or stacked frames.
- Contextual image export: **Save panel** in panel view and **Save page** in ordinary page view. Panel export produces a PNG crop at the original image's resolution. Whole-page preview cannot silently export a full page as a panel.
- Reader menu information card with cover, title, page information, synopsis, metadata/credits, and a current-time clock.
- Information card lifecycle cleanup on reader disposal and app pause.

## Development note

**Built through vibe coding:** the app and these changes were developed through natural-language direction of AI coding tools and iterative generated-code updates. Bugs are possible; clear reproduction reports are welcome.

## Compatibility

- Android 8.0 or later (minimum API 26); target API 35.
- Native libraries for ARM64, ARMv7, x86, and x86-64 are retained.
- Apollon installs alongside Inkframe/Inkframe Preview. Re-add your folders and configure settings/API keys in Apollon; earlier apps' private data is not migrated.
- Keep the new release signing key private and retain it for future updates. The old disposable preview key is not used for this release.

## Verification and limits

Automated checks cover page-count ordering, sensitivity labels, crop coordinates, image-based speech-bubble joining, and injected app-member references. The actual user-supplied example page is used locally as a fixture and is not included in the public materials.

The APK's manifest/application label, version, signing certificate, ZIP alignment, and archive contents are checked during release preparation. See `VALIDATION.md` for the final recorded results.

**Not yet verified on an Android device:** reader-card layout, native Canvas rendering, real gestures/buttons, installation, and frame rate. Detection is heuristic and may need tuning for unusual artwork. This build should be treated as a first release candidate until those checks are completed.

## Rebuild materials

The kit contains decoded resources and smali plus Java patch additions, rather than the original Kotlin/Gradle project. Compilation-only stubs must never be packaged as application classes. Public materials exclude private signing keys and credentials. The kit does not include comic pages or sample comic books.
