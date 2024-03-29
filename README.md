# Click Click Vengeance

## Description
As a groupt of three, we made this game, written in the functional programming language OCaml, as our project for CS 3110: Functional Programming and Data Structures. It is based on the games Tap Tap Revenge and Dance Dance Revolution. Both follow the same objective: gain points by hitting specific key/buttons when an icon reaches the bottom of the screen. Our game also follows this objective. We have a window that displays arrows moving down the screen until they reach a certain position at the bottom of the screen. At that point, players should hit the arrow, in order to gain points. The game is multiplayer, so that two players can compete against each other at the same time. We’ve also implemented a leaderboard so that players can try to top their previous scores. We’ve created multiple default modes, each at a different difficulty level. We’ve also implemented hot streaks, in which a player will receive double points if they’ve completed a sequence of ten hits without any mistakes. To increase difficulty, harder modes start at a faster speed, and speed dynamically increases as you continue to play the game. Key combinations also become more complex. Since we could not find a library in OCaml that allows us to play music, we removed that component from our game. 

![Start Page](/screenshots/start_page.png)
![Select Player Page](/screenshots/select_player.png)
![Single Player](/screenshots/single_player.png)
![Double Player](/screenshots/double_player.png)
![End Page](/screenshots/end_page.png)

## Installation and Running Instructions
After cloning this repo and installing OCaml on your system...

Users need to have the following packages installed:
* Yojson
* Graphics
* camlimages

To install these, enter the following commands into the command line:<br>
```opam install yojson``` <br>
```opam install graphics``` <br>
```opam install camlimages```

To build and play the game:<br>
```make build``` <br>
```make play``` <br>
You can read instructions on how to play the game by clicking on the help icon in the bottom left corner of the start screen.

The leaderboard shown when you finish playing a level or lose in endless mode is created each time the game window is opened. Therefore, if you open the game, close it, and open it again, the scores from the first opening will not persist. 

Sometimes the graphics will glitch because of the OCaml graphics library. There isn't anything we can do about this :(.
Also, there may be some functions in the graphics module that don't work on Windows, so this may cause errors. No one in our group has Windows so it works on Mac and we haven't gotten to try it on Windows. If any strange errors occur, trying it on Mac should help. Sorry! OCaml graphics isn't the best :/

DISCLAIMER: There is a small bug, where if you miss the last hit on a level mode, the game will not be able to restart. If you wish to continue playing, simply quit the game and ```make play``` again. This will refresh your leaderboard scores though.

## Documentation
To make docs:<br>
```make docs```<br>
This will generate some errors and warnings. The docs are still generated though, so no worries.

The documentation can be found in the ```doc.private``` and ```doc.public``` folders generated by make docs.

