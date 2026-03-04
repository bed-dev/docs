# Menu Templates

Templates allow you to quickly create new menus using pre-defined structures.

### Templates Folder

All templates are stored in `plugins/Sheets/menus/templates/`.

### Default Templates

Sheets comes with several default templates:
*   `basic_gui`: A standard inventory GUI.
*   `simple_inventory`: A basic inventory-based menu.
*   `anvil_input`: A template for [Anvil input menus](editor.md#2-anvil-input).

### Usage

#### Commands
Run [`/sheets create <name> <template>`](../basics/commands.md#management-commands) to create a new sheet from a template.

```bash
/sheets create my_new_menu basic_gui
```

#### Graphical Interface
1.  Run `/sheets create`.
2.  Select **Create from Template**.
3.  Choose your desired template from the list.
4.  Enter the name for your new sheet.

### Creating Your Own Templates

1.  Navigate to `plugins/Sheets/menus/templates/`.
2.  Create a new YAML file.
3.  Design your menu as usual.
4.  Save the file and run `/sheets reload`.
5.  Your new template will now appear in the template selector.
