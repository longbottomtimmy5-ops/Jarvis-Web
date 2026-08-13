# J.A.R.V.I.S. Web App

This is the phone-friendly version of Jarvis — a single web page (no install
needed) with the same HUD look, that talks to a free Groq AI model.

## Set it up in VS Code

1. Open this folder in VS Code.
2. Open `index.html` and find this line near the top of the `<script>` tag:
   ```
   const GROQ_API_KEY = "PASTE_YOUR_GROQ_API_KEY_HERE";
   ```
   Replace the text between the quotes with your real key from
   https://console.groq.com/keys (same key type as your desktop version —
   you can even reuse the same one, or make a new one just for this).
3. Save the file (Cmd+S).

## Try it on your Mac first

Double-click `index.html`, or right-click it in VS Code's file list and choose
"Open with Live Server" if you have that extension installed. Typing works
immediately. The 🎤 SPEAK button needs microphone access, which most browsers
only allow securely — Live Server (or any `localhost` address) works fine;
just double-clicking the file sometimes doesn't ask for mic permission.

## Getting it onto your old phone

Two options, both free:

- **Easiest — GitHub Pages:** create a free GitHub account, make a new
  repository, upload `index.html`, then turn on "GitHub Pages" in the
  repository settings. GitHub gives you a free `https://` link you can open
  on your phone's browser from anywhere — and `https://` is required for the
  microphone button to work on a phone.
- **Fastest to test locally:** run a tiny local server from this folder
  (in VS Code's terminal: `python3 -m http.server 8000`), then on your
  phone (connected to the same WiFi) visit `http://<your-mac's-local-ip>:8000`.
  Note: text chat and speaking (TTS) will work this way, but voice *input*
  (the mic button) may be blocked by the phone's browser since it isn't
  `https://` — GitHub Pages avoids that.

## Notes

- Voice input (🎤 SPEAK) uses your browser's built-in speech recognition.
  Works well in Chrome/Edge and most Android browsers. Not supported in
  Safari on iPhone.
- Voice output (Jarvis talking back) works in basically every modern browser.
- Anyone who opens this HTML file can see your API key in it, so don't post
  this file publicly (e.g. don't make the GitHub repository public without
  removing the key first, or use a private repository).
