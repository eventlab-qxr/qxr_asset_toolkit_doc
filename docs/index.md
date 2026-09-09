# Welcome to QXR Asset Toolkit

The **QXR Asset Toolkit** is a production-ready pipeline designed to optimize 3D assets and avatars for real-time engines like Unity and Unreal Engine. 

## Core Modules

The toolkit is built upon three modular components, each handling a critical step in the 3D optimization workflow:

* **Avatar Setup:** This module standardizes the skeleton and posture of imported characters. It uses heuristic algorithms to automatically detect and map bones, enforces a strict T-Pose, and scales the avatar to a standardized height. It also features an advanced volumetric medial axis engine for precise hand and finger rigging.
* **Mesh LOD:** Designed to maximize real-time performance. This module generates automated Levels of Detail (LODs) based on customizable decimation ratios. Simultaneously, it consolidates multiple meshes and materials by baking them into a single, highly optimized PBR texture atlas.
* **FBX Exporter:** The final step of the pipeline. It guarantees the asset is perfectly packaged for game engines by applying all global transforms, fixing unit scales, and embedding the processed textures into a clean, production-ready FBX file.

## Deployment Options

You can integrate this pipeline into your workflow in two ways: locally as a **[Blender Add-on](sections/addon/index.md)**, or deployed as an automated, containerized **[Cloud Web Service](sections/cloud/index.md)**. 

Use the sidebar to navigate through the detailed documentation and setup guides for each version.