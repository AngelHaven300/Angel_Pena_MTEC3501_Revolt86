## Project Overview

---
## Revolt 86
---
Revolt 86 is a tactical two player game where players deploy custom card decks, and roll to split movement and shooting across an 8 x 12 board, and fight to destroy their opponents Mothership. 

---
This project is trying to achieve the creation of a new strategy board game hybrid. A mix between my very own game, Revolt 86 and electronics to enhance an automate my games existing mechanics.

---
## North Star Vision

In its most complete form this project becomes a well developed strategy board game that has a microcomputer integrated into the board, creating an electronic smart board that can read physical objects to dictate how the game plays out. Two players will sit across from eachother, each player will have a screen that is attatched to their side of the board. The display will light up and ask them to login into their Revolt 86 accounts through a device by connecting to the same wifi that the board is connected to. They set up all of their pieces on the board as well as have their Revolt 86, 24 card deck in its designated spot beside the board. First each player will draw 5 cards and place them into their hands, the display will assign each player a role, either one player plays as the rebels or they play as the oppressors. The rebels will always have the first turn, the player who is assigned to be the rebels will roll a bluetooth die that is connected to the microcomputer over bluetooth. The board will receive the information on what the player has rolled and then display the number they rolled as points. The player decides which one of their pieces they would like to spend their points on, as soon as they touch the piece the board will sense it and light up a path on the board based on the pieces valid paths it could move or shoot in. The display will give the option to either move the piece or have the piece shoot from where they are on the board. If the player wants to move the piece, they simply place the piece on a square within a lit up path on the board. To shoot the player will choose what path and what square to shoot at using the display. If they hit a piece then the other player must put a damage counter on the bottom of the piece that was hit. If a player kills an enemy piece the board will remind them to draw a card. During a players turn they can decide to place down a card on their card reader, the board will read the card and then apply its effects on the board using the game logic that is programmed into it. Once either player manages to destroy their opponents mothership they win and the game ends. 
Revolt 86 is powered by a custom engineered physical 8x12 grid layout of electronic components. At the core of the board there is a high-performance ESP32-S3 microcontroller that manages all 96 RFID readers. These readers can scan each piece in millisecond intervals. Visual feedback is driven by 96 surface mounted LED's situated beneath the light diffusing 3D printed squares on the board, this is paired with touch displays that display live health stats and turn phases. The system connects and interfaces wirelessly with a Blurtooth die to automatically register rolls. On the software side, the board runs a custom programmed, real time state engine that executes the movement and attacks on the board, card readings and overrides, and health logs. There is a integrated Wi-fi module that connects the board to a cloud database, this enables live account syncing, global leaderboards, and firmware updates whenever new physical card expansions or war pieces are released. 
Revolt 86 takes place in a dystopian future set in the year 2086, this point in time marks the start of a revolution. For decades, in the country of Vanska there has been a extreme power imbalance between the upper class and the lower class. Constant abuse and mistreatment of the lower class was considered normal, that is until the victims of said abuse have had enough. They no longer consider themselves less than anyone, they strive to break these societal confines by gaining military weapons won through acts of rebellion. They throw away their previous identities and label themselves as Rebels. Their one purpose... overthrow and destroy those who have unjustly oppressed them in the past to create a better tomorrow. Each piece on the board is a custom model, designed to be weapons of mass destruction. The cards have detailed artworks that portray what it does as well as containing a description of what it does. 

---
## Proof of Concept

Before even being able to program a propietary game state engine for Revolt 86 that is capable of executing game logic onto the physical board and have it display information on the touch display. The core game mechanics and rules must be sound and balanced. Being able to playtest the board game without any electronics is crucial to develop and create future game logic for its successor. This semester's prototype will have the following core features.

- Playtested rules and mechanics
- 3D printed prototype of the board
- Custom 3D models for the game's pieces
- Prototype trading cards. 

Players will have the ability to move their pieces on the board, use cards throughout the game, deal and receive damage, and keep track of it. 

*What it Won't do*

- RFID Readers
- Touch Display
- Bluetooth die
- Microcomputer 
- Digital Art

---
## Least Viable Product

By MTEC 4501 the project will demonstrate a prototype board that has all 96 RFID Readers integrated and capable of reading data stored in each piece using RFID stickers. As well as have LED's that can light up a path on the board. I plan on further developing the artistic elements by drafting digital artworks for each individual card. Although this prototype will not be able to execute Revolt 86's card mechanics and game logic quite yet, this is the proof, start, and base of creating the Revolt 86 Smart Board Console. 

*What it Won't do*

- Touch Display
- Bluetooth die
- Programmed Game Engine

---
## Existing Projects & References

- ChessUp and Chessnut Smart board.
- Warhammer 40K
- Titan Fall 2
- Chess

*What I need to learn* 

- 3D printing 
- PCB Design
- Electronics
- Digital Artwork
- Programming 

---
## Self-Reflection & Open Questions

*What Feels Strong?*

Core Game Mechanics & Design: High confidence in the turn-based structure, the 8×12 grid layout, vector movement rules, and card-based ability interactions.

Asset Creation & 3D Modeling: Complete confidence in designing, modeling, and 3D-printing the physical mechs, Mothership pieces, and art style inspired by Titanfall 2.

Graphic Design & Worldbuilding: The visual theme, dystopian narrative, card art execution, and physical board aesthetic are fully realized creative strengths.

*What Feels Weak?*

Hardware Reliability Assumption: Assuming that dozens of off-the-shelf electronic modules can run simultaneously over long gaming sessions without overheating, losing signal, or crashing.

Digital Translation Gap: Assuming that every unique card effect, trap trigger, or complex board modifier can be cleanly represented in microcontroller code without creating game-breaking edge cases.

Hardware-to-Mobile Latency: Assuming low-latency Wi-Fi/Bluetooth synchronization between the physical ESP32 board, health bars, and the mobile application backend.

*What Needs Testing?*

Proof-of-Concept Sensors: Wire a small 4-square RFID and LED circuit using to test signal interference, scanning latency, and piece-detection speed before committing to the full 96-square PCB.

Bluetooth Die and Display Bridge: Test whether the ESP32 can continuously maintain a Bluetooth Low Energy connection with the wireless die while simultaneously updating the touch screen UI.

RF Signal Cross-Talk: Place two RFID-tagged 3D printed pieces on adjacent squares to verify if the RFID readers misread between tight grid spaces.