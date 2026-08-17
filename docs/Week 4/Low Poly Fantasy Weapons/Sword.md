# The Sword

Welcome to to the next tutorial in the lowpoly fantasy weapon series!

In this section we will be going over how to make the Sword, using very simple techniques.

![Weapons hero card](../images/LP_Fantasy_Weapons/WeaponsHeroCard.png)

!!! Note
    If you are starting on this tutorial, you may need to jump to the Hammer tutorial for material setup.

## Modeling The Sword

Now that you've got a hammer under your belt, let's build something a little more advanced: a sword!

This one has three parts instead of two, and we'll pick up a couple of new tricks along the way (like a modifier that mirrors your work for you, so you only have to shape half of something).

To block it out, we'll use 3 basic shapes:

* Cube (the blade)
* Cube (the crossguard)
* Cylinder (the handle)

### The Blade

Add a new cube to the scene the same way you did for the hammer's head (++"add"++ > Mesh > Cube).

![](<../images/LP_Fantasy_Weapons/LP_Weapons%20(55).png>)

We need to turn this cube into a long, thin blade shape. Enter edit mode with ++tab++ and select all with ++a++.

Rather than scaling every axis at once, we'll do it one axis at a time so we have full control over the shape. Press ++s++, then ++x++ to lock to the X-axis, and type `0.25` before pressing enter. Do the same again for ++y++, scaling it to `0.5`. Finally, scale ++z++ up to `3`, which stretches the cube into a long blade.

![](<../images/LP_Fantasy_Weapons/LP_Weapons%20(59).png>)

Jump back to object mode with ++tab++, then press ++g++ and ++z++ to move the blade upwards, typing `4` to move it exactly 4 metres up. This leaves room underneath for the crossguard and handle.

![](<../images/LP_Fantasy_Weapons/LP_Weapons%20(61).png>)

Now let's add the crossguard. Add another cube (++"add"++ > Mesh > Cube) - this one will stay in object mode while we shape it.

![](<../images/LP_Fantasy_Weapons/LP_Weapons%20(62).png>)

With the new cube selected, scale it on each axis individually just like before: ++s++ ++x++ `0.5`, ++s++ ++y++ `2`, ++s++ ++z++ `0.2`. This flattens it into a long, thin bar.

![](<../images/LP_Fantasy_Weapons/LP_Weapons%20(63).png>)

!!! Note
    You'll notice a small warning appear at the bottom left of the viewport saying "Active object has non-uniform scale". This just means the object's scale values aren't equal on every axis anymore. It's nothing to worry about for now, but we'll need to deal with it later before we bevel this object.

Move the crossguard up with ++g++ ++z++ `0.8` so it sits just below the blade.

![](<../images/LP_Fantasy_Weapons/LP_Weapons%20(64).png>)

Last of our 3 shapes: add a Cylinder (++"add"++ > Mesh > Cylinder). In the operator panel at the bottom left, set Vertices to `8` and Radius to `0.5m`.

![](<../images/LP_Fantasy_Weapons/LP_Weapons%20(65).png>)

While that panel is still open you can also change the Depth - set it down to `3m` to make a shorter handle.

![](<../images/LP_Fantasy_Weapons/LP_Weapons%20(66).png>)

Move the cylinder down with ++g++ ++z++ `-0.9` so it sits below the crossguard, forming the handle.

![](<../images/LP_Fantasy_Weapons/LP_Weapons%20(67).png>)

You should now have a rough blockout of all 3 parts of the sword.

![](<../images/LP_Fantasy_Weapons/LP_Weapons%20(68).png>)

Select the blade cube and enter edit mode with ++tab++. We're going to use the loop cut tool to add some geometry we can shape.

With the loop cut tool active, hover over the blade so a single yellow line appears running down its length, and click to add **1** cut down the centre.

![](<../images/LP_Fantasy_Weapons/LP_Weapons%20(71).png>)

Use the loop cut tool again, but this time hover so the yellow lines run across the blade, and in the popup window on the bottom left set the number of cuts to **5**. This splits the blade into 6 segments we can taper individually.

![](<../images/LP_Fantasy_Weapons/LP_Weapons%20(72).png>)

Now for the fun part - shaping the blade's silhouette. Switch to edge select (++2++), then select one of the horizontal loops using Alt-click (this selects the whole ring in one go).

![](<../images/LP_Fantasy_Weapons/LP_Weapons%20(75).png>)

Press ++s++, then ++y++ to lock the scale to the Y-axis, and type in a value to narrow or widen that section of the blade. Do this for each ring, working your way toward the tip and using smaller and smaller values (try something like `0.75`, then `0.25` for another ring further along, and `0.8` for one nearer the guard) until you get a shape you're happy with.

![](<../images/LP_Fantasy_Weapons/LP_Weapons%20(76).png>)

Keep adjusting the rings until the blade tapers nicely from a wide base to a narrow tip, like this:

![](<../images/LP_Fantasy_Weapons/LP_Weapons%20(79).png>)

To finish the tip, we need to pinch it into a point. Switch to a front orthographic view by pressing ++1++ on your numpad, then select both of the blade's side edges - click one, then hold ++ctrl++ and click the other to select the shortest path between them.

![](<../images/LP_Fantasy_Weapons/LP_Weapons%20(85).png>)

With both edges selected, press ++s++ then ++x++ and type `0.2` to squeeze them together into a sharp point.

![](<../images/LP_Fantasy_Weapons/LP_Weapons%20(88).png>)

You can nudge the tip with ++g++ ++z++ afterwards if it needs fine-tuning. Back in object mode, you should have a nicely tapered, pointed blade.

![](<../images/LP_Fantasy_Weapons/LP_Weapons%20(91).png>)

### The Crossguard

Select the crossguard and enter edit mode. Before we shape it, we're going to add a **Mirror Modifier**.

!!! Note
    A modifier is a tool that changes how an object looks without permanently editing its mesh. The **Mirror Modifier** takes whatever you build on one side of an object and automatically copies it to the other side. Since the crossguard needs to be symmetrical, this means we only have to shape one wing, and Blender takes care of the other one for us.

Head to the Modifier Properties tab (the wrench icon) in the panel on the right, click **Add Modifier**, and search for **Mirror**. Make sure the **Y** axis is enabled, since that's the direction our crossguard extends in.

![](<../images/LP_Fantasy_Weapons/LP_Weapons%20(101).png>)

Just like the blade, add a loop cut with **1** cut running down the length of one wing, then another loop cut with **5** cuts running across it to create segments.

![](<../images/LP_Fantasy_Weapons/LP_Weapons%20(103).png>)

Select each horizontal ring in turn and taper the wing to a point, the same way you shaped the blade - moving and scaling along the X-axis this time, since the guard runs along Y. Try values like `0.6`, `0.5`, and `0.65` for different rings.

!!! Note
    Look for the **Mirror Editing** checkbox in the operator panel at the bottom left after each move or scale. With it ticked, your edits are applied to both wings at once, so you don't have to repeat every step twice.

![](<../images/LP_Fantasy_Weapons/LP_Weapons%20(111).png>)

Keep going until both wings taper symmetrically to a point.

![](<../images/LP_Fantasy_Weapons/LP_Weapons%20(115).png>)

Before we bevel the tips, we need to deal with that non-uniform scale warning from earlier. Back in object mode, go to **Object > Apply > Scale** to bake the scale values into the mesh.

![](<../images/LP_Fantasy_Weapons/LP_Weapons%20(116).png>)

Now enter edit mode again, select the edges around each wing tip, and press ++ctrl++ + ++b++ to bevel them. Set the Width to `0.1m` in the popup window to soften the points slightly.

![](<../images/LP_Fantasy_Weapons/LP_Weapons%20(117).png>)

Back in object mode, apply the Mirror Modifier the same way you applied the scale - this bakes the mirrored half into the real mesh permanently. You should now have a complete, symmetrical crossguard sitting nicely with the blade.

![](<../images/LP_Fantasy_Weapons/LP_Weapons%20(118).png>)

### The Handle

Select the cylinder and enter edit mode. Select the bottom edge loop (Alt-click one of the bottom edges) and move it down slightly with ++g++ ++z++ `-0.25` to leave room for a pommel at the end.

![](<../images/LP_Fantasy_Weapons/LP_Weapons%20(121).png>)

Select the loops running down the grip and scale them in on both X and Y together (++s++ then type a value, without locking to an axis) to shape a comfortable-looking grip. Try tapering it in stages - `0.75`, `0.8`, `0.85` - so it isn't perfectly straight.

![](<../images/LP_Fantasy_Weapons/LP_Weapons%20(125).png>)

Finally, select the bottom-most edge loop and bevel it (++ctrl++ + ++b++) with a Width of around `0.2m` to round off the pommel.

![](<../images/LP_Fantasy_Weapons/LP_Weapons%20(127).png>)

Back in object mode, all three parts of the sword should now be individually modeled and sitting in place.

![](<../images/LP_Fantasy_Weapons/LP_Weapons%20(128).png>)

### Joining It All Together

Select all three objects - click the blade, then ++shift++ click the crossguard and the handle - making sure the handle is selected last so it becomes the active object.

![](<../images/LP_Fantasy_Weapons/LP_Weapons%20(133).png>)

Press ++ctrl++ + ++j++ to join them into a single object.

![](<../images/LP_Fantasy_Weapons/LP_Weapons%20(134).png>)

Double-click the object in the outliner and rename it to "Sword".

Enter edit mode and take a look at where the parts overlap - you'll notice extra faces and edges left over from when the shapes intersected. Select any unnecessary edges running through these areas and use **Mesh > Delete > Dissolve Edges** to clean them up.

![](<../images/LP_Fantasy_Weapons/LP_Weapons%20(140).png>)

You'll also find some overlapping faces sitting inside the mesh, where the blade meets the guard, and where the guard meets the handle. Select these and delete just the **Faces** (++x++ > Faces), leaving a hole with bare edges around it.

![](<../images/LP_Fantasy_Weapons/LP_Weapons%20(142).png>)

!!! Note
    Holding ++z++ and hovering over "Wireframe" lets you see straight through the mesh, just like we did for the hammer. This makes it much easier to select the hidden faces and edges sitting inside the model.

Working around each hole, select a group of 3 or 4 edges at a time and press ++f++ to fill in a new face, continuing all the way around until the gap is completely closed up.

![](<../images/LP_Fantasy_Weapons/LP_Weapons%20(152).png>)

Repeat this for the second junction between the crossguard and the handle.

![](<../images/LP_Fantasy_Weapons/LP_Weapons%20(156).png>)

Once both junctions are fully filled in and there are no gaps left in the mesh, jump back to object mode and take a look at your finished sword!

![](<../images/LP_Fantasy_Weapons/LP_Weapons%20(168).png>)

Congratulations! You have successfully modeled the sword!

## Unwrapping The Sword

Switch over to the "UV Editing" workspace in the top ribbon, just like we did for the hammer.

![](<../images/LP_Fantasy_Weapons/LP_Weapons%20(304).png>)

Enter edit mode and select all the faces with ++a++. If you look at the UV layout on the left, you'll see it's a messy jumble of overlapping shapes - that's just Blender's default unwrap, and it's not something we can texture properly yet.

![](<../images/LP_Fantasy_Weapons/LP_Weapons%20(305).png>)

Rather than manually marking a seam around every single section like we did for the hammer, we only need a couple this time. Select the edge loop where the handle meets the crossguard, and mark it as a seam by right clicking and choosing **Mark Seam** in the popup window.

![](<../images/LP_Fantasy_Weapons/LP_Weapons%20(309).png>)

![](<../images/LP_Fantasy_Weapons/LP_Weapons%20(310).png>)

Do the same thing again for the edge loop near the bottom of the handle, just above the pommel. You should end up with two red seam rings running around the handle.

![](<../images/LP_Fantasy_Weapons/LP_Weapons%20(311).png>)

Now select all the faces again with ++a++, open the UV menu at the top of the viewport, and choose **Smart UV Project**.

![](<../images/LP_Fantasy_Weapons/LP_Weapons%20(312).png>)

A popup window will appear - the default settings are fine, so you don't need to change anything.

Take a look at the UV layout now. Instead of the messy jumble from before, you should have a set of neat, separate islands for the blade, crossguard, handle, and pommel.

![](<../images/LP_Fantasy_Weapons/LP_Weapons%20(313).png>)

!!! Note
    Smart UV Project automatically figures out sensible seams for you based on the shape of the mesh, using the seams you've already marked as a starting point. It won't always give perfect results on more complicated models, but it's a great time-saver for something like this.

Congratulations! You have unwrapped the sword!

## Texturing the Sword

As we have already set up the material in the Hammer tutorial, we will use the same Material for the sword.

Head to the Material Properties tab (the sphere icon) in the panel on the right. Instead of clicking **New**, click the little browse icon next to the material name box and select the **Material** you already created for the hammer from the list.

![](<../images/LP_Fantasy_Weapons/LP_Weapons%20(314).png>)

!!! Note
    Because this Material already has the colour palette image plugged into its Base Color, linking it here does all the same setup work we did manually back in the Shading workspace for the hammer - just in one click. Any object that uses this Material will pull its colours from the same palette image.

The whole sword will now be textured with the colour palette, though it'll look like a jumbled mess for now since every face is bunched up in the same spot on the UV layout.

![](<../images/LP_Fantasy_Weapons/LP_Weapons%20(316).png>)

Jump back into the UV Editing workspace. Just like with the hammer, select each shell in the UV layout and drag it onto the colour square you want that part of the sword to be.

Let's start with the crossguard. Select its shell and move it (++g++) onto one of the gold squares.

![](<../images/LP_Fantasy_Weapons/LP_Weapons%20(321).png>)

Do the same for the handle's grip, moving its shell onto a red square instead.

![](<../images/LP_Fantasy_Weapons/LP_Weapons%20(326).png>)

You can scale shells down first with ++s++ if you want more of the square's colour gradient to show, then move them into place with ++g++.

![](<../images/LP_Fantasy_Weapons/LP_Weapons%20(327).png>)

Repeat this for the remaining shells - the blade looks great on one of the grey squares, and the pommel can share the same gold square as the crossguard.

Once every shell has been moved onto a colour you're happy with, jump back to object mode to see the finished result.

![](<../images/LP_Fantasy_Weapons/LP_Weapons%20(329).png>)

Congratulations! You have successfully textured the sword!