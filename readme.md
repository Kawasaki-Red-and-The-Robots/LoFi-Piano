# Lo-Fi Piano Patch/Preset/Sample Pack.
This is a little piano sound patch I noodled off of my magic Korg Monologue, probably pretty useful for making lo-fi stuff.  

Currently a work in progress as I get better at managing my time between work and practice and projects, but I digress.

For me, I intend to use the soundfont as a way to get around the monophonic limitations of the Monologue by sampling it's own sound and then using it to trigger said sound off a computer using MIDI.


## Considerations
The Monologue is monophonic, but it's a great MIDI controller and even greater piece of sound design equipment; for starters it has six key `velocity tracking` channels, meaning each key is sensitive to how hard they're being hit.  

I want this set to use the `velocity` tracking to indicate `decay`; the harder the key is hit the longer the note will play out.  

So that means that for each of the 72 notes being recorded six different versions must be produced, each with a longer `decay` time than the last and bringing the total sample count up to 432 distinct sounds to be processed.


## The Sampling Proccess
I use Audacity for recording and editing sound.  In the `sample-tracks.aup3` file temporarily included in the repository, we have recorded the full range of keys for every step on the `decay` parameter into their own channels.

These channels then have a Noise Gate applied with a reduction of -100dB and then detached along silences.  Then, each and every note in the project is selected and then normalized.

After slicing and normalizing, the next step is labelling each note in step from E2 through E7 along with an extension denoting it's `velocity` channel.  The nomenclature goes like: `E1.V1::E7.V6`.  
Once the notes have been labeled, we export as multiple`.ogg` files based on labels.  

It's important to remember to only do one track at a time because exporting like this is a multi-track, time-based thing so if you leave two tracks in muted then you may end up with a sound file with parts of two notes.


## Soundfont Tuning
Once all 510 sounds have been processed and extracted as sound files we can begin to build our soundfont in Polyphone.
