# EditorFileDialog for opening a file

Godot has a `EditorFileDialog` and `FileDialog` class, which is similar to Unity's [EditorUtility.OpenFilePanel](https://docs.unity3d.com/ScriptReference/EditorUtility.OpenFilePanel.html).

```csharp
EditorFileDialog fileDialog = new EditorFileDialog();
fileDialog.FileMode = EditorFileDialog.FileModeEnum.OpenFile; // This makes it an "open file dialog"
fileDialog.CurrentDir = "res://MyFolder";
EditorInterface.Singleton.GetEditorViewport3D().AddChild(fileDialog);
fileDialog.FileSelected += (string filePath) => {
    GD.Print("User selected: " + filePath);
    // Read file from filePath
};
fileDialog.Popup();
```
