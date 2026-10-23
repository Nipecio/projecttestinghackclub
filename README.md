# Soundsight

A music visualizer that lives in one HTML file. Drop some songs on it (or turn on your mic) and it draws the audio as moving color. Nothing gets uploaded, it all happens in your browser.

MP3, WAV, M4A, OGG, FLAC, AAC, Opus and WebA all work, as long as your browser can decode them.

There are five looks: bars, wave, blob, radial, and particles. They all react to bass hits, so you get flashes, ring pulses, and a bit of extra motion on the beat. There's also an auto mode that flips between styles every 15 seconds if you don't want to pick.

## What it does

You can load a bunch of files at once. The queue lets you click a track to play it, remove it, or drag it to a new spot. There's prev/next, shuffle, repeat (off, all, one), a seek bar, volume, and playback speed from 0.75x to 2x. Title, artist and cover art come from ID3 tags when it can read them, and the OS media controls get the metadata too.

There's a sleep timer (15, 30, 45 or 60 min) that fades out over the last 30 seconds.

For looks, there are five themes: Aurora, Ocean, Sunset, Ember and Daylight, which is the default. Switch them under More... > Theme. You can turn glow on or off, go fullscreen, and open the Adjust panel to change sensitivity (0.5x to 3x) and smoothing (0.1 to 0.95).

Snapshot saves the current frame as a PNG. Record saves a `.webm` of the visualizer, with audio if something's playing. Recording relies on `MediaRecorder`, so it may not work in Safari.

On a narrow screen it drops from 64 bars to 32 and tucks the secondary controls into More...

## Keyboard

`1` through `5` switch styles, in the order above. The Help panel mentions other shortcuts, but those aren't hooked up yet.

## What gets saved

A few things go in `localStorage` under keys starting with `ss:`: volume, theme, glow, style, and the names of your queued tracks. The audio itself isn't stored, so after a reload you'll have to add your songs again.

## Network stuff

It pulls in two things from outside. Instrument Sans comes from Google Fonts, and it falls back to system fonts if that's blocked. jsmediatags 3.9.5 comes from cdnjs and is only used for tags and cover art. Playback and visuals work fine without it.

## License

Not picked yet.