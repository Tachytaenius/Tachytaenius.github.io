# Game Boy Tiles

[GitHub](https://github.com/Tachytaenius/gameboytiles)

Game Boy Tiles is my first successful attempt at tiled movement with map loading etc on the Game Boy.
It was very difficult to debug, but I am fairly skilled at debugging for the Game Boy (using the BGB emulator).

The movement system is fairly simple at its core: if you're stationary, pressing the d-pad into a movable tile will cause you to start a moving animation, and when it finishes, your position will update.
But it also has things like warps and slippery floors!

Maps are made in Tiled and converted using a tool I wrote in Lua.

## Screenshots

In the starting house

<img src="../../images/gameboytiles_screenshot_1.png?raw=true">

Outside of the starting house

<img src="../../images/gameboytiles_screenshot_2.png?raw=true">

Slipping on ice, good for puzzles

<img src="../../images/gameboytiles_screenshot_3.png?raw=true">
