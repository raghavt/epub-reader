# Focused Reading Environment: Local EPUB Reader & TTS

**🚀 Try the Live Demo:** [local-epub-reader.netlify.app](https://local-epub-reader.netlify.app)

A private, self-contained, and distraction-free EPUB reader powered by your device's native Text-to-Speech (TTS) engine.

Sitting down to read dense, long-form text for hours can be tough on the eyes. This project removes the physical friction of reading by combining audio with active sentence highlighting and smooth auto-scrolling. It keeps your eyes anchored, making the entire experience effortless.

Designed with a strict focus on privacy and a preference for independent, self-hosted architecture, this tool contains no algorithms, no telemetry, no tracking, and no backend servers. A smart device and an EPUB file are all that is needed to create a quiet environment for deep work.

## Core Features

* **100% Local & Private:** The application has no backend server. EPUBs are unzipped and processed entirely within your browser's memory using `JSZip`. Your data never leaves your device.
* **Persistent Offline Library:** Books and reading progress (chapter, exact sentence, and percentage) are saved automatically to your browser's internal `IndexedDB`. You can close the tab, go offline, and resume exactly where you left off.
* **Native TTS Engine:** Leverages the `window.speechSynthesis` API built into your operating system, ensuring zero latency and zero server costs.
* **Active Tracking:** Automatically highlights the currently spoken sentence and handles smooth auto-scrolling to keep the active text perfectly in frame.
* **Wake Lock Integration:** Automatically acquires a screen wake lock while reading so your device doesn't go to sleep mid-chapter.
* **Dynamic Pacing:** Customize reading speed (0.5x to 3.0x) and inject custom pauses (in milliseconds) between sentences for better comprehension of dense material.

---

## How to Use

The application is fully responsive and optimized for both desktop and mobile environments.

### 💻 Desktop Controls

* **Upload:** Click "Open EPUB" to load a local file.
* **Playback (Quick Toggle):** Press the `Spacebar` to Play/Pause instantly.
* **Navigation:** Use the `Left Arrow` and `Right Arrow` keys to switch chapters.
* **Jump:** Click on any sentence in the text to immediately jump the audio to that spot.
* **Settings:** Use the top toolbar to adjust reading speed and pause duration.

### 📱 Mobile Controls

* **Upload:** Tap the floating menu (`☰`) to open the toolbar and load a file.
* **Navigation:** Swipe left or right anywhere on the screen to turn chapters.
* **Playback:** Tap the floating Play button to start.
* **Jump:** Tap any specific sentence to start reading from there.

---

## Installation & Setup

Because this is a purely client-side application with all dependencies included, setup is completely frictionless.

1. **Clone or download** this repository to your machine.
2. **Choose how to run it:**
* **Option A (Quickest - Offline Mode):** Just double-click `index.html` to open it directly in your web browser. The core reader and TTS engine will work perfectly offline.
* **Option B (Recommended for Mobile/Long Sessions):** Serve the folder using a local web server (e.g., run `python -m http.server` in the directory, or use a VS Code Live Server extension). Browsers require a secure context (`localhost` or `https`) to grant permissions for the Screen Wake Lock feature, which keeps your screen from sleeping while reading.


3. **Open the app** and click "Open EPUB" to begin.

---

## Getting Better Voices (Pro Tip)

Because this app uses the native Text-to-Speech engine built into your device, the audio quality depends entirely on your local OS settings. If you only hear robotic voices, you likely need to download high-quality voice packs:

* 🍏 **iOS / macOS:** Go to **Settings > Accessibility > Spoken Content > Voices**. Download the "Enhanced" or "Premium" versions of preferred voices (like Siri, Alex, or Zoe).
* 🤖 **Android:** Go to **Settings > Accessibility > Text-to-Speech output**. Tap the gear icon next to your preferred engine to install new voice data packs.
* 🪟 **Windows:** Go to **Settings > Time & Language > Speech**. Under "Manage voices," click "Add voices" to install natural-sounding localized language packs.
