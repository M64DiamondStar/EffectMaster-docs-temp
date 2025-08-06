---
description: EffectMaster is a powerful plugin to create shows with, but how do you use it?
---

# Creating your first show

## Some important things to remember

* Most plugins will only use a name to store data but EffectMaster uses a category and a show name! You'll notice this in a lot of commands for example.
* All timings are currently measured in ticks! `1 tick = 0.05 seconds` or `1/20 of a second.`

***

## Creating a show

### Creating a new show

Use `/em create <category> <name>` to create your first show! Replace `<category>` with the name of the category, this can be any name you want.. Replace `<name>` with the name of the show you want to create, this can also be any name you want.

{% hint style="info" %}
Make good use of categories, it can come in very handy when u have a ton of shows.
{% endhint %}



### Creating a new effect

Use `/em editor <category> <name>` to open the in-game editor of a show. After that, click on `New Effect` and choose an effect to your liking! We'll use the Particle effect in this example.



### Editing an effect

After you have created a new effect you'll be automatically redirected to the main editor, you can also see that your effect is now in the effect list! Click on the effect to start editing it, you can also see the ID of the effect next to it's name, this may come in handy later.

In the effect you'll see a lot of paper items. Every paper is a different so called 'parameter', the settings which will decide how your effect will look.

When you click one of the parameters you'll get a (usually) short message containing information about the parameter. Now you can type in chat what you want this parameter to be. If you want more information about an effect and it's parameters you can search it up in the [effects](../effects/ "mention") section.



### Starting a show

There are multiple ways to start a show.

1. If you quickly want to test if the effect you just made/editted looks like how you want it to, you can use the 'Play' buttons in the effect editor and the main show editor.
2. If you want to play the whole show you can use the command `/em play <category> <name>`.
3. If you want to play the effect starting at a specific effect ID, you can use the command `/em play <category> <name> from <ID>`.
4. If you only want to play one effect from a show you can use the command `/em play <category> <name> only <ID>`.
5. If you want to play a show, but only visible to a selected amount of players, you can use the command `/em privateplay <category> <name> <selector>`. Learn more about selectors [here](https://minecraft.wiki/w/Target_selectors).

{% hint style="warning" %}
You need [ProtocolLib](https://www.spigotmc.org/resources/protocollib.1997/) in your server to be able to use private shows!
{% endhint %}

