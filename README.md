Soundsight

So this is a music visualizer I made for Hack Club. You drop a song in and it turns the sound into stuff that moves. Bars bounce, a blob swells when the bass hits, you get the idea.

It works with basically any song. The visuals come straight from the audio while it plays, nothing is timed by hand.

How to use it
Open index.html in your browser (or use the Live Server extension in VS Code)
Drag a song onto the page, or hit Choose a file
Pick a style up top, or press 1, 2, 3, 4
Press space to pause
Cycle through the color themes and toggle the glow from the player controls

Your song never gets uploaded anywhere. It just plays in your browser.

The four styles
Bars: frequency bars with little peak caps that float back down
Wave: a smooth line that wiggles with the sound
Blob: a soft shape that swells with the bass and sticks out in different directions
Radial: bars in a circle, mirrored so it looks even on every side

The player also includes five full-page color themes and a glow toggle to tune the look.

How it works (the short version)

The Web Audio API has an AnalyserNode that runs an FFT on whatever's playing, which splits the sound into frequencies. I group those on a log scale so the bass gets more room, and then smooth everything so it isn't jittery (it goes up fast and falls slowly).

There's also a basic beat detector. It keeps a running average of how loud the low end is, and when the bass suddenly jumps above that average it counts as a kick drum. That's what makes the rings shoot out.

Stuff I used

Just plain HTML, CSS, and JavaScript in one file. No libraries, no server.

Things I might add:
Particles that burst on the beat
Microphone input