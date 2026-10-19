# Pulse — Advanced HIIT Timer

A responsive, zero-dependency HIIT timer that runs as a static site on GitHub Pages.

## Features
- Per-exercise names, work and rest durations
- Multiple rounds, preparation period, and between-round rest
- Pause/resume, skip, restart, interval progress and total remaining time
- Browser text-to-speech and Web Audio beeps
- Saved workouts using localStorage; JSON import/export
- Optional screen wake lock where supported
- Installable PWA with offline asset caching after first visit

## Deploy to GitHub Pages
1. Create a public GitHub repository, for example `pulse-hiit`.
2. Upload **all files in this folder** to the repository root and commit.
3. Go to **Settings → Pages**.
4. Under **Build and deployment**, choose **Deploy from a branch**, choose **main** and **/(root)**, then save.
5. Open `https://YOUR_USERNAME.github.io/pulse-hiit/` after deployment.

You can also preview locally using `python3 -m http.server 8000` and opening `http://localhost:8000`.

## Notes
- Browsers require user interaction to initiate audio, and voice availability depends on installed voices/browser support.
- Mobile operating systems can suspend websites when the phone locks or switches apps. Timestamp-based countdown corrects elapsed time when execution resumes, but **sounds cannot be guaranteed while backgrounded**. Keep the screen on for reliable cues.
- Presets are stored only in the browser on the current device; export JSON for backups or transfers.
- Exercise edits apply at the start of the next workout. Restart to apply them.
- App updates: change the `CACHE` version in `sw.js` when replacing cached assets.
- Optional: for broad home-screen icon compatibility, supply PNG icons (e.g. 192×192 and 512×512) in the manifest.
