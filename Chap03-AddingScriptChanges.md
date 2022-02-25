# Thinking about the changes

First, you need to think what is required. So, a button input is required, maybe Left Shift key (a common key input used in games) and then some changes to trigger when this button is input from keyboard.

Secondly, a coroutine is required that triggers the dash based on a specific cooldown period.

So, let's initialize some variables that would be required as shown:

![Initialize](https://user-images.githubusercontent.com/44625252/155745970-307b31ce-aff1-4141-b24d-84ee6785831f.png)

The canDash variable will be useful to define when the player can actually dash and the isDashing variable can be helpful to state the situation when the player in already dashing, hence, if the player inputs the key once again, the dash shouldn't happen again.

The IEnumerator is used to create a delayed effect, combined with a coroutine. Remember to import the required library which contains the implementation for IEnumerator ("using System.Collections;") otherwise you will get an error.

![ImportCollections](https://user-images.githubusercontent.com/44625252/155746280-335f9e8b-74f6-4751-8653-d7bd18e7845d.png)

Next, you can define the if() condition in the Update() function since this handles player input.

An example of this addition in script in shown below:

![GetKeyShift](https://user-images.githubusercontent.com/44625252/155745724-af07b87e-3dec-4290-8e5f-3c18e290ec51.png)

We haven't yet implemented the function Dash() yet. So, let's do that next. 

![Ienumeratordash](https://user-images.githubusercontent.com/44625252/155749096-a7b13dec-1eb6-4178-8498-f011d911032d.png)

You can use the 2 variables 'dashDuration' and 'dashCooldown' as fields that can be set to defines the duration of the dash and the cooldown period respectively after which the next Dash is possible.

The WaitForSeconds() function is used to set a delay time in seconds.

Finally, we can add the physics related calculations in fixedUpdate() function which handles physics related functions in Monobehaviour.

![DashPhysics](https://user-images.githubusercontent.com/44625252/155748741-b98f4e4e-ae35-42f4-b3fd-a48144d40a64.png)

Remember to use the Player's Rigidbody to add the required Impulse force. And also that the direction variable needs to be changed to -1 or 1 depending on which direction the player is moving.

![DirectionChange](https://user-images.githubusercontent.com/44625252/155750127-cd4e0dac-eef4-430b-bca9-cfe34a8527c6.png)

And that's it.

What do you see now when you play the game and hit the Left Shift key as input?

![](https://media.giphy.com/media/goecxQfvcY8LMVBKaJ/giphy.gif)

Amazing! isn't that cool?
