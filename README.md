# Doom-Nukem-42
Based on advanced raycasting, recreate the first Wolfenstein/Doom experience in C using a Library 'just to display the pixels', everything needs to be running on a CPU. (in 1992 GPU were a dream)

## **Get Started**

Easy to compile and run!

Mac:
```
make && ./doom-nukem
```

Linux:
```
sudo make && ./doom-nukem
```



## **What I have done on this project ?**

***Map editor***
When I first arrived in the team, I was assigned to do the map editor. I tried to make it as practical to use as possible, despite my limited knowledge in UX/UI, and the fact that I had to do everything from scratch. The result isn't anything spectacular but I'm pretty happy with it.
This includes:
 - Map editing with basic features (line selection with shift, block selection with ctrl, map displacement with middle mouse button, eraser, ...).
 - Block placement with specific presets (Chose what features you want to add at a specific coordinate.
 - Block preset creation and editing for easier editing.
 - Prompts for preset names/map name

**Refactoring**
I arrived on this project about one month into it's creation where it only had a simple menu and the engine was pretty barebones (Raycasting with added features of looking up and down).
After making the editor engine, I first worked on refactoring the code for the menu which was too slow and greatly impeded our ability to test the engine, so I hastly improved it in order to have a solid base to work on and to start adding new functionalities.

**Engine**
I worked together with dlartigu mostly to help fix a few visual bugs with the engine at first, in order to get more comfortable with the codebase, then proceded to add many features:
- ***Floor/Roof***
  I worked on adding the floor/roofs together with dlartigu so they could work properly with the looking up/down mechanic.
- ***Skybox***
  Skybox with varying width/rotation speed, so we could work with multiple skyboxes to add a better distance effects. Though this wasn't implemented in the end and     only the simple skybox feature remained.

- ***Windows***
   Added see-through walls or partially see-through walls.

- ***Sprites***
  The sprite feature in it's entirety, using standard methods for showing sprites in a raycasting algorithm, just adapting them to the improved algorithm we had.
  This includes Items, Enemies and Transparent Walls
- ***Wall Sprites***
  Namely for the bullet impacts when shooting on different walls, done with a buffer of the last n shots.

- ***Sprites Actions/Pathfinding/Sounds***
  I learned how to use the fmod library in this project, and used it to add audio to monsters/music and the gunshots
  I created a very basic AI for the mobs so they patrolled back and forth, and went attacking the player if he was close enough.

- ***Management***
  I also worked on helping struggling group members in implementing many features like the HUD or visual effects like rain, and directing them altogether to work on 
  the different features we needed to add.

- ***Parsing***
  I also added many parsing features for configuration files when I had time to do so, to streamline the process of adding new sounds/textures per example
***Conclusion***
  This was a pretty hectic project in the middle of the covid crisis, and it lasted much longer than it should have (I started working on it middle august and it     ended late november, but I learned a lot during this time, from the libraries we used (SDL2/SDL2_TTF for graphics, fmod for audio), in programming itself, and in project planning/management. Whereas I arrived to support the project, I finally ended up managing most of the features, along with dlartigu, but during the end he mostly contributed to the artistic part of the project (textures, sound design, game design)
------

## **How to play ?**

It's relatively common, here are the main ones (you can see them in the setting menu)

| ACTION | KEY             |
| ------ | --------------- |
| Fire   | Mouse Left Clic |
| Reload | R               |
| Move   | WASD            |
| Jump   | Spacebar        |
| Crouch | Left CTRL       |

------

## **Wanna see some gameplay footage ?**

In the menu selection you can play the story or try to high score in arcade mode.
If you have a very powerful computer you can try to run the game in 1080p (or higher) with every setting maxed. You'll see a big texture difference!

- Low vs High texture quality + AA

  ![Low vs High](https://github.com/dlartigu/Doom-Nukem-42/blob/main/gif/lowvshigh.png)
  

- Main Menu

  ![Main Menu](https://github.com/dlartigu/Doom-Nukem-42/blob/main/gif/Menu.gif)

- Basics on level 1

  ![Basics](https://github.com/dlartigu/Doom-Nukem-42/blob/main/gif/level1/1.gif)
  ![Press F to fly](https://github.com/dlartigu/Doom-Nukem-42/blob/main/gif/level1/2.gif)

- It is forbidden to get off before the train has come to a complete stop

  ![Train](https://github.com/dlartigu/Doom-Nukem-42/blob/main/gif/level2/1.gif)

- Don't forget the ticket to the next level!

  ![Ticket](https://github.com/dlartigu/Doom-Nukem-42/blob/main/gif/level3/2.gif)

- The Den

  ![The Den](https://github.com/dlartigu/Doom-Nukem-42/blob/main/gif/level3/1.gif)

- The Arena

  ![The Arena](https://github.com/dlartigu/Doom-Nukem-42/blob/main/gif/levelfinal/1.gif)

Arcade:

- CIRCUS

  ![Circus](https://github.com/dlartigu/Doom-Nukem-42/blob/main/gif/arcade1/1.gif)

- MINE

  ![Mine](https://github.com/dlartigu/Doom-Nukem-42/blob/main/gif/arcade2/1.gif)

- MAGMA

  ![MAGMA](https://github.com/dlartigu/Doom-Nukem-42/blob/main/gif/arcade3/1.gif)







