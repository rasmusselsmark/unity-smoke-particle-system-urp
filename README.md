# unity-smoke-particle-system-urp

### Unity project with a very simple terrain

1. Create new Unity 3D URP project (can also be used with built-in/core renderer project)
1. Create a plane and paint it green (using a material)

### Simple smoke particle system

1. Create Effects -> Particle System
1. Set particle size, speed and color
   ![Set particle size, speed and color](./Assets/Documentation/Images/particle-system-setup-color.png)
1. Set emission
   ![Set emission](./Assets/Documentation/Images/particle-system-setup-emission.png)
1. Set shape
![Set shape](./Assets/Documentation/Images/particle-system-setup-shape.png)

Already by now, we have a simple working smoke effect

_Optional: [Install Starter Assets - Third Person Character Controller](https://assetstore.unity.com/packages/essentials/starter-assets-third-person-character-controller-196526), so we can easily walk around in scene (if URP project, use Edit -> Rendering -> Materials -> Convert... to convert materials for character to URP)_

Your scene could now look something like this:

![Playmode with default material](./Assets/Documentation/Images/playmode-with-default-material.png)

### More realistic smoke using a texture material

1. Download the zip file containing all smoke textures from https://opengameart.org/content/smoke-aura
1. Copy the file `0000.png` into Unity project
1. Create a new material and name it "Smoke"
1. Use shader "Mobile/Particles/Alpha Blended" and set the smoke tecture image
   ![Playmode with default material](./Assets/Documentation/Images/smoke-material-shader.png)
1. Use the material in particle system
   ![Use smoke material](./Assets/Documentation/Images/particle-system-setup-material.png)
1. Since the texture images are darker, perhaps adjust the color a bit
1. Adjust "Size over lifetime" to make smoke smaller at the top
   ![Size over lifetime](./Assets/Documentation/Images/particle-system-setup-size-over-lifetime.png)

When going to playmode, should look something like the following:
![Playmode with smoke material](./Assets/Documentation/Images/playmode-with-smoke-material.png)

Additionally you can configure the following settings for the particle system to make it look even more realistic:

* Noise (set Strength to somewhere between `0.1` and `0.25`)
* Color over lifetime, to make smoke brighter at top

The above steps are based on the Youtube video [How to Create SMOKE with Particles in Unity!](https://www.youtube.com/watch?v=YwGS73QpPt0), so you can watch that for more details.