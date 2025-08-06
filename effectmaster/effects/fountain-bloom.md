---
description: A beautiful fountain in the shape of a bloom.
---

# Fountain Bloom

## Parameters

<table><thead><tr><th width="167.33333333333331">Parameters</th><th width="375">Information</th><th>Example</th></tr></thead><tbody><tr><td>Location</td><td>The origin of the fountain in the format of <code>world, x, y, z</code>.</td><td><code>world, 196.3, 64, -381.8</code></td></tr><tr><td>Sequencer</td><td>With the sequencer, you can edit the velocity of the fountain over time. The first number is the time in ticks, the second is the velocity width and the third is the velocity height (ticks:width,height). You can also add multiple values separated by semicolons (ticks1: width1, height1; ticks2: width2, height2; ...).</td><td><code>0: 0.1, 0.8; 50: 0.6, 0.8; 100: 0.1, 0.8</code></td></tr><tr><td>Block</td><td>The <a href="https://hub.spigotmc.org/javadocs/bukkit/org/bukkit/Material.html">block</a> to use as falling block. Items will not work!</td><td><code>BLUE_STAINED_GLASS</code></td></tr><tr><td>BlockData</td><td>The <a href="https://minecraft.wiki/w/Block_states">block data</a> of the block (if it has any). For example an open gate, a rotated stair, ... Use <code>[]</code> to set none.</td><td>[open=true]</td></tr><tr><td>Duration</td><td>The duration of the effect (in ticks!).</td><td><code>20</code></td></tr><tr><td>Amount</td><td>The amount of falling blocks to spawn each tick.</td><td><code>15</code></td></tr><tr><td>Randomizer</td><td>This randomizes the value of the velocity a bit. The higher the value, the more the velocity changes. I suggest keeping this between <code>0</code> and <code>1</code>.</td><td><code>0.5</code></td></tr><tr><td>Delay</td><td>The amount of ticks this effect waits after the show starts before its activation.</td><td><code>40</code></td></tr></tbody></table>

<details>

<summary>YML Preset</summary>

{% code lineNumbers="true" %}
```yaml
'1':
  Type: FOUNTAIN_BLOOM
  Location: 'world, 0, 0, 0'
  Sequencer: '0: 0.1, 0.8; 50: 0.6, 0.8; 100: 0.1, 0.8'
  Block: BLUE_STAINED_GLASS
  BlockData: []
  Duration: 20
  Amount: 15
  Randomizer: 0
  Delay: 0
```
{% endcode %}

</details>

## Preview

<figure><img src="../../.gitbook/assets/fountain_bloom.gif" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
### Sequencer additional information

The general format of the sequencer is:

`tick_a, width_a, height_a; tick_b, width_b, height_b; ...`

But this is not all you can do. You can also set automatic values and set materials in the sequencer.\
\
**Automatic values**

If you want to _skip_ a value you can do that by using an automatic value, formatted as `~`. The plugin will calculate automatically what the value for that tick should be.

Example:&#x20;

```
0: 0.0, 0.0;
50: ~, 0.75;
100: 0.3, ~;
```

\
**Materials**\
You can also add materials in a sequencer to change the block which is used. This can be done by adding an extra value at the end of each section with the material. The automatic values also come in handy here!

Example:

```
0: 0.0, 0.0, RED_WOOL;
50: ~, ~, YELLOW_WOOL;
100: 0.3, 0.75, ORANGE_WOOL;
```
{% endhint %}

