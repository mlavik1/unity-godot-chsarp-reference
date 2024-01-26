# EditorFileDialog for saving a file

This is similar to Unity's [EditorUtility.OpenFilePanel](https://docs.unity3d.com/ScriptReference/EditorUtility.SaveFilePanel.html).

```csharp
EditorFileDialog fileDialog = new EditorFileDialog();
fileDialog.FileMode = EditorFileDialog.FileModeEnum.SaveFile; // This makes it a "save file dialog"
fileDialog.CurrentDir = "res://MyFolder";
EditorInterface.Singleton.GetEditorViewport3D().AddChild(fileDialog);
fileDialog.FileSelected += (string filePath) => {
    GD.Print("User selected: " + filePath);
    // Save file to filePath
};
fileDialog.Popup();
```
