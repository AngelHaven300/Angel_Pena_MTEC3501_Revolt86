
## Student / Team

Angel Pena Bazan
10/1/26

## Working Title

Revolt 86

## Project Format

Game

## Project Description

Revolt 86 is a tactical two player game where players deploy custom card decks, and roll to split movement and shooting across an 8 x 12 board, and fight to destroy their opponents Mothership. 

## User / Integrator Experience

The participent sits across an 8x12 grid game board, then selects 5 physical trading cards from the top of their deck, and rolls a wireless bluetooth die onto the table. When lifting a piece from it's square, LED's from underneat the board immediately light up valid paths to move or shoot in, (Green for movement and orange for shooting) based on the pieces movement set and remaining die points. The player chooses a target piece in the board by tapping it, causing the board to flash an animation while a display updates the remaining movement and health. To activate special abilities or fire the mothership, the player places an RFID tagged card onto the dedicated card reader zone on the board frame. This in turn alters the active LED's and rules on the grid. As pieces take damage, players manually slide damage counters underneath the pieces. The board tracks eliminations and will signal the player to draw a new card. 

## System Description

The project operates as an electronic table top game system built around a microcomputer mounted within a 8x12 grid. Inputs consist of a physical 6 sided bluetooth die that transmits roll values. There will be 96 RFID readers that scan each indivdual piece on the boardand two more RFID readers that read which cards are active and discarded. The Microcomputer takes these inputs and interprets it with the already programmed game logic and then updates the display. There are LED's under the board that flash patterns. Health will be diplayed on the display as well. Uncertain elements inlcude the implementation of Wi-fi syncronization to a mobile app, cloud updates, and the digital translation of complex cards. 

## Explicit Dependency

This project depends on the Microcomputer reliably reading the RFID sensors and the card readers in real time without latency when scanning or any signal cross talk between adjacent RFID readers. If the sensor grid fails to accurately register piece lifts, placements, or card reads within milliseconds, the board cannot update its LED movement pathways or apply the correct card logic and this breaks the real time turn structure and this will render the automated game rules non-functional. 