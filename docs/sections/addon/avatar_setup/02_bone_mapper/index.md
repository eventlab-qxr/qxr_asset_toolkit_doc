# Bone Mapper

Characters downloaded from different sources or 3D marketplaces rarely share the same bone naming conventions. The **Bone Mapper** acts as a translation layer, identifying the specific bones in your imported armature and mapping them to the standardized internal QXR nomenclature. 

To make navigation intuitive, the interface groups the skeletal hierarchy into four main tabs, directly inspired by Unity’s Humanoid mapping system: **Body, Head, L. Hand,** and **R. Hand**.

![Bone Assignation](bone_mapper.png)

## Mapping Workflow

1. **Auto-Detect Bones:** Start by clicking the `Auto-Detect` button (magnifying glass icon) at the bottom of the panel. The toolkit will run a heuristic scan based on naming conventions to intelligently find and assign as many empty slots as possible.
2. **Manual Assignment:** If the auto-detection misses a bone due to a highly unconventional naming scheme, you can easily map it yourself by clicking the search field next to any unassigned bone and selecting the correct bone from the dropdown list.

## Bone Status Indicators

The UI provides immediate visual feedback on the state of your skeletal mapping through specific icons next to each bone field:

* **⚠️ Warning Icon:** Indicates a **mandatory** bone that is currently **unassigned**. All mandatory bones must be mapped before you can proceed to the Avatar Pose or subsequent rigging phases.
* **⚪ Filled Circle:** Indicates a **mandatory** bone that has been **successfully assigned**.
* **⚫ Empty Circle:** Indicates an **optional** bone (e.g., Upper Chest, Jaw). It remains an empty circle whether it is assigned or left empty. While mapping them provides higher animation fidelity, the pipeline will safely adapt and function without them.

## Special Case: Topological Hips Resolution

You will notice that the **Hips** bone field is disabled and cannot be assigned manually. Instead, the toolkit calculates its exact position dynamically. 

Once the Spine, Left Upper Leg, and Right Upper Leg bones are mapped, the core mapper algorithm executes a topological resolution. It traverses upwards through the hierarchical parent paths of these three bones to find their intersection. The first common ancestor bone shared by the spine and both legs is automatically locked in as the true Hips.
