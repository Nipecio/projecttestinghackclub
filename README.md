# Soundsight

Soundsight is a browser-based music visualizer that turns audio into real-time visuals. Load a song from your device or use your microphone to see the visuals move with the sound.

## Getting Started

1. Open `index.html` in a modern browser. There's no installation or build step.
2. Click **Choose a file** or drag your audio files onto the page.
3. Pick a visualizer style from the controls at the top.
4. Use the player to control playback, skip through tracks, adjust volume, and manage your queue.

To use your microphone, allow access when prompted. Depending on your browser, you may need to open the page through `localhost` or HTTPS.

## Features

**Visualizers:** Choose between Bars, Wave, Blob, and Radial.

**Queue:** Add multiple songs, drag to reorder them, or remove tracks whenever you want.

**Track info:** Display available song titles, artist names, and embedded album artwork.

**Microphone:** Use live microphone input to create visuals from sounds around you.

**Audio settings:** Adjust sensitivity and smoothing to change how the visuals react to sound.

**Themes:** Switch between Aurora, Ocean, Sunset, Ember, and Daylight. You can also enable the glow effect or let the visualizer cycle through styles automatically.

**Capture:** Save a screenshot as a PNG or record the visualizer as a WebM video. Audio can be included in recordings when supported by your browser.

**Playback:** Shuffle tracks, repeat songs, change playback speed, seek through audio, and adjust volume.

## Keyboard Shortcuts

Press `1`, `2`, `3`, or `4` to switch between Bars, Wave, Blob, and Radial. The page needs to be focused for these shortcuts to work.

## Privacy

Audio files are processed locally in your browser and aren't uploaded by Soundsight. The app loads jsmediatags from cdnjs to read track metadata and Instrument Sans from Google Fonts for its typeface.

## Built With

HTML, CSS, and JavaScript, with HTML Canvas for the visuals and the Web Audio API for audio playback and analysis. Track metadata is handled by [jsmediatags](https://github.com/aadsm/jsmediatags).