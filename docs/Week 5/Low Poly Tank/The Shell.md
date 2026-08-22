# The Shell

Now that the tank itself is built, let's model something to go with it: a shell for the barrel to fire.

![](<../images/Shell%20(1).png>)

!!! Note
    If you are starting on this tutorial, you may need to jump to the Tank tutorial first for the colour palette and material setup.

## Modeling The Shell

Like the shield before it, the shell is modeled from a single shape using just a couple of tools.

Add a Cylinder (++"add"++ > Mesh > Cylinder). In the popup window on the bottom left, set Vertices to `8`, Radius to `0.2m`, Depth to `0.5m`, and set Rotation X to `90°` so it lies on its side like a shell casing.

![](<../images/Shell_Modeling%20(2).png>)

Enter edit mode with ++tab++ and switch to edge select (++2++). Using **Loop Select**, select the edge loop at the base of the shell (setting Delimit to **Outer Corners** in the popup window).

![](<../images/Shell_Modeling%20(3).png>)

Bevel this loop (++ctrl++ + ++b++) with a small Width of `0.05m` to soften the rear edge of the casing.

![](<../images/Shell_Modeling%20(4).png>)

Now select the edge loop at the opposite end, this will become the pointed nose of the shell.

Bevel this loop too, but this time set the Width Type to **Percent** in the popup window, with a Width Percent of `75%` and `3` Segments. This rounds the tip off into a smooth, bullet-like nose instead of a flat end.

![](<../images/Shell_Modeling%20(5).png>)

Back in object mode, double-click the object in the outliner and rename it "Shell".

Congratulations! You have successfully modeled the shell!

## Unwrapping The Shell

Switch to the "UV Editing" workspace in the top ribbon.

Select all faces with ++a++. Because the shell is a single simple shape, we don't need to mark any seams by hand this time - open the UV menu and choose **Smart UV Project** instead, leaving the default settings as they are.

![](<../images/Shell_UV%20(5).png>)

Blender automatically works out sensible seams for you based on the shape of the mesh, laying the faces of the shell out into a neat, non-overlapping set of islands.

![](<../images/Shell_UV%20(6).png>)

Congratulations! You have unwrapped the shell!

## Texturing the Shell

As we already set up the material on the tank, we will reuse the same material for the shell. Head to the Material Properties tab, click the browse icon next to the material name box, and select the material you created for the tank.

![](<../images/Shell_UV%20(2).png>)

The whole shell will now be shaded with the colour palette, though it'll look jumbled since every face is currently bunched up in the same spot on the UV layout.

Jump into the UV Editing workspace. Just like with the tank, select each shell in the layout and drag it onto the colour square you want that part of the model to be.

Let's start with the main body. Select the shells that make up the sides of the casing and move them (++g++) onto the green square, scaling down with ++s++ if you'd like more of the gradient to show.

![](<../images/Shell_Texturing%20(1).png>)

Select the shell for the pointed nose and move it onto one of the grey squares instead, giving the tip a metallic look.

![](<../images/Shell_Texturing%20(2).png>)

Finally, select the small shells for the rear rim of the casing and move them onto the gold square, matching the detailing on the tank's barrel.

![](<../images/Shell_Texturing%20(5).png>)

Once every shell has a colour, jump back to object mode to see your finished shell!

![](<../images/Shell_Texturing%20(6).png>)

Congratulations! You have successfully textured the shell!
