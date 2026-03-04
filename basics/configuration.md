# Configuration

Sheets uses YAML for configuration files.

### Global Configuration (`config.yml`)

The global configuration file for Sheets is located at `plugins/Sheets/config.yml`.

```yaml
# Mode for plugin messages
small-caps: false

# Debug mode
debug:
  enabled: false

# Custom messages
messages:
  insufficient-requirements: "&cYou have not meet the requirements to do this"
  insufficient-funds: "&cYou do not have enough money to do this"
  insufficient-items: "&cYou do not have the required items to do this"
```

### Menu Configurations

Each menu is stored in its own YAML file in the `plugins/Sheets/menus/` folder.

#### Basic Settings
*   `name`: Unique name for the menu.
*   `title`: The title shown at the top of the menu (Java/Bedrock).
*   `type`: The type of menu (`normal` or `anvil`).
*   `size`: The size of the Java GUI (e.g., 9, 18, 27, 36, 45, 54).
*   `commands`: List of commands that open this menu.

#### Button Settings
Buttons are defined in the `buttons` list.
*   `slot`: The slot number or dynamic slot range.
*   `material`: The Minecraft material for the item.
*   `image`: The image URL or path for Bedrock form buttons.
*   `name`: The display name of the item.
*   `lore`: List of lore lines for the item.
*   `requirements`: Conditions for visibility and interaction. See [Requirements](../features/requirements.md).
*   `actions`: Actions to perform when clicked. See [Actions](../features/actions.md).

### Variables

Global variables are defined in the `variables/` folder.

```yaml
prefix: "&c&sServername"
server-ip: "123.45.67.89"
```

Use them in your menus with `{{variable_name}}`. See [Placeholders](../features/placeholders.md).
