# Character

Generate a hierarchy of rigid bodies along with constraints and a control structure automatically, with optional markup in your native Maya joints to determine initial size, shape and behavior of the various limbs.

**Table of Contents**

- [Markup](#markup)
- [Special Cases](#special-cases)
    - [Tri-fork](#tri-fork)
    - [Y-fork](#y-fork)
- [Normalise Shapes](#normalise-sizes)

<br>

### Markup

Native Maya joints have an attribute in the Attribute Editor called "Joint Labelling". These can now be used for providing hints to Ragdoll during the creation of a character.

![image](https://user-images.githubusercontent.com/2152766/100616188-a4a98b00-3310-11eb-98a8-bb819be9966a.png)

| Label  | Result
|:-------|:---------
| `Knee`,<br>`Elbow` | Uses a **Hinge** rather than Socket constraint
| `Head`,<br>`Foot`<br>`Hand`<br>`Toe` | Uses **Box** shape, instead of Cylinder
| `"Stop"` | From the root, do not progress further down the hierarchy. This can be *handy* when wanting to build a character from everything except fingers, toes and other complex sub-hierarchies.
| `"Skip"` | (Not yet implemented) From the root, skip this joint and continue with the immediate child. This is meant for special joints in a hierarchy that doesn't necessarily need a physical counterpart. Like helper joints for skinweight or attachment points for props.

<br>

### Special Cases

I'm working on turning the Character tool into a one-click solution for creating an animatable character and rig from a skeleton. Here are a few more steps along that road.

- [Tri-fork](#tri-fork)
- [Y-fork](#y-fork)

<br>

#### Tri-fork

Common in the root of any skeleton of two legs and a spine, but general to any configuration without a clear up, down, right or left direction.

| Before | After
|:--|:--
| ![image](https://user-images.githubusercontent.com/2152766/100615318-5778e980-330f-11eb-82cd-7f2e3ca7bb0d.png) | ![image](https://user-images.githubusercontent.com/2152766/100614985-de799200-330e-11eb-9a51-13d307579bea.png)

<br>

#### Y-fork

Typical for chest/should areas, where there is a clear vertical direction but no clear left or right.

| Before | After
|:--|:--
| ![image](https://user-images.githubusercontent.com/2152766/100615337-6069bb00-330f-11eb-91d0-abf5ad6587b7.png)  | ![image](https://user-images.githubusercontent.com/2152766/100615187-2698b480-330f-11eb-9ed3-4e7fa6330677.png)
