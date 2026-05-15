# VUSIC — Music Visualizer

A single-file HTML/CSS/JS web app that visualises audio in real time. Everything lives in `index.html`.

## What it does

- **Audio input**: microphone via Web Audio API (`getUserMedia`)
- **Spotify integration**: polls a user-supplied Spotify token to show currently-playing track info and album art
- **Visualisation modes**: spectrum bars, radial, single-bar VU, multi-colour themes
- **UI**: header with Spotify panel + controls, full-screen canvas, bottom control bar, slide-in settings drawer, calibration overlay, help overlay
- **Gestures**: touch swipe/pinch handled directly on the canvas
- **Persistence**: user settings saved to `localStorage`

## Architecture

All code is in `index.html` — one `<style>` block, one `<body>` with the DOM, and one `<script>` block at the bottom.  There is no build step, no bundler, and no server-side component.

## Linting

```bash
npm run lint          # HTMLHint on index.html
```

No automated tests exist — correctness is verified by loading the page in a browser.

## Assets

- `icon.png` — app icon / PWA icon / album-art placeholder

## Local development

Open `index.html` directly in a browser (no server needed). Microphone prompts appear on first use. Spotify requires a valid OAuth access token entered in the settings drawer.
