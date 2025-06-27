> [!WARNING]
> The information presented here depends on Yotan Mod Core.
>

# Destroyable objects

This page will show you how to create world objects that may be destroyed by raids/etc.

**Before you continue** make sure you know the basics of custom items, as this won't go through the basics.

- [Introduction](./_introduction.md)
- [Your first static item](./your-first-item.md)

You also should have an actual item that may be put into the world already.

Making the object destroyable requires you to do the following steps:

1. Add a disabled broken sprite (`BrokenSpr`) as a children of the main object
2. Add a disabled triggerable box collider (`BrokenColl`) for the broken area (as a separate children object)
3. Add the `Destroyable Object` script to the main object

Suppose you have the following item:

```
GameObject: myitem_obj
|	|- Component: Box Collider (not a trigger)
|	|- Script: Custom Item Info
|
|-- GameObject: NormalSpr -- Display sprite

```

It must now look like:

```
GameObject: myitem_obj
|	|- Component: Box Collider (not a trigger)
|	|- Script: Custom Item Info
|	|- Script: Destroyable Object -- Add this
|
|-- GameObject: NormalSpr -- Display sprite
|
|	** Add these **
|-- GameObject: BrokenSpr (Disabled) -- Sprite when broken
|-- GameObject: BrokenColl (Disabled) -- Collider when broken
	|	|- Component: Box Collider (trigger)

```

### Destroyable Object

This configures how the object breaks down.

- **Item Info**: The main item object (`myitem_obj`)
- **Active**: Unknown. Set it to `true`
- **Defence Type**: Unknown. Set it to `Defence`
- **Attack**: Unknown. Set it to 0
- **Active Objects**: Add the children objects that should be active when the object is **functional**
  - In this example, this would be `NormalSpr`
- **Broken Objects**: Add the children objects that should be active when the object is **broken**
  - In this example, this would be `BrokenSpr` and `BrokenColl`
- **Destroy FX**: Unknown. Set it to `4`
- **Destryo SE**: Unknown. Set it to `39`
- **Coll Offset**: Unknown. Set it to `(0, 0, 0)`
