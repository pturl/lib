---
layout: post
title: "The Early Days of MMOs - Behind the Scenes of Ultima Online`s Development"
date:   2024-01-02 01:23:32 +0000
categories: Gaming
excerpt_image: https://www.mmogames.com/wp-content/uploads/2014/02/ultima-online-uo-fantasy-mmorpg-mmo-games-screenshot-1.jpg
image: https://www.mmogames.com/wp-content/uploads/2014/02/ultima-online-uo-fantasy-mmorpg-mmo-games-screenshot-1.jpg
---

### The Technology
Ultima Online was ran on custom **game servers** built by Origin for the game. The servers used Sparc processors and were housed in a converted closet with a cooling fan. Each game world, or **"shard"**, spanned multiple servers to handle the load and persisted player data to a shared database. Game data like items and creatures were defined in text files edited with vi. In-game maps and object placements were stored in binary files edited with a special "god client" tool.

![](https://www.mmogames.com/wp-content/uploads/2014/02/ultima-online-uo-fantasy-mmorpg-mmo-games-screenshot-1.jpg)
### The Programming Team  
The game was coded primarily in C and C++ by a small initial team led by **Rick Delashmit**. Two custom scripting languages powered much of the game logic. **Wombat**, the main language, handled object interactions, AI, and more in an event-driven syntax. **Escript** was a simpler language for large-scale procedural map edits. Most developers worked directly on Linux copies of the game server for testing.
### The Network Protocol
A custom network protocol transported tightly compressed packets over TCP to optimize bandwidth usage on 1995 modem connections. Changing packet structures required coordinated client and server updates. Load was balanced across bounded map regions managed by separate **"areaservers"**. When players crossed boundaries, all their data was bundled and shipped to the new server.
### Data Storage and Backups  
At launch, all persistent player and world data resided in volatile memory only. No databases were used. Backups worked by pausing inter-server travel and having each region fork a copy of its running process, then dump memory to disk files archived together. These memory snapshots occurred every 30 minutes to safeguard against crashes.
### Design Challenges   
Server limitations like the 256 file descriptor cap meant special "player server" processes were needed just to manage connections. Boundary races could still allow duping of items or gold. Over time, costly simulation systems were downsized or only run locally for performance. Even monster combat stopped unless watched by players. 
### Ongoing Development
As the team expanded, most development moved to Linux copies of the live game code. Scripted systems evolved while the core C/C++ codebase remained. Load balancing improved as the hardware and budgets did. Bugs took time to eliminate, especially around persistence across servers.
### Legacy of Ultima Online
While its code is long gone, Ultima Online established conventions still used in modern MMOs for scripting, simulation, and persistence architectures. Its tightly engineered multiplayer gaming experience also proved the potential of online virtual worlds and the genre they founded.