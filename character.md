# Character

Generate a hierarchy of rigid bodies along with constraints and a control structure automatically, with optional markup in your native Maya joints to determine initial size, shape and behavior of the various limbs.

<br>

### Markup

Ragdoll currently takes these optional attribute into account when building your character.

- `joint.type` Determines the constraint behavior and shape *type*
- `joint.radius` Affects the shape *dimensions*
- `joint.translateX` Affects shape *length*

These types are currently considered.

| Joint Type | Result
|:-----------|:------------
| Elbow      | Hinge Constraint
| Knee       | Hinge Constraint
| Head       | Box shape
| Hand       | Box shape
| Foot       | Box shape
