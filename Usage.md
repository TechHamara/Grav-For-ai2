# Grav Extension for MIT App Inventor

An extension for MIT App Inventor 2 that provides beautiful animated particle effects.

**Created by:** TechHamara  
**Compiled by:** FAST

## Overview

The Grav extension allows you to create stunning particle animations in your App Inventor apps. It provides a highly customizable particle system with various generators for colors, positions, shapes, and animations.

## Quick Start

### 1. Initialize the Component

First, add the Grav extension to your project and add it to your screen (it's a non-visible component).

Then, use an arrangement (Horizontal, Vertical, or Canvas) where you want the animation to appear:

```blocks
When Screen1.Initialize
  Call Grav1.Initialize arrangement = HorizontalArrangement1
```

### 2. Start the Animation

After initialization, start the animation:

```blocks
When Grav1.Initialized
  Call Grav1.Start
```

### 3. Customize (Optional)

Before calling Start, you can customize colors, particle positions, shapes, and animations.

## Function Reference

### Lifecycle Methods

#### `Initialize(arrangement)`
Initialize the Grav view inside an arrangement component. **Must be called first.**
- **arrangement**: Any arrangement component (HorizontalArrangement, VerticalArrangement, Canvas, etc.)
- **Fires**: `Initialized` event when complete

#### `Start()`
Start the particle animation.
- **Fires**: `AnimationStarted` event

#### `Stop()`
Stop the particle animation.
- **Fires**: `AnimationStopped` event

### Color Generators

Choose how particles are colored. **Only one color generator can be active at a time.**

#### `RandomColorGenerator()`
Each particle gets a random color from the full spectrum.

#### `OneColorGenerator(color)`
All particles use a single color.
- **color**: App Inventor color value

**Example:**
```blocks
Call Grav1.OneColorGenerator color = Blue
```

#### `ArrayColorGenerator(colors)`
Particles cycle through a list of colors.
- **colors**: List of color values or hex strings

**Example:**
```blocks
Call Grav1.ArrayColorGenerator colors = make a list ["#FF0000", "#00FF00", "#0000FF"]
```

### Point Generators

Choose where particles appear on screen. **Only one point generator can be active at a time.**

#### `RegularPointGenerator(cellSize, variance)`
Particles arranged in a regular grid pattern.
- **cellSize**: Spacing between particles in pixels (smaller = more particles)
- **variance**: Random position offset in pixels (0 = perfect grid)

**Example:**
```blocks
Call Grav1.RegularPointGenerator cellSize = 100 variance = 20
```

#### `CircularPointGenerator(cellSize, variance)`
Particles in a circular/radial pattern from center.
- **cellSize**: Radial spacing in pixels
- **variance**: Random position offset in pixels

#### `PercentPointGenerator(percentPoints)`
Place particles at specific screen positions using percentages.
- **percentPoints**: List of x,y coordinates as percentages (0-100)

**Example:**
```blocks
// One particle at center, one in top-left
Call Grav1.PercentPointGenerator percentPoints = make a list [50, 50, 25, 25]
```

### Particle Shape Generators

Choose the shape of particles. **Only one shape generator can be active at a time.**

#### `BallGenerator(fromSize, toSize)`
Render particles as circles.
- **fromSize**: Minimum particle size in pixels
- **toSize**: Maximum particle size in pixels (use same value for uniform size)

**Example:**
```blocks
Call Grav1.BallGenerator fromSize = 10 toSize = 30
```

#### `RectangleGenerator(width, height)`
Render particles as rectangles.
- **width**: Rectangle width in pixels
- **height**: Rectangle height in pixels

#### `CustomShapeGenerator(shapeType, width, height)` 🆕
Render particles as custom shapes with 16 different options!
- **shapeType**: Shape name (case-insensitive)
- **width**: Shape width in pixels
- **height**: Shape height in pixels

**Supported shapes:**
- `circle`, `ellipse`, `triangle`, `rectangle`
- `trapezium`, `parallelogram`, `capsule`, `leaf`
- `rhombus`, `heart`, `drop`, `star`
- `diamond`, `pentagon`, `hexagon`, `cloud`

**Example:**
```blocks
Call Grav1.CustomShapeGenerator shapeType = "heart" width = 30 height = 30
```

### Animators

Add motion and effects to particles. **You can add multiple animators together.**

#### `AlphaAnimator(from, to, minDuration, maxDuration)`
Fade particles in and out.
- **from**: Starting opacity (0-255, 0=transparent)
- **to**: Ending opacity (0-255, 255=opaque)
- **minDuration**: Minimum animation time in milliseconds
- **maxDuration**: Maximum animation time in milliseconds

**Example:**
```blocks
Call Grav1.AlphaAnimator from = 50 to = 255 minDuration = 500 maxDuration = 1500
```

#### `BallSizeAnimator(fromSize, toSize, minDuration, maxDuration)`
Make balls pulse/grow and shrink. **Only works with BallGenerator.**
- **fromSize**: Minimum size in pixels
- **toSize**: Maximum size in pixels
- **minDuration**: Minimum animation time in milliseconds
- **maxDuration**: Maximum animation time in milliseconds

#### `ShakeAnimator(variance, minDuration, maxDuration, direction)`
Make particles shake/vibrate.
- **variance**: Shake intensity in pixels
- **minDuration**: Minimum shake time in milliseconds
- **maxDuration**: Maximum shake time in milliseconds
- **direction**: 0=Horizontal, 1=Vertical

#### `SideToSideAnimator(minDuration, maxDuration, direction)`
Move particles across the screen.
- **minDuration**: Minimum travel time in milliseconds
- **maxDuration**: Maximum travel time in milliseconds
- **direction**: 0=LeftToRight, 1=RightToLeft, 2=UpToDown, 3=DownToUp

#### `PathAnimator(path, minVariance, maxVariance, originalWidth, originalHeight, minDuration, maxDuration)`
Move particles along a custom SVG path. **Advanced feature.**
- **path**: SVG path string (e.g., "M 0,0 L 100,100")
- **minVariance**: Minimum random offset from path
- **maxVariance**: Maximum random offset from path
- **originalWidth**: Path coordinate system width
- **originalHeight**: Path coordinate system height
- **minDuration**: Minimum travel time in milliseconds
- **maxDuration**: Maximum travel time in milliseconds

#### `ShapePathAnimator(shapeType, minVariance, maxVariance, originalWidth, originalHeight, minDuration, maxDuration)` 🆕
Move particles along pre-built shape paths without writing SVG!
- **shapeType**: Shape name (case-insensitive)
- **minVariance**: Minimum random offset from path
- **maxVariance**: Maximum random offset from path  
- **originalWidth**: Path size width (recommended 100)
- **originalHeight**: Path size height (recommended 100)
- **minDuration**: Minimum travel time in milliseconds
- **maxDuration**: Maximum travel time in milliseconds

**Supported shapes:**
- `circle`, `ellipse`, `triangle`, `rectangle`
- `trapezium`, `parallelogram`, `capsule`, `rhombus`
- `heart`, `star`, `diamond`, `pentagon`, `hexagon`
- `leaf`, `drop`

**Example:**
```blocks
Call Grav1.ShapePathAnimator 
  shapeType = "heart"
  minVariance = 2
  maxVariance = 5
  originalWidth = 100
  originalHeight = 100
  minDuration = 2000
  maxDuration = 4000
```

#### `ShapePathAnimatorWithSize(shapeType, width, height, minDuration, maxDuration)` 🆕
Simplified version - move particles along pre-built shape paths with custom size.
- **shapeType**: Shape name (same 15 shapes as above)
- **width**: Path width in pixels
- **height**: Path height in pixels
- **minDuration**: Minimum travel time in milliseconds
- **maxDuration**: Maximum travel time in milliseconds

**Example:**
```blocks
Call Grav1.ShapePathAnimatorWithSize 
  shapeType = "star"
  width = 150
  height = 150
  minDuration = 3000
  maxDuration = 5000
```

#### `ClearAnimators()`
Remove all animators. Particles become static.

## Events

### `Initialized()`
Triggered when the Grav view is ready. Safe to call other methods after this event.

### `AnimationStarted()`
Triggered when animation begins.

### `AnimationStopped()`
Triggered when animation stops.

## Complete Examples

### Example 1: Colorful Pulsing Particles

Here's a complete example creating a colorful, pulsing particle effect:

```blocks
When Screen1.Initialize
  // Initialize in an arrangement
  Call Grav1.Initialize arrangement = VerticalArrangement1
  
When Grav1.Initialized
  // Set random colors
  Call Grav1.RandomColorGenerator
  
  // Create a regular grid of particles
  Call Grav1.RegularPointGenerator cellSize = 80 variance = 15
  
  // Make them circles with varying sizes
  Call Grav1.BallGenerator fromSize = 5 toSize = 20
  
  // Add fade animation
  Call Grav1.AlphaAnimator from = 100 to = 255 minDuration = 800 maxDuration = 1500
  
  // Add size pulsing
  Call Grav1.BallSizeAnimator fromSize = 5 toSize = 25 minDuration = 1000 maxDuration = 2000
  
  // Add gentle shake
  Call Grav1.ShakeAnimator variance = 3 minDuration = 500 maxDuration = 1000 direction = 0
  
  // Start the animation
  Call Grav1.Start
```

### Example 2: Hearts Moving in Heart Paths 🆕

Create a romantic effect with heart-shaped particles moving along heart paths:

```blocks
When Screen1.Initialize
  Call Grav1.Initialize arrangement = VerticalArrangement1
  
When Grav1.Initialized
  // Use array of romantic colors
  Call Grav1.ArrayColorGenerator colors = make a list ["#FF1744", "#F50057", "#E91E63"]
  
  // Place particles at specific positions
  Call Grav1.PercentPointGenerator percentPoints = make a list [50, 50]
  
  // Make particles heart-shaped
  Call Grav1.CustomShapeGenerator shapeType = "heart" width = 40 height = 40
  
  // Make hearts move in a heart-shaped path
  Call Grav1.ShapePathAnimatorWithSize shapeType = "heart" width = 200 height = 200 
    minDuration = 3000 maxDuration = 5000
  
  // Add gentle pulsing
  Call Grav1.AlphaAnimator from = 150 to = 255 minDuration = 1000 maxDuration = 2000
  
  // Start the animation
  Call Grav1.Start
```

### Example 3: Star Field Effect 🆕

Create a dynamic star field with various shapes:

```blocks
When Screen1.Initialize
  Call Grav1.Initialize arrangement = VerticalArrangement1
  
When Grav1.Initialized
  // Gold and white colors for stars
  Call Grav1.ArrayColorGenerator colors = make a list ["#FFD700", "#FFFFFF", "#FFA500"]
  
  // Random star positions
  Call Grav1.RegularPointGenerator cellSize = 100 variance = 40
  
  // Star-shaped particles
  Call Grav1.CustomShapeGenerator shapeType = "star" width = 25 height = 25
  
  // Twinkling effect
  Call Grav1.AlphaAnimator from = 80 to = 255 minDuration = 500 maxDuration = 1500
  
  // Gentle rotation via circular path
  Call Grav1.ShapePathAnimatorWithSize shapeType = "circle" width = 50 height = 50
    minDuration = 4000 maxDuration = 8000
  
  Call Grav1.Start
```

## Tips

1. **Call Initialize first**: Always initialize before calling any other methods
2. **Mix and match**: Combine different generators and animators for unique effects
3. **Performance**: Fewer particles (larger cellSize) = better performance
4. **Instant updates**: Changing generators while animating updates immediately
5. **Layer effects**: Add multiple animators for complex motion
6. **Custom shapes** 🆕: Use `CustomShapeGenerator` for 16 unique particle shapes
7. **Easy paths** 🆕: Use `ShapePathAnimatorWithSize` for simple shape path animations without SVG

## Troubleshooting

**Particles not showing?**
- Make sure you called `Initialize` with a valid arrangement
- Ensure the arrangement has width and height (not 0)
- Check that you called `Start`

**Animation not updating when I change settings?**
- All changes take effect immediately - no need to restart

**Too many/too few particles?**
- Adjust the `cellSize` parameter in point generators (smaller = more particles)

## Credits

Based on the Grav library by glomadrian.  
Extension developed by TechHamara.
