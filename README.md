# Windmill Addon for Minecraft Bedrock

A Bedrock addon that adds a craftable windmill that grinds wheat into flour with spinning blades made of wool and wood.

## Features

- **Windmill Blade Item**: Craftable item made from sticks and white wool
- **Windmill Block**: Craft using 4 windmill blades and dark oak wood
- **Spinning Blades**: Animated wool and wood blades that continuously spin
- **Flour Crafting**: Grind 1 wheat into 4 flour using a crafting recipe
- **Flour Item**: New flour item that can be used for crafting bread and other recipes

## Crafting Recipes

### Windmill Blade (makes 1)
```
S W S
W   W
```
Where S = Stick, W = White Wool

### Windmill Block (makes 1)
```
B W B
W B W
B W B
```
Where B = Windmill Blade (4 needed), W = Dark Oak Wood

### Flour (makes 4)
```
W
```
Where W = Wheat (1 needed)

## Installation

1. Download the addon folder
2. Place both `behavior_pack` and `resource_pack` folders into:
   - **Windows 10/11**: `%localappdata%\Packages\Microsoft.MinecraftUWP_8wekyb3d8bbwe\LocalState\games\com.mojang\`
   - **Mobile**: Find the Minecraft app data folder
3. Open Minecraft and enable the addon in world settings

## File Structure

```
Windmill/
├── behavior_pack/
│   ├── manifest.json
│   ├── blocks/
│   │   └── windmill.json
│   ├── entities/
│   │   └── windmill_blades.json
│   ├── items/
│   │   ├── windmill_blade.json
│   │   └── flour.json
│   └── recipes/
│       ├── windmill_blade_craft.json
│       ├── windmill_build.json
│       └── flour_crafting.json
└── resource_pack/
    ├── manifest.json
    ├── animations/
    │   └── windmill_blades.animation.json
    ├── models/
    │   ├── windmill_base.geo.json
    │   └── windmill_blades.geo.json
    ├── entity/
    │   └── windmill_blades.entity.json
    └── textures/
        ├── blocks.json
        └── items/
```

## Next Steps

To complete the addon, you need to create texture files (16x16 PNG images):

1. `resource_pack/textures/blocks/windmill_base.png` - Wood/wool base texture
2. `resource_pack/textures/items/windmill_blade.png` - Windmill blade texture
3. `resource_pack/textures/items/flour.png` - Flour item texture
4. `resource_pack/textures/entity/windmill_blades.png` - Spinning blades texture

## Customization

- Modify blade speed in `windmill_blades.animation.json` (adjust timeline values)
- Change recipes in the recipes JSON files
- Adjust model sizes in geometry JSON files
- Create custom textures for unique visuals
