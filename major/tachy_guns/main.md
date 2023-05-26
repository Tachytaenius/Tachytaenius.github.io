# Tachy Guns

[GitHub](https://github.com/wolfboyft/tachy-guns)

Tachy Guns is a detailed Dwarf Fortress gun mod using [DFHack](https://github.com/DFHack/dfhack) to add my own functionality into the game.
It is modular not just in the sense that I use multiple files well and pioneered the format in the DFHack modding guide (alongside someone else), but that you can add and remove packs of content, and make your own.

The mod itself is an engine that drives functionality on item definitions etc that use custom data read using [a utility I wrote](https://github.com/DFHack/dfhack/blob/develop/library/lua/custom-raw-tokens.lua) and contributed to the DFHack Lua library, and those item definitions are provided separate to the mod itself.
