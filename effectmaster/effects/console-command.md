---
description: Runs a command from the console.
---

# Console Command

## Parameters

<table><thead><tr><th width="141">Parameter</th><th width="363.3333333333333">Information</th><th>Example</th></tr></thead><tbody><tr><td>Command</td><td>The command to execute WITHOUT a <code>/</code> in front of it.</td><td><code>say EffectMaster is cool!</code></td></tr><tr><td>Delay</td><td>The amount of ticks this effect waits after the show starts before its activation.</td><td><code>40</code></td></tr></tbody></table>

<details>

<summary>YML Preset</summary>

{% code lineNumbers="true" %}
```yaml
'1':
  Type: CONSOLE_COMMAND
  Command: 'say EffectMaster is cool!'
  Delay: 0
```
{% endcode %}

</details>

## Youtube Tutorial

{% embed url="https://youtu.be/BH6qy8Tp_Y0" fullWidth="false" %}
