# MonsterGenerator
Using WaveFunction Collapse to make monstrous bodies!

This is a set of rules used with [Maxim Gumin's WFC in C#.](https://github.com/math-fehr/fast-wfc) It uses the Simple Tiled Model with custom tilesets.

## Outputs
Produces a NxN image made of 32x32px tiles.
<p align="center"><img alt="big Zombie" src="./exampleOutput/bigZombie.png"></p>
We have provided two tilesets - zombie and centipede.
<p align="left"><img alt="zombie" src="https://i.imgur.com/FQA98n4.png"><img alt="centipede" src="https://i.imgur.com/WmPIhV0.png"></p>

## How to use
1. Open samples.xml
    1. Edit parameters: which monsters to output, width and height of output in tiles
2. In root directory, enter command: dotnet run WaveFunctionCollapse.csproj
3. After running, output will appear in the root directory.

## Progress shots
Here are some images showing the process of making the project.
We had some issues with arms:
<p align="left"><img alt="ARMy" src="https://i.imgur.com/IxgJ432.png">
<img alt="SuperArms" src="https://i.imgur.com/2VZTTZO.png">
<img alt="mindControlArms" src="https://i.imgur.com/H9A6D2m.png"></p>

## Tiles
To make your own tilesets, you need the following tiles in the .png format.
Tiles must be oriented the same way as ours.
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
