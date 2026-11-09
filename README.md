# Apollon Comic Reader

**Version 1.0.1 prerelease · A free Android comic reader for your own local collection.**

Read comic archives and PDFs offline, browse a rich library, follow the artwork panel by panel, and tailor the reader's appearance and controls to the way you read.

**Current test build:** The original 1.0 APK crashes when opening a comic on a Galaxy Tab S9 FE+. Version 1.0.1 fixes the field-access error found in the crash report. It is awaiting an on-device reader test. Download the 1.0.1 prerelease below.

## Highlights

- **CBZ, CBR including RAR5, CB7, CBT, and PDF.** Optional scanning of plain ZIP, RAR, and 7z image archives.
- **Guided panel reading** with multiple detection methods, six sensitivity choices, adjustable transitions, and a new option to keep panels connected by a speech bubble together.
- **A unified local library** from multiple folders, with cover-wall, grid, and list layouts.
- **Browse by series, characters, creators, publishers, story arcs, tags, or folders.** Search across titles, series, characters, creators, and tags.
- **Reading progress and favorites**, a Continue Reading row, and read/unread controls.
- **14 visual themes**, light/dark preferences, wallpaper colors, and a separate accent color for each theme.
- **Flexible reading layouts**, manga direction, two-page spreads, scrolling, margin cropping, seven fit modes, and configurable background fill.
- **ComicInfo.xml metadata** and optional ComicVine matching for richer credits, characters, story arcs, and summaries.
- **Customizable tap zones and button mappings** for volume buttons, keyboards, page-turner remotes, and game controllers.
- **Context-aware image export:** Save page in page view; Save panel in panel view.

See [FEATURES.md](FEATURES.md) for the detailed feature catalogue.

## New in Apollon 1.0

- Sort folders and other library groups by their **combined page count**, fewest or most first. The same choices sort individual comics by their page count.
- Use page-edge color, blurred art, black, white, or a custom color around the artwork in panel view.
- Choose **Join speech-bubble panels**, between **Eager** and **Find every panel**. This mode uses a local image heuristic to join neighboring frames when a white speech balloon crosses their divider.
- Export the selected panel as a PNG in panel view. Page view keeps the original whole-page export action.
- Open the reader menu to see a cover, title, page information, synopsis, available credits and metadata, and the current time. The information area scrolls for longer descriptions.
- New app identity: **Apollon Comic Reader**, version **1.0**, package `com.apollon.comicreader`.

## Install

1. Download **Apollon-Comic-Reader-1.0.1.apk** from this repository's release assets.
2. Open the APK on an Android device and allow installation from the app used to open it, if Android asks.
3. Open Apollon Comic Reader and add the folders containing your comics.
4. Optional: enter your own ComicVine API key in Settings for online metadata.

**Requirements:** Android 8.0 or later. The APK contains ARM64, ARMv7, x86, and x86-64 native libraries. Physical-device compatibility and visual checks are still pending for this build.

Apollon installs as a separate app from the earlier Inkframe and Inkframe Preview builds. It does not automatically import their library database, reading history, settings, or API key. Your comic files remain in their existing folders; add those folders again in Apollon.

## Quick start

- **Library → Sort:** choose a total-pages option to find shorter or longer folders and series.
- **Reading settings → Sensitivity:** choose **Join speech-bubble panels** for pages like two frames linked by an overlapping balloon. Choose another mode when a page's art is better served by separate frames.
- **Reader shortcut bar → Fill:** choose how empty space and hidden panel surroundings look.
- **Panel view → Save panel:** move into a detected panel first. A whole-page preview is not exported as a panel.
- **Tap the reader menu zone:** open the reader controls and comic information card.

## Offline reading and optional online services

Reading local comics does not require a ComicVine account or an internet connection. ComicVine metadata lookup needs your own API key and a connection; it sends metadata queries such as series names and issue numbers to ComicVine. Publisher-logo downloads can contact ComicVine or Wikipedia. These services are optional.

The app requests storage access to read selected comic folders and, where enabled, save images or delete files. Removing a folder from the library differs from deleting its files; the app's delete commands can remove files from storage.

## Development note

**Apollon Comic Reader was built through vibe coding:** its development and updates were guided through natural-language conversations with AI coding tools, with generated code, iterative changes, and automated checks.

This is an independently developed project. Please report bugs with your Android version, device, file format, relevant settings, and steps to reproduce the problem. Automated checks do not replace testing on real devices.

## Build status and source materials

This release was adapted from the supplied Inkframe 1.3 preview APK and its patch/rebuild kit. That kit contains **decoded Android resources and Dalvik smali code**, plus Java patch additions; it is not the original Kotlin/Gradle project. The rebuild materials describe this limitation explicitly.

The new detection mode is a heuristic, not OCR or semantic understanding. It can miss unusual balloons or join frames incorrectly on complex artwork. Its analysis and blurred-background preparation run when a panel page is prepared and are cached; image analysis is not repeated for every transition frame. On-device speed has not been benchmarked.

See [RELEASE_NOTES.md](RELEASE_NOTES.md) for changes and verification details.

## Credits

The app includes theme fonts distributed under the SIL Open Font License; their notices remain inside the APK and rebuild materials. It also includes third-party Android libraries. Free availability does not itself establish an open-source license; no new license for the entire application has been selected in this preparation package.
