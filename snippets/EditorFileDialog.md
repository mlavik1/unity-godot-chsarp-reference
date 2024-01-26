# EditorFileDialog

```csharp
EditorFileDialog fileDialog = new EditorFileDialog();
fileDialog.FileMode = EditorFileDialog.FileModeEnum.OpenFile;
fileDialog.CurrentDir = "res://MyFolder";
EditorInterface.Singleton.GetEditorViewport3D().AddChild(fileDialog);
fileDialog.FileSelected += (string filePath) => {
    GD.Print("User selected: " + filePath);
};
fileDialog.Popup();
```
