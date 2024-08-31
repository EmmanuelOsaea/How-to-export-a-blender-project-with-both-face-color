# How-to-export-a-blender-project-with-both-face-color
Here's a comprehensive step-by-step written tutorial for complete beginners on how to export a simple Blender object with both face color and UV color texture to Roblox Studio:

### Step 1: Set Up Your Blender Object

1. **Open Blender**:
   - Launch Blender and create a new project.

2. **Create or Import a Simple Object**:
   - You can either create a new object (e.g., a cube, sphere, etc.) by going to the **Add** menu and choosing **Mesh**.
   - Alternatively, if you have an object prepared, you can import it into Blender using **File > Import**.

3. **Apply Material and Face Colors**:
   - Select your object and switch to the **Shading** workspace.
   - In the **Shader Editor**, click **New** to create a new material.
   - In the **Material Properties** panel, adjust the **Base Color** to the desired face color.
   - If you want face colors instead of textures, ensure that the **Principled BSDF** shader is connected to the **Material Output** node.

4. **UV Unwrapping**:
   - With your object selected, press **Tab** to enter **Edit Mode**.
   - Press **A** to select all faces.
   - Press **U** and select **Smart UV Project** (or any appropriate UV unwrapping method).
   - Switch to the **UV Editor** to verify the UV map of your object.

5. **Apply a UV Texture**:
   - Switch back to the **Shading** tab.
   - In the **Shader Editor**, press **Shift + A** to add a new node, and choose **Image Texture**.
   - Open a texture file (e.g., PNG or JPEG) and connect the **Color** output of the Image Texture node to the **Base Color** input of the **Principled BSDF** shader.
   - This texture will now be applied to your object's UV map.

### Step 2: Bake Face Colors (Optional)
If you used face colors and want to convert them to a texture for easier use in Roblox:

1. **Prepare for Baking**:
   - Switch to **Cycles Render Engine** in the **Render Properties** panel.
   - Add an **Image Texture** node in the **Shader Editor**, create a new blank texture, and leave it unconnected to the material.
   
2. **Bake the Colors**:
   - In **Render Properties**, scroll down to the **Bake** section.
   - Select **Diffuse** as the Bake Type, ensuring that **Direct** and **Indirect** lighting are unchecked, leaving only **Color** checked.
   - With your object selected, press **Bake**. This will create a new texture with the colors applied to the faces of your object.

3. **Save the Baked Texture**:
   - Once baking is done, save the generated texture image by going to the **UV Editor** and choosing **Image > Save As**.

### Step 3: Export the Model from Blender

1. **Export as FBX**:
   - With your object selected in **Object Mode**, go to **File > Export > FBX (.fbx)**.
   - In the export settings, configure the following:
     - **Limit to Selected Objects**: Ensures only the selected object is exported.
     - **Path Mode**: Set to **Copy**, then click the box next to it labeled **Embed Textures**.
   - Choose a location and save the FBX file.

### Step 4: Importing into Roblox Studio

1. **Open Roblox Studio**:
   - Launch Roblox Studio and open your desired project or create a new one.

2. **Import the FBX**:
   - In Roblox Studio, go to the **View** tab and open the **Asset Manager**.
   - In the **Asset Manager**, right-click in the **Meshes** section and select **Add Meshes**.
   - Find the FBX file you exported from Blender and import it.

3. **Insert the Mesh into Your Scene**:
   - Once imported, right-click on the mesh in the **Asset Manager** and choose **Insert with Location**.
   - The mesh will now appear in your scene.

4. **Apply Textures in Roblox Studio**:
   - If the textures were correctly embedded in the FBX file, they should automatically appear on the model.
   - If they do not appear:
     - Select your object in the **Explorer** panel.
     - In the **Properties** panel, look for the **MeshPart**. Here, you can apply your textures manually by clicking **TextureID** and uploading the saved textures.

### Step 5: Final Adjustments in Roblox Studio

1. **Scale and Position**:
   - Adjust the position, rotation, and scale of the object within the scene by using the **Move**, **Scale**, and **Rotate** tools in Roblox Studio.

2. **Check the Physics**:
   - Ensure that your mesh interacts correctly with Roblox physics by testing it in **Play Mode**.
   - You can also tweak the **CollisionFidelity** and **RenderFidelity** settings in the **Properties** panel of the mesh.

3. **Optimize the Mesh**:
   - To make sure the mesh works well in-game, check for optimization issues by ensuring the mesh is appropriately sized and doesn’t have unnecessary complexity.

### Conclusion
You have successfully exported a Blender object with face color and UV texture to Roblox Studio. Now you can integrate it into your Roblox game with textures applied and enjoy the result!

If anything doesn't appear correctly, you can always go back to Blender to adjust materials or textures and repeat the export process.
