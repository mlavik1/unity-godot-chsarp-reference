# Quaternion.FromEuler: Getting euler angles from a Quaternion

This is similar to Unity's [Quaternion.Euler](https://docs.unity3d.com/ScriptReference/Quaternion.Euler.html), except the input values are asumed to be in radians (Unity uses degrees).

You can convert from degrees to radians by using `Mathf.DegToRad`.

**Unity:**
```csharp
Quaternion quat = Quaternion.Euler(270.0f, 0.0f, 0.0f);
```

**Godot:**
```csharp
Quaternion quat = Quaternion.Euler(new Vector3(Mathf.DegToRad(90.0f), 0.0f, 0.0f));
```
