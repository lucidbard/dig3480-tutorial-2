# Tutorial 2: Ruby's Adventure!

This repository is used for the 2D tutorial in DIG3480.

The steps are outlined both here as well as in the README.md file in the repository.

## Your Friend, `caam`

You will be using the script `caam` to submit assignments. Each time you checkout a repository for the first time, you will enter the "register" command. Then, when you wish to submit your work, you will use the "submit" command.

### Register

`./caam register`

This will configure your repository and enable you to submit. Do this first.

### Submit

`./caam submit`

### Results

`./caam results`

## Main Character and First Script

In this tutorial, you learn how to import assets and set up the main character.

## [Character Controller and Keyboard Input](https://learn.unity.com/tutorial/main-character-and-first-script?uv=2019.2)

### 1. Control Movement with Keyboard Input

This version of the tutorial will use the new Unity Input System.

You can find more information on why it is better than the previous and how it will be standard in Unity 2020.1 [here](https://blogs.unity3d.com/2019/10/14/introducing-the-new-input-system/).

---

Before we begin, review the blog post above and the [Quick Start Guide](https://docs.unity3d.com/Packages/com.unity.inputsystem@1.0/manual/QuickStartGuide.html?_ga=2.69693840.165808591.1594148458-1789172491.1588356245), as this time you'll be implementing the input mappings yourself.

You’ve created a script to move the Ruby GameObject. Now let’s adjust it so that movement is driven by pressing a key on the keyboard.

Let’s start by changing your code to make the character move horizontally.
Instead of adding 0.1 to the x coordinate every frame, like your code did in the previous tutorial, it should only add it if the player presses the right arrow key on their keyboard.

When the player presses the left arrow key, it should remove 0.1 so that the object moves to the left.

To do this, you’re going to use the Unity Input System, which is composed of Input Settings and input code (which Unity gives you to query the value of an axis for that frame).

### 2. View the Default Input Settings

Let’s start by looking at the default Input Settings, which define what kind of input your game uses:
Go to Edit > Project Settings, and select the Input page in the Settings window.

The Input page lists the Axes values for all the player input controls, such as a button on a gamepad. Values range from -1 to 1, depending on what the player is doing.
For a thumbstick on a gamepad, for example, the horizontal axis could be set to:
-1 when the stick is to the left
0 when it’s in the middle
1 when it’s to the right
For keyboard keys, the axis is defined by 2 keys:

A negative key that sets the axis to -1 when it’s pressed
A positive key that sets it to 1 when it’s pressed

If you look at the horizontal axis, you can see that left (for left arrow key) is on the negative button and right (right arrow) is on the positive button.
