# Actions

Actions allow you to add functionality to your buttons. When a player interacts with a button, the associated actions are executed.

### Action Syntax

Actions can be defined as simple strings or as structured maps in YAML.

**String Syntax:**
```yaml
actions:
  - message: "Hello world!"
  - command: "say %player_name% clicked this!"
```

**Map Syntax:**
```yaml
actions:
  - open: "another_menu"
  - sound: "entity.experience_orb.pickup"
```

### Supported Action Types

| Action | Description | Aliases |
| :--- | :--- | :--- |
| `message` | Sends a message to the player. | |
| `command` | Executes a command as the player. | `player` |
| `console` | Executes a command as the console. | |
| `sudo` | Executes a command as the player, bypassing permissions. | |
| `open` | Opens another menu for the player. | `menu` |
| `close` | Closes the current menu. | |
| `sound` | Plays a sound to the player. | |
| `broadcast` | Broadcasts a message to all players. | |
| `broadcast-sound`| Plays a sound to all players. | |
| `teleport` | Teleports the player to a location or player. | `tp` |
| `world` | Teleports the player to a specific world. | |
| `server` | Connects the player to another BungeeCord server. | `connect` |
| `item` | Gives an item to the player. | `give` |
| `balance` | Modifies the player's Vault balance. | |
| `permission` | Modifies the player's permissions. | |
| `refresh` | Refreshes the current menu content. | |
| `argument` | Sets a local variable for subsequent actions. | |
| `input` | Prompts for text input via an Anvil menu. | |

### Specialized Click Actions (Java Only)

Execute different actions based on the click type:
*   `left`: Executed on left-click.
*   `right`: Executed on right-click.
*   `shift`: Executed on shift-click.
*   `middle`: Executed on middle-click.

**Example:**
```yaml
actions:
  - left: "message: You left-clicked!"
  - right:
      message: "You right-clicked!"
  - middle:
      input:
        title: "Rename Item"
        command: "rename {text}"
```

### Input Action

The `input` action is used to get text input from the player.

```yaml
actions:
  - input:
      title: "Enter your name"
      command: "say hello {text}"
```

*   `{text}`: The text entered by the player.

### Argument Action

Set local variables that can be used later.

```yaml
actions:
  - argument:
      target: "%player_name%"
  - message: "Hello {target}!"
```
