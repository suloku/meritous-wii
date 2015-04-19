## Meritous 1.2 Wii port Release2 by suloku ##
30-june-2009

### Changelog: ###

[R2](https://code.google.com/p/meritous-wii/source/detail?r=2):

-Solved the problem with accessing the help file. The code wasn't parsing the newline character '\r'.
-Added wii controls to help file (helpfile\_wii.txt when building for wii).
-Changed the message given when starting a new game for the wii build.

[R1](https://code.google.com/p/meritous-wii/source/detail?r=1):

-initial release

### Original Meritous: ###
http://www.asceai.net/meritous/

MERITOUS v 1.2
for Windows 98/2K/XP/other operating systems
by Lancer-X/ASCEAI

### Controls: ###


**USB Keyboard:**

Arrow keys - Move around. To walk through doors, simply walk up to
> them and push against them.

Space      - Charge your PSI circuit for attacking.

Escape     - Exit the game.

H          - View the help file.

Tab        - View the map (you can then use the arrow keys to scroll
> around the map, speed up holding space).

Enter      - Activate a trigger tile that you are standing on.
> Enter is also used for various other things, such as
> for reading in-game dialogue.

P          - Pause the game.

**Wiimote:**

Arrow keys - Analog Pad
Space      - B
Escape     - Home
H          - One
Tab        - Minus
Enter      - A
P          - Plus

**Classic:**

Arrow keys - Analog Pad
Space      - B
Escape     - Home
H          - Minus
Tab        - X
Enter      - A
P          - Plus

**Gamecube:**

Arrow keys - Analog Pad
Space      - A
Escape     - Start
H          - Z trigger
Tab        - Y
Enter      - B
P          - X

### Cheats: ###

"Those who seek power, should have been granted with a great sense of coordination to "trigger" a new source of energy".

Note: this isn't a cheat I added or that's in the pc game, but some debug code I thought could work and be fun as a cheat.

### Other notes: ###

I haven't tested myself, but it should work if run from a usb device from homebrew channel or another app passing the first argument as the file path such as "usb:/apps/meritous/boot.dol".


### Known bugs: ###

-For some reason there's some code regarding the title screen that will code dump. I tried backtracing it but I couldn't see the failure, so that part of code only compiles for the pc version. Anyway I'm still yet to notice what that code does to the game, so it doesn't affect gameplay.


### Source notes: ###

-Only modified files are: levelblit.c, ending.c and help.c
-The source should compile exactly just like original 1.2 source when using Makefile.pc.
-With the current sdl-wii release you can't compile the source, as there are some audio problems. Also the PAL display isn't fixed. I had solved that myself to just find that afterwars sdl-wii's svn got the same changes.

### Compiled with: ###

SDL-WII svn rev 55 and it's dependencies: libfreetype, libpng, libmpeg and libtremor.
libogc svn rev 3608 (global rev 3643)
libfat svn rev 3635 (global rev 3643)