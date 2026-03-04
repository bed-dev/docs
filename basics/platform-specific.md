# Platform-Specific Features

Sheets is designed to provide a unified experience across Java and Bedrock Edition, but some features are platform-specific.

### Unified Titles

You can provide different titles for Java and Bedrock within a single configuration.

```yaml
title:
  java: "&cJava Inventory"
  bedrock: "&bBedrock Form"
```

If a simple string is provided, it will be used for both platforms.

### Bedrock-Specific Features

#### Button Images
Bedrock forms support images on buttons. You can provide a URL or a resource path.

```yaml
buttons:
  - slot: 0
    material: DIAMOND
    name: "&bDiamond Button"
    image: "https://example.com/diamond_icon.png"
```

#### Bedrock-Only Content
You can define items and content that will only be visible to Bedrock players.

```yaml
buttons:
  - slot: 1
    material: BEDROCK
    name: "&cBedrock Players Only"
    requirements:
      view:
        - "%sheets_is_bedrock% = true"
```

See [Requirements](../features/requirements.md) for more information on conditions.

### Java-Specific Features

#### Chest Edit Mode
The visual [chest editor](../features/editor.md#1-chest-edit-mode-java-only) is only available to Java players.

#### Inventory Types
Java supports various inventory types (e.g., HOPPER, DISPENSER, BREWING_STAND), which are rendered as standard forms on Bedrock.

#### Advanced Lore and Formatting
Java Edition supports more complex text formatting and multi-line lore that may be rendered differently in Bedrock forms.
