# Team Logan: Install minecraft to code a working analog clock, and a replica model of the solar system.

Instruction Borrowed:
https://www.stuffaboutcode.com/p/minecraft.html

# Materials List
- Raspberry Pi 4 
- Monitor 
- Mouse/Keyboard
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
 
### Minecraft Pi Working Analog 

https://www.stuffaboutcode.com/2013/02/raspberry-pi-minecraft-analogue-clock.html

Note: Minecraft has to be opened for this to work

Open the Terminal and type in the following code 

`sudo apt-get install git-core
cd ~
git clone https://github.com/martinohanlon/minecraft-clock.git
cd minecraft-clock
python minecraft-clock.py`

This code is used to download the code directly from https://github.com/martinohanlon/minecraft-clock.git.

### Minecraft Pi Solar System Replica

https://www.stuffaboutcode.com/2013/03/raspberry-pi-minecraft-planetary.html

Note Minecraft has to be opened for this to work

Open the Terminal and type in the following code 

`sudo apt-get install git-core
cd ~
git clone https://github.com/martinohanlon/minecraft-planets.git
cd minecraft-planets
python minecraft-planets.py`

This code is used to download the code directly from https://github.com/martinohanlon/minecraft-planets.git.



