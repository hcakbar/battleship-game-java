# Battleship game
## Requirements: 
A player will place 5 of their ships on a 10 by 10 grid. The computer player will deploy five ships on the same grid. Once the game starts the player and computer take turns, trying to sink each other's ships by guessing the coordinates to "attack". The game ends when either the player or computer has no ships left.
### How I created this/How to play:
#### Step 1 – Create the ocean map
The ocean map is represented by a 10 by 10 grid of different characters. The grid is managed by a two-dimensional array where the user and computer decide to place their ships, as well as when someone tries to attack a location and misses. At the start of the game the array will be empty and as the game is played will change what is stored at each index of the array accordingly.
#### Step 2 – Deploy player’s ships
Ask the user where they would like to place their ship.  The player should deploy 5 ships. A ship will be stored in a single index of the array as a special character. 
As the user places their ships, need to check if that is an appropriate location:
1. Can NOT place two or more ships on the same location
2. Can’t place ships outside the 10 by 10 grid
3. If the player is trying to put the ship somewhere it can't be, re-prompt them until they choose legal coordinates for the ship.
Show the map of the current state of their ships.
#### Step 3 – Deploy computer’s ships
The computer will deploy 5 ships by randomly picking X and Y coordinates. Generating these coordinate locations, checking if they are valid and if so placing the ships accordingly. As the ships are being deployed, give the user some feedback about what is happening.
#### Step 4 – Battle
##### Player's Turn
During the battle, the player and computer will take turns guessing X and Y coordinates of the opponent’s ships. Every coordinate guessed should be marked so they players know not to guess there again.
When the player enters X and Y coordinates check if those coordinates are valid within the Ocean Map and haven't been guessed by the user yet, keep re-prompting until the user enters a valid guess. Once the guess is valid program evaluate the result of the move.
There are three possible results of a valid guess:
* Player correctly guessed coordinates of computer’s ship (computer loses ship).
* If successful tell the user "Boom! You sunk the ship!"
* Mark this as a hit when printing the map as a "!". 
Player entered coordinates of his/her own ship (player loses ship).
* Tell the user "Oh no, you sunk your own ship :("
* Mark this as an "x" when printing the map, replacing the "@"
* Player missed. No ship on the entered coordinates. "Sorry, you missed"
* Mark this as an "-" when printing the map.
##### Computer's Turn
After the player guesses a coordinate it's the computer's turn to guess. The computer's attacks are in two randomly generated coordinates.
When the computer produces a valid guess there are three possible outcomes:
* Computer guessed coordinates of the player’s ship (player loses ship).
* Inform the user "The Computer sunk one of your ships!"
* Mark as an "x" when printing the map
* Computer guessed coordinates of its own ship (computer loses ship).
* Inform the user "The Computer sunk one of its own ships"
* Mark as a "!" when printing the map
* Computer missed. No ship on guessed coordinates.
* Inform the user "Computer missed".
* The computer doesn't duplicate guesses.
 

