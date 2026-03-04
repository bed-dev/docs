# Quickstart

### Introduction

The Sheets plugin for Minecraft Java Edition provides an extensive toolkit for creating dynamic menus and interactive forms, enhancing player engagement and overall gameplay experience. This section will guide you through the installation and basic setup of the Sheets plugin, helping you create your first menu and utilize its features effectively.

Want to learn about writing menu from scratch? Head to the [Basics](../README.md) section to learn more.


### Installation

#### Prerequisites

Before installing the Sheets plugin, ensure you have the following:

* **Java** version 21 installed
* A **Minecraft Java Edition** server running a compatible version of [Spigot ](#user-content-fn-1)[^1]1.21+.
* [**Geyser**](https://geysermc.org/download/) installed (optional) if you plan to support cross-play with Bedrock Edition players.
* [**PlaceholderAPI**](https://www.spigotmc.org/resources/placeholderapi.6245/) installed (optional) if you want to use placeholders
* [**Vault**](https://www.spigotmc.org/resources/vault.34315/) and an economy plugin installed (optional) if you want to use economy

#### Installation Steps

* **Download the Plugin**
    * Go to the [BuiltByBit resource page](https://builtbybit.com/resources/sheets-unified-menus-forms-for-java.51876/) and download the latest version of the Sheets plugin.
* **Add the Plugin to Your Server**
    * Move the downloaded `.jar` file into the `plugins` folder of your Minecraft server directory.
* **Restart Your Server**
    * Restart your server to enable the plugin. Check the server console for messages confirming that Sheets has been loaded successfully.

If you encounter any problem installing the plugin you can request support at [our discord](https://discord.bed.codes)

### Basic Configuration

Sheets doesn't require any configuration to work directly after installing. The only option in the configuration right now is debug.

You can add or configure menus in the `plugins/Sheets/menus/` folder. You don't need to add the menu to a configuration; every file in the `menus` folder is loaded, no matter if it's in another folder inside like `plugins/Sheets/menus/anotherfolder/`.

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
*   Check out the [Configuration](../basics/configuration.md) to customize the plugin.
*   Learn how to use [Requirements](../features/requirements.md) for button visibility.
*   Use [Placeholders](../features/placeholders.md) to create dynamic content.
