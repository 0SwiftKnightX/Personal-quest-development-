# Unified XR Integration

## Rule

Everything that belongs together moves together. Project settings are reconciled at the root; incompatible Project.godot files never override the root project.

## Active ownership

- Platform/runtime: root project.godot and OpenXR.
- XR foundation: addons/godot-xr-tools.
- Android/Quest vendor source: references/openxr-vendors. Its packaged addon is not yet promoted into the active root.
- Scene staging: XR Tools staging.
- Interaction lab: scenes/xr_lab.tscn.

## References

The original repositories are exact submodules. This preserves their working scenes and dependency relationships without pretending that Godot 3-era or custom XR Tools2 scenes are already compatible with the active runtime.

## Promotion process

1. Map scene dependencies.
2. Map script/API dependencies.
3. Check Godot and XR Tools generation.
4. Port the complete dependency closure.
5. Validate scene import/headless parsing.
6. Only then promote the scene into the active project.

Godot 4 provides a command-line 3-to-4 conversion tool, but conversion can require manual follow-up, so converted source is not treated as production-ready without validation.

## Current state

The root project is the active unified project. The vendor addon remains a staged source dependency until its packaged addon layout is promoted without changing resource paths. The first integrated lab uses the current XR Tools foundation and is independent of the legacy/custom demo configurations.
