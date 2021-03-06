[Home](http://3h4.uk)
# inkyblinky
*3 minute read*

This is a very short tutorial/guide of a very simple Raspberry Pi project, inspired by Sandy's guides over at Pimoroni!

## things you need
- Raspberry Pi Zero/Zero W
- InkypHAT
- Blinkt
- Mini Black Hat Hack3r
- 3* Male 40-pin header
- 1* Female 40-pin header
- Soldering tools

![things you need](https://github.com/3hundred4teen/3hundred4teen/blob/master/assets/images/inkyblinky-1.jpg?raw=true "things you need")

## soldering the stuff
### step 1 - soldering the black hat
The Mini Black Hat is what we will use to stack the the InkypHAT and Blinkt modules together, and to keep our project on a lovely plate. The Mini Black Hat is the big brother of the Pico Hat Hacker, and the small brother of the pHATStack.

You *can* solder the headers in whatever inversion you like, as long as the corresponding headers on the pHATS are compatible. For my project, I decided to use a female header on the bottom stack, as my Pi Zero already had a male header on the back

![soldering the black hat](https://github.com/3hundred4teen/3hundred4teen/blob/master/assets/images/inkyblinky-4.jpeg?raw=true "soldering the black hat")

1. First, pop the first header into the the Black Hat Hacker, making sure it is perpendicular and flush to the board
2. Then, tape up the left side of the header with some electrical tape, making sure it is securely held in place
3. Flip the board, over, and place it into a third hand (or into a breadboard if you don't have one)
4. Carefully solder the pins, making sure the solder doesn't bridge! (A full guide to soldering can be found [here](https://learn.pimoroni.com/tutorial/sandyj/the-ultimate-guide-to-soldering))
5. Repeat this for all three headers on the Black Hat Hacker

![soldered black hat](https://github.com/3hundred4teen/3hundred4teen/blob/master/assets/images/inkyblinky-3.jpeg?raw=true "soldered the black hat")

### step 2 - soldering the pi
For this project **don't get the Pre-Soldered Pi Zero H or Zero WH**, as we will need to reverse-mount the headers.

![soldering the pi](https://github.com/3hundred4teen/3hundred4teen/blob/master/assets/images/inkyblinky-5.jpg?raw=true "soldering the pi")

1. Pop the *correctly gendered header* into the back of the Pi Zero, and tape it up as before
2. Carefully solder up the pins - and be extra careful around the middle, making sure not to de-solder any of the components on the board its self

## building the plate
### step 3 

![building the plate](https://github.com/3hundred4teen/3hundred4teen/blob/master/assets/images/inkyblinky-6.jpg?raw=true "building the plate")

1. Once everything is soldered and checked for no bridging, pop the pHATs and Pis in as shown above
2. You can of course swap any components out, or use a pHATStack for more pHATs, but make sure they are compatible! Check here -> https://pinout.xyz/phatstack to make sure your pHAT don't clash with any pins

![the plate](https://github.com/3hundred4teen/3hundred4teen/blob/master/assets/images/inkyblinky-7.jpg?raw=true "the plate")

## powering the pi
### step 4 - Setting up the OS
1. If you've got a pre-flashed NOOBS card, skip this step
2. If not, flash a Micro SD (at least 4GB) with Raspian (stretch or lite), but keep it plugged into your computer
3. Follow this dead simple Gist -> https://gist.github.com/gbaman/975e2db164b3ca2b51ae11e45e8fd40a to control your Pi over SSH from another laptop - no external display or keyboard required!
4. Once youv'e changed the config, cmdline, and added the ssh file, pop the SD card into the pi, and connect it **from the USB port** (not the power port) into a computer
5. Type into command line/terminal `sudo ssh pi@raspberrypi.local`, enter your sudo password, and enter the default user password `raspberry` when prompted
6. Your computer should then SSH into the Raspberry Pi as if by magic!
7. Run `sudo raps-config` to set up the Pi how you want, and reboot

### Step 5 - apt get!
1. Once the Pi is all set up, run the commands to set up the Python libraries we will need: curl `https://get.pimoroni.com/inkyphat  | bash` for the inkyphat and `curl https://get.pimoroni.com/blinkt | bash`
2. Answer yes (y) to all the prompts, and let the libraries install
3. Once they have finished cd into the Pimoroni folder (`cd Pimoroni`) and have a play with the examples!

![the inkyblinky](https://github.com/3hundred4teen/3hundred4teen/blob/master/assets/images/inkyblinky-9.jpeg?raw=true "the inkyblinky")

### Step 6 - name badge and lights
1. cd into the inkyphat examples folder (`cd inkyphat/examples`) and run the Name badge example (`sudo python3 hello.py [your_name_here]`)
2. cd into the blinkt examples folder (`cd`, then `cd Pimoroni/blinkt/examples`) and run any of the examples you like (for example, `sudo python3 rainbow.py`)

![final shot](https://github.com/3hundred4teen/3hundred4teen/blob/master/assets/images/inkyblinky-10.jpg?raw=true "final shot")
