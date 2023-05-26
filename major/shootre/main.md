# Shootre

[GitHub](https://github.com/wolfboyft/shootre)

Shootre is my current main project, as of 2023-05-19.
It is going to be a base engine for top down shooters, which will allow for content to be put on top.
I am planning to create a game called Hope & Rage that is content (levels, dialogue, etc) packaged with a version of shootre to use it.

It's not a perfectionist project (i.e. not a dream game of mine), but I do sometimes put extra effort in to make features better than they need to be, to practise making them and to make references for when those features are used in perfectionist projects.

Projectiles are implemented into the collision engine as directed line segments representing a point (the projectile) moving from one position to the next, which stop on tilemap collisions or entity collisions, whichever happens the least far along the segment.

## Screenshots


In this image, a shotgun is being fired into the distance, the tilemap is visible, and the other actor has been shot with a shotgun already.

<img src="../../images/shootre_screenshot.png?raw=true"/>
