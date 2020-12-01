# Dynamic Control

Turn any animation control into a *dynamic control* for automatic overlapping and secondary animation.

**Videos**

- [Single Control](https://www.youtube.com/watch?v=Zhe9pAaAd7s&list=PLL4XIS5Woc6nVsTdsvs0XLmiKmXVCdwXy&index=6)
- [Control Chains](https://www.youtube.com/watch?v=xzC3N1zxM6U&list=PLL4XIS5Woc6nVsTdsvs0XLmiKmXVCdwXy&index=10)
- [Control Branches](https://www.youtube.com/watch?v=NSShJ9sm4Eo&list=PLL4XIS5Woc6nVsTdsvs0XLmiKmXVCdwXy&index=12)
- [Colliders](https://www.youtube.com/watch?v=NSShJ9sm4Eo&list=PLL4XIS5Woc6nVsTdsvs0XLmiKmXVCdwXy&index=12)
- [Animation + Simulation](https://www.youtube.com/watch?v=ZR1NKv7ZRCg&list=PLL4XIS5Woc6nVsTdsvs0XLmiKmXVCdwXy&index=13)

![ragdolldynamic4](https://user-images.githubusercontent.com/2152766/100746824-2107a100-33d9-11eb-9498-e2f4bcacff6e.gif)

<br>

### Capsules

Dynamic Control works best with controls that wrap around the character geometry. If you aren't that lucky, then you can instead use the position of each control to automatically figure out dimensions for a simplified capsule geometry.

1. Select **root**
    - This will be made *passive* i.e. follow your original animation exactly
2. Select **child**
    - These will be *active* and *connected* in the order you select
3. Select **tip**
    - To be used for determining the length of that final capsule

![ragdolldynamic3](https://user-images.githubusercontent.com/2152766/100735662-82277880-33c9-11eb-9704-a154d9077ae8.gif)
