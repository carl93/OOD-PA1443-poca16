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
![model](https://github.com/carl93/OOD-PA1443-poca16/blob/master/Assignments/model.jpeg "Diagram")

1. Detailed Use Cases

| # | Actor | Use Case | Description |
| - |:-----:|---------:|------------:|
| 1 | Player | Player setup | _The Player entered setup screen via the main menu and is presented with various customization options._ |
| 1 | Player | Create game | _The Player attempts to create and host a new game._ |
| 1 | Player | Join game | _The Player attemts to join an existing game._ |
| 1 | Map builder | Map - Radom generated | _As a new game is being created a new map will be generated. In this case a random generated map will be created._ |
| 1 | Map builder | Map | _As a new game is being created a new map will be generated. In this case a map generated using the Twitter API will be created._ |
| 1 | Player | Move | _The Player has changed position within the map and become eligable for a random encounter._ |
| 1 | Player | Encounter | _The Player has triggered an encountered which will present itself as one of its three derivations, Item, NPC, Player._ |
| 1 | - | Item | _Encounter type Item. When an item is encountered it is automaticly added to the players inventory until the player explicitly drops the item._ |
| 1 | Player | Examine item | _The Player examines an item from their inventory and is presented with a short description of said item._ 
| 1 | Player | Use item | _The Player uses an item from their inventory._ |
| 1 | Player | Combine items | _The Player attempts to combines two items from their inventory._ |
| 1 | Player | Drop items | _The Player drops an item from their inventory._ |
| 1 | - | NPC | _Encounter type NPC. When an NPC is encountered the player may choose how to interact with said NPC._ |
| 1 | Player | NPC | _._ |

| 1 | Player | Fight NPC | _The Player has encountered an npc and chosen to do battle._ |
| 2 | Player | Ignore encounter | _The Player has encountered an item,npc or another player but chosen to ignore said encounter._ |

| 5 | Player | Trade with Player | _The Player has encountered another Player and requested a trade of items._ |
