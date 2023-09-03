# Alive

Alive is one of my dream games.
It's supposed to be a top-down 2D experience.
The intention is to make an immersive survival game with/simulating things such as:
- Soil constituents
- Grass health
- A unique top-down far vision system
- View occluded/recoloured by walls/coloured glass
- Hunting
- Underground areas (like in the 2D game Minicraft)
- Fluid dynamics with conservation of total water quantity

...and  much else besides.

The idea has currently spawned two repositories:
- [Alive-old](https://github.com/Tachytaenius/Alive-old) (initial commit 2018-09-16), which has a few iterations within its (very bad) commit history
- (As of 2023-09-03) [Alive](https://github.com/Tachytaenius/Alive) (initial commit 2022-09-20) for which I used issues to track to-dos, which was not necessarily wise.

They both use the LÖVE framework, and the latter was doing very well until I hit limitations in Lua that were difficult to overcome, at which point I decided the next (and as always, hopefully final) iteration of the project would be made in Rust, very likely using the Bevy game engine.

## A screenshot of Alive

In the image, you can see a small "biome" of less healthy grass, and the view occluded by lots of randomly-placed walls of earth.
Everything is smoother and more blended than in the previous attempt.

<img src="../../images/alive_screenshot_1.png?raw=true"/>

## A screenshot of Alive-old

In this image, the grass health is randomised, and there is another entity.
In the bottom right is an exertion graph, and the current amount of food and water and how full the playeer is.
In the bottom left is the player's health.
You can punch and kill the other entity, which is not much different to the player besides not being the player entity.

<img src="../../images/alive_screenshot_2.png?raw=true"/>

## Alive Rendering

[Alive Rendering Document](https://github.com/Tachytaenius/Alive/blob/c4d48c654266a84f44e3007db65e07055ee8f89b/docs/rendering.md)

The GLSL shaders responsible for the black view occlusion behind the wall blocks scattered on the grass was a good technical achievement (as was the crushing of things further away to let you see further), though the basic method is not particularly well-optimised and will need to be redone for a future iteration.
It essentially marches through all fragments from player eye position to current fragment position, filtering the current colour with the `min` function (to black in the case of an opaque wall).
It also reveals part of the texture of a wall before letting it filter.
The shader can be found [here](https://github.com/Tachytaenius/Alive/blob/c4d48c654266a84f44e3007db65e07055ee8f89b/shaders/lighting.glsl).
An earlier, lower-quality version of the shader can be found in the Alive-old repository [here](https://github.com/Tachytaenius/Alive-old/blob/ff3e96adeeabe35ce96fee8b76103865a1a81513/resources/shaders/light.glsl).
