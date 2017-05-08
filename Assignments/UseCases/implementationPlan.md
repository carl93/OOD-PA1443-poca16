# Implementation Plan for System _TwitterNetHack_
1. Title Page
    1. Title: Implementation Plan
    1. Sub-title: "Assignment in the course PA1443 Introduction to Software Design and Architecture"
    1. 2017-04-23
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

1. Implementation Plan
    1. Motivation
    I have priortised the use cases in such an order that a viable product can be reached early in the development process. When the system has reached this stage one can begin expanding base functionality with more complex interactions and implementing external services such as the Twitter API.
    1. Iterations

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
| 0.1 | Ignore Encounter |

First iteration. The included uses cases are the minimum required for the system to be considered a viable product. A player will be able to navigate a generated map and preform basic interactions with items and npcs. Complex encounter interactions and functionality realted to external services are being left out for the moment. __Weight total: 2.0__

| Weight | Use Case |
| --- |:------------:|
| 0.5 | Generate map(Twitter API). |
| 0.3 | Join game |
| 0.3 | Get existing map|
| 0.5 | Encounter, Player |
| 0.3 | Chat with Player |

Second iteration. Through this iteration the system will be expanded to support basic multiplayer gameplay and maps generated using the Twitter API. __Weight total: 1.9__

| Weight | Use Case |
| --- |:------------:|
| 0.1 | Examine item |
| 0.3 | Combine item |
| 0.3 | Debate NPC |
| 0.5 | Challenge NPC|
| 0.3 | Trade with Player |
| 0.3 | Use item on Player |
| 0.1 | Player setup |

Third iteration. This final iteration will add complex features to encounters and add player costumization. __Weight total: 1.9__

