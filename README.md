# Rustic Windmill Addon for Minecraft Bedrock

A complete Bedrock addon for building functional rustic windmills that grind wheat into flour using wind power.

## Block Components

### Power Flow System

The windmill uses a directional power flow system where power travels from the blades through the system:

**Blades → Rear Shaft → Horizontal Shaft → Gearbox → Vertical Shaft → Grindstone**

### Blocks

1. **Windmill Blades Block** (Power Source)
   - Spinning blades at the top that generate power
   - Has rear shaft output for power transmission
   - Power flows out the back to horizontal shafts/gearbox
   - Rotates continuously in wind
   - Crafted with sticks and white wool

2. **Horizontal Shaft Block** (Power Transfer - Rear Direction)
   - Carries rotational power horizontally from blades
   - Connects blades to gearbox at the rear
   - Stackable in horizontal lines
   - Crafted from 3 dark oak wood logs

3. **Gearbox Block** (Power Converter)
   - Receives horizontal power from the rear/sides
   - Converts and redirects power downward
   - Contains meshing gears for mechanical look
   - Reduces rotation speed for grindstone efficiency
   - Crafted with iron ingots, dark oak wood, and diamonds

4. **Shaft Block** (Vertical Power Transfer)
   - Carries rotational power vertically downward
   - Connects from gearbox down to grindstone
   - Stackable vertically for tall mills
   - Crafted from 3 dark oak logs

5. **Grindstone Block** (Processing Unit)
   - Receives vertical power from shaft above
   - Converts wheat into flour continuously
   - Stone grinding wheel rotates when powered
   - Crafted with stone and dark oak wood

### Crafting Recipes

#### Windmill Blades Block (1 block)
```
S W S
S W S
S W S
```
- S = Stick
- W = White Wool

#### Horizontal Shaft Block (1 block)
```
W W W
```
- W = Dark Oak Log (3 logs in a row)

#### Shaft Block (1 block)
```
W
W
W
```
- W = Dark Oak Log (3 logs stacked)

#### Gearbox Block (1 block)
```
I P I
P G P
I P I
```
- I = Iron Ingot (4 corners)
- P = Dark Oak Wood (4 sides)
- G = Diamond (center gear hub)

#### Grindstone Block (1 block)
```
S S S
S W S
S S S
```
- S = Stone or Cobblestone (8 blocks)
- W = Dark Oak Wood (center)

#### Flour (4 flour)
```
W
```
- W = Wheat (1 wheat = 4 flour)

## How to Build the Windmill

### Step 1: Place the Windmill Blades
- Position the **Windmill Blades** block at the top
- This is your power generation unit

### Step 2: Connect Rear Shaft
- Place **Horizontal Shaft** blocks behind/away from the blades
- These carry the rotation power backwards

### Step 3: Position the Gearbox
- Place the **Gearbox** at the end of the horizontal shaft run
- The gearbox receives horizontal power and converts it to vertical
- Orient so inlet connects to horizontal shaft, outlet points down

### Step 4: Connect Vertical Shafts
- Stack **Shaft** blocks vertically below the gearbox
- These carry the power straight down
- Stack as many as needed for your design

### Step 5: Place the Grindstone
- Position the **Grindstone** at the bottom of the vertical shaft
- This grinds the wheat into flour

### Complete Power Flow
```
Windmill Blades
    ↓(spins)
Back Shaft Output
    ↙(power travels back)
Horizontal Shaft → Horizontal Shaft → Horizontal Shaft
    ↓(power enters side)
Gearbox (converts to vertical)
    ↓(power travels down)
Vertical Shaft
    ↓
Vertical Shaft (stack as needed)
    ↓
Grindstone (processes wheat → flour)
```

## How It Works

1. **Windmill Blades**: Spin continuously due to wind, generating rotational power
2. **Horizontal Shafts**: Carry the rotation from the blades backward toward the gearbox
3. **Gearbox**: 
   - Receives horizontal spinning motion
   - Uses internal gears to redirect power 90 degrees downward
   - Adjusts rotation speed for optimal grinding
4. **Vertical Shafts**: Transmit the downward rotation
5. **Grindstone**: Uses the spinning motion to grind wheat into flour continuously

## Harvesting Flour

- Wheat is automatically processed into flour by the spinning grindstone
- The grindstone outputs flour as it grinds
- Collect the flour and use it for bread, cakes, cookies, or other recipes

## Installation

1. Place both `behavior_pack` and `resource_pack` folders into your Minecraft data folder:
   - **Windows 10/11**: `%localappdata%\Packages\Microsoft.MinecraftUWP_8wekyb3d8bbwe\LocalState\games\com.mojang\`
   - **Mobile**: Check Minecraft app storage location

2. Enable the addon in world settings before creating/loading a world

3. Creative mode: All windmill blocks are available in the construction category

## File Structure

```
Windmill/
├── behavior_pack/
│   ├── manifest.json
│   ├── blocks/
│   │   ├── windmill_blades.json
│   │   ├── horizontal_shaft.json
│   │   ├── shaft.json
│   │   ├── gearbox.json
│   │   └── grindstone.json
│   ├── items/
│   │   └── flour.json
│   └── recipes/
│       ├── horizontal_shaft_craft.json
│       ├── gearbox_craft.json
│       ├── flour_crafting.json
│       └── other_recipes.json
└── resource_pack/
    ├── manifest.json
    ├── animations/
    │   └── windmill.animation.json
    ├── models/
    │   ├── windmill_blades_block.geo.json
    │   ├── shaft_horizontal.geo.json
    │   ├── shaft.geo.json
    │   ├── gearbox.geo.json
    │   └── grindstone.geo.json
    ├── entity/
    └── textures/
        ├── blocks.json
        └── blocks/
```

## Required Textures (16x16 PNG images)

Create texture files for authentic rustic appearance:

1. `resource_pack/textures/blocks/windmill_blades.png` - Wood beams and white wool blades
2. `resource_pack/textures/blocks/shaft.png` - Dark wood vertical shaft
3. `resource_pack/textures/blocks/shaft_horizontal.png` - Dark wood horizontal shaft
4. `resource_pack/textures/blocks/gearbox.png` - Iron with visible internal gears
5. `resource_pack/textures/blocks/grindstone.png` - Stone grinding wheel
6. `resource_pack/textures/items/flour.png` - White flour pile

## Building Tips for Authentic Rustic Windmill

- **Structure**: Use dark oak wood and stone blocks for framing
- **Layout**: Blades on top, horizontal shafts extending backward to gearbox on the side
- **Height**: Use multiple vertical shaft blocks for tall mills
- **Details**: Add decorative beams, supports, and scaffolding around the mechanism
- **Base**: Build a stone foundation for the grindstone
- **Stairs**: Add wooden stairs leading up to the blade mechanism
- **Texture**: Use natural wood tones and aged stone textures

## Customization

- **Blade Speed**: Modify animation timeline in `windmill.animation.json`
- **Gear Ratios**: Adjust animation speeds to simulate different mechanical advantages
- **Processing Rate**: Modify flour output in flour crafting recipe
- **Appearance**: Create custom textures for specific regional styles
- **Block Models**: Edit geometry JSON files for different designs

---

**Your rustic windmill is ready to build!** Create an efficient flour-grinding operation with power flowing from the spinning blades, through horizontal shafts, down through the gearbox, and into the grindstone.
