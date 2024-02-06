# Getting the delta time

In Unity you can use [Time.deltaTime](https://docs.unity3d.com/ScriptReference/Time-deltaTime.html) to get the time passed since last frame.

In Godot you can instead override the `public override void _Process(double delta)` of a Node, and use the `double delta` parameter.

**Unity:**
```csharp
using UnityEngine;
public class FloatingObject : MonoBehaviour
{
    public float degreesPerSecond = 2.0f;
    void Update()
    {
        transform.position += Vector3.up * Time.deltaTime;
    }
}
```

**Godot:**
```csharp
using Godot;
using System;

public partial class FloatingObject : Node3D
{
	public override void _Process(double delta)
	{
		this.Position += Vector3.Up * (float)delta;
	}
}
```
