# Getting the forward vector of a Node3D

In Unity you can use [Transform.forward](https://docs.unity3d.com/ScriptReference/Transform-forward.html) to get the forward vector of an object.

In Godot you can use `Node3D.GlobalTransform.Basis.Z`.

**Unity:**
```csharp
transform.position += this.transform.forward * Time.deltaTime;
```

**Godot:**
```csharp
this.Position += -this.GlobalTransform.Basis.Z * (float)delta;
```
