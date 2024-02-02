# ImageTexture (Godot) vs Texture2D (Unity)

In Unity the [Texture2D](https://docs.unity3d.com/ScriptReference/Texture2D.html) class is used to create 2D textures. There are several ways of filling up their pixel data, such as by calling [SetPixels](https://docs.unity3d.com/ScriptReference/Texture2D.SetPixels.html) or [SetPixelData](https://docs.unity3d.com/ScriptReference/Texture2D.SetPixelData.html).

In Godot the texture data is stored in an `Image`, which is then passed to an `ImageTexture` to be used on the GPU.

**Unity:**
```csharp
Color[] colourData = new Color[TEXTURE_WIDTH * TEXTURE_HEIGHT];
// fill colourData
// ...
texture = new Texture2D(TEXTURE_WIDTH, TEXTURE_HEIGHT, TextureFormat.RGBAFloat, false);
texture.SetPixels(colourData);
texture.Apply();
```

**Godot:**
```csharp
Color[] colourData = new Color[TEXTURE_WIDTH * TEXTURE_HEIGHT];
// fill colourData
// ...
byte[] byteArray = new byte[colourData.Length * 4];
Buffer.BlockCopy(colourData, 0, byteArray, 0, byteArray.Length);
Image image = Image.CreateFromData(TEXTURE_WIDTH, 1, false, Image.Format.Rgbaf, byteArray);
ImageTexture texture = ImageTexture.CreateFromImage(image);
```
