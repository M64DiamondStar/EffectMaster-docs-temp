---
description: The best plugin to create awesome rides with!
---

# TrainCarts

## General Sign

Do you want to immerse your players even more in the fantastic world of rides? You can use the playshow traincarts sign to start shows when activated by a train!

Here's the format of the sign:

{% code fullWidth="false" %}
```
[train]
playshow
<category>
<name>
```
{% endcode %}



## Only play with passengers

Do you want the show to only be played when there are passengers in the train? No problem! Just add the `-p` parameter to the sign like this:

```
[train]
playshow -p
<category>
<name>
```



## OpenAudioMc Fix

{% hint style="warning" %}
If you're using OpenAudioMC, you'll probably notice that the sign doesn't work for EffectMaster shows. This can be easily fixed by using `emshow` instead of `playshow`!
{% endhint %}

Of course, you'll also need [TrainCarts](https://www.spigotmc.org/resources/traincarts.39592/) and its dependency [BKCommonLib](https://www.spigotmc.org/resources/bkcommonlib.39590/).
