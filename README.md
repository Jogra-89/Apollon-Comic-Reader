# OmniPanel

OmniPanel is a free Android comic reader for a local collection. Read archives and PDFs, browse your library, and follow a page panel by panel. See [FEATURES.md](FEATURES.md) for the full feature catalogue.

## Windows 11 preview

[Download OmniPanel for Windows Preview 1](https://github.com/Jogra-89/Apollon-Comic-Reader/releases/tag/windows-v1.0-preview.1). Extract the complete portable x64 ZIP and run app/OmniPanel.exe. Includes offline archives/PDFs, library, progress, keyboard controls and a ComicVine picker. Source and a full desktop feature list are included in the release. Guided panels, creator photos and Android themes are planned; this preview does not yet have Android feature parity.

## Android install

Download [OmniPanel-1.0.20.apk](https://github.com/Jogra-89/Apollon-Comic-Reader/releases/download/v1.0.20/OmniPanel-1.0.20.apk) from the release assets and open it on Android 8.0 or later. If Android asks, allow installation from the app you used to open the APK. OmniPanel uses the same app ID and signing key as the earlier Apollon builds, so it updates them in place. It is separate from Inkframe and does not import Inkframe's app data automatically.

## Highlights

- Read CBZ, CBR, CB7, CBT and PDF files from local folders.
- Browse a library by series, creators, characters, publishers, story arcs, tags and folders.
- Read by page or guided panel, with reading directions, fit modes, backgrounds and controls you can customize.
- See an uncropped cover, synopsis, credits, creator photos when available, page number and time in the reader menu. Choose a thumbnail size in reader settings. Find details for an unmatched comic using ComicVine, with your own API key and an internet connection.
- Sort library groups by combined page count, choose from 14 themes, track reading progress and export pages or panels.

## Development and build materials

OmniPanel was created through **vibe coding**: development was guided through natural-language conversations with AI coding tools and iterative checks. It is adapted from the supplied Inkframe 1.3 preview APK and its patch kit. The rebuild kit contains decoded resources and smali with Java patch additions, not the original Kotlin/Gradle project. The release includes the rebuild kit and checksums; the private signing key is not included.

The reader menu and one-comic ComicVine lookup were tested on a Galaxy Tab S9 FE+ in version 1.0.5. In 1.0.20, the full-screen page dim in page and panel view, reader information and creator photos were checked on that tablet. Other combinations and devices need further testing. See the release notes for details and limitations.

Local reading is offline. Optional ComicVine lookup and creator photos send comic and creator identifiers to ComicVine. Photos require a matched issue, a configured API key, and internet access; unavailable or ambiguous matches use a placeholder. Publisher logos appear when already cached by the app. The app includes third-party components and font notices; free availability does not itself establish an open-source license for the entire application.
