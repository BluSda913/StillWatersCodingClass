# Team Logan: Install minecraft to code a working analog clock, and Build a House.

Instruction Borrowed:
https://www.stuffaboutcode.com/p/minecraft.html

# Materials List
- Raspberry Pi 4 
- Monitor 
- Peripherals

# Minecraft Pi

### How to download Minecraft Pi Edition 

First navigate to the Menu->Preferences->Recommended Software->Games then find Minecraft to download.

To open minecraft navigate to Menu->Games->Minecraft Pi.

(Opening Minecraft in the Terminal: open Terminal type `minecraft-pi`)

### How to Connect Minecraft Pi to the Terminal 

Note: Minecraft has to be opened for this to work

Open Thonny Python IDE. Open a new file, then type 

`import mcpi.minecraft`

`mc = mcpi.minecraft.Minecraft.create();`
 
 After this you should be connected to minecraft.
 
 this is a simple code to write a message in chat
 
( open Thonny PythonIDE)

`import mcpi.minecraft`

 `mc = mcpi.minecraft.Minecraft.create()`
 
 `mc.postToChat("Hello World")`
 
### Minecraft Pi Working Analog 

https://www.stuffaboutcode.com/2013/02/raspberry-pi-minecraft-analogue-clock.html

Note: Minecraft has to be opened for this to work

Open the Terminal and type in the following code 

`sudo apt-get install git-core`

`cd ~`

`git clone https://github.com/martinohanlon/minecraft-clock.git`

`cd minecraft-clock`

`python minecraft-clock.py`

This code is used to download the code directly from https://github.com/martinohanlon/minecraft-clock.git.

# Build Your House in Minecraft

### Getting Started

Instructions borrowed: 
https://gist.github.com/jonwitts/2ac5b12d7231a95f959f0fabd17cd66b

(Open Thonny PythonIDE)

Now that you got a little comfortable with code lets build a house.
Lets connect to minecraft first.

Use the import command from before, now you are connected.

After you are connected now you need to get your position in Minecraft

`x, y, z = mc.player.getPos()`

define your block palette, discuss with your teammates, and note down, what kind of blocks you want to use to build your house .
then use this to get the block ID for the blocks

https://www.raspberrypi-spy.co.uk/2014/09/raspberry-pi-minecraft-block-id-number-reference/

then in the code write the block name = then the block ID number
(example: air = 0)

IMPORTANT!!!!(BLOCKS YOU NEED TO ADD)
fence = 85
glass_pane = 102

### Lets BUILD!

Clear out your area first 

`mc.setBlocks(x-10, y, z-10, x+10, y+15, z+10, air)`

Now lets set the foundations 

`mc.setBlocks(x-7, y-1, z-7, x+7, y-3, z+7, stone)`

Lets add some fences around your house

`mc.setBlocks(x-7, y, z-7, x+7, y, z-7, fence)`
`mc.setBlocks(x-7, y, z-7, x-7, y, z+7, fence)`
`mc.setBlocks(x+7, y, z+7, x+7, y, z-7, fence)`
`mc.setBlocks(x+7, y, z+7, x-7, y, z+7, fence)`

Now lets set your house block( choose the block type your team has selected for the house and put it at the very end) 

`mc.setBlocks(x-5, y, z-5, x+5, y+9, z+5,)`

hollow it out

`mc.setBlocks(x-4, y, z-4, x+4, y+8, z+4, air)`

Floor decor( choose the block type your team has selected for the floor and put it at the very end) 

`mc.setBlocks(x-4, y-1, z-4, x+4, y-1, z+4,)`

Second Floor level( choose the block type your team has selected for the floor and put it at the very end) 

`mc.setBlocks(x-4, y+4, z-4, x+4, y+4, z+4,)`

Ceiling( choose the block type your team has selected for the ceiling and put it at the very end)

`mc.setBlocks(x-4, y+9, z-4, x+4, y+9, z+4,)`

Lets add a door

`mc.setBlock(x-5, y, z, 64, 0)`
`mc.setBlock(x-5, y+1, z, 64, 8)`

Lets add windows

`mc.setBlocks(x-5,y+1,z-2,x-5,y+2,z-3,glass_pane)`

`mc.setBlocks(x-5,y+1,z+2,x-5,y+2,z+3,glass_pane)`

`mc.setBlocks(x-5,y+6,z-2,x-5,y+7,z-3,glass_pane)`

`mc.setBlocks(x-5,y+6,z+2,x-5,y+7,z+3,glass_pane)`

`mc.setBlocks(x+5,y+1,z-2,x+5,y+2,z-3,glass_pane)`

`mc.setBlocks(x+5,y+1,z+2,x+5,y+2,z+3,glass_pane)`

`mc.setBlocks(x+5,y+6,z-2,x+5,y+7,z-3,glass_pane)`

`mc.setBlocks(x+5,y+6,z+2,x+5,y+7,z+3,glass_pane)`

Now lets add some stairs to the second floor

Create a hole to the second floor 

`mc.setBlocks(x+3,y+4,z+4,x,y+4,z+3,air)`

Now a loop through our steps

`for i in range(5):`
    `mc.setBlock(x+i-1,y+i,z+3,stairs)`
    `mc.setBlock(x+i-1,y+i,z+4,stairs)`
    
Lets add the stair banistairs
 
`mc.setBlocks(x-1,y+5,z+4,x-1,y+5,z+2,fence)`
`mc.setBlocks(x-1,y+5,z+2,x+2,y+5,z+2,fence)`

Lets add the roof of the house

First add the pitches

`for i in range(5):`
    `mc.setBlocks(x-5+i, y+10+i, z-5, x-5+i, y+10+i, z+5, roof)`
    `mc.setBlocks(x+5-i, y+10+i, z-5, x+5-i, y+10+i, z+5, roof, 1)`
    
Now the top of the roof 

`mc.setBlocks(x, y+14, z-5, x, y+14, z+5, roof_flat`

Now the sides

`for i in range(4):`
    `mc.setBlocks(x-1-i, y+13-i, z-5, x+1+i, y+13-i, z-5, brick)`
`for i in range(4):`
    `mc.setBlocks(x-1-i, y+13-i, z+5, x+1+i, y+13-i, z+5, brick)`
    
### Now your house is complete. CONGRAJULATIONS!!!!!!!!

Example: this is Jon Witt's (maker of the code) house build.

 https://gist.github.com/jonwitts/2ac5b12d7231a95f959f0fabd17cd66b
