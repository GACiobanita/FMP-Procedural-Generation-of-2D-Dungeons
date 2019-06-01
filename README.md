# FMP-Procedural-Generation-of-2D-Dungeon

This repository serves as version control for my Final Year Project that will dabble into procedural generation with an environment of a 2D dungeon.

Used Unity 5, in order to display graphics and create minimal gameplay with C# and the UnityEngine modules. 
Created a system that delivers randomly generated 2D dungeons, using the tileset of the first The Legend of Zelda game on the Nintendo Entertainment System.
Dungeons are generated using Binary Space Partitioning, to create dungeon layouts, and Cellular Automata to create different dungeon rooms, while also allowing designer input by creating rooms which can be added to a separate room pool and making available variables which modify the resulting dungeons.

Scenes: 
1. roombuilder:
-Tool for designers to create their own custom rooms.
-Saves layouts, in .txt format, to a default path or an input path.
-Allows for files to be loaded and modified again.
-UI is self explanatory,e.g. tile sprites are present in the UI for easy identification.
-Usage:
  a. Input room width and height, then "Generate Room"
  b. Select any tile in the "None" dropdown and click on any tile in the generated room.
  c. Enter a file name before saving.
  d. Optional to input a file path to save, default is "C:\Users\Public\Documents\"
  e. Check the text file contents.


2. test:
-LevelBuilder goes first,using Binary Space Partitioning, to define a maximum size of the level, which will be split into sections, then room are fit into each section, depending directly on defined room size and final section size
-RoomBuilder goes after the LevelBuilder, creating the custom rooms,using Cellular Automata, you will notice some rooms have leaf shapes.
-Usage:
  a. "Play" the scene.
  b. A "Link" player character will spawn, controlled using Arrows or WASD, Spacebar for attack.
  c. Gameplay order: Spawn->Find Key->Find "DungeonExit"
  d. Along the way the player will enter different rooms which will close their exits upon entry.
  e. Fight the enemy or the item needed to open the rooms.
  f. Upon exit a new dungeon layout is generated.

