# MotionLab — Universal Animation Studio

A responsive, browser-based animation prototype for general creative use. It is intentionally framework-free so it can run on GitHub Pages.

## Included working features

- Canvas 2D scene preview with animated circle, rectangle, star, text, and image placeholder objects.
- Add objects, select them from the timeline or preview, edit color, text, position, size, and motion preset.
- Timeline playback, stop, start/end navigation, and time scrubbing.
- Project duration, frame rate, and canvas aspect-ratio settings.
- Export project data as JSON; save/restore locally in the same browser.
- Record the animated canvas to WebM in browsers that support Canvas CaptureStream and MediaRecorder.
- CSS 3D rotating-cube demonstration.
- Local prompt-template assistant for drafting animation prompts.

## Important limitations

- The prompt assistant is a local template, not an external AI model. No AI image/video service is connected.
- The 3D cube is a CSS demo, not a complete 3D modeling, rigging, or rendering engine.
- The image tool creates a placeholder; it does not upload or render images yet.
- WebM export depends on browser support and records the preview canvas. Export is not guaranteed to work in every mobile browser.
- Projects are saved in the current browser's local storage only. Download the JSON file for a portable backup.
- This is a functional starter project, not a replacement for a professional non-linear video editor.

## Run locally

Open `index.html` in a modern browser. No build step or package install is required.

For a local HTTP server, from this directory run:

```bash
python -m http.server 8000
```

Then open `http://localhost:8000`.

## Publish with GitHub Pages

1. Push this folder to your GitHub repository.
2. In the repository, open **Settings → Pages**.
3. Under **Build and deployment**, choose **Deploy from a branch**.
4. Select branch `main` and folder `/ (root)` if you publish this folder as the repository root. If it remains in `animation-studio/`, GitHub Pages does not publish that subfolder as the site root automatically; move/copy these files to the root of a dedicated repository, or configure a build workflow that publishes the subfolder.
5. Save and wait for GitHub Pages to finish deploying.

## Future integrations

To connect actual AI generation, use a server-side endpoint that keeps provider API keys private. Never place secret API keys in this static HTML or in public repository files.
