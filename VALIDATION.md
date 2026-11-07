# Apollon Comic Reader 1.0 — Validation record

Prepared November 7, 2026.

## Passed

- **12 geometry/image checks:** source-resolution crop coordinates, clamping, nonempty edge crops, page-count arithmetic and overflow, ordinary-divider rejection, white-blank-page rejection, adjoining speech-balloon joins in horizontal and vertical arrangements, empty/single-panel handling, and the supplied reference image.
- **10 application-logic checks:** ascending/descending folder totals, stable tie ordering, preservation of original lists and existing sort choices, individual-comic page-count sorting, and all three sensitivity labels around the inserted mode.
- **432 injected application-member references** resolved against the decoded app, including references from original classes into the patch helpers.
- Java additions compiled and converted to Android bytecode with minimum API 26. Compilation-only stubs were excluded from the shipped classes.
- Combined bytecode assembled successfully as **DEX 038**, matching the input app's DEX generation and Android 8 minimum. DEX integrity checks are also recorded during final archive validation.
- Package inspection reports label **Apollon Comic Reader**, application ID `com.apollon.comicreader`, version name **1.0**, version code **1**, minimum SDK **26**, and target SDK **35**.
- Retained ARM64, ARMv7, x86, and x86-64 libraries.
- Final APK verified with Android `apksigner`: **APK Signature Scheme v2 and v3**, one RSA 4096-bit release signer.
- Stored APK entries aligned to four-byte boundaries; native libraries aligned to **16 KiB** boundaries.
- Private signing files are excluded from the APK and public archives.

Release certificate SHA-256:

```text
ffc1a885d92414922a2e56339084e443e4046be3390b6db1d49e74893dc44173
```

## Scope of the tests

Host-side Android mocks are used only to load and test the pure sorting/label logic. They do not simulate Android views, Canvas, touch, storage permissions, or installation.

The comic image fixture tests the balloon-bridge/merge stage with the two expected frame rectangles. It is not an end-to-end, on-device test of the original panel detector. The image is kept outside the public rebuild kit.

## Still needs a real Android device

- Fresh installation and launch.
- Opening representative CBZ, CBR/RAR5, CB7, CBT, and PDF files.
- Reader-card layout on portrait/landscape screens, long summaries, and absent metadata.
- Center/menu-zone tapping and reader close/pause/resume cleanup.
- Each panel-fill mode, masking choice, transition style, and manual zoom.
- Panel export, permission handling, output dimensions, and file contents.
- Speech-balloon mode on a varied collection of artwork.
- Real frame-rate, battery, memory, and remote/controller behavior.

## Build route

The Windows-native resource compiler and ZIP-writing alignment tool crashed in this environment. The final build therefore preserves the input APK's compiled resources, changes the existing string pools and manifest identity without moving resource IDs, assembles patched bytecode, and uses a checked Python alignment step before Android's Java signer. This route is included in the rebuild materials.

The supplied materials do not contain the original Kotlin/Gradle source project. The public kit contains decoded resources/smali and Java additions. Resource changes beyond the identity edits require a working resource-compilation pipeline; the included packaging script deliberately reuses the baseline compiled resources.
