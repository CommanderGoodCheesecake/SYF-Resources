# Project Setup

In this section we will go through seting up your project to get ready to create the game!

## Creating the project

With unreal Open you will be faced with the landing page. navigate to new project.

From here we will use the First Person Project, soley because the core Blueprints are already setup and player movement is just what we need.
Name the Project approriatly, "TankGame" will do just nicely. But I called mine TankTute in this instance.

![New Project Window](<../images/Project_Setup%20(1).png)

## Level the playing feild

With the project open, you will notice the platforms in the middle, delete it, we dont need it.

![First look at the project](<../images/Project_Setup%20(2).png)

Start with selecting it all.

![Middel Platform Selected](<../images/Project_Setup%20(3).png)

And delete it!

![Middel Platform Deleted](<../images/Project_Setup%20(4).png)

Now the Level is set.

## Importing Assets

### Folder creation

Open the content draw with ++ctrl++ + ++space++

![Content draw open](<../images/Project_Setup%20(5).png)

While in the content folder, click the add button and then Ne Folder

![Create folder](<../images/Project_Setup%20(6).png)

Name the new folder "Assets"

![Assets Folder Created and Named](<../images/Project_Setup%20(7).png)

### Importing the Assets

Opening the newly created the folder, we will now click the "Import" Button.

![Import Highlighted](<../images/Project_Setup%20(8).png)

Navigate to where you had filed the FBX files of the Tank and shell files and click open.

The window that opens is where we can change certain aspects of the objects when importing them.

Inm this instance we will be changing nothing as we have already fixed some of the problem areas on export from Blender.

![Asset Import Screen](<../images/Project_Setup%20(9).png)

Click import and you will notice the Tracks, Turret, and Shell have all been imported along with the materials and Textures.

![Content Draw with Imported Assets](<../images/Project_Setup%20(10).png)

### Material Setup

First item of importance, is renaming the material to something more appropriate. M_TankMaterial will do just nicely

![Material Renamed](<../images/Project_Setup%20(11).png)

M_TankMaterial will serve as the parent material for all instance of the Material.

To setup Material instance, right click on the material you wish to create the instnace from and second from the top you will see "Create Material Instance"

![](<../images/Project_Setup%20(12).png)

Here you will 

![](<../images/Project_Setup%20(13).png)



![](<../images/Project_Setup%20(14).png)



![](<../images/Project_Setup%20(15).png)



![](<../images/Project_Setup%20(16).png)



![](<../images/Project_Setup%20(17).png)
