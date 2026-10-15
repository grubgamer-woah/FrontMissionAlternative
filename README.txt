FRONT MISSION ALTERNATIVE - TRANSLATION STUDIO (portable)
========================================================

An editor for the translation of Front Mission Alternative (PlayStation).
It runs entirely on your PC: no account, no internet required.
It comes with the current English translation already loaded.

WHAT YOU NEED
- Windows 10 or 11 (64-bit).
- Your own copy of the original Japanese game as a BIN/CUE disc image:
  "Front Mission Alternative (Japan).bin", clean and unpatched
  (MD5 3aaa987ef3794a78682a94d570eb68b7, 329,701,008 bytes).
  The game is not included. The Studio only reads your file; it never changes or copies it.
- About 1 GB of free space (each build writes a 330 MB disc image).

FIRST START
1. Optional: copy your Japanese .bin into the "Put your game here" folder.
2. Double-click "Start Translation Studio.bat".
3. A setup window appears. If you used step 1 the file is already filled in;
   otherwise press Browse and pick your .bin wherever it is. Press Start.
4. Setup checks the disc, unlocks the translation data and builds the English
   base image (under a minute). Your browser then opens the Studio at
   http://127.0.0.1:8796

Later starts skip setup and open the Studio directly.
- Moved your game file? Double-click "Change Game Location.bat".
- To shut the Studio down, double-click "Stop Translation Studio.bat"
  (closing the browser tab leaves it running in the background).

USING THE STUDIO
- Pick a tab (dialogue, briefings, menus, shops, prompts, bitmap text...), select an
  entry, type the English and press "Save entry". Edits save automatically to
  workspace\session.fma.json; "Undo" (Ctrl+Z) steps back.
- "Validate" checks every limit (line lengths, shared memory, scene sizes).
- "Build xdelta" creates a new folder in "builds" containing:
    FMA-studio.bin / FMA-studio.cue        - the patched English game, ready for an emulator
    FMA-studio-from-Japan.xdelta           - a patch to share; apply it to the clean Japanese .bin
- "Export project" saves a copy of all your edits in "exports"; "Open project" loads one.
- Start the patched game from a fresh boot (old save states can bring back old text).

HOW THE GAME DATA IS HANDLED
The parts of the Studio that come from the game (the base disc image patch and the
Japanese text tables the editor shows) are stored in data\locked-pack.bin, locked
with a key that only the clean Japanese disc provides. Setup unlocks them into
"sources" on your PC. Bitmap text uses Windows' own Arial font, copied from
C:\Windows\Fonts during setup.

TROUBLESHOOTING
- "does not match the clean Japanese disc": the file is patched, a different
  release, or a different dump. Use the original unpatched Japanese BIN.
- The Studio does not open: see settings\server.log for the error.
- Something else uses port 8796: close that program and start again.
- To start over completely, delete the "settings" folder (your translation in
  "workspace" is kept).
- The opening cinematic is VERY finnicky to translate, even a one line difference causes bugs
- Only latin text is usable, feel free to try and incorporate other types of alphabets into the code!

INCLUDED THIRD-PARTY SOFTWARE
runtime\python  - Python 3.12 (PSF license, runtime\python\LICENSE.txt)
Pillow, Capstone - sources\3 Scene Prototype\tools\python_packages (licenses in their dist-info folders)
xdelta3 3.0.11   - sources\3 Scene Prototype\tools (Apache License 2.0)


Licensing and use information:
This software, or any derivitive, fork, etc using code from this software is to be used only for non-commercial purposes. Charging money, or recieving "donations" in exchange for distribution of this software or any translation made with it (or any derivitive) is hereby completely prohibited.

If you intend to use this to make your own translation, I only ask that you credit the "Guild of Remembrance" in your eventual release

Happy translating!
