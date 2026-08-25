# Exporting To UE5

With the tank and shell modeled, unwrapped, and textured, it's time to get them out of Blender and ready to bring into Unreal.

Ensure the tank and shell are oriented towards the positive X direction.

![](<../images/Exporting_To_UE5%20(1).png>)

Select all assets including the shell by pressing ++a++ and rotating on the Z axis to whichever way faces positive X.

![](<../images/Exporting_To_UE5%20(2).png>)

![](<../images/Exporting_To_UE5%20(3).png>)

!!! Note
    Unreal's forward direction is +X. Orienting the model this way in Blender means it will already be facing the right way once imported, saving you from having to rotate it again inside Unreal.

Navigate to File > Export > FBX

![](<../images/Exporting_To_UE5%20(4).png>)

In the blender FBX export window;

Check the Limit to Selected Objects box:

![](<../images/Exporting_To_UE5%20(5).png>)

!!! Note
    This tells Blender to only export the objects you currently have selected, rather than everything in the scene. Handy for keeping cameras, lights, or other scratch objects you may have out of the file.

Scroll down to find the geometry section, set smoothing to Face.

![](<../images/Exporting_To_UE5%20(6).png>)

!!! Note
    This preserves the faceted, low poly shading we set up with all those bevels earlier. Leaving this on the default can cause Unreal to smooth the shading across the whole mesh, softening away the angular look we modeled.

Finally click export to get the assets you have created out of blender.

![](<../images/Exporting_To_UE5%20(7).png>)

Congratulations! Your tank and shell are ready to bring into Unreal.