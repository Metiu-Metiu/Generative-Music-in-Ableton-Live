# Generative-Music-in-Ableton-Live
Max 4 Live device generating melodies and exposing several ways of controls over probabilities and numerical ranges of pitches, harmonies and rhythms. Inspired from Patter by Adam Florin (https://www.ableton.com/en/packs/patter/).

This is a Max for Live (MIDI instrument) device (developed with Ableton Live 9 and Max 7). It produces MIDI note on messages to be used inside an Ableton Live environment.
Drop the generativeNotesControl.amxd file inside any MIDI track in Ableton Live. Then, drop any Instrument after the device to play the notes produced from the device.

The comments in the patch explain the programming techniques behind the device; while I tended to not repeat the same comments over iterated procedures (where the same code is copied many times), the black comments explain low level code (single objects interaction), and the green comments explain some higher level approaches.

## Fragments

Fragments are series of events, where each event can be a note or a rest.

## Representation of rhythmic durations

All rhythmic durations are expressed in Ableton object notation (4n means 1 quarter note, 8n means 1 eight note, ecc.)

## GUI
Histograms usually represents probabilities; each column's value represents the probabilities of the parameter specified below the column. The red dot is a live marker signaling what parameter value is currently being played.

### Misc view

Preset save, load and interpolation (between 2 given presets).
The Rhythm and Fragments sections respectively control the probabilities for rhythmic durations of events (a base value is multiplied or divided by a multiplier/divider), and the probabilities for the number of notes and rests, which can be swapped (either notes first or rests first, for each fragment).

<img src="Misc view.png" width="767" height="149"/>

### Notes view

Specifies the probabilities of different pitches being played. Use the piano keyboard to select the pitches likely to be played.
The duration section can make notes overlap.

<img src="Notes view.png" width="767" height="149"/>

### Director view

Takes care of specifing the seed numbers, or seed numbers probabilities. The seed numbers are used for both pitch and rhythmic generation.
Each histogram's bin represents a fragment's seed (for generative and loop mode).

The indefinite mode explores indefinitely the possibilities offered by 1 and only 1 seed number.
The generative mode can select a new seed at the end of each fragment, depending on that seed's probability.
The loop mode represents the seeds for the loop length in number of fragments.

<img src="Director view.png" width="767" height="149"/>


