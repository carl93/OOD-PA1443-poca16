# Use Case Overview for System _TwitterNetHack_
1. Title Page
    1. Title: Use Case Overview
    1. Sub-title: "Assignment int the course PA1443 Introduction to Software Design and Architecture"
    1. Authors and Author Contribution

| Author Name   | Social Security Number| Thinking  |Writing  |
| ------------- |:-------------:| -----:|-----:|
| Pontus Carlsson  | 9308181636 | 100% |100% |

1. System Description

A version of the game 'NetHack' featuring multiplayer gameplay and a modernized navigation system. The game focuses on exploration and will incoporate Twitter to mutate the games stage generation process based on the content of tweets resulting in a constantly changing and  dynamic experience.
1. Use Case Diagram
![model](https://github.com/carl93/OOD-PA1443-poca16/blob/master/Assignments/model-rev.jpeg "Diagram")
1. Actors
### Player
The User.
### Map builder
Handels the random map generator.
### Map fetcher
Handels map fetching when joining existing games.
### Twitter API
Handels communications via the Twitter API to get the data used to generate maps.
1. Detailed Use Cases

| # | Actor | Use Case | Description |
| - |:-----:|---------:|------------:|
| 1 | Player | Player setup | _The Player entered setup screen via the main menu and is presented with various customization options._ |
| 2 | Player | Create game | _The Player attempts to create and host a new game._ |
| 3 | Player | Join game | _The Player attemts to join an existing game._ |
| 4 | Map builder | Generate map | _As a new game is being created a new map will be generated. A map can be either random generated or generated using the twitter API. In this case a random generated map will be created._ |
| 5 | Twitter API | Generate map | _As a new game is being created a new map will be generated. In this case a map generated using the Twitter API will be created._ |
| 6 | Map fetcher | Get exsisting map | _As the player attempts to join a existing game the Map fetcher will attempt to load the corresponding map._ |
| 7 | Player | Move | _The Player has changed position within the map and become eligable for a random encounter._ |
| 8 | Player | Encounter Item | _When an item is encountered it is automaticly added to the players inventory until the player explicitly drops the item._ |
| 9 | Player | Show inventory | _Lists the items currently in the players inventory._ |
| 10 | Player | Examine item | _The Player examines an item from their inventory and is presented with a short description of said item._ 
| 11 | Player | Use item | _The Player uses an item from their inventory._ |
| 12 | Player | Combine items | _The Player attempts to combines two items from their inventory._ |
| 13 | Player | Drop items | _The Player drops an item from their inventory._ |
| 14 | Player | Encounter NPC | _When an NPC is encountered the player may choose how to interact with said NPC._ |
| 15 | Player | Debate NPC | _The Player has encountered an npc and chosen to start a debate._ |
| 16 | Player | Fight NPC | _The Player has encountered an npc and chosen to do battle._ |
| 17 | Player | Challenge NPC | _The Player has encountered an npc and chosen to challenge said NPC to a game of chess._ |
| 18 | Player | Encounter Player | _When another Player is encountered the player may choose how to interact with the other player._ 
| 19 | Player | Chat with Player | _The Player has encountered another player and requested to chat._ |
| 20 | Player | Trade with Player | _The Player has encountered another player and requested a trade of items._ |
| 21 | Player | Use item on Player | _The Player has encountered another player and attemted to use an item on said player._ |
| 22 | Player | Ignore encounter | _The Player has encountered an item,npc or another player but chosen to ignore said encounter._ |
