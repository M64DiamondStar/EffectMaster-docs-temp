---
description: Use the EffectMaster API to start a show!
---

# Starting a show

## Java

{% code lineNumbers="true" %}
```java
Show show = new Show("category", "name"); // Get a show instance
show.play(); // The general start option
show.playFrom(1); // Start a show from a specific effect ID
show.playOnly(1); // Only play one effect from a show
```
{% endcode %}

## Kotlin

{% code lineNumbers="true" %}
```kotlin
val show = Show("category", "name") // Get a show instance
show.play() // The general start option
show.playFrom(1) // Start a show from a specific effect ID
show.playOnly(1) // Only play one effect from a show
```
{% endcode %}
