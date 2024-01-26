# Unity-to-Godot C# reference

This document is an attempt at mapping Unity C# methods/classes/concepts to the corresponding Godot versions.

Unity and Godot are quite different by nature, but for everything you can do in Unity there's usually a way to do the same in Godot. Hope this can help others!

## Callback methods

| Unity | Godot |
| ----- | ----- |
| [Awake](https://docs.unity3d.com/ScriptReference/MonoBehaviour.Awake.html) | [_EnterTree](https://docs.godotengine.org/en/stable/tutorials/scripting/overridable_functions.html#overridable-functions) |
| [Start](https://docs.unity3d.com/ScriptReference/MonoBehaviour.Start.html) | [_Ready](https://docs.godotengine.org/en/stable/tutorials/scripting/overridable_functions.html#overridable-functions) |
| [Update](https://docs.unity3d.com/ScriptReference/MonoBehaviour.Update.html) | [_Process](https://docs.godotengine.org/en/stable/tutorials/scripting/overridable_functions.html#overridable-functions) |
| [OnDestroy](https://docs.unity3d.com/ScriptReference/MonoBehaviour.OnDestroy.html) | [_ExitTree](https://docs.godotengine.org/en/stable/tutorials/scripting/overridable_functions.html#overridable-functions) |

## Methods and properties

| Unity | Godot |
| ----- | ----- |
| [Application.isEditor](https://docs.unity3d.com/ScriptReference/Application-isEditor.html) | [Engine.IsEditorHint](https://docs.godotengine.org/en/stable/classes/class_engine.html#class-engine-method-is-editor-hint) |
| [EditorUtility.OpenFilePanel](https://docs.unity3d.com/ScriptReference/EditorUtility.OpenFilePanel.html) | [EditorFileDialog](https://docs.godotengine.org/en/stable/classes/class_editorfiledialog.html) |
| [EditorUtility.SaveFilePanel](https://docs.unity3d.com/ScriptReference/EditorUtility.SaveFilePanel.html) | [EditorFileDialog](https://docs.godotengine.org/en/stable/classes/class_editorfiledialog.html) |
| [Material.SetColor](https://docs.unity3d.com/ScriptReference/Material.SetColor.html) | [SetShaderParameter](https://docs.godotengine.org/en/stable/classes/class_shadermaterial.html#method-descriptions) |
| [Material.SetFloat](https://docs.unity3d.com/ScriptReference/Material.SetFloat.html) | [SetShaderParameter](https://docs.godotengine.org/en/stable/classes/class_shadermaterial.html#method-descriptions) |
| [Material.SetInt](https://docs.unity3d.com/ScriptReference/Material.SetInt.html) | [SetShaderParameter](https://docs.godotengine.org/en/stable/classes/class_shadermaterial.html#method-descriptions) |
| [Material.SetTexture](https://docs.unity3d.com/ScriptReference/Material.SetTexture.html) | [SetShaderParameter](https://docs.godotengine.org/en/stable/classes/class_shadermaterial.html#method-descriptions) |

## Classes

| Unity | Godot |
| ----- | ----- |
| [Editor](https://docs.unity3d.com/ScriptReference/Editor.html) | [EditorInspectorPlugin](https://docs.godotengine.org/en/stable/classes/class_editorinspectorplugin.html) |
| [Texture2D](https://docs.unity3d.com/ScriptReference/Texture2D.html) | [ImageTexture](hhttps://docs.godotengine.org/en/stable/classes/class_imagetexture.html) |
| [Texture3D](https://docs.unity3d.com/ScriptReference/Texture3D.html) | [ImageTexture3D](https://docs.godotengine.org/en/stable/classes/class_imagetexture3d.html) |

## Preprocessor definitions:
| Unity | Godot |
| ----- | ----- |
| [UNITY_EDITOR](https://docs.unity3d.com/Manual/PlatformDependentCompilation.html) | [TOOLS](https://docs.godotengine.org/en/stable/tutorials/scripting/c_sharp/c_sharp_features.html#preprocessor-defines) |
| [UNITY_EDITOR_WIN + UNITY_STANDALONE_WIN](https://docs.unity3d.com/Manual/PlatformDependentCompilation.html) | [GODOT_WINDOWS](https://docs.godotengine.org/en/stable/tutorials/scripting/c_sharp/c_sharp_features.html#preprocessor-defines) |
| [UNITY_EDITOR_LINUX + UNITY_STANDALONE_LINUX](https://docs.unity3d.com/Manual/PlatformDependentCompilation.html) | [GODOT_LINUXBSD](https://docs.godotengine.org/en/stable/tutorials/scripting/c_sharp/c_sharp_features.html#preprocessor-defines) |
| [UNITY_EDITOR_OSX + UNITY_STANDALONE_OSX](https://docs.unity3d.com/Manual/PlatformDependentCompilation.html) | [GODOT_MACOS](https://docs.godotengine.org/en/stable/tutorials/scripting/c_sharp/c_sharp_features.html#preprocessor-defines) |
