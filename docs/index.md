---
tags:
  - plugin
resource_link: "https://www.redguides.com/community/resources/mq2discord.80/"
support_link: "https://www.redguides.com/community/threads/mq2discord.62755/"
repository: "https://github.com/RedGuides/MQ2Discord"
config: "MQ2Discord.yaml"
authors: "alynel, Knightly"
tagline: "Issue commands from discord to EverQuest"
quick_start: "#setup"
---

# MQ2Discord

<!--desc-start-->
Plugin that does pretty much what the name says, connects MacroQuest to Discord. Chat messages that match a filter get sent to a Discord channel, and any commands you enter in that channel get executed.
<!--desc-end-->

## Commands

<a href="cmd-discord/">
{% 
  include-markdown "projects/mq2discord/cmd-discord.md" 
  start="<!--cmd-syntax-start-->" 
  end="<!--cmd-syntax-end-->" 
%}
</a>
:    {% include-markdown "projects/mq2discord/cmd-discord.md" 
        start="<!--cmd-desc-start-->" 
        end="<!--cmd-desc-end-->" 
        trailing-newlines=false 
     %} {{ readMore('projects/mq2discord/cmd-discord.md') }}

## Settings

``` yaml title="Here's an example MQ2Discord.yaml"
--8<-- "docs/projects/mq2discord/MQ2Discord.example.yaml"
```

## Setup

1. Create a server & channel(s) from the [Discord client](https://support.discord.com/hc/en-us/articles/204849977-How-do-I-create-a-server-).
2. Create a Discord bot & add it to your server: see [Create a Discord Bot Account](Create_Bot_Account.md).
3. Enable developer mode in the Discord app (Discord client settings -> advanced). See: [Enable developer mode](https://support.discord.com/hc/en-us/articles/206346498-Where-can-I-find-my-User-Server-Message-ID).
4. Open the `MQ2Discord.yaml` in a code editor. We recommend [Visual Studio Code](https://code.visualstudio.com/). ("notepad" is not recommended for YAML files!)
5. Enter the **token** for the bot in your `MQ2Discord.yaml`. (The token you made in [step 2.](Create_Bot_Account.md))
6. Enter your **user_id** (right click your username in Discord, copy id) in `MQ2Discord.yaml`.
7. Enter your `server_Character` name and the channel **id** in `MQ2Discord.yaml`. Server name must be the shortname.
8. In game, load the plugin with `/plugin mq2discord`.
9. If it's already loaded, reload the config with `/discord reload`. If there are any errors in your .yaml file, it should tell you the line to look at.

## See also

- [Discord official site](https://discord.com)
- [Create a Discord Bot Account](Create_Bot_Account.md)
- [Discord Developer Portal – Applications](https://discord.com/developers/applications)
- [Discord Docs – OAuth2 overview](https://discord.com/developers/docs/topics/oauth2)
- [Discord Docs – Permissions](https://discord.com/developers/docs/topics/permissions)
- [Discord Docs – Privileged Gateway Intents](https://discord.com/developers/docs/topics/gateway#privileged-intents)
