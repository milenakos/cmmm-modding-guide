---
sidebar_position: 6
title: Adding sound effects
description: Programmer... effects?
---

# Adding your own sound effect to the game folders

Before you do anything in the Unity editor, you'll first need to add the sound effect into the game. So, in File Explorer, open the `Assets` folder.
Then, double click the `Assets` folder (yes, I know, weird) and open the `Music` folder. Here, you will put all your sound effects.

### Adding the sound effect into the game

First, open your project in Unity. If you don't have a project, please visit [Introduction](../intro).

In the file explorer at the bottom, you will want to go to the same directory that contains your sound effects. Then, copy one of the existing prefabs
and rename the prefab to whatever you want. Then, drag your sound effect file into the AudioClip tab.

Now, go into the file explorer and open the `Scripts` folder. Next, open the `Audio` folder, and open up the `Game Assets` script. Here,
scroll down and write: 
```cs
public AudioClip audioClipName;
```
where `audioClipName` is the name you want to give to the AudioClip.

After that, go to the `Scenes` folder. Here, double-click the `MainMenu` scene. Then, open the `GameAssets` object. Expand the `Game Assets`
script if it is collapsed, and drag the sound effect file into the newly created tab.

### Playing the sound effect in code

If you want to play the sound effect in code, it's very simple. All you have to do, is add this line of code:
```cs
AudioManager.i.PlaySound(GameAssets.i.audioClipName);
```
where `audioClipName` is the name you gave to the AudioClip.
