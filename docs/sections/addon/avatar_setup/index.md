# Avatar Setup

The **Avatar Setup** module is the foundational step of the QXR pipeline. It standardizes incoming 3D character models by normalizing dimensions, correcting skeletal postures, and preparing the rig for full-body tracking and IK compatibility. 

This module can be executed either fully automatically or step-by-step through its specific submodules.

---

## Master Pipeline (Automatic Setup)

The **Master Pipeline** is designed for maximum efficiency and mirrors the exact behavior of our headless Cloud Service. 

By clicking **Automatic Setup**, the toolkit sequentially executes all the individual submodules (Mesh Cleaner, Bone Mapper, Pose, Head, and Hand Rigger) using their default, production-tested parameters. 

![Master Pipeline UI](master_pipeline.png)

> **Performance Note:** Because this process chains multiple complex algorithms (including topological mapping and volumetric voxel analysis) the Blender UI will freeze for a few seconds. This is completely normal behavior.

---

## Manual Submodules

If your asset requires specific tweaks or fails the automatic process due to an unconventional rig structure, you can run and configure each step manually using the module tabs.
