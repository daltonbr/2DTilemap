# 2DTilemap

In this live session we will explore worldbuilding in 2D using Tilemap and 2D Cinemachine. Tilemap makes it fast and easy to create and iterate level design cycles right in Unity, so artists and designers can rapidly prototype when building 2D game worlds. We will look at how you can paint levels using the new tile and brush tools which allow you to define rules for how tiles behave when placed, creating platforms with dynamic edges, animated tiles, random tiles, and more. Cinemachine, is a dynamic, procedural camera system which it easy to automate composition and tracking to enhance gameplay. Cinemachine is now available for 2D games. In this segment we introduce our project and goals.

## 2D Extras

Currently some of the Tilemap features are in development and can be found at
[github.com/Unity-Technologies/2d-extras](https://github.com/Unity-Technologies/2d-extras)

## Disclaimer

Based on a [Live Session: 2D World building w/ Tilemap & Cinemachine for 2D](https://unity3d.com/learn/tutorials/topics/2d-game-creation/intro-2d-world-building-w-tilemap?playlist=17093)
by Matthew Schell - Unity Evangelist

This course was originally checked for Unity 2017.2, but I am using a more recent version 2018.3.0b1 (beta). So I am making the necessary adjustments.

## Tips

### Colliders

To add a collider to a tilemap, select the Tilemap that you want to put a collider (normally is a child of a **Grid** in your Hierarchy), then add a `TilemapCollider2D`, and then a `CompositeCollider2D`. In the first one select `Used by Composite`

Optionally select `Generation Type: Synchronous` (in the CompositeCollider2D). The Collider will 'regenerate' itself, if you remove it.

### Cinemachine

Add a `Cinemachine` -> `Create 2D Camera`  

Select the Soft and Hard Zones in Game Screen.  

`Add Extensions` (at bottom of the Cinemachine Virtual Camera) -> `Cinemachine Confiner`
Then add a CompositeCollider2D or a PolygonCollider2D to your Background object and then use this collider as a `Bounding Shape 2D` for our Confiner.

