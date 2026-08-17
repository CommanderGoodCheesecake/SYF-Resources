# The Staff

Welcome to to the next tutorial in the lowpoly fantasy weapon series!

In this section we will be going over how to make the Staff, using very simple techniques.

![Weapons hero card](../images/LP_Fantasy_Weapons/WeaponsHeroCard.png)

!!! Note
    If you are starting on this tutorial, you may need to jump to the Hammer tutorial for material setup.


## Modeling The Staff

Last but not least, the staff! This one is a tall shaft with a gem resting on top, and it gives us a chance to learn a really useful tool: **Proportional Editing**, which lets us shape things in a smooth, organic way instead of everything looking perfectly straight and mechanical.

Add a Cylinder (++"add"++ > Mesh > Cylinder) and set the Vertices to `8`, Radius to `0.5m`, and Depth to `10m` in the operator panel. This gives us a tall, thin shaft to work with.

![](<../images/LP_Fantasy_Weapons/LP_Weapons%20(203).png>)

Enter edit mode and add a loop cut with **12** cuts running along the length of the shaft, giving us plenty of geometry to shape.

![](<../images/LP_Fantasy_Weapons/LP_Weapons%20(204).png>)

Select the bottom-most edge loop. Before scaling it, press ++o++ to toggle on **Proportional Editing** - you'll see a circle appear around your selection.

!!! Note
    Proportional Editing spreads the effect of a move, scale, or rotation out to nearby geometry, with the effect fading the further away it gets. Scroll your mouse wheel to grow or shrink the circle, which controls how far the effect reaches. It's great for smooth, organic shapes like a wooden shaft, rather than sharp mechanical bends.

With Proportional Editing on, scale the bottom loop down so the shaft tapers smoothly to a point, rather than staying a flat cylinder width all the way down.

![](<../images/LP_Fantasy_Weapons/LP_Weapons%20(207).png>)

Select the very bottom edge loop and bevel it (++ctrl++ + ++b++) with a Width of `0.2m` and 2 Segments to round off the tip.

![](<../images/LP_Fantasy_Weapons/LP_Weapons%20(210).png>)

Now for the fun part - let's make the shaft feel like a gnarled wooden staff instead of a perfectly straight rod. With Proportional Editing still on, select a loop partway up the shaft and press ++g++ to move it slightly sideways, letting the falloff bend the nearby geometry with it. Repeat this at a few different heights along the shaft, nudging each one a small amount in a different direction.

![](<../images/LP_Fantasy_Weapons/LP_Weapons%20(213).png>)

!!! Note
    Don't overdo it - small, subtle movements at a few points along the length are enough to make the staff feel natural and hand-carved, without making it look broken or bent out of shape.

Back in object mode, you should have a gently curving, tapered shaft.

![](<../images/LP_Fantasy_Weapons/LP_Weapons%20(216).png>)

!!! Note
    Originally this tutorial carved a forked V-shaped notch into the top of the shaft to cradle the gem, using the Knife tool to cut it out. It ended up not looking great, so instead we're keeping things simple - the gem just sits on top of the shaft rather than being carved into it.

Add an Ico Sphere (++"add"++ > Mesh > Ico Sphere) with 1 Subdivision and a Radius of `0.5m` - this will be our gem.

Move the ico sphere up so it rests directly on top of the shaft's tip. It doesn't need to overlap or merge with the shaft at all - just sitting on top of it looks great.

Back in object mode, select both the shaft and the gem, and press ++ctrl++ + ++j++ to join them into one object. Double-click it in the outliner and rename it "Staff".

Congratulations! You have successfully modeled the staff!

## Unwrapping The Staff

Switch to the "UV Editing" workspace. Because the staff's geometry is quite simple - just loop cuts running down a cylinder - it doesn't need any manual seams at all this time.

![](<../images/LP_Fantasy_Weapons/LP_Weapons%20(369).png>)

Select all with ++a++, open the UV menu, and choose **Smart UV Project**.

![](<../images/LP_Fantasy_Weapons/LP_Weapons%20(370).png>)

!!! Note
    Sometimes a mesh is simple enough that Smart UV Project can produce a great result all on its own, without needing any seams marked beforehand. It's always worth trying this first before reaching for seams - you can always add them afterwards if the result doesn't look clean enough.

You should end up with a tidy set of vertical strips for the shaft, and a neat triangulated pattern for the gem.

![](<../images/LP_Fantasy_Weapons/LP_Weapons%20(371).png>)

Congratulations! You have unwrapped the staff!

## Texturing the Staff

As with the sword and shield, we'll reuse the same Material we set up for the hammer rather than starting from scratch.

Head to the Material Properties tab and link the existing **Material** to the staff, the same way you did for the other weapons.

![](<../images/LP_Fantasy_Weapons/LP_Weapons%20(373).png>)

Jump into the UV Editing workspace. Select the shaft's shells and move them onto one of the brown squares, giving the staff a warm, wooden look.

![](<../images/LP_Fantasy_Weapons/LP_Weapons%20(376).png>)

For the gem, let's try something a little different. Rather than giving the whole thing one flat colour, select just one of its triangular facets and move it onto a colour of your choice - try a purple or gold square. Then select another facet and move it onto a different colour.

![](<../images/LP_Fantasy_Weapons/LP_Weapons%20(379).png>)

!!! Note
    Because the gem is made up of lots of small triangular faces, colouring different facets differently makes it catch the light like a real, multi-faceted gemstone, rather than looking like a single flat-coloured ball.

Keep going until the gem has a couple of different colours across its facets, and the shaft is a solid wood tone.

![](<../images/LP_Fantasy_Weapons/LP_Weapons%20(383).png>)

Jump back to object mode to see your finished staff!

![](<../images/LP_Fantasy_Weapons/LP_Weapons%20(384).png>)

Congratulations! You have successfully textured the staff - and finished the whole Lowpoly Fantasy Weapons series!