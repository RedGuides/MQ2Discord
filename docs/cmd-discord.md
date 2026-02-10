---
tags:
  - command
---

# /discord

## Syntax

<!--cmd-syntax-start-->
```eqcommand
/discord {reload|process|debug|stop}
```
<!--cmd-syntax-end-->

## Description

<!--cmd-desc-start-->
Sends commands to be processed by the config file, reloads the config file, and controls debugging.
<!--cmd-desc-end-->

## Options

| Option  | Description |
|---------|-------------|
| `reload` | Reloads the .yaml file, useful when making changes. |
| `process` | Will allow you to send a command to be processed by your config under allowed, blocked or notify. See example. |
| `debug` | Toggles debug mode on or off. |
| `stop` | Issues a stop command for debugging. |

## Examples

Here's an example [Knightly made](https://www.redguides.com/community/threads/mq2discord.62755/post-478037) of using the `/discord process` option with MQ2Say,

In your MQ2Discord.yaml, set an alert for MQ2Say under notify:
```yaml
notify:
- "[MQ2Say]#*#"
```

In your MQ2Say.ini, set the "/discord process" option like this:

```ini
[Settings]
SaveByChar=1
AlertPerSpeaker=1
[Default]
AlertCommand=/discord process [MQ2Say] ${SayWnd.LastSpeaker} says: ${SayWnd.LastSay}
```
