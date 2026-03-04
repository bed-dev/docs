# Editor & Input

Sheets provides interactive ways to edit and interact with menus.

### 1. Chest Edit Mode (Java Only)

Chest Edit Mode allows you to visually edit your menus in-game.

#### How to Open
*   Run `/sheets edit <menu> chest`.
*   Alternatively, open the edit menu with `/sheets edit` and right-click on the sheet you want to edit.

#### Functionality
1.  Once in Chest Edit Mode, you can drag and drop items from your inventory into the menu or rearrange existing items.
2.  Closing the inventory will automatically save the new layout to the menu's YAML file as `buttons`.
3.  Each item in the menu will be saved with its material, name, and lore.

### 2. Anvil Input

Anvil menus can be used to capture text input from players.

#### Usage via Actions
Define an `input` action in your YAML:
```yaml
actions:
  - input:
      title: "Enter text"
      command: "say you entered {text}"
```

#### Dynamic Anvil Menus
If you specify a title in the `input` action that doesn't correspond to a pre-defined menu, Sheets will dynamically create an Anvil menu with that title.

#### Real-time Updates
Anvil menus refresh every second (20 ticks), allowing placeholders like `{text}` to update in item names and lore as the player types.

#### Confirmation Button
Slot 2 in an Anvil menu is typically used as the confirmation button. The action defined in the `input` command will be executed when this button is clicked.
