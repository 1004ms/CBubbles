# ChatBubbles

**ChatBubbles** is a tiny Paper plugin that shows player chat messages as floating bubbles above their head.

Made by **PupillaViola**.

---

## Features

* Floating chat bubbles above players
* Multi-language support
* Toggle command for players
* Admin reload command
* Custom MiniMessage format
* Configurable duration, distance, message length and visibility
* Permission support
* Lightweight and easy to configure

---

## Commands

| Command                        | Description                          | Permission           |
| ------------------------------ | ------------------------------------ | -------------------- |
| `/chatbubbles toggle`          | Enable/disable your own chat bubbles | `chatbubbles.toggle` |
| `/chatbubbles on`              | Enable your own chat bubbles         | `chatbubbles.toggle` |
| `/chatbubbles off`             | Disable your own chat bubbles        | `chatbubbles.toggle` |
| `/chatbubbles test <message>`  | Test a chat bubble above yourself    | `chatbubbles.test`   |
| `/chatbubbles reload`          | Reload the config and language files | `chatbubbles.reload` |
| `/chatbubbles lang <language>` | Change plugin language               | `chatbubbles.lang`   |

Aliases:

```text
/cbubble
/cbubbles
```

---

## Permissions

| Permission           | Description                            | Default |
| -------------------- | -------------------------------------- | ------- |
| `chatbubbles.use`    | Allows players to create chat bubbles  | `true`  |
| `chatbubbles.toggle` | Allows players to toggle their bubbles | `true`  |
| `chatbubbles.test`   | Allows players to use the test command | `op`    |
| `chatbubbles.reload` | Allows reloading the plugin            | `op`    |
| `chatbubbles.lang`   | Allows changing the plugin language    | `op`    |

---

## Languages

ChatBubbles includes these languages:

| Code                           | Language                                       |
| ------------------------------ | ---------------------------------------------- |
| `it` / `ita` / `it_IT`         | Italian                                        |
| `en` / `eng` / `en_US`         | English                                        |
| `es` / `esp` / `spa` / `es_ES` | Spanish                                        |
| `fr` / `fra` / `fr_FR`         | French                                         |
| `custom`                       | Uses the `messages:` section from `config.yml` |

Example:

```text
/chatbubbles lang it
/chatbubbles lang en
/chatbubbles lang es
/chatbubbles lang fr
/chatbubbles lang custom
```

---

## Placeholders

You can use these placeholders inside the bubble format:

| Placeholder | Description  |
| ----------- | ------------ |
| `<player>`  | Player name  |
| `<message>` | Chat message |
| `<newline>` | New line     |

Example:

```yaml
format: "<gray><player></gray><newline><white><message></white>"
```

Players cannot inject MiniMessage tags inside their chat message.

---

## Basic Configuration

```yaml
# ChatBubbles by PupillaViola
# Tiny visual chat bubbles

settings:
  enabled: true
  language: "it_IT"
  use-permission: "chatbubbles.use"
  disabled-worlds:
    - "example_disabled_world"
  cooldown-millis: 600

bubble:
  duration-ticks: 100
  follow-period-ticks: 1
  vertical-offset: 0.55
  view-range: 32.0
  max-message-length: 96
  line-width: 180
  show-own-bubble: true

  shadowed: true
  see-through: false
  default-background: false
  background:
    enabled: true
    alpha: 0

  format: "<gray><player></gray><newline><white><message></white>"
```

---

## Installation

1. Download the plugin jar.
2. Put it inside your server `plugins` folder.
3. Restart the server.
4. Edit `plugins/ChatBubbles/config.yml` if needed.
5. Use `/chatbubbles reload`.

---

## Requirements

* Paper server
* Minecraft 1.21+
* Java 25+
