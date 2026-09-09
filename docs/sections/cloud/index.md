# Automated Pipeline: Cloud Service

The Cloud version of the QXR Asset Toolkit is a web-based, fire-and-forget solution. It processes `.glb` files asynchronously without requiring local software installations.

## Web Interface
To process an asset, navigate to the web portal and drag-and-drop your `.glb` file.

![Web Interface with Drag and Drop Zone](ui.png)

### Optimization Settings
Before queuing your asset, you can tweak the generation parameters:
* **LOD Count:** The number of detail levels to generate.
* **Atlas Resolution:** The final PBR texture size (e.g., 2048px).
* **Decimation Ratio:** The polygon reduction aggressiveness per LOD level.

## Notifications
Once the server finishes the pipeline, you will receive an automated email containing a secure download link for your production-ready `.fbx` package.

![Example of the Success Email](email.png)

*Note: For privacy and server health, processing data is destroyed immediately, and the final ZIP file is purged after 24 hours.*