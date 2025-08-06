---
description: If you're not a nerd, get outta here!
icon: code
---

# Developer API

## Repository

{% tabs %}
{% tab title="Gradle (Groovy)" %}
```gradle
repositories {
	mavenCentral()
	maven { url 'https://jitpack.io' }
}
```
{% endtab %}

{% tab title="Gradle (Kotlin)" %}
```kts
repositories {
	mavenCentral()
	maven { url("https://jitpack.io") }
}
```
{% endtab %}

{% tab title="Maven" %}
```xml
<repositories>
	<repository>
		<id>jitpack.io</id>
		<url>https://jitpack.io</url>
	</repository>
</repositories>
```
{% endtab %}
{% endtabs %}

## Dependency

{% tabs %}
{% tab title="Gradle (Groovy)" %}
```gradle
dependencies {
        implementation 'com.github.M64DiamondStar:EffectMaster:1.4.9'
}
```
{% endtab %}

{% tab title="Gradle (Kotlin)" %}
```kts
dependencies {
        implementation("com.github.M64DiamondStar:EffectMaster:1.4.9")
}
```
{% endtab %}

{% tab title="Maven" %}
<pre class="language-xml"><code class="lang-xml"><strong>&#x3C;dependencies>
</strong>	&#x3C;dependency>
		&#x3C;groupId>com.github.M64DiamondStar&#x3C;/groupId>
		&#x3C;artifactId>EffectMaster&#x3C;/artifactId>
		&#x3C;version>1.4.9&#x3C;/version>
	&#x3C;/dependency>
&#x3C;/dependencies>
</code></pre>
{% endtab %}
{% endtabs %}



{% hint style="danger" %}
## Java or Kotlin?

Though it is possible to interact with EffectMaster using Java, I suggest using Kotlin if you understand the language. EffectMaster is written in Kotlin which makes it a lot easier to interact with if you use kotlin yourself.
{% endhint %}

## Using the API

Please select one of the following:

[starting-a-show.md](starting-a-show.md "mention")

[creating-a-custom-effect.md](creating-a-custom-effect.md "mention")
