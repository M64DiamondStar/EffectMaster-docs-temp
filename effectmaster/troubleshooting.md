---
description: Can't figure out why something isn't working? This page may have the solution!
icon: square-exclamation
---

# Troubleshooting

## My fountain isn't going to the right direction!

First of all, check if your `Velocity` parameter is actually set correctly. If you've already verified that, then check if the location at which your effect spawns, isn't against another block. The hitbox of a falling block is always a full block, no matter which material you use.



## The ... path effect does not go over the location I set!

This may be because the `Smooth` parameter is set to `true`. This will make it so that the effect follows a bezier's curve which doesn't go over the exact locations, but calculates a smooth path between them. If you want to go over the exact locations, set `Smooth` to `false`.



## "The value entered is not possible"

You may get this error when you're using specific mods or plugins (like a chat decoration plugin which modifies the player message). As an alternative, you can use the enter command: `/em enter <value....>`.



## Something else...

Haven't found a solution here? Ask for support in our [Discord](https://discord.com/invite/Scv9afJwXp) server.
