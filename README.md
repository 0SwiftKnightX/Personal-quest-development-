# Personal Quest Development — Unified XR

This is the single Godot project assembled from the linked XR reference projects.

## Active runtime

- Godot 4.7
- OpenXR
- Godot XR Tools current master
- OpenXR Vendors source preserved under references/openxr-vendors
- Compatibility renderer
- Meta Quest target

## Composition

The active project uses one project.godot, one staging/XR initialization path, one XR Tools foundation, and one interaction lab.

The linked projects are preserved as exact Git submodules under references/ so their scenes, project settings, assets, and history remain available without allowing incompatible Project.godot files or addon generations to override the active project.

## Reference sources

- GodotVR/godot-xr-template
- GodotVR/godot-xr-tools
- BastiaanOlij/godot-xr-flynn-demo
- Malcolmnixon/godot-xr-tools-demo
- 0SwiftKnightX/Startup

## First integrated proof

Boot -> XR staging -> interaction lab -> pointer interaction -> physical pickup of three test cubes.

Flynn and Malcolm-specific systems are retained as reference sources and will be promoted only after their dependencies are ported to the active Godot/XR Tools generation.
