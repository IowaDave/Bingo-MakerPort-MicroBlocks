# Bingo-MakerPort-MicroBlocks

## Let's Play Bingo!
Make an interactive, audible Bingo game caller using MicroCode with Roger Wagner's MakerPort.

To build this project you will need:

* a MakerPort
* three "touchpoints", explained below
* optional microSD card to contain audio files
* USB-C cable connection to a computer
* MakeCode IDE, either by:
    * installing the standalone IDE on a compatible computer, or
    * using a Web browser capable of running the free online IDE [available through this link](https://microblocks.fun/run-pilot/microblocks.html).
* optional accessory power supply, when you want to run the game without a computer connection.

## Contents


## Introduction
### The MakerPort
You've heard the saying, "Hey, Take It Easy"? Now there's a new saying, "Hey, Make It Easy!"

A wide variety of different displays, sensors, lights and motors can plug directly into a MakerPort. It's like an Arduino that doesn't need shields because it has ports instead. It's like a USB hub designed for Makers. 

Suppose you want to make something that interacts with people or controls something, but without the need to wire up a circuit board. Make It Easy, with a MakerPort.

Even more, it contains an MP3 audio player and built-in speaker. This project uses the feature to say the names of the Bingo balls out loud.

The MakerPort is built around the same, advanced microcontroller as the modern Arduino Zero. It can be programmed using the Arduino IDE, but that is not necessary. This project demonstrates an accessible and user-friendly alternative, called MicroBlocks.

### MicroBlocks
This is a graphical programming language. Users build programs by selecting and connecting colorful "blocks", similar to the popular Scratch and Snap! In fact, some of the same people who originated those two languages are leading the development of MicroBlocks.

A very nice feature of MicroBlocks is how the blocks read like instructions given in a natural, human language. Incidentally, MicroBlocks is available in 16 major, world languages.

Extensive documentation is available at [the dedicated MicroBlocks Wiki site](https://wiki.microblocks.fun/en/home). 

The Wiki includes a User Guide that covers all the basics. Here is a link to a separate, [introductory tutorial] showing how to use MicroBlocks to blink an LED plugged into a MakerPort. No circuit board required!

### The MakerPort Library
MicroBlocks supports many different Maker devices. 

### All About Touchpoints
A touchpoint is a physical object that works as a kind of electronic pushbutton. Merely touch it. The MakerPort will detect the touch and activate code you write to respond to it.

Almost anything metallic or moist can be a touchpoint: an empty tin can or piece of aluminum foil will do nicely; you can even use fruit. MakerPort includes a port for connecting up to 12 of these versatile sensors through wires. For example, see Figure 1.

This project uses inexpensive earring backs, commonly available in the jewelry-making area of craft stores. Their small size and uniform shape makes them especially suitable for interactive displays. 

In this project, we insert three touchpoints into special, extra ports provided on the MakerPort enclosure itself. Figure 2 illustrates their placement. No further wiring is required, except to connect a power source to the MakerPort.

### Optional Audio
The example code provided for this project takes advantage of the MakerPort's MP3 player and built-in speaker.

Copy the folder named "81" from this GitHub repository onto a microSD card. Install the card into the MakerPort. Important: slide the small switch on the side of the MakerPort so it is closest to the USB socket. This position enables the MP3 player to access the files on the microSD card. 

## How the Program Works
Each of the three touchpoints initiates a different action:

* Start a new game.
* "Draw" and announce one "ball". Repeated touches select successive ball numbers.
* List all of the balls that have been drawn so far in the current game. Touching again repeats the list including balls added since the previous touch.

Six, separate "scripts" make up the program. A script is a list of blocks connected together under a "hat". The hat identifies the script and tells MicroBlocks when to run the code in it. 

Each script performs just one action. Five of them respond to user actions, such as touching a touchpoint. The sixth defines a "helper" function that runs when one of the other scripts call for it.

MicroBlocks activates the scripts as needed to create the game experience.

### When Started
![Picture of when-started script](./images/when-started.png)

### When PinTouch Event
![Picture of when-pintouch-event script](./images/when-pintouch-event.png)

### When NextBall Received
![Picture of when-nextball script](./images/when-nextball-received.png)

### When NewGame Received
![Picture of when-newgame script](./images/when-newgame-received.png)

### When TypeBalls Received
![Picture of when-typeballs script](./images/when-typeballs-received.png)

### Define BallName
![Picture of define-ballname script](./images/define-ballname.png)


