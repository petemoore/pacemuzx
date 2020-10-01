Pac-Man Emulator for Sinclair Spectrum (v1.5)
---------------------------------------------

This program requires a Spectrum +2A/+2B/+3, and won't work on earlier models.

The Pac-Man ROMs cannot be supplied with this program, so you must supply your
own copies of the following files (from the Midway ROM set):

  pacman.6e pacman.6f pacman.6h pacman.6j

Copy them to the same directory as this file, then perform the following steps:

* Install https://github.com/simonowen/tile2sam (e.g. in a python3 virtual environment)
* Build/install https://github.com/mkoloberdin/pasmo
* Run `make.bat` (Windows) or `make dist` (Mac/Linux/Un*x)
* Mac/Linux/Un*x: Copy/move the `pacman.6*` ROM files into the generated `dist` directory,
  `cd dist` and run `make` to generate `pacemuzx.tap`

Then load the .tap tape image in a Spectrum emulator of your choosing (making sure
to select a Spectrum +2A/+2B/+3 model, as noted above).

Controls:

  1 = 1 player start
  2 = 2 player start
  3 = insert coin (NOTE: you need to do this first, once per player!)

  C = colour sprites
  M = mono sprites
  H = hard difficulty (hold during ROM boot)

  Cursor keys, Q/A/O/P, Kempston/Sinclair joysticks = joystick control

  Sym-1 to Sym-7 = set display colour, add Shift for bright

Many thanks to #zx and WOS for feedback and testing :)

Enjoy!

---

Version 1.5 (2016/11/19)
- Fixed code overflow crash on mono/colour toggle (thanks Matthew Logue)
- Changed maze colours to be bright by default, with Shift to dim
- Changed green ghost to non-bright yellow, to be closer to orange original

Version 1.4 (2014/03/01)
- Added support for diagonal control inputs from keyboard and 8-way joysticks

Version 1.3 (2012/01/08)
- Added run-time colour/mono sprite selection
- Added boot-time selection of Hard difficulty
- Restored traditional blue/white maze flash when using blue/white colours
- Restored sprite trimming at maze edges in colour version
- Added loading message to show version number

Version 1.2 (2011/12/06)
- Added colour sprites
- Added Spectranet support, to prompt for trap disable
- Added key combos to change maze colour
- Maze flash now toggles current bright instead of blue
- Various minor fixes and speed-ups

Version 1.1 (2011/11/09)
- Added DivIDE support, using pages 3+0 for ROM if present
- Improved control handling, favouring newest direction pressed
- Holding a key after loading delays the emulation starting until released
- Moved Blinky's downward-facing mouth down a pixel

Version 1.0 (2011/11/08)
- Initial release

---

Simon Owen
http://simonowen.com/spectrum/pacemuzx/
