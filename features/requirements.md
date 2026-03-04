# Requirements

Requirements are conditions that must be met for a button to be visible or clickable.

### Usage

Requirements are defined as lists of conditions. If all conditions in a list are met, the requirement is satisfied.

**YAML Example:**
```yaml
requirements:
  view:
    - "%player_has_permission_sheets.admin% = true"
  click:
    - "%vault_eco_balance% >= 100"
    - item:
        material: DIAMOND
        amount: 1
```

### Types of Requirements

| Requirement | Description |
| :--- | :--- |
| `view` | Controls if the button is visible in the menu. |
| `click` | Controls if the player can click the button. |

### Supported Conditions

Conditions can use [placeholders](placeholders.md) and logical expressions to determine if a requirement is met.

| Condition | Description |
| :--- | :--- |
| `condition` | A logical expression (e.g., `%balance% > 100`). |
| `permission`| Checks if the player has a specific permission. |
| `balance` | Checks the player's Vault balance. |
| `item` | Checks for specific items in the player's inventory. |

### Logical Expressions

You can use standard comparison operators in your conditions:
*   `=`, `!=`, `>`, `>=`, `<`, `<=`
*   `contains`, `startsWith`, `endsWith`

**Example:**
```yaml
- "%player_name% = bed"
- "%vault_eco_balance% >= 500"
```
