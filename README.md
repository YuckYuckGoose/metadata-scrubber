# Weird Boob Magic: Metadata Scrubber

**[Open the tool →](https://weirdboobmagic.com/)**

Remove AI Content Credentials (C2PA), EXIF, GPS and encoder tags from video and images. Lossless, and nothing leaves your browser.

## Privacy

Your files never leave your device. The whole tool is one HTML file ([`index.html`](index.html)) with no external scripts, no analytics and no network requests. You can read every line, or download the file and run it offline.

## What it removes

| | |
|---|---|
| **Video**: MP4, MOV, M4V | Content Credentials (C2PA), XMP, title/software/encoder tags, GPS location, creation & modification dates, handler and compressor names, language tags, timecode and timed-metadata tracks, and encoder text written into the H.264/HEVC stream (SEI user data) |
| **JPEG** | C2PA, EXIF (camera, lens, serial numbers, GPS, dates), XMP, IPTC/Photoshop, comments, MPF and trailing data. Keeps the color profile and the rotation flag |
| **PNG** | C2PA, text chunks (including AI prompt text), EXIF, XMP, timestamps. Keeps color and transparency info |

Before you download, it shows a report of everything it found.

## How it works

Video is **remuxed, not re-encoded**: the tool rebuilds the MP4/MOV container around the original compressed audio and video, so quality is untouched and even large files take seconds. Decoded frames and audio are identical to the source.

## Limits

- It can't remove invisible watermarks embedded in the pixels or audio themselves (e.g. SynthID). Platforms may still detect these.
- Not yet supported: fragmented MP4 (some live-stream/DASH exports) and DRM-protected files.
- Platform and client rules on AI disclosure still apply. This tool removes tags; it doesn't change what you're required to disclose.

## Credits

Title font: [Moirai One](https://fonts.google.com/specimen/Moirai+One), SIL Open Font License 1.1, embedded in the page so no font requests leave your browser.

## License

[MIT](LICENSE)
