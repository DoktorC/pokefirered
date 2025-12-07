# Modification of the New Game

  * folder: src
  * File: new_game.c

  You can change a lot of settings concerning the new game scene.
  For instance, you can set spawning point of the player after the Oak Speech scene (function `WarpToPlayersRoom`).

# Sound Modification

  * folder: sound

  Sounds (pkm cries, background music, .../) are stored in this folder.
  The sounds are ASM snippets, which trigger the GBA sound system.
  It is possible to convert WAV files to ASM or MIDI to to ASM through the tools `wav2agb` and `midi2agb`.

  When adding a new sound, you have to update the related .inc files and add an entry in the linker script.
