# Tank Turret Rotation

## Getting a Lockon

You may have noticed at the end of the last section that the turret was not moving. In this section we will fix that by having the turret rotate to face wherever the mouse is pointing in the level.

Head back to the EventGraph of BP_FirstPersonCharacter, this is where we left off after wiring up the tracks.

![](<../images/Tank_Turret_Rotation%20(1).png>)

Right click in an empty area of the graph and add an Event Tick node, this will run every single frame, which is exactly what we need for the turret to smoothly track the cursor.

![](<../images/Tank_Turret_Rotation%20(2).png>)

Drag off the Event Tick's execution pin and add a Set Relative Rotation node, setting the Target to the Turret component. We will fill in the New Rotation shortly.

![](<../images/Tank_Turret_Rotation%20(3).png>)

Next we need to work out where the mouse is pointing in the world. Add a Get Player Controller node.

![](<../images/Tank_Turret_Rotation%20(4).png>)

From the Player Controller's Return Value, drag out and add a Get Hit Result Under Cursor by Channel node, setting the Trace Channel to Visibility and ticking Trace Complex. This fires a trace from the camera, through the mouse cursor, and into the world, returning everything about whatever it hits.

!!! Note
    A trace (sometimes called a raycast) is an invisible line Unreal fires through the world to see what it hits, this is the same technique used for things like bullet hit detection. The Trace Channel decides what kinds of objects it's allowed to hit, Visibility covers most solid level geometry, which is what we want the cursor to be able to point at. Trace Complex makes it test against the actual mesh shape rather than a simplified collision shape, giving a more accurate hit location at the cost of being a little more expensive to calculate.

![](<../images/Tank_Turret_Rotation%20(5).png>)

Drag off the Hit Result pin and add a Break Hit Result node, this splits the hit result out into its individual parts, we only care about the Location, the point in the world the trace hit.

![](<../images/Tank_Turret_Rotation%20(7).png>)

Drag off the Location pin to start wiring it up to the turret's rotation.

![](<../images/Tank_Turret_Rotation%20(8).png>)

Add a Get Actor Location node, leaving the Target as self, to get the tank's own position. Feed this and the Break Hit Result's Location into a Find Look at Rotation node, with Start as the tank's position and Target as the point the cursor hit. This returns the rotation needed to look from the tank towards that location.

![](<../images/Tank_Turret_Rotation%20(9).png>)

We don't want the turret tilting up, down, or rolling about, just spinning on the spot to face the cursor, so right click on the New Rotation pin of the Set Relative Rotation node and choose Split Struct Pin. This breaks it out into its Roll, Pitch, and Yaw components individually.

![](<../images/Tank_Turret_Rotation%20(10).png>)

Do the same to the Find Look at Rotation's Return Value, splitting it into Roll, Pitch, and Yaw as well.

![](<../images/Tank_Turret_Rotation%20(11).png>)

Connect the Return Value Z (Yaw) over to the New Rotation Z (Yaw), leaving Roll and Pitch on the Set Relative Rotation node at their default of `0.0`. This way only the turret's yaw is affected, keeping it sitting flat on top of the hull no matter where the cursor is pointing.

![](<../images/Tank_Turret_Rotation%20(12).png>)

Compile, save, and hop back into the viewport to give it a try, the turret should now smoothly rotate to face your cursor wherever it points in the level!

Congratulations! You have successfully rotated the tank turret, that wraps up Jumping Into Unreal for this week.
