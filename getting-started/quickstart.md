# Quickstart

Getting started with Sheets is simple. Follow these steps to install the plugin and create your first menu.

### Installation

1.  Download the latest version of Sheets.
2.  Place the `Sheets.jar` file into your server's `plugins/` folder.
3.  Restart your server or use a plugin manager to load Sheets.

### Creating Your First Menu

There are two ways to create a menu: using a command or manually creating a YAML file.

#### Using Commands

Run the following command to create a new sheet using the default template:

```bash
/sheets create my_first_menu basic_gui
```

This will create a new file at `plugins/Sheets/menus/my_first_menu.yml` and open it for you.

#### Manual Creation

1.  Navigate to `plugins/Sheets/menus/`.
2.  Create a new file named `hello_world.yml`.
3.  Paste the following content:

```yaml
name: hello_world
title: "Hello World!"
type: normal
size: 27
buttons:
  - slot: 13
    material: DIAMOND
    name: "&bWelcome to Sheets!"
    lore:
      - "&7Click me to receive a message"
    actions:
      - message: "&aYou clicked the diamond!"
```

4.  Save the file and run `/sheets reload`.
5.  Open your menu with `/sheets open hello_world`.

### Next Steps

*   Learn about more [Commands](../basics/commands.md) to manage your menus.
*   Explore [Actions](../features/actions.md) to add functionality to your buttons.
*   Use [Placeholders](../features/placeholders.md) to create dynamic content.
