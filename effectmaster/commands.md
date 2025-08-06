---
description: All the commands currently in EffectMaster!
icon: square-terminal
---

# Commands

{% hint style="warning" %}
The user is required to have the `effectmaster.command` permission to access the `/em` command! If they have the permissions for specific sub-commands but not this permission, it will not work!
{% endhint %}

## Commands

### Cancel Command

Cancels the current editing session when editing an effect parameter. Can be useful when something blocks the ability to chat, modifies your chat message or you just simply want to implement your own system.

<table data-header-hidden data-full-width="false"><thead><tr><th width="135.33333333333331"></th><th></th></tr></thead><tbody><tr><td>Syntax</td><td><code>/em cancel</code></td></tr><tr><td>Permission</td><td><code>effectmaster.command.cancel</code></td></tr></tbody></table>

***

### Create Command

Used to create a new show with a specific name and category.

<table data-header-hidden data-full-width="false"><thead><tr><th width="135.33333333333331"></th><th></th></tr></thead><tbody><tr><td>Syntax</td><td><code>/em create &#x3C;category> &#x3C;name></code></td></tr><tr><td>Permission</td><td><code>effectmaster.command.create</code></td></tr></tbody></table>

***

### Edit Command

Used to edit, create or delete an effect of a show.&#x20;

#### Create

Create a new effect in a show.

<table data-header-hidden data-full-width="false"><thead><tr><th width="136.33333333333331"></th><th></th></tr></thead><tbody><tr><td>Syntax</td><td><code>/em edit &#x3C;category> &#x3C;show> create &#x3C;effect type></code></td></tr><tr><td>Permission</td><td><code>effectmaster.command.edit</code></td></tr></tbody></table>

#### Delete

Delete an effect with a specific ID.

<table data-header-hidden data-full-width="false"><thead><tr><th width="135.33333333333331"></th><th></th></tr></thead><tbody><tr><td>Syntax</td><td><code>/em edit &#x3C;category> &#x3C;show> delete &#x3C;effect ID></code></td></tr><tr><td>Permission</td><td><code>effectmaster.command.edit</code></td></tr></tbody></table>

#### Edit

Edit an effect with a specific ID.

<table data-header-hidden data-full-width="false"><thead><tr><th width="135.33333333333331"></th><th></th></tr></thead><tbody><tr><td>Syntax</td><td><code>/em edit &#x3C;category> &#x3C;show> edit &#x3C;effect ID> &#x3C;parameter> &#x3C;value>...</code></td></tr><tr><td>Permission</td><td><code>effectmaster.command.edit</code></td></tr></tbody></table>

***

### Editor Command

Opens the editor GUI of a show. You can also specify an ID to open the effect editor of that effect.

<table data-header-hidden data-full-width="false"><thead><tr><th width="135.33333333333331"></th><th></th></tr></thead><tbody><tr><td>Syntax</td><td><code>/em editor &#x3C;category> &#x3C;name> [id]</code></td></tr><tr><td>Permission</td><td><code>effectmaster.command.editor</code></td></tr></tbody></table>

***

### Enter Command

Enter a specific value while editing a parameter if you do not have access to the chat or simply want to implement your own system for editing shows.

<table data-header-hidden data-full-width="false"><thead><tr><th width="135.33333333333331"></th><th></th></tr></thead><tbody><tr><td>Syntax</td><td><code>/em enter &#x3C;value>...</code></td></tr><tr><td>Permission</td><td><code>effectmaster.command.enter</code></td></tr></tbody></table>

***

### Help Command

Shows the help page.

<table data-header-hidden data-full-width="false"><thead><tr><th width="135.33333333333331"></th><th></th></tr></thead><tbody><tr><td>Syntax</td><td><code>/em help</code></td></tr><tr><td>Permission</td><td><code>effectmaster.command.help</code></td></tr></tbody></table>

***

### Location Command

Useful command to retrieve different locations located to your current location. You can get your own location, the location above your head (2 blocks above your own), your location as a block coordinate and the block location you're looking at (if you are looking at a block).

<table data-header-hidden data-full-width="false"><thead><tr><th width="135.33333333333331"></th><th></th></tr></thead><tbody><tr><td>Syntax</td><td><code>/em location</code></td></tr><tr><td>Permission</td><td><code>effectmaster.command.location</code></td></tr></tbody></table>

***

### Play Command

Used to start a specific show. You can also start a show from a specific effect ID or only play one effect, this may be useful while testing.

<table data-header-hidden data-full-width="false"><thead><tr><th width="135.33333333333331"></th><th></th></tr></thead><tbody><tr><td>Syntax</td><td><code>/em play &#x3C;category> &#x3C;show></code></td></tr><tr><td>Permission</td><td><code>effectmaster.command.play</code></td></tr></tbody></table>

#### Play From

Play a show starting at a specitic effect ID including that one.

<table data-header-hidden data-full-width="false"><thead><tr><th width="135.33333333333331"></th><th></th></tr></thead><tbody><tr><td>Syntax</td><td><code>/em play &#x3C;category> &#x3C;show> from &#x3C;effect ID></code></td></tr><tr><td>Permission</td><td><code>effectmaster.command.play</code></td></tr></tbody></table>

#### Play Only

Only play one effect from a show.

<table data-header-hidden data-full-width="false"><thead><tr><th width="135.33333333333331"></th><th></th></tr></thead><tbody><tr><td>Syntax</td><td><code>/em play &#x3C;category> &#x3C;show> only &#x3C;effect ID></code></td></tr><tr><td>Permission</td><td><code>effectmaster.command.play</code></td></tr></tbody></table>

***

### Privateplay Command

Start a show only visible to a selected amount of players. You can use vanilla selectors for this command. For example `@a[distance=..10]`

<table data-header-hidden data-full-width="false"><thead><tr><th width="135.33333333333331"></th><th></th></tr></thead><tbody><tr><td>Syntax</td><td><code>/em privateplay &#x3C;category> &#x3C;show> &#x3C;selector></code></td></tr><tr><td>Permission</td><td><code>effectmaster.command.privateplay</code></td></tr></tbody></table>

{% hint style="warning" %}
You need to have [ProtocolLib](https://www.spigotmc.org/resources/protocollib.1997/) installed if you want to use this command!
{% endhint %}

***

### Play At Command

Starts a show at a specific location.

<table data-header-hidden data-full-width="false"><thead><tr><th width="135.33333333333331"></th><th></th></tr></thead><tbody><tr><td>Syntax</td><td><code>/em playat &#x3C;category> &#x3C;show> &#x3C;world> &#x3C;x> &#x3C;y> &#x3C;z></code></td></tr><tr><td>Permission</td><td><code>effectmaster.command.playat</code></td></tr></tbody></table>

{% hint style="warning" %}
This command will not work when you've not set a center location for your show! Please check [relative-shows.md](settings/relative-shows.md "mention") for more information.
{% endhint %}

***

### Reload Command

Simply reloads the config.yml after making changes to it. The show configurations automatically get reloaded so don't worry about those.

<table data-header-hidden data-full-width="false"><thead><tr><th width="135.33333333333331"></th><th></th></tr></thead><tbody><tr><td>Syntax</td><td><code>/em reload</code></td></tr><tr><td>Permission</td><td><code>effectmaster.command.reload</code></td></tr></tbody></table>

***

### Stop Command

Stops all shows, all shows in a category or all shows with a specific name in a category.

<table data-header-hidden data-full-width="false"><thead><tr><th width="135.33333333333331"></th><th></th></tr></thead><tbody><tr><td>Syntax</td><td><code>/em stop all</code><br><code>/em stop category &#x3C;category></code><br><code>/em stop show &#x3C;category> &#x3C;show></code></td></tr><tr><td>Permission</td><td><code>effectmaster.command.reload</code></td></tr></tbody></table>

***

### Rename Command

Simply renames a show.

<table data-header-hidden data-full-width="false"><thead><tr><th width="135.33333333333331"></th><th></th></tr></thead><tbody><tr><td>Syntax</td><td><code>/em rename &#x3C;category> &#x3C;show> &#x3C;new name></code></td></tr><tr><td>Permission</td><td><code>effectmaster.command.rename</code></td></tr></tbody></table>

***

### Wiki Command

Brings you to the wiki.

<table data-header-hidden data-full-width="false"><thead><tr><th width="135.33333333333331"></th><th></th></tr></thead><tbody><tr><td>Syntax</td><td><code>/em wiki</code></td></tr><tr><td>Permission</td><td><code>effectmaster.command.wiki</code></td></tr></tbody></table>
