# Adding New Scene

First, we can add a new scene separately for this project.

You can create a new scene from the File Menu, File->New Scene and copy all assets.

If you need same components as a scene, another shortcut is to copy a scene using CTRL+D, selecting the current scene with mouse.

![Copy_Scene](https://user-images.githubusercontent.com/44625252/155743160-49e70d0a-5206-45cc-b1e1-d74cda0c0b31.png)

# Sorting the Camera and Player position

Next, you would have noticed that when you play the game, the player is a bit offset from the center of Camera view and hence, when you change direction of player, the position shifts a bit everytime.

The easiest way to do this is to remove the camera from the child hierarchy of Player first, then changing the transform position of player to be exactly aligned with the camera position.

![Camera_center](https://user-images.githubusercontent.com/44625252/155743589-230d4545-c13b-4312-a863-cf6bc166035f.png)

Now that, that is sorted we can move ahead with adding scripts in the Player Movement script to implement the new feature.

![](https://media.giphy.com/media/j6PdsN0ssvKOe39dDM/giphy.gif)
