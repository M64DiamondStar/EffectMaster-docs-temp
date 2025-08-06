---
description: Play a sound effect from a location or to a specific selection of players.
---

# Sound Effect

## Parameters

<table><thead><tr><th width="155">Parameter</th><th width="280.3333333333333">Information</th><th>Example</th></tr></thead><tbody><tr><td>Location</td><td>The location to play the Sound Effect at.</td><td><code>world, 196.3, 64, -381.8</code></td></tr><tr><td>Selector</td><td>The selection of players who are able to hear the sound. The @e and @s selectors do not work!</td><td><code>@a[distance..5]</code></td></tr><tr><td>Sound</td><td>The sound to play, this can also be a custom sound from a resourcepack.</td><td><code>minecraft:entity.pig.ambient</code></td></tr><tr><td>SoundSource</td><td>The category of the sound. This can be: <code>AMBIENT</code>, <code>BLOCKS</code>, <code>HOSTILE</code>, <code>MASTER</code>, <code>MUSIC</code>, <code>NUTRAL</code>, <code>PLAYERS</code>, <code>RECORDS</code>, <code>VOICE</code>, <code>WEATHER</code>.</td><td><code>MASTER</code></td></tr><tr><td>Volume</td><td>The volume of the sound, needs to be greater than <code>0.0</code></td><td><code>2.0</code></td></tr><tr><td>Pitch</td><td>The pitch of the sound, needs to be a value between <code>0.0</code> and <code>2.0</code>.</td><td><code>0.5</code></td></tr><tr><td>Delay</td><td>The amount of ticks this effect waits after the show starts before its activation.</td><td><code>40</code></td></tr></tbody></table>

<details>

<summary>YML Preset</summary>

{% code lineNumbers="true" %}
```yaml
'1':
  Type: SOUND_EFFECT
  Location: world, 0, 0, 0
  Selector: 'null'
  Sound: minecraft:entity.pig.ambient
  SoundSource: AMBIENT
  Volume: 1.0
  Pitch: 1.0
  Delay: 0
```
{% endcode %}

</details>

## Youtube Tutorial

Doesn't exist yet :(
