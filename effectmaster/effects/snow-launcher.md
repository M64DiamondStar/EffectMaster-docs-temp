---
description: Emits snow particles with spread over a specific time span.
---

# Snow Launcher

## Parameters

<table><thead><tr><th width="151.33333333333331">Parameter</th><th width="339">Information</th><th>Example</th></tr></thead><tbody><tr><td>Location</td><td>The location of the block.</td><td><code>world, 196, 64, -381</code></td></tr><tr><td>Velocity</td><td>In which direction should the snow shoot.</td><td><code>0, 1, 0</code></td></tr><tr><td>Amount</td><td>The amount of particles to spawn each shot.</td><td><code>5</code></td></tr><tr><td>Spread</td><td>Works the same as the randomizer parameter. It spreads out the shots a little bit. Try to keep this at low values for the best effect.</td><td><code>0.3</code></td></tr><tr><td>Force</td><td>Whether the particle should be forcibly rendered by the player or not.</td><td><code>false</code></td></tr><tr><td>Duration</td><td>The duration of the effect in ticks.</td><td><code>40</code></td></tr><tr><td>Interval</td><td>Every how many ticks it should shoot snow. For example if set to <code>5</code> it'll shoot every 5 ticks. </td><td><code>5</code></td></tr><tr><td>StartUp</td><td>The time it takes to display the full amount of particles. Set to <code>0</code> to disable it.</td><td><code>20</code></td></tr><tr><td>Delay</td><td>The amount of ticks this effect waits after the show starts before its activation.</td><td><code>40</code></td></tr></tbody></table>

<details>

<summary>YML Preset</summary>

{% code lineNumbers="true" %}
```yaml
'1':
  Type: SNOW_LAUNCHER
  Location: world, 0, 0, 0
  Velocity: 0, 1, 0
  Amount: 3
  Force: false
  Duration: 100
  Interval: 1
  StartUp: 0
  Delay: 0
```
{% endcode %}

</details>
