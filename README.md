# Video Player

A single-file, browser-based video player. No install, no server, no upload —
just open the HTML file and play. Everything runs locally; your files never
leave your machine.

## Features

### Playback
- Play / pause, 10-second skip back/forward, draggable seek bar with hover thumbnail preview
- **Scroll-wheel volume control** — scroll over the video or the volume icon to adjust volume, no need to grab the slider
- Variable playback speed, 0.25× – 3×
- Mute toggle, Picture-in-Picture, native-feeling custom fullscreen UI

### Multi-file playlist with session persistence
- Drag and drop multiple video files at once, or browse for them
- Switch between loaded files from a playlist panel attached to the player
- **Remembers your files across reloads** (Chrome/Edge): using the File System
  Access API, the player keeps a reference to files you've opened so they
  reappear in the playlist next time you open the page — click to resume
  instantly, or grant access again with a single tap if the browser needs
  it re-confirmed
- Per-file remove (✕) and a **Reset** button to clear the whole saved playlist
- Automatically skips re-adding a file that's already in the current playlist
- Falls back gracefully to a normal session-only playlist in browsers without
  File System Access support (Safari, Firefox)

### Resizable player
- Drag any edge or corner handle to resize the player to whatever size fits your screen

### Visual adjustments
- Live color controls: brightness, contrast, saturation, sharpness — with one-click reset
- Display/fit modes: Fit, Stretch, Crop, Wide, Tall

### Scene navigation
- "Scan Video" auto-generates a grid of scene thumbnails (4–48, or auto-detected) — click any thumbnail to jump straight there

### A → B Loop
- Mark an in-point and out-point and loop that section on repeat — handy for studying a clip or rehearsing a section

### Subtitles
- Load an .srt file and it's synced to playback automatically

### Other
- One-key screenshot capture of the current frame
- Toast notifications for quick feedback (volume %, files added, errors, etc.)

## Keyboard Shortcuts

| Key | Action |
|---|---|
| `Space` / `K` | Play / Pause |
| `←` / `→` | Seek −10s / +10s |
| `↑` / `↓` | Volume up / down |
| `M` | Mute |
| `F` | Fullscreen |
| `P` | Picture-in-Picture |
| `S` | Screenshot |
| `L` | A→B Loop |
| `C` | Color panel |
| `Q` | Playlist |
| `>` / `<` | Speed up / down |
| `PgUp` / `PgDn` | Previous / Next file |
| `?` | Shortcuts overlay |

Mouse scroll over the video or volume control also adjusts volume.

## Supported Formats

MP4, MKV, WebM, MOV, AVI, and more — actual playback support depends on the
codecs your browser can decode.

## Getting Started

1. Open the HTML file in a browser (Chrome or Edge recommended for the full
   feature set, including saved playlists).
2. Drag in a video, or click **Browse Files**.
3. Use the controls, or press `?` any time for the full shortcut list.

## Browser Support Notes

| Feature | Chrome / Edge | Firefox / Safari |
|---|---|---|
| Core playback, color, A→B loop, subtitles, scenes, resize | ✅ | ✅ |
| Playlist persists across reloads | ✅ | ❌ (session only) |

## Privacy

Files are read directly from your device using the browser's File API and
played via local blob URLs. Nothing is uploaded anywhere.
