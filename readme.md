# Lo-Fi Piano Patch/Preset/Sample Pack.
This repository consists of an all around breaking-out of a custom sound I've designed to emulate the sound of a piano being played off of a warbled
tape cassette using my Korg Monologue.  As an example of getting the most out of my hardware, I'm attempting to create a soundfont using Polyphone to
get around the monophonic limitations of the Monologue by sampling its own sound and triggering these samples with the Monologue using MIDI.


## Sampling Proccess
The first step is to record a complete range of 85 notes of varying lengthto give the patch a _responsive_ feel by allocating for velocity.  The Monologue's
keyboard recognizes __six__ varying levels of velocity to simulate __how hard__ the key is being hit; for our purposes we will record six tracks of
the complete 85 note range, each with a different `decay` parameter applied to each of the notes for a gradient of short to long notes.

The result is a set of 85 keys that ring out depending on how hard they're hit.  With each key having six different ways to be played, in all the
system has 510 different sounds it can make.  That being said; as of initial uploading the individual notes have not been sliced into their appropriate
sample files.


## Soundfont Tuning
Once all 510 sounds have been processed and extracted as sound files we can begin to build our soundfont in Polyphone.
