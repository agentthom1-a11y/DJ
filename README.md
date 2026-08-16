# DJ — Virtual Mixer

A focused, browser-native two-deck DJ mixer designed as a lightweight DJ-only adaptation of the ideas in [gantasmo/theDAW](https://github.com/gantasmo/theDAW).

## What works

- Two independent local-audio decks
- Drag-and-drop or file picker loading
- Real waveform rendering and click-to-seek
- Play / pause and cue points
- ±8% tempo control
- BPM estimation and tempo sync
- Jog/nudge control
- Per-channel gain, 3-band EQ, bipolar filter, channel faders
- Equal-power crossfader
- Real channel and master meters
- Four hot cues per deck
- BPM-quantized 1/2/4/8-beat loops
- Master limiter
- Master-output recording via MediaRecorder
- Keyboard shortcuts and fullscreen mode
- Responsive desktop/tablet/mobile layout

Everything runs locally in the browser. No upload server is required.

## Run locally

Because this is dependency-free, any static server works:

```bash
python -m http.server 8080
```

Then open `http://localhost:8080`.

You can also open `index.html` directly, although a local HTTP server is recommended for consistent browser behavior.

## Deploy

This repository can be deployed directly to GitHub Pages, Netlify, Cloudflare Pages, Vercel static hosting, or any basic web server. There is no build step.

## Browser notes

Use a current Chrome, Edge, Firefox, or Safari release. Browser audio decoding support depends on the codec available in that browser/OS. WAV and MP3 are the safest general choices.

Recording format is selected from the formats supported by the current browser, usually WebM/Opus.

## Credits

Product direction is intentionally focused on the DJ workflow. The original theDAW project is a much larger DAW/DJ/VJ application and was used as architectural/product inspiration for this standalone mixer.
