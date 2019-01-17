# MonsterGenerator
Using WaveFunction Collapse to make monstrous bodies!
A project by Devi Acharya, Rehaf Aljammaz, and Mirek Stolee

This is a set of rules used with [Maxim Gumin's WFC in C#.](https://github.com/math-fehr/fast-wfc). It uses Gumin's SimpleTiledModel as a base. We add our tileset and rules for placing those tiles.

## Outputs
Produces a NxN image made of 32x32px tiles.
<p align="center"><img alt="big Zombie" src="./exampleOutput/bigZombie.png"></p>
We have provided two tilesets - zombie and centipede.
<p align="center"><img alt="zombie" src="https://i.imgur.com/FQA98n4.png"><img alt="centipede" src="https://i.imgur.com/WmPIhV0.png"></p>

## How to use
1. Open samples.xml
    1. Edit parameters: which monsters to output, width and height of output in tiles
2. In root directory, enter command: dotnet run WaveFunctionCollapse.csproj
3. After running, output will appear in the root directory.

## Process
The rules for the tiles are in ./samples/"MonsterName"/data.xml
Tiles are assigned a symmetry value depending on their number of unique rotations. For example, the empty tile is assigned "X" because its orientations do not matter. The arm has 4 unique rotations, so it is assigned the letter "L". These symmetry values automatically generate implicit placement rules from the neighbor rules you set in the next section.
<p align="left"><img alt="tiles" src="https://i.imgur.com/EEGM2sr.png"></p>
Then, tiles are assigned neighbor rules that determine which tiles and in which orientations can be next to each other. By saying which tiles can be on the left and right of each other, the vertical rules are implied using the symmetry values set above. A tile with no number after it is in its original orientation, and the 1-3 variants represent subsequent 90 degree turns counter-clockwise.
<p align="left"><img alt="tiles" src="https://i.imgur.com/58aVo0N.png"></p>

Here is our original tileset without any rules:
<p align="left"><img alt="tiles" src="https://i.imgur.com/6yeiUbB.png"></p>
After updating rules, we had some issues with arms before making some changes to the symmetry values:
<p align="left"><img alt="ARMy" src="https://i.imgur.com/IxgJ432.png">
<img alt="SuperArms" src="https://i.imgur.com/2VZTTZO.png">
<img alt="mindControlArms" src="https://i.imgur.com/H9A6D2m.png"></p>

## Tiles
To make your own tilesets, you need the following tiles in the .png format.
Tiles must be oriented the same way as ours and placed in ./samples/"YourMonsterName"
1. Head
![alt text](https://i.imgur.com/RiMIcTR.png "Head Image")
2. Chest
![alt text](https://i.imgur.com/nP0EXBv.png "Chest Image")
3. Abs
![alt text](https://i.imgur.com/eNmM7wJ.png "Abs Image")
4. Legs
![alt text](https://i.imgur.com/1sXJjtI.png "Legs Image")
5. Feet
![alt text](https://i.imgur.com/moZ6lJk.png "Feet Image")
6. Arm
![alt text](https://i.imgur.com/Xp7nZdh.png "Arm Image")
7. Hand
![alt text](https://i.imgur.com/S2xE52R.png "Hand Image")
8. Empty
![alt text](https://i.imgur.com/owWpdcU.png "Empty Image")
