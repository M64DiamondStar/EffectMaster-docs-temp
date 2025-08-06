---
description: Do you want to customize EffectMaster even more? Create your own effects!
---

# Creating a custom effect

This is an example of how a custom effect is structured and registered.

## Java Example

### Effect Class

{% code lineNumbers="true" %}
```java
package org.yourname.yourplugin;

import me.m64diamondstar.effectmaster.locations.LocationUtils;
import me.m64diamondstar.effectmaster.shows.EffectShow;
import me.m64diamondstar.effectmaster.shows.utils.Parameter;
import me.m64diamondstar.effectmaster.shows.utils.ShowSetting;
import org.bukkit.Bukkit;
import org.bukkit.Location;
import org.bukkit.Material;
import org.bukkit.Particle;
import org.bukkit.entity.Player;
import org.jetbrains.annotations.NotNull;
import org.jetbrains.annotations.Nullable;

import java.util.ArrayList;
import java.util.List;

public class CoolEffect extends Effect {

    /**
     * The execute method of the effect. This method is called when the effect should be executed.
     *
     * @param players    the list of players when it's played privately. This list will be null if the effect should be played for everyone.
     * @param effectShow the show the effect is placed in
     * @param id         the index of the effect
     */
    @Override
    public void execute(@Nullable List<? extends Player> players, @NotNull EffectShow effectShow, int id, Set<ShowSetting> settings) {
        String locationString = this.getSection(effectShow, id).getString("Location");
        Location location = LocationUtils.INSTANCE.getLocationFromString(locationString); // Use the location utils to retrieve the location from the string.
        int amount = this.getSection(effectShow, id).getInt("Amount"); // Get the amount of particles to spawn.

        if (players == null) {
            players = new ArrayList<>(Bukkit.getOnlinePlayers());
        }

        for (Player player : players) {
            if (location != null) {
                player.spawnParticle(Particle.FLAME, location, amount, 0.5, 0.5, 0.5, 0.3); // Create whatever cool visual effect you want.
            }
        }
    }

    /**
     * The default parameter setup of the effect. Check the ParameterType class for available types.
     *
     * @return the default parameters
     */
    @NotNull
    @Override
    public List<Parameter> getDefaults() {
        List<Parameter> list = new ArrayList<>();

        /*
         * Add parameters here.
         * The first value is the name of the parameter.
         * The second value is the default value.
         * The third value is the description.
         * The fourth value is the type of the parameter. This is needed so the plugin can correctly save the value in the config.
         * The fifth value is the validator. This checks whether the parameter is valid, or the player should re-enter the value.
         */
        list.add(new Parameter(
                "Location",
                "world, 0, 0, 0",
                "The location at which the particles should spawn.",
                value -> value,
                value -> LocationUtils.INSTANCE.getLocationFromString(value) != null
        ));

        list.add(new Parameter(
                "Amount",
                10,
                "The amount of cool particles to spawn.",
                Integer::parseInt,
                value -> {
                    Integer intValue = toInteger(value);
                    return intValue != null && intValue > 0;
                }
        ));

        list.add(new Parameter(
                "Delay",
                0,
                "The delay between the start of the show and this effect.",
                Integer::parseInt,
                value -> {
                    Integer intValue = toInteger(value);
                    return intValue != null && intValue > 0;
                }
        ));

        return list;
    }

    private Integer toInteger(String value) {
        try {
            return Integer.parseInt(value);
        } catch (NumberFormatException e) {
            return null;
        }
    }

    /**
     * The description of the effect. This will be shown when the user hovers over the effect in the effect creation gui.
     *
     * @return the description
     */
    @NotNull
    @Override
    public String getDescription() {
        return "A super cool effect.";
    }

    /**
     * The display material of the effect. This material is used in the guis.
     *
     * @return the display material
     */
    @NotNull
    @Override
    public Material getDisplayMaterial() {
        return Material.DIAMOND;
    }

    /**
     * This is the identifier (with other words, the name) of the effect.
     *
     * @return the identifier
     */
    @NotNull
    @Override
    public String getIdentifier() {
        return "COOL_JAVA_EFFECT"; // The effect won't load if the identifier already exists from another effect.
    }

    /**
     * Tells whether the effect should be run synchronously or asynchronously.
     *
     * @return true if the effect should be run synchronously and false if it should be run asynchronously
     */
    @Override
    public boolean isSync() {
        return false;
    }

}

```
{% endcode %}



### Main Class

{% code lineNumbers="true" %}
```java
class YourPlugin extends JavaPlugin(){

    @Override
    public void onEnable() {
        // Register the effect when your plugin enables
        Effect.Type.registerExternalEffect(new CoolEffect(), this);
    }
    
}
```
{% endcode %}





## Kotlin Example

### Effect Class

{% code lineNumbers="true" %}
```kotlin
package org.yourname.yourplugin

import me.m64diamondstar.effectmaster.locations.LocationUtils
import me.m64diamondstar.effectmaster.shows.EffectShow
import me.m64diamondstar.effectmaster.shows.utils.Effect
import me.m64diamondstar.effectmaster.utils.Pair
import org.bukkit.Bukkit
import org.bukkit.Material
import org.bukkit.Particle
import org.bukkit.entity.Player

import me.m64diamondstar.effectmaster.locations.LocationUtils
import me.m64diamondstar.effectmaster.shows.EffectShow
import me.m64diamondstar.effectmaster.shows.utils.Effect
import me.m64diamondstar.effectmaster.shows.utils.Parameter
import me.m64diamondstar.effectmaster.shows.utils.ShowSetting
import org.bukkit.Bukkit
import org.bukkit.Material
import org.bukkit.Particle
import org.bukkit.entity.Player

class CoolKotlinEffect: Effect() {

    /**
     * The execute method of the effect. This method is called when the effect should be executed.
     * @param players the list of players when it's played privately. This list will be null if the effect should be played for everyone.
     * @param effectShow the show the effect is placed in
     * @param id the index of the effect
     * @param settings the settings which should be applied for the effect. This can for example be the Play At setting.
     */
    override fun execute(players: List<Player>?, effectShow: EffectShow, id: Int, settings: Set<ShowSetting>) {
        val location = LocationUtils.getLocationFromString(this.getSection(effectShow, id).getString("Location")) // Use the location utils to retrieve the location from the string.
        val amount = this.getSection(effectShow, id).getInt("Amount") // Get the amount of particles to spawn.

        (players ?: Bukkit.getOnlinePlayers()).forEach { // Loop through the list of players.
            location?.let { p1 -> it.spawnParticle(Particle.FLAME, p1, amount, 0.5, 0.5, 0.5, 0.3) } // Create whatever cool visual effect you want.
        }
    }

    /**
     * The default parameter setup of the effect. Check the ParameterType class for available types.
     * @return the default parameters
     */
    override fun getDefaults(): List<Parameter> {
        val list = ArrayList<Parameter>()

        /*
         * Add parameters here.
         * The first value is the name of the parameter.
         * The second value is the default value.
         * The third value is the description.
         * The fourth value is the type of the parameter. This is needed so the plugin can correctly save the value in the config.
         * The fifth value is the validator. This checks whether the parameter is valid, or the player should re-enter the value.
         */
        list.add(Parameter(
            "Location",
            "world, 0, 0, 0",
            "The location at which the particles should spawn.",
            { it },
            { LocationUtils.getLocationFromString(it) != null}
        ))

        list.add(Parameter(
            "Amount",
            10,
            "The amount of cool particles to spawn.",
            { it.toInt() },
            { it.toIntOrNull() != null && it.toInt() > 0 }
        ))

        list.add(Parameter(
            "Delay",
            0,
            "The delay between the start of the show and this effect.",
            { it.toInt() },
            { it.toIntOrNull() != null && it.toInt() > 0 }
        ))

        return list
    }

    /**
     * The description of the effect. This will be shown when the user hovers over the effect in the effect creation gui.
     * @return the description
     */
    override fun getDescription(): String {
        return "A super cool effect."
    }

    /**
     * The display material of the effect. This material is used in the guis.
     * @return the display material
     */
    override fun getDisplayMaterial(): Material {
        return Material.DIAMOND
    }

    /**
     * This is the identifier (with other words, the name) of the effect.
     * @return the identifier
     */
    override fun getIdentifier(): String {
        return "COOL_KOTLIN_EFFECT" // The effect won't load if the identifier already exists from another effect.
    }

    /**
     * Tells whether the effect should be run synchronously or asynchronously.
     * @return true if the effect should be run synchronously and false if it should be run asynchronously
     */
    override fun isSync(): Boolean {
        return false
    }

}
```
{% endcode %}



### Main Class

{% code lineNumbers="true" %}
```kotlin
class EffectMasterTestIntegration : JavaPlugin() {

    override fun onEnable() {
        Effect.Type.registerExternalEffect(CoolKotlinEffect(), this)
    }

}
```
{% endcode %}

