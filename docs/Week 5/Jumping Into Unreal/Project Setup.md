# Project Setup

In this section we will go through setting up your project to get ready to create the game!

## Creating the project

With Unreal open you will be faced with the landing page. Navigate to New Project.

From here we will use the First Person Project, solely because the core Blueprints are already set up and player movement is just what we need.
Name the Project appropriately, "TankGame" will do just nicely. But I called mine TankTute in this instance.

![New Project Window](<../images/Project_Setup%20(1).png>)

## Level the playing field

With the project open, you will notice the platforms in the middle, delete them, we don't need them.

![First look at the project](<../images/Project_Setup%20(2).png>)

Start with selecting it all.

![Middle Platform Selected](<../images/Project_Setup%20(3).png>)

And delete it!

![Middle Platform Deleted](<../images/Project_Setup%20(4).png>)

Now the Level is set.

## Importing Assets

### Folder creation

Open the content drawer with ++ctrl++ + ++space++

While in the content folder, click the add button and then New Folder

![Content drawer open](<../images/Project_Setup%20(9).png>)

Name the new folder "Assets"

![Create folder](<../images/Project_Setup%20(10).png>)

### Importing the Assets

Opening the newly created folder, we will now click the "Import" Button.

![Assets Folder Created and Named](<../images/Project_Setup%20(11).png>)

Navigate to where you had filed the FBX files of the Tank and shell files and click open.

The window that opens is where we can change certain aspects of the objects when importing them.

![Import Highlighted](<../images/Project_Setup%20(12).png>)

In this instance we will be changing nothing as we have already fixed some of the problem areas on export from Blender.

Now you will notice the Tracks, Turret, and Shell have all been imported along with the materials and Textures.

![Asset Import Screen](<../images/Project_Setup%20(13).png>)

### Material Setup

For this step you will need another texture.

[Download the blue tank colour palette here (PNG)](../textures/Tanks_CP_Blue.png){download="Tanks_CP_Blue.png"}

![](../textures/Tanks_CP_Blue.png)

First item of importance, is renaming the material to something more appropriate. M_TankMaterial will do just nicely

![Material Renamed](<../images/Project_Setup%20(14).png>)

M_TankMaterial will serve as the parent material for all instances of the Material.

!!! Note
    A Material Instance lets you reuse a material's setup while swapping out individual parameters, like a texture, without duplicating the whole material. This is why we're making two instances here, one for each team colour, rather than two separate materials.

To set up a Material instance, right click on the material you wish to create the instance from and second from the top you will see "Create Material Instance"

![](<../images/Project_Setup%20(15).png>)

Here you will create 2 material instances, The first called MI_Tank_Green and then MI_Tank_Blue.

![](<../images/Project_Setup%20(16).png>)

Click and drag the blue colour palette into the content drawer if you have not already.

![](<../images/Project_Setup%20(17).png>)

Open MI_Tank_Blue. In the details panel on the right, navigate to "DiffuseColorMap" and tick the box, then in the drop down box select the blue colour palette.

![](<../images/Project_Setup%20(18).png>)

## Getting a good view

We need to allow the player to have a good view of the playing feild. we can allow this by adding a camera actor from the place actor panel on the left side of the editor.

![](<../images/Project_Setup%20(19).png>)

Drag the camera into the scene and set its transforms to the following values:

Location: X=-1100, Y=0, Z=3500.

Rotation: X=0, Y=-75, Z=0.

Scale: X=1, Y=1, Z=1.

![](<../images/Project_Setup%20(20).png>)

Lastly we need to tell the engine that the player needs to see out of this camera we set this in the details pannel all the way down in the Auto Player Activationm section, setting it to "Player 0"

![](<../images/Project_Setup%20(21).png>)

Now the project is setup and ready to go