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

# Tilesets

## Animation

  Tileset animation (like 'flowers') is handled in the file `src/tileset-anims.c`.
  The routine `InitTilesetAnim_General` sets the animiation counter and trigger the animation with the callback
  `TilesetAnim_General`.
  Thisroutine appends the animations to a queue of events to process.
  The update happens via `UpdateTilesetAnimations` (`/src/tileset_anims.c`).

## Developing a Day-Night Cycle System

  * Add a routine to read an external clock (how?)
  * Update the palette with the `LoadTilesetPalette` (`src/fieldmap.c`).
