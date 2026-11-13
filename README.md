# Shrek 2 Web

Experimental PS2 static recompilation of Shrek 2 (PS2, USA) for desktop browsers.

Play at https://down1oads.github.io/SHREK2WEB/

On the first visit, select your own Shrek 2 PS2 USA ISO (1,264,648,192 bytes). The page copies it into
this browser's private site storage, so later visits start the game automatically. The disc is never
uploaded. To use a different disc or free the space, open https://down1oads.github.io/SHREK2WEB/?change-disc
and choose "Forget the stored disc". The same page has the 30 FPS mode switch for slower devices (the game
still runs at full speed; only every other frame is shown). Outside 30 FPS mode the game renders at twice
the PS2 resolution.

The disc boots as on a console: its loader plays the intro movie and then starts the game.
Tested: intro, title menu, new game, story intro, memory card, and the first level. The rest of the game is
unverified; this is a work in progress.

Use current Chrome, Edge, or Brave with WebGPU and hardware acceleration. Click the game or press a key to
enable audio. Controls: see [CONTROLS.md](CONTROLS.md).

The player keeps the original game logic and uses ps2-web-recomp, which statically recompiles EE code to
WebAssembly while modeling PS2 hardware and interpreting the IOP. Upstream:
https://github.com/snuri00/ps2-web-recomp. Its MIT license is included in LICENSE-runtime.txt.
Shrek 2 belongs to its respective rights holders; this is an unofficial project.

## Hosting

Prebuilt static files served from the main branch root by GitHub Pages. The service worker supplies the
cross-origin isolation headers threaded WebAssembly needs, so a first visit may reload once.
