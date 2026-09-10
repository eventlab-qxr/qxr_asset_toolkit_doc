# FBX Exporter

The **FBX Exporter** is the final step in the QXR Asset Toolkit pipeline. Its primary function is to guarantee that the optimized avatar is perfectly packaged and correctly formatted for immediate use in real-time game engines like Unity and Unreal Engine.

## Core Features

Exporting directly from Blender to game engines can often result in scale mismatches or broken rig orientations. This module automates the necessary fixes before export:

* **Global Transform Application:** Automatically applies all translation, rotation, and scale data to the mesh and armature, ensuring a clean `(0, 0, 0)` origin and `(1, 1, 1)` scale.
* **Unit Scale Correction:** Adjusts the internal metric scaling so the avatar imports seamlessly into engines without requiring an artificial scale factor (preventing the common `100x` scale bug).
* **Media Embedding:** Ensures that the PBR texture atlas generated in the Mesh LOD step is properly baked and embedded directly into the final `.fbx` file, making it a portable, plug-and-play asset.

## Interface & Controls

The **FBX Exporter Panel** provides a streamlined, one-click solution:

* **Export Path:** Defines the output directory where the final `.fbx` file will be saved. By default, it will attempt to use the same directory as your currently saved `.blend` file.
* **Export Asset Button:** Triggers the final cleanup and packaging script.

## Recommended Workflow

1. Ensure you have run the **Avatar Setup** and **Mesh LOD** modules.
2. Select your final avatar collection or the main armature in the 3D Viewport.
3. Open the **FBX Exporter** panel in the QXR tab.
4. Verify your target export directory.
5. Click **Export Asset**. 

Your avatar is now ready to be dragged and dropped directly into your Unity or Unreal Engine project!