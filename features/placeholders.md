# Placeholders

Sheets features a multi-tier placeholder system to provide dynamic content in your menus.

### 1. Multi-Tier System

Sheets evaluates placeholders in the following order:

1.  **Global Variables**: `{{variable_name}}`
    *   Defined in `variables/*.yml`.
2.  **Arguments/Local Variables**: `{variable_name}`
    *   Passed via commands or actions like `input`.
3.  **Special Placeholders**:
    *   `[index]`: Current index in a dynamic slot range.
    *   `[slot]`: Current slot number in a dynamic slot range.
4.  **Math Expressions**: `{math:expression}` or `{math:int:expression}`
    *   Example: `{math:1 + 1}` results in `2.0`.
    *   Example: `{math:int:%player_health% * 2}` results in an integer.
5.  **Sheets Internal Placeholders**:
    *   `%sheets_sheet_[index]_name%`: Name of the Nth sheet.
    *   `%sheets_sheet_[index]_exists%`: Whether the Nth sheet exists.
    *   `%sheets_template_[index]_name%`: Name of the Nth template.
6.  **PlaceholderAPI**: Full support for standard `%player_name%` style placeholders.

### 2. Math Expressions

You can perform calculations directly within your YAML configurations.

```yaml
name: "&aYour Health: {math:int:%player_health%}"
lore:
  - "&7Double health: {math:int:%player_health% * 2}"
```

### 3. Dynamic Slots

Use `[slot]` and `[index]` to create dynamic content based on slot ranges.

```yaml
slots:
  - 0to44

buttons:
  - slot: "[slot]"
    name: "&aItem #[index]"
    lore:
      - "&7This is slot number [slot]"
```
