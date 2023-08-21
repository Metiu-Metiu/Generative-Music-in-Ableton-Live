# Generative-Music-in-Ableton-Live
Max 4 Live device generating melodies and exposing several ways of controls over probabilities and numerical ranges of pitches, harmonies and rhythms. Inspired from Patter by Adam Florin.

This is a Max for Live (MIDI instrument) device (developed with Ableton Live 9 and Max 7). It produces MIDI note on messages to be used inside an Ableton Live environment.
Drop the generativeNotesControl.amxd file inside any MIDI track in Ableton Live. Then, drop any Instrument after the device to play the notes produced from the device.

The comments in the patch explain the programming techniques behind the device; while I tended to not repeat the same comments over iterated procedures (where the same code is copied many times), the black comments explain low level code (single objects interaction), and the green comments explain some higher level approaches.

## GUI
<img src="Director view.png" width="767" height="149"/>

<img src="Notes view.png" width="767" height="149"/>