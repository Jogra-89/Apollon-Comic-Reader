# Apollon Comic Reader 1.0 — Feature catalogue

This catalogue is based on the supplied decoded app, its existing patch source, and the Apollon additions. It describes implemented options, not a claim that every combination has been verified on a physical device.

## Formats and local files

- CBZ / ZIP-based comic archives.
- CBR / RAR-based comic archives, including RAR5.
- CB7 / 7z-based comic archives.
- CBT / TAR-based comic archives.
- PDF documents.
- Optional scanning of image archives with ordinary `.zip`, `.rar`, and `.7z` extensions.
- Opening supported content files through Android's Open With mechanism.
- Multiple source folders in one library.
- Folders on internal storage or accessible SD-card storage.
- A system folder picker and an all-files-access route for locations such as Downloads.
- Comics are indexed in their existing folders rather than copied into a separate library directory.
- Rescanning folders on launch can be enabled.
- Scanning progress can be shown or hidden.
- Recently opened archives are cached unpacked for faster reopening.
- Configurable page-cache size and a display of cache usage.

## Browsing and organization

- Cover wall, grid, and list layouts.
- Adjustable cover size.
- Adjustable cover-wall spacing.
- Browse all individual comics.
- Browse series.
- Browse characters.
- Browse creators, with role selection.
- Browse publishers.
- Browse story arcs.
- Browse tags.
- Browse folders.
- Choose which browse tabs appear.
- Search titles, series, characters, creators, and tags.
- Sort by series and issue number.
- Sort by title.
- Sort by recently added.
- Sort by recently read.
- Sort by year.
- **Sort by total pages, ascending or descending.** For a group or folder, the total is the sum of its indexed comics' page counts. For individual comics, it is that comic's page count.
- Filter all, unread, currently reading, finished, or favorite comics.
- Add and remove personal tags.
- Mark individual comics as read or unread.
- Mark groups of comics as read or unread.
- Continue Reading row.
- Saved current-page progress.
- Reading progress bars that can be shown or hidden.
- Individual issue and aggregate group page counts that can be shown or hidden.
- Issue-count and read-status cover badges that can be shown or hidden.
- Series-name cover labels that can be shown or hidden.
- Publisher logos on covers can be shown or hidden.
- Open a single-comic folder or series directly in the reader.
- Choose which top-bar buttons remain visible; hidden buttons move into the overflow menu.
- Library title and counts can be shown or hidden.
- Finished comics and completed series can look normal, desaturated, black and white, blurred, or faded, with adjustable effect strength.
- Remove source folders from the library.
- Explicit deletion commands for comics and folders, with confirmation text distinguishing file deletion from library removal.

## Metadata and discovery

- Read embedded `ComicInfo.xml` metadata.
- Display title, series, issue number, volume, year, and publisher where available.
- Display writer, penciller, inker, colorist, letterer, cover artist, and editor credits.
- Display characters, genres, metadata tags, personal tags, story arcs, and summaries where available.
- Read manga-direction metadata when present.
- Optional ComicVine API-key entry and key testing.
- Search ComicVine for a series and select a matching issue.
- Match a single series from its library page.
- Scrape unmatched series across the whole library.
- Choose whether ComicVine fills missing fields or replaces file-supplied metadata.
- Forget online details and return to file metadata while retaining reading progress and personal tags.
- Automatic scraping only when new comics are added.
- Existing-library baseline prevents an immediate new-additions scrape on first load.
- Addition detection waits for scanning and a short debounce.
- Unchanged libraries, metadata-only changes, and removals do not trigger the new-additions mode.
- Automatic scraping can be disabled or set to the existing daily, weekly, fortnightly, and monthly schedules.
- Wi-Fi-only setting for automatic scraping.
- Display of the last library scrape and its result.
- Optional publisher-logo downloads, retained for offline use.
- Supply a custom publisher logo by long-pressing its logo.
- Open an available ComicVine item page.

## Page reading

- Left-to-right reading.
- Right-to-left manga reading.
- Per-comic reading-direction setting.
- Slide, page-turn, fade, stack, vertical-slide, and instant page animations.
- Continuous vertical scrolling.
- Continuous horizontal scrolling.
- Adjustable gap between pages in scrolling modes.
- Fit screen.
- Fit width.
- Fit height.
- Smart fit.
- Stretch.
- Fill and crop.
- Original-size display.
- Automatic trimming of white or black margins.
- Two-page side-by-side layouts.
- Keep the cover on its own to preserve printed page pairing.
- Wide-page handling: split in portrait, always split, rotate the device, rotate the image, or show the whole spread.
- Follow device orientation, lock portrait, or lock landscape.
- Automatic landscape rotation for wide pages, including when the reader's rotation setting is locked.
- Page-edge-color background fill.
- Blurred-art background fill.
- Black background fill.
- White background fill.
- Custom-color background fill.
- Double-tap zoom, which can be disabled for immediate single-tap handling.
- Low-resolution-scan sharpening option.
- Follow system brightness or choose reader brightness.
- Warm-light tint.
- Keep the screen awake while reading.
- Show or hide the page number.
- Five page-number positions: bottom center, top left, top right, bottom left, and bottom right.
- Page numbers can remain visible or appear for two seconds after opening or turning a page.
- Long pull at the end of an issue to open the next issue in the series.
- Long pull at the first page to open the previous issue in the series.
- Destination preview and configurable pull distance.
- Previous/next navigation also accounts for single-page issues.
- Whole-page image export in page view.

## Guided panel reading

- Open comics directly in panel view.
- Optionally show the whole page before entering its panels.
- Smart detection combining gutters, drawn borders, and shapes.
- Gutters-only detection.
- Panel-border detection for full-bleed artwork.
- Row mode that glides down a page at full width without panel detection.
- Six sensitivity choices: **Only clear panels**, **Cautious**, **Balanced**, **Eager**, **Join speech-bubble panels**, and **Find every panel**.
- The new join mode can combine side-by-side or stacked panels when a white speech balloon crosses their divider.
- A whole-page or scrolling-row fallback when panels are not detected.
- Show, dim, or hide the surroundings of the current panel.
- Adjustable surrounding dimming.
- Glide, zoom out/in, fade, slide, and instant panel transitions.
- Adjustable transition duration.
- Optional detected-panel outlines and numbering on the whole-page view.
- **The same five background-fill choices as page view**, including cached blurred artwork around hidden panel surroundings.
- **Save panel** exports the current detected panel as a PNG, using the original exported page's resolution.
- The export control switches between **Save panel** and **Save page** with the reading mode.
- Whole-page previews in panel mode require selecting a panel before panel export.
- Detection, joining, and small blurred backgrounds are prepared outside the transition drawing path and cached.

## Controls and reader information

- Edge tap zones.
- Half-screen tap zones.
- Menu-only tapping mode.
- Invert tap zones.
- Turn pages with volume buttons.
- Swap the volume-button directions.
- Map keyboard, remote, controller, or volume-button input.
- Available mapped actions include next/previous panel or page, next/previous whole page, show/hide menu, toggle panel view, and close comic.
- Configurable reader shortcut bar.
- Reader shortcuts for panel mode, animation, cropping, fit, direction, two-page mode, orientation, auto-rotation, fill, and image export.
- Tap the menu zone to display reading controls and the comic information card.
- Information card shows the cover, title, current page/total pages, and panel-view status.
- Scrollable synopsis and available series, issue, volume, year, publisher, credits, characters, genres, story arc, and tags.
- Current time shown using Android's clock and time-format preference.
- Missing synopsis is stated explicitly rather than invented.
- Cover decoding runs away from the main UI thread.
- Information card is removed when the reader is disposed or the app is paused.

## Appearance

- **14 themes:** Modern, Terminal, Desktop 95, Synthwave, Holo HUD, Atomic Age, Golden Age Pulp, Manga Ink, Deco Noir, Blueprint, Grimoire, Sketchbook, Bauhaus, and Bubblegum.
- Themes have their own colors, fonts, shapes, and decorative treatment.
- System, light, and dark appearance preferences; theme-specific designs may impose their own palette.
- Optional wallpaper-derived colors.
- Separate saved accent color per theme.
- Accent presets and a custom hue choice.
- Theme fonts bundled with their SIL Open Font License notices.

## Limits to keep in mind

- Password-protected PDFs are not supported by the supplied reader.
- The speech-bubble option is a local white-region/divider heuristic. It does not understand dialogue or guarantee correct grouping for every page.
- Metadata-dependent categories require suitable embedded data or online matching.
- Online lookup and logo downloads require connectivity; local reading does not.
- This APK has a separate application identity from Inkframe and cannot automatically inherit that app's private data.
- The current release has build, logic, signature, and package checks; physical-device rendering, input, and performance testing remain pending.
