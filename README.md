<div align="center">
<h1><kbd>🧩 Grav</kbd></h1>
An extension for MIT App Inventor 2.<br>
The Grav extension allows you to create stunning particle animations in your App Inventor apps. It provides a highly customizable particle system with various generators for colors, positions, shapes, and animations. Developed by TechHamara using Fast.<br><a href='https://github.com/TechHamara/Th_Free_Extensions' target='_blank'><small><u>Find More Extension</u></small></a><br><a href='https://github.com/TechHamara/Th_Extensions_List/blob/main/LICENSE.md#terms-and-conditions-for-the-extension' target='_blank'><small><u>Terms & Conditions</u></small></a><br><a href='https://buymeacoffee.com/techhamara' target='_blank'><small><u>Find More On BuyMeCoffee Page</u></small></a>
</div>

## 📝 Specifications
* **
📦 **Package:** io.th.grav<br>
💾 **Size:** 47.24 KB<br>
⚙️ **Version:** 1.0<br>
📱 **Minimum API Level:** 7<br>
📅 **Updated On:** [date=2025-12-20 timezone="Asia/Calcutta"]<br>
💻 **Built & documented using:** [FAST](https://community.appinventor.mit.edu/t/fast-an-efficient-way-to-build-extensions/129103?u=jewel) <small><mark>v2.8.4</mark></small><br>


## Blocks

<img width="199" height="60" alt="Initialized_Event" src="https://github.com/user-attachments/assets/c71689bf-60cb-4b4f-b8b7-4519e1e9c428" />
<img width="259" height="60" alt="AnimationStopped_Event" src="https://github.com/user-attachments/assets/aee665d1-7c9c-480a-8497-58de4658801d" />
<img width="251" height="60" alt="AnimationStarted_Event" src="https://github.com/user-attachments/assets/d00a4a72-31da-41bd-a01b-0e1c94070b24" />

-----

<img width="233" height="130" alt="AlphaAnimator_Method" src="https://github.com/user-attachments/assets/34eab5a8-0a88-49b9-8940-dffab7e8df5d" />
<img width="158" height="30" alt="Stop_Method" src="https://github.com/user-attachments/assets/5ce41fe8-41c2-4719-9d0c-aab70cdaa337" />
<img width="159" height="30" alt="Start_Method" src="https://github.com/user-attachments/assets/c637b33e-5114-4036-af2f-706db74e8bf4" />
<img width="486" height="105" alt="SideToSideAnimator_Method" src="https://github.com/user-attachments/assets/4000899f-7586-497c-859d-cc0be6a4661e" />
<img width="486" height="155" alt="ShapePathAnimatorWithSize_Method" src="https://github.com/user-attachments/assets/40ef4328-8d37-49b1-b803-5a8a2593e456" />
<img width="428" height="205" alt="ShapePathAnimator_Method" src="https://github.com/user-attachments/assets/d71dd22a-2ed3-456d-bfc6-48e89380ec0f" />
<img width="449" height="130" alt="ShakeAnimator_Method" src="https://github.com/user-attachments/assets/ca8329e7-f6e9-44af-9ea6-0a8080299ab3" />
<img width="289" height="80" alt="RegularPointGenerator_Method" src="https://github.com/user-attachments/assets/3e1841bc-8e69-4b2c-86be-7ea1dcb3d34e" />
<img width="270" height="80" alt="RectangleGenerator_Method" src="https://github.com/user-attachments/assets/749795e8-f534-49ab-840d-2af46910895f" />
<img width="286" height="30" alt="RandomColorGenerator_Method" src="https://github.com/user-attachments/assets/8f2f656a-9112-443e-9d0a-e6200ed977d6" />
<img width="226" height="205" alt="PathAnimator_Method" src="https://github.com/user-attachments/assets/983be462-61ec-49c2-96ec-3e86881553c6" />
<img width="189" height="55" alt="Initialize_Method" src="https://github.com/user-attachments/assets/2b41cc2a-5227-440b-8592-90cb6b46c337" />
<img width="457" height="105" alt="CustomShapeGenerator_Method" src="https://github.com/user-attachments/assets/43a8c141-b060-4f7a-a48b-3868b44faa89" />
<img width="229" height="30" alt="ClearAnimators_Method" src="https://github.com/user-attachments/assets/8d915cb7-1b88-4cb9-bf8b-8b020cc4c427" />
<img width="288" height="80" alt="CircularPointGenerator_Method" src="https://github.com/user-attachments/assets/013336be-eb7e-4bf4-a76e-ef4df562a6d9" />
<img width="249" height="130" alt="BallSizeAnimator_Method" src="https://github.com/user-attachments/assets/56d0336c-34e9-4987-8631-b715d454f7b6" />
<img width="227" height="80" alt="BallGenerator_Method" src="https://github.com/user-attachments/assets/890ccd12-dbff-4496-b60b-865abeb3f17a" />

-----

<img width="311" height="30" alt="OneColorGenerator_Set_Property" src="https://github.com/user-attachments/assets/29fd9ea0-5dd4-4b2b-9f8c-6fe61ac8be8b" />
<img width="319" height="30" alt="ArrayColorGenerator_Set_Property" src="https://github.com/user-attachments/assets/7f0db4d0-d30d-48cb-8314-d9bac3510680" />
<img width="332" height="30" alt="PercentPointGenerator_Set_Property" src="https://github.com/user-attachments/assets/cb523fe9-c9cb-47b9-b22f-8216e9b5988b" />

## Descriptions

## <kbd>Events:</kbd>
**Grav** has total 3 events.

### Initialized
Event triggered when the Grav animation view has been successfully initialized and added to the arrangement. You can safely call configuration methods after this event.

### AnimationStarted
Event triggered when the particle animation has started. Use this to update UI elements or perform actions when animation begins.

### AnimationStopped
Event triggered when the particle animation has stopped. Use this to update UI elements or perform cleanup actions.

## <kbd>Methods:</kbd>
**Grav** has total 17 methods.

### Initialize
Initialize the Grav animation view inside an arrangement component. Call this method first before using any other functions. The view will fill the entire arrangement.

| Parameter | Type
| - | - |
| arrangement | component

### Start
Start the particle animation. All configured generators and animators will begin animating the particles on screen.

### Stop
Stop the particle animation. All animators will be halted and particles will freeze in their current positions.

### RandomColorGenerator
Set the color generator to Random mode. Each particle will be assigned a random color from the full color spectrum. Changes take effect immediately.

### RegularPointGenerator
Generate particles in a regular grid pattern. cellSize determines the spacing between particles (in pixels), and variance adds randomness to positions (in pixels). Smaller cellSize creates more particles. Changes take effect immediately.

| Parameter | Type
| - | - |
| cellSize | number
| variance | number

### CircularPointGenerator
Generate particles in a circular/radial pattern from the center. cellSize determines the radial spacing (in pixels), and variance adds randomness to positions (in pixels). Creates an organic, expanding pattern. Changes take effect immediately.

| Parameter | Type
| - | - |
| cellSize | number
| variance | number

### BallGenerator
Set particles to render as circles/balls. fromSize and toSize define the size range in pixels - each particle will be randomly sized between these values. Use the same value for both to have uniform-sized particles. Changes take effect immediately.

| Parameter | Type
| - | - |
| fromSize | number
| toSize | number

### RectangleGenerator
Set particles to render as rectangles. Specify the width and height in pixels. All particles will be the same size. Changes take effect immediately.

| Parameter | Type
| - | - |
| width | number
| height | number

### CustomShapeGenerator
Set particles to render as custom shapes. Supported shapes (case-insensitive): 'circle', 'ellipse', 'triangle', 'rectangle', 'trapezium', 'parallelogram', 'capsule', 'leaf', 'rhombus', 'heart', 'drop', 'star', 'diamond', 'pentagon', 'hexagon', 'cloud'. Specify width and height in pixels. Changes take effect immediately.

| Parameter | Type
| - | - |
| shapeType | ShapeType <small><mark>(helper blocks)</mark></small>
| width | number
| height | number

* Enums for **ShapeType**: `Circle`, `Ellipse`, `Triangle`, `Rectangle`, `Trapezium`, `Parallelogram`, `Capsule`, `Leaf`, `Rhombus`, `Heart`, `Drop`, `Star`, `Diamond`, `Pentagon`, `Hexagon`, `Cloud`

### AlphaAnimator
Add a transparency/fade animation to particles. 'from' and 'to' are opacity values (0-255, where 0 is transparent and 255 is opaque). minDuration and maxDuration are in milliseconds - each particle's animation duration is randomized within this range. Use multiple calls to add multiple animators.

| Parameter | Type
| - | - |
| from | number
| to | number
| minDuration | number
| maxDuration | number

### BallSizeAnimator
Add a size pulsing animation to ball particles. fromSize and toSize define the size range in pixels. minDuration and maxDuration are in milliseconds. Particles will continuously grow and shrink between these sizes. Only works with Ball generator.

| Parameter | Type
| - | - |
| fromSize | number
| toSize | number
| minDuration | number
| maxDuration | number

### ShakeAnimator
Add a shaking/vibration animation to particles. variance controls shake intensity in pixels. minDuration and maxDuration are in milliseconds. direction: 0 for horizontal shake, 1 for vertical shake. Particles will shake back and forth continuously.

| Parameter | Type
| - | - |
| variance | number
| minDuration | number
| maxDuration | number
| direction | ShakeDirection <small><mark>(helper blocks)</mark></small>

* Enums for **ShakeDirection**: `Horizontal`, `Vertical`

### SideToSideAnimator
Add a smooth side-to-side movement animation. minDuration and maxDuration are in milliseconds. direction: 0=LeftToRight, 1=RightToLeft, 2=UpToDown, 3=DownToUp. Particles will move across the screen in the specified direction and loop back.

| Parameter | Type
| - | - |
| minDuration | number
| maxDuration | number
| direction | DirectionType <small><mark>(helper blocks)</mark></small>

* Enums for **DirectionType**: `LeftToRight`, `RightToLeft`, `TopToBottom`, `BottomToTop`

### PathAnimator
Add an animation that moves particles along a custom SVG path. 'path' is an SVG path string (e.g., 'M 0,0 L 100,100'). minVariance and maxVariance add randomness to the path. originalWidth and originalHeight define the path's coordinate system. minDuration and maxDuration are in milliseconds for the complete path traversal.

| Parameter | Type
| - | - |
| path | text
| minVariance | number
| maxVariance | number
| originalWidth | number
| originalHeight | number
| minDuration | number
| maxDuration | number

### ShapePathAnimator
Add an animation that moves particles along a pre-built shape path. Supported shapes (case-insensitive): 'circle', 'ellipse', 'triangle', 'rectangle', 'trapezium', 'parallelogram', 'capsule', 'rhombus', 'heart', 'star', 'diamond', 'pentagon', 'hexagon'. minVariance and maxVariance add randomness to the path. originalWidth and originalHeight define the path's coordinate system (recommended 100x100). minDuration and maxDuration are in milliseconds for the complete path traversal.

| Parameter | Type
| - | - |
| shapeType | ShapeType <small><mark>(helper blocks)</mark></small>
| minVariance | number
| maxVariance | number
| originalWidth | number
| originalHeight | number
| minDuration | number
| maxDuration | number

* Enums for **ShapeType**: `Circle`, `Ellipse`, `Triangle`, `Rectangle`, `Trapezium`, `Parallelogram`, `Capsule`, `Leaf`, `Rhombus`, `Heart`, `Drop`, `Star`, `Diamond`, `Pentagon`, `Hexagon`, `Cloud`

### ShapePathAnimatorWithSize
Add an animation that moves particles along a pre-built shape path with custom size. Supported shapes (case-insensitive): 'circle', 'ellipse', 'triangle', 'rectangle', 'trapezium', 'parallelogram', 'capsule', 'rhombus', 'heart', 'star', 'diamond', 'pentagon', 'hexagon'. width and height define the size of the path in pixels. minDuration and maxDuration are in milliseconds for the complete path traversal.

| Parameter | Type
| - | - |
| shapeType | ShapeType <small><mark>(helper blocks)</mark></small>
| width | number
| height | number
| minDuration | number
| maxDuration | number

* Enums for **ShapeType**: `Circle`, `Ellipse`, `Triangle`, `Rectangle`, `Trapezium`, `Parallelogram`, `Capsule`, `Leaf`, `Rhombus`, `Heart`, `Drop`, `Star`, `Diamond`, `Pentagon`, `Hexagon`, `Cloud`

### ClearAnimators
Remove all animators from particles. Particles will remain visible but stop all movement and effects. Use this before adding a new set of animators or to create static particles. Changes take effect immediately.

## <kbd>Setters:</kbd>
**Grav** has total 3 setter properties.

### OneColorGenerator
Set all particles to use a single color. Provide the color as an App Inventor color value (e.g., from the color picker). Changes take effect immediately.

* Input type: `number`

### ArrayColorGenerator
Set particles to cycle through a list of colors. Provide colors as a list of App Inventor color values or hex strings (e.g., '#FF0000'). Particles will use colors from this array in sequence. Changes take effect immediately.

* Input type: `list`

### PercentPointGenerator
Generate particles at specific percentage positions on the screen. Provide a list of coordinates as percentages (0-100) in format: [x1, y1, x2, y2, ...]. For example, [50, 50] creates one particle at screen center, [25, 25, 75, 75] creates two particles. Changes take effect immediately.

* Input type: `list`

