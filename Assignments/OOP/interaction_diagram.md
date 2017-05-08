# Interaction Diagram for System _TwitterNetHack_
1. Title Page
    1. Title: Interaction Diagram (Iteration 1)
    1. Sub-title: "Assignment in the course PA1443 Introduction to Software Design and Architecture"
    1. 2017-05-07
    1. Authors and Author Contribution

| Author Name   | Social Security Number| Thinking  |Writing  |
| ------------- |:-------------:| -----:|-----:|
| Pontus Carlsson  | 9308181636 | 100% |100% |

1. System Description
A version of the game 'NetHack' featuring multiplayer gameplay and a modernized navigation system. The game focuses on exploration and will incoporate Twitter to mutate the games stage generation process based on the content of tweets resulting in a constantly changing and  dynamic experience.

1. Prioritised List of Use Cases
    1. Motivation for Priorities
    
    The uses casese are prioritised by system essentiality. 
    
    1. Use Cases
    
| Weight | Use Case |
| --- |:------------:|
| 0.1 | Create game |
| 0.5 | Generate Map(Map builder) |
| 0.3 | Move |
| 0.1 | Encounter, Item |
| 0.3 | Use item |
| 0.1 | Drop item |
| 0.1 | Show inventory |
| 0.1 | Encounter, NPC |
| 0.3 | Fight NPC |
| 0.1 | Ignore Encounter | <!--END OF FIRST ITTERATION.-->
| 0.3 | Join game |
| 0.3 | Get existing map|
| 0.5 | Encounter, Player |
| 0.3 | Chat with Player | <!--END OF SECOND ITTERATION.-->
| 0.5 | Generate map(Twitter API) | <!--END OF THIRD ITTERATION.-->
| 0.1 | Examine item |
| 0.3 | Combine item |
| 0.3 | Debate NPC |
| 0.5 | Challenge NPC|
| 0.3 | Trade with Player |
| 0.3 | Use item on Player |
| 0.1 | Player setup | <!--END OF FOURTH ITTERATION.-->
1. Estimated Velocity Per Iteration

| MAX | MIN | AVG |
| --- |:----:|----:|
| 1 | 2 | 0.5 |

1. System events
    1. System Events for Use Case Create game
        * newGame()

    1. System Events for Use Case Move
        * move()

    1. System Events for Use Case Encounter, Item
        * move()
        * dropItem()

    1. System Events for Use Case Use item
        * useItem()

    1. System Events for Use Case Drop item
         * dropItem()

    1. System Events for Use Case Show inventory
        * showInventory()

    1. System Events for Use Case Encounter, NPC
        * move()

    1. System Events for Use Case Fight, NPC
        * fight()

    1. System Events for Use Case Ignore Encounter
        * ignoreEncounter()

1. Interaction diagrams
    1. Interaction Diagram for Use Case Create game
        ![model](https://github.com/carl93/OOD-PA1443-poca16/blob/master/Assignments/OOP/ID/newGame().png?raw=true "ID_create")

    1. Interaction Diagram for Use Case Move
        ![model](https://github.com/carl93/OOD-PA1443-poca16/blob/master/Assignments/OOP/ID/move().png "ID_move")
    
    1. Interaction Diagram for Use Case Drop item
        ![model](https://github.com/carl93/OOD-PA1443-poca16/blob/master/Assignments/OOP/ID/dropItem().png "ID_drop")
    
    1. Interaction Diagram for Use Case Use item
        ![model](https://github.com/carl93/OOD-PA1443-poca16/blob/master/Assignments/OOP/ID/useItem().png "ID_use")
    
    1. Interaction Diagram for Use Case Show inventory
        ![model](https://github.com/carl93/OOD-PA1443-poca16/blob/master/Assignments/OOP/ID/showInventory().png "ID_show")
    
    1. Interaction Diagram for Use Case Fight, NPC
        ![model](https://github.com/carl93/OOD-PA1443-poca16/blob/master/Assignments/OOP/ID/fight().png "ID_fight")

    1. Interaction Diagram for Use Case Ignore Encounter
        ![model](https://github.com/carl93/OOD-PA1443-poca16/blob/master/Assignments/OOP/ID/ignoreEncounter().png "ID_ignore")
