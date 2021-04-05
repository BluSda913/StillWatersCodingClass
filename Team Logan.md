# Team Logan: Install minecraft to code a working analog clock, bring a 3d model from sketchup to minecraft

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

### Build Your House in Minecraft

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

raspberrypi-spy.co.uk/2014/09/raspberry-pi-minecraft-block-id-number-reference/

then in the code write the block name = then the block ID number
(example: air = 0)

