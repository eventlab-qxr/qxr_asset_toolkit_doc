# Mesh Cleaner

Before any skeletal work begins, the mesh data must be clean and properly linked to the armature. Often, imported avatars come with scattered geometry, unapplied transforms, or separated body parts that unnecessarily increase rendering draw calls.

The **Mesh Cleaner** module analyzes all meshes driven by the active skeleton, cleans their topology, and organizes them into specific functional categories:

* **HEAD MESHES (Unmerged):** This category is reserved for facial geometry, including the main head, eyes, teeth, and eyelashes. **Crucial:** Meshes placed in this category are explicitly *ignored* during the merge process. This isolation guarantees that any existing facial Blendshapes (Shape Keys)—which are essential for lip-syncing, eye tracking, and expressions—are perfectly preserved.
* **UPPER & LOWER BODY (Merge & Weld):** These categories hold the structural parts of the character, such as the torso, limbs, and clothing. To maximize real-time engine performance, the pipeline will permanently merge these meshes together and automatically weld any disconnected vertices along their seams.

![Mesh Cleaner Tab](mesh_cleaner.png)

## Managing Mesh Categories

Upon clicking **Refresh Meshes**, the toolkit attempts to auto-assign categories based on mesh nomenclature and spatial positioning. 

* **Identify:** Each mesh name in the list functions as a clickable button. Clicking it will select the corresponding mesh directly in the Blender 3D Viewport, allowing you to quickly identify it and verify its assignment.
* **Reassign:** If a mesh is in the wrong category, click the **down arrow (▼)** located on its right side to open the quick-assign menu, and select its correct target group (Head, Upper Body, or Lower Body).

Once you are confident that every mesh is placed in its correct category, click the **Clean & Merge Meshes** button at the bottom of the panel to execute the consolidation process.
