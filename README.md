# Tetris

Made for CS349 (User Interfaces) at the University of Waterloo, Fall 2016.
**Source code will be available after Aug 2017**

## Description
Tetris is a classic arcade game in which a random sequence of pieces fall from the top of a playing field that is 10 squares wide and 24 squares high. The piece stops falling (and a new piece begins to fall) when it encounters the bottom of the playing field or rests on top of previously fallen pieces. The player manipulates the falling piece to position it from side to side or to rotate it to achieve a packing at the bottom that leaves few gaps. Each time an entire row is filled, it disappears and any pieces above it fall to fill in the gaps. The game ends when the playing field fills so that there is no room for new pieces.

## Requirements

1.  Respond to the following keyboard events to manipulate the currently falling piece:

    | Game Action | Keyboard | Numpad |
    | --- | --- | --- |
    | **Move Left** | LEFT Arrow | Numpad 4 |
    | **Move Right** | RIGHT Arrow | Numpad 6 |
    | **Drop** | Space Bar | Numpad 8 |
    | **Rotate Right** | UP Arrow, X | Numpad 1, 5, 9 |
    | **Rotate Left** | Control, Z | Numpad 3, 7 |
    | **Pause** | P | --- |

2.  Respond to the following mouse events to manipulate the currently falling piece:

    | Event | Action |
    | --- | --- |
    | MousePress (on unselected falling piece) | Select the piece for further manipulation |
    | MouseMotion | Selected piece follows the mouse from side-to-side. |
    | MouseWheel | Rotate the selected piece. |
    | MousePress (on selected falling piece) | Drop the selected piece into position. |

    Note that there is a mouse press to select a piece but the mouse does not need to stay pressed to act on the piece further.

3.  Code to process the following command-line arguments is provided. You will make use of the arguments in the obvious ways in your code:
    *   -fps _n_: Set the frames per second (FPS) to _n_. Default to 30FPS. Your program may be tested with values as small as 1 or as large as 60.
    *   -speed _n_: Adjust the speed so that a falling block traverses the playing field from top to bottom in _n_ seconds, where _n_ is a double. Default to 7.0 seconds. Your program may be tested with values as small as 2.0 and as large as 20.0.
    *   -seq _s_: Specify a sequence of shapes that should fall (for testing purposes). Each shape is specified by one of the letters `ILJSZOT`. When the sequence is exhausted, simply repeat from the beginning.
4.  Use `javax.swing.Timer` to animate the falling pieces. Changing the speed should leave the FPS unchanged. Similarly, changing the FPS should have no effect on the speed.
5.  Handle window resize events appropriately while the game is paused. You may assume that the window will not be resized during game play.
6.  Implement a splash screen with instructions for play.

## Extra Features

Scoring - Each line cleared gives points proportional to level

Levels - Each level increments at 10 lines cleared. At each level increment, pieces fall 60% faster. 

Soft Drop - DOWN key drops the block by 1 piece

Quit - Q key restarts the game

Next Piece - Preview of the next piece
