# Commands

Manage your sheets and the plugin using the following commands.

### General Commands

*   `/sheets open <menu>`: Opens the specified menu for the player.
*   `/sheets reload`: Reloads all plugin configurations and menus.
*   `/sheets reload <menu>`: Reloads only the specified menu.
*   `/sheets list [page]`: Displays a paginated list of all loaded menus.
*   `/sheets info <menu>`: Shows detailed information about a specific menu.

### Management Commands

*   `/sheets create [name] [template]`:
    *   `/sheets create`: Opens the graphical template selector.
    *   `/sheets create <name> [template]`: Creates a new sheet. If a [template](../features/templates.md) is specified, it will be used as the base.
*   `/sheets edit [name] [chest]`:
    *   `/sheets edit`: Opens the [graphical edit menu](../features/editor.md) to manage all sheets.
    *   `/sheets edit <name>`: Opens the edit menu for the specified sheet.
    *   `/sheets edit <name> chest`: Opens the visual [chest editor](../features/editor.md#1-chest-edit-mode-java-only) for the specified sheet.
*   `/sheets delete <name> [confirm]`: Deletes the specified sheet. Add `true` to skip the confirmation menu.
*   `/sheets rename <old> <new>`: Renames an existing sheet.
*   `/sheets copy <menu> <newname>`: Creates a copy of a menu with a new name.

### Data Management

*   `/sheets export <menu> <path>`: Exports the menu configuration to the specified file path.
*   `/sheets import <filepath> [name]`: Imports a menu from a file path.

### Development Commands

*   `/sheets test <path>`: Runs a test on the specified configuration path.
*   `/sheets debug <path>`: Toggles debug information for the specified path.
*   `/sheets load <path>`: Directly loads a menu from a specific file path.
