# Tank Movement

## Gutting the player character

To begin I will let you in on what we are about to do.

We will be turning the existing player character into the tank character through a few easy steps.

The main reason we are using the first person player character and not building it from scratch is user input is already set up and perfect for what we need.

That being said, navigate to the BP_FirstPersonCharacter in Content > FirstPerson > Blueprints.

![](<../images/Tank_Movement%20(1).png>)

### Frontend

I will begin with the viewport, you will notice the mannequin character is exactly where we don't need it.

![](<../images/Tank_Movement%20(3).png>)

Start by selecting first person mesh components and the camera component.

and delete them.

![](<../images/Tank_Movement%20(4).png>)

There is still a mannequin mesh in the scene, as this is a default component, it can not be deleted, rather we will go over to the details panel and remove the skeletal mesh reference from the slot.

![](<../images/Tank_Movement%20(6).png>)

Next add 2 new static mesh components and name them, tracks and turret.

![](<../images/Tank_Movement%20(10).png>)

We also need to keep track of where the shell will spawn when fired.

We will do this by adding a scene component.

!!! Note
    A Scene Component has no mesh and is invisible in game, it's just a position and rotation in space. It's useful anywhere you need a reference point to attach to or spawn things from, like the tip of the barrel here, without adding any visible geometry of its own.

We will later move this when we know where the muzzle of the turret will be.

![](<../images/Tank_Movement%20(11).png>)

Name the Component "ShellSpawnLocation"

![](<../images/Tank_Movement%20(12).png>)

For both the tracks and turret, in the details panel navigate down to the static mesh section and set the appropriate meshes.

![](<../images/Tank_Movement%20(13).png>)

Now select the Capsule, this acts as the player collision and can not be deleted.

Set the Capsule Radius to 70 and the half height to 70, it will not allow you to do it the other way around.

!!! Note
    A capsule is a cylinder with a rounded cap on each end, and those caps are shaped by the Radius. Because of this, the Half Height can never be smaller than the Radius, if it were, the rounded caps would overlap and the shape wouldn't make sense. That's why Unreal makes you set the Radius first.

![](<../images/Tank_Movement%20(15).png>)

To ensure the tank is not hovering off the ground when moving, we need to drop the tracks and turret by 30 units, like so:

![](<../images/Tank_Movement%20(16).png>)

### Backend

Jumping over to the event graph, we will start with selecting the code we do not need.

This includes the camera aim and jump functionality.

![](<../images/Tank_Movement%20(17).png>)

Delete said nodes leaving only the movement logic, this is what we came for.

![](<../images/Tank_Movement%20(18).png>)

Double clicking on the Move Node will open another graph, this is the Move function where the movement input logic is held.

![](<../images/Tank_Movement%20(19).png>)

Leaving the existing code. Drag from the last node and search for "Set world rotation tracks"

![](<../images/Tank_Movement%20(20).png>)

You will then get a set world rotation node with the tracks static mesh reference already attached.

Calculating the rotation for the tracks is trivial, we simply need to rotate it in the direction we are traveling. Unreal keeps track of travel direction through a vector called Velocity. Simply get the velocity and convert it into a rotator to set the tracks rotation.

!!! Note
    A Rotator is how Unreal represents an orientation, as Roll, Pitch, and Yaw angles. Velocity on the other hand is a vector, a direction and speed in 3D space, it doesn't have a rotation. Converting a vector to a rotator works out the rotation needed to point in that vector's direction, which is exactly what we want here.

![](<../images/Tank_Movement%20(22).png>)

If everything worked out, you will now be able to drive the tank around the level!

![](<../images/Tank_Movement%20(21).png>)

You may have noticed that the turret is not moving... Let's fix that in the next section!
