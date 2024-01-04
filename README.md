# Bare-Godot-Mulitplayer
A Godot 4, multiplayer game using LAN, with Godot 4 networking nodes.
_____________________________________________

<img width="581" alt="Screenshot 2024-01-04 at 1 53 59 PM" src="https://github.com/had2020/Bare-Godot-Mulitplayer/assets/59424667/550e4ee9-ad4f-4188-a36d-33d321af3b4a">

Simple Multiplayer project, players locally connect via lan. To make a online game, someone must press connect on the same network, then to join other can press the join button.

_____________________________________________

# Main Scene Node tree 

<img width="258" alt="Screenshot 2024-01-04 at 1 54 26 PM" src="https://github.com/had2020/Bare-Godot-Mulitplayer/assets/59424667/3022c3a4-56b2-4a8a-bf18-c91739ec397c">

_____________________________________________

# Code analyist 

Gui - Node 2D
holds code to handel gui input, and multiplayer code
 
 - code
A signal is connected from each button, this is done to handel the inputs, for joining and hosting.
If a signal from any of the button comes in they have repective events, this will trigger the joining or hosting code.
Hosting, a server is created on a port using the Multiplayer Spawner Node, then your player is added.
Joining, a client is created on a port using the Multiplayer Spawner Node, then your player is added.
Joined, if a player trys to join on using the same port, that the server was hosted on, the player will be created.

 - Player code within the player scene
Every physics frame then if the user is the owner of this player, the player's velocity is changed to match the movement, from the input.
