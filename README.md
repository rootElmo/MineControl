# MineControl

This is a script I made in 2019 for a school project. We had the liberty to choose something to manage with Linux and I chose to make a Minecraft server with a small script controlling it

## Why the script?

The script was made to avoid constant switching between tmux-screens and to generally make the whole server upkeep more user friendly. The issue was that if I had the server running on a VPS, as soon as I logged out/lost connection, the server process would stop.

## Basic functionality

The script start the Minecraft server, _server.jar_, on a new tmux terminal in the background. This way when connecting to a server hosting the Minecraft server the user doesn't need to worry about timeouts of the connection causing the server to crash. Other administration tasks can also be completed on the server without interrupting the Minecraft server.

When the script in placed in the ***/usr/local/bin*** folder, the commands can be called everywhere with the scripts name.

##To-do:

* Fix possibly infinite 'while'-loops with some sort of time-out
* In function ***srv_stop*** instead of trusting the _sleep_ timer to wait for saving of blocks etc. find a more reliable solution for checking if saved or not (if saving takes a long time, server might shutdown before saving of blocks is completed).
* Use a function to check status of ***server.jar*** to make code more compact
* COMMENT SCRIPT
* Learn more about tmux to increase complexity of functions and reliability.

