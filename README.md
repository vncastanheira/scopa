# Scopa

*Scopa* ("broom" in Latin) is a Unity level design plugin that adds Quake / Half-Life .MAP importing. Kind of like [Qodot](https://github.com/QodotPlugin/qodot-plugin) but for Unity.

# WARNING: this is in early development, it's broken and not ready for public use yet.

- .MAP import (Quake 1 / Valve 220 format)
    - generates a prefab with 3D meshes, colliders, and parsed entity data
    - built-in procedural environment art tools (mesh normal smoothing, hotspot UV texturing, (PLANNED) detail placement like grass)
- .WAD import / export (Quake 1 WAD2 / Half-Life WAD3 format)
- .FGD generator (to export entity definitions to the level editor)
- works at editor time or runtime (for modding support)

To build .MAP levels, we strongly recommend [TrenchBroom](https://github.com/TrenchBroom/TrenchBroom).

## Installation

This is a [Unity Package](https://docs.unity3d.com/Manual/PackagesList.html) for Unity 2020.1 or later. It is self-contained with zero dependencies.

To install, just open [Package Manager](https://docs.unity3d.com/Manual/upm-ui.html) and add `https://github.com/radiatoryang/scopa.git` [(more info and help)](https://docs.unity3d.com/2021.2/Documentation/Manual/upm-ui-giturl.html)

## Usage

Put a .MAP or .WAD file in your `/Assets/` folder and it'll import automatically, generating assets / prefabs for you to use.

**Do your edits in the level editor, not in Unity!** If you edit the prefab instance, your changes may be erased when you re-import the .MAP again. Treating the .MAP file as the "single source of truth." 

To learn about more features, such as runtime support, entity handling, and the FGD generator, read the [Documentation](https://github.com/radiatoryang/scopa/blob/main/Documentation~/Scopa.md).

## Limitations

- **This package doesn't have game code.** It imports the file, sets up colliders, and imports entity data. You still have to make the game yourself.

## Contributions

Issues and pull requests are currently NOT accepted at this time. Development is still very early.

## Acknowledgments / Credits

- based on [Sledge Formats](https://github.com/LogicAndTrick/sledge-formats)
- hotspot UV implementation based on [Unity Hotspot UV](https://github.com/BennyKok/unity-hotspot-uv)
- looking for a BSP plugin? try [Unity3D BSP Importer](https://github.com/wfowler1/Unity3D-BSP-Importer)
