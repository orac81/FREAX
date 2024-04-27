
  FREAX  - Help and notes.
  ------------------------
  
FREAX is a simple Alien shootem-up game that compiles for the VIC20, CBM64 & CBM16/+4.
It is very playable, and yet it is only 2K in size!

The files in this archive are:

freax.txt        - this file.

freax.s          - CA65 compatible 6502 assembler source code.

freax-c64.prg    - Commodore 64 version.

freax-v20.prg    - VIC20 version (unexpanded).

freax-c16.prg    - Commodore 16 or Plus-4 version.


To move left/right use keys I,P.   hit SHIFT to fire. To exit game hit key X.
In the title screen you can select different modes by hitting M key. 
For a fast game select 1 (bit 0). For a simpler "classic" alien motion, select 2 (bit 1). For both, 3..

When the aliens move, different rows move in the opposite direction.
The game has a pattern of alien movements that span over 8 levels, each level lower and more difficult.
After 8 levels, the game "wraps" and keeps playing, but at a faster speed.
When an alien reaches the bottom, or you use all your lives, the game is over.
HINT: When shooting, shave the "side" aliens first, then try to eliminate all the ones going in one particular direction.

Compiling the source.
---------------------
The source code is included, and released under the GNU GPL3 licence (see end of this document).

FREAX is a "work in progress" - I started it as a little test program for my own 6502 assembler a long time ago.
It is now quite playable, even though I intend to add more at some stage. It has a few interesting ideas, so its worth a look.
It is very compact, currently about 2k. Most of the glitches and bugs on previous versions have been fixed.

The colour is simple pre-fixed areas. (like the old games when they used coloured tape over a b/w monitor!) 
The VIC20 version may be better with a wider screen, say 28 columns.

The single source file comiles to multiple targets, with condition .if .. .endif macros selecting the code for the right targets.
When Compiling set either  IS_V20, IS_C64, IS_C16  to 1, the others to zero. 
Note: other target systems not yet done.

I modified my asm to mostly match CA65. Ensure paths CC65_INC and CC65_LIB are set.
To compile under CA65 set the USE_CA65 flag. I set target system to "none" to kill
request for Segment settings - its a bit of a kludge, and to be honest I coded for my own 
assembler, ASM502, which is a CA65 subset.

Anyway thats it for now. Enjoy!


=======================================================================
The source code is released as free software under the GNU GPL3 licence,
see GNU website:      www.gnu.org/licenses/gpl-3.0.html 
=============================================================================
