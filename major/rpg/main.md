# RPG

[GitHub](https://github.com/Tachytaenius/rpg)

RPG is a poorly-named Minecraft-like project using physically-based rendering (PBR) (using the maths library [CPML](https://github.com/excessive/cpml)).
Blocks are organised into cubic chunks each with their own mesh.
In commits before the marching cubes attempt, each block is destructible through different stages (though the clicking doesn't work on Linux due to me not testing on Linux at the time) that have different cracking textures, which affect the normals of the block's texture.

The master branch contains a marching cubes attempt, which wasn't perfect.
It does also demonstrate a dynamically-updating mesh responding to destruction.

In the branch `worldwrap`, the world wraps around, and its generation tiles perfectly.

## Screenshots

Showcasing different damage levels from 0 to block-actually-destroyed, and different grass block side textures depending on whether there is more grass below.
It also shows the outline of the currently highlighted block.

<img src="../../images/rpg_screenshot_1.png?raw=true">

A marching cubes terrain attempt

<img src="../../images/rpg_screenshot_2.png?raw=true">

A weird mask dude test entity.
This is from the `worldwrap` branch.

<img src="../../images/rpg_screenshot_3.png?raw=true">
