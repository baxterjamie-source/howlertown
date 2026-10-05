Howlertown sound files
======================

Put sound files in this folder with exactly these names. Any that are missing are simply silent.
MP3 works everywhere. Keep them short and small (well under 1 MB each), because they load over the internet.

Ambient (Sound panel: "Ambient sounds")
  wind.mp3            Gust of wind. Plays at random during the night.
  howl-distant.mp3    Soft, far-off howl. Plays at random during the night.
  murmur.mp3          Quiet crowd murmur. Loops during the day's discussion. Make it loop cleanly.
  bell.mp3            Village bell. Plays when voting opens.

Events (Sound panel: "Event sounds")
  howl-loud.mp3       Loud howls. When the wolves win.
  howl-card.mp3       A single howl. During the card deal, once for every card drawn (the wolf by the well
                      throws its head back each time), and at nightfall the moment the howling wolf appears
                      in the animation. About 2 seconds long is ideal.
  witch-cackle.mp3    Witch's cackle. At random during the night, only while the Witch is alive.
  wolf-snarl.mp3      Mauling / snarling. At random during the night.
  wolf-attacks.mp3    The wolves attack. 3 to 5 seconds (at random) after the pack agrees on a victim.
                      Doesn't play on a night the wolves can't agree.
  death-reveal.mp3    Door creak or scream. When dawn reveals who died.
  gavel.mp3           Gavel or crowd gasp. When the verdict is announced.
  trapdoor.mp3        Hangman's trapdoor dropping. 1.5 seconds after someone is voted to hang.
  village-win.mp3     The village wins.
  fool-win.mp3        The Town Fool wins (also when the Fool is hanged and the game goes on).

To add variety later, a slot can list several files and one is picked at random:
see the SOUNDS list near the top of the script in index.html.

Each sound also has its own volume in the game (the murmur already plays at 35%, the
distant howl at 60%). If one sounds too loud or too soft in play, ask for it to be adjusted
there rather than re-editing the file.


Preparing files in Audacity (free: audacityteam.org)
====================================================

Sounds from different websites are recorded at very different volumes. Bringing them all
to the same loudness first means nothing blasts or whispers compared with the rest.
(Menu names are from Audacity 3.x.)

One file at a time
------------------
1. File > Open... and choose the sound.
2. Trim it: select any silence or unwanted part at the start or end and press Delete.
   Keep event sounds short (about 1-3 seconds).
3. Optional, for a smooth ending: select the last half second, then
   Effect > Fading > Fade Out. (Do NOT fade murmur.mp3: it has to loop.)
4. Select everything: Ctrl+A.
5. Effect > Volume and Compression > Loudness Normalization...
     Normalize:              perceived loudness
     to:                     -18 LUFS
     Treat mono as stereo:   unticked
   Click Apply. This makes every sound feel about equally loud.
6. Still selected (Ctrl+A), Effect > Volume and Compression > Normalize...
     Remove DC offset:                         ticked
     Normalize peak amplitude to:              -1.0 dB
     Normalize stereo channels independently:  unticked
   Click Apply. This is a safety step so nothing clips or crackles.
7. Optional, to halve the file size: Tracks > Mix > Mix Stereo Down to Mono.
   (Fine for every sound here; mono plays from all speakers.)
8. File > Export Audio...
     Format:        MP3 Files
     Channels:      Mono (or Stereo if you skipped step 7)
     Sample rate:   44100 Hz
     Quality:       Bit Rate Mode = Constant, Quality = 128 kbps
     File name:     exactly the name in the list above, e.g. howl-loud.mp3
   Save it into this sounds folder.

A whole folder at once (set up once, then reuse)
------------------------------------------------
1. Tools > Macro Manager... > New, and name it "Howlertown sounds".
2. Use "Insert" to add these steps, in this order. Click "Edit..." on each to set the values:
     Select All
     Loudness Normalization     perceived loudness, -18 LUFS
     Normalize                  remove DC offset ticked, peak -1.0 dB, channels together
     Mix Stereo Down to Mono
     Export as MP3
3. Click OK to save the macro.
4. To use it: Tools > Macro Manager..., choose "Howlertown sounds", click "Files..." and pick
   all your downloaded sounds. Audacity processes each one and saves the results in a
   "macro-output" folder next to the originals.
5. Trim any that need it (steps 2-3 above), rename each to the exact name in the list,
   and copy it into this sounds folder.

Checking
--------
In the game's lobby, turn on Test mode, then use the Sound button > Test sound to make sure
audio works. Play a test game and listen: if one sound still feels off, say which one and its
in-game volume can be adjusted.
