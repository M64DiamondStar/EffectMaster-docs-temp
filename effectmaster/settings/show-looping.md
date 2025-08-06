---
description: >-
  Do you have a show you want to automatically start every x ticks? You can do
  that with show loops!
---

# Show Looping

## How to edit show looping?

1. Open the show editor by using `/em editor <category> <name>`
2. Click on the button called `Settings`
3. On this page you can edit the values. You can enable or disable show looping, you can edit the delay and you can edit the interval!



## How does it work?

When the server starts, the plugin registers all shows which have looping enabled. When the server has successfully started up, EffectMaster will create a new running task that will check each tick if a show needs to be run.&#x20;

### Looping Delay

The delay of the show is the amount of ticks between the server startup and the first time the loop gets played. After that it plays according to the looping interval

### Looping Interval&#x20;

After the show has run for the first time, the interval descides how many ticks are between each loop. It does this by checking if the passed time in ticks - the looping delay is dividable by the interval. This also means that it may look like it sometimes won't work correctly when you're editing the looping settings while the server is enabled, but it actually works fine!
