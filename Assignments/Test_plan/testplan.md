#  System Test Plan for _TwitterNetHack_
1. Title Page
    1. Title:  System Test Plan for _TwitterNetHack_
    1. Sub-title: "Assignment in the course PA1443 Introduction to Software Design and Architecture"
    1. 2017-05-16
    1. Authors and Author Contribution

| Author Name   | Social Security Number| Thinking  |Writing  |
| ------------- |:-------------:| -----:|-----:|
| Pontus Carlsson  | 9308181636 | 100% |100% |

2. System Description

A version of the game 'NetHack' featuring multiplayer gameplay and a modernized navigation system. The game focuses on exploration and will incoporate Twitter to mutate the games stage generation process based on the content of tweets resulting in a constantly changing and  dynamic experience.

3. Test Strategy

As this document only cover the first iteration of a relatively small system no automated testing will be performed.
Given the compact scope of the system and how limited the user's inputs are at least in the systems first iteration manual testing becomes manageable and  tests can be written to cover the system as a whole without coming across as unwieldy.
The developers will manually perform a set of tests covering the features of the systems first iteration. The result of each test will be evaluated against its expected outcome and deemed as a pass of a fail. If a test is a fail a retest will be performed after alteration to the code has been made.

The test process can be visualized as such.
![Test process model][tfd-model]

[tfd-model]: http://www.agiledata.org/images/tddSteps.jpg "Test Process Model"

4. System tests

##  Move
  ### Preconditions
  * Create game
  ### Allowed Input
  * Direction
  ### Expected output
  * Alert the player of his present location.
  * Alert the player that he has attemted an invalid move.
  
| Senario | Test step | Expected outcome | Actual outcome |
|---------|:---------:|:----------------:|:--------------:|
| Verify that player location updates accodingly after a valid move. | Attempt a valid move. | The player's location has updated and he is alerted to his present location. | ... |
| Verify that player location remains unchanged after an invalid move. | Attempt an invalid move. | The player's location is unchanged and he is alerted that the attempted move was invalid. | ... |

 ##  Ignore encounter
  ### Preconditions
  * Encounter
  ### Allowed Input
  * None
  ### Expected output
  * Alert the player that the encounter has been ignored.
  
| Senario | Test step | Expected outcome | Actual outcome |
|---------|:---------:|:----------------:|:--------------:|
|Attemp to ignore encounter| Initiate ignore option when available | Enocunter is ignored and the player is free to initiate a new move. | ... |

  ##  Encounter, item
  ### Preconditions
  * Move
  ### Allowed Input
  * Drop item
  * Ignore encounter
  ### Expected output
  * Alert the player of encounter.
  * Alert the player that his inventory is full.
  * Request that the player drops an item.
  * The name of the item.
  * Alert the player that the new item has been added to his inventory.

| Senario | Test step | Expected outcome | Actual outcome |
|---------|:---------:|:----------------:|:--------------:|
| Verify that an item is picked up when there is room in the players inventory. |  Move until an item encounter is triggered. | The new item is presented and added to the players inventory. | ... |
| Verify that the player is prompted to drop an item if there is no room in his inventory. |  (While player inventory is full)Move until an item encounter is triggered. | The player is promted to drop an item. | ... |
| Verify that the player can choose to ignore the encounter when prompted to drop an item. |  When prompted to drop an item, choose to ignore encounter. | The new item was not picked up and the player is free to initiate a new move. | ... |

  ##  Drop item
  ### Preconditions
  * Encounter, item
  ### Allowed Input
  * Item name
  ### Expected output
  * Alert the player of successful item drop.
  * Alert the player when input does not match an item in the players inventory.
  
| Senario | Test step | Expected outcome | Actual outcome |
|---------|:---------:|:----------------:|:--------------:|
| Verify that an item is removed from the players inventory when dropped. |  Attempt item drop. | The  item is successfully dropped. | ... |
| Verify that the player is alerted when attempting to remove an item not in his inventory. |  Attempt item drop of item not in player inventory. | Player is alerted of the invalid drop. | ... |

##  Encounter, NPC
  ### Preconditions
  * Move
  ### Allowed Input
  * Fight NPC
  * Ignore encounter
  ### Expected output
  * Alert the player of encounter.
  * NPC description.
  * Alert the player that he has initiated a fight.
  
| Senario | Test step | Expected outcome | Actual outcome |
|---------|:---------:|:----------------:|:--------------:|
| Verify that an NPC can be encountered. |  Move until an NPC encounter is triggered. | The  Player is presented with a valid NPC description and the option to fight or ignore the NPC. | ... |
| Verify that the player can initiate a fight with an NPC |  Choose to fight when NPC is encountered. | Player is alerted that a fight has been initiated. | ... |
| Verify that the player can choose to ignore an NPC encounter. |  Choose to ignore when NPC is encountered. | Player is alerted that the NPC has been ignored and is free to initiate a new move. | ... |

##  Fight NPC
  ### Preconditions
  * Encounter, NPC
  ### Allowed Input
  * None
  ### Expected output
  * Alert the player of victory.
  * Present reward.
  * Alert the player of defeat.
  * Present penalty.
  
| Senario | Test step | Expected outcome | Actual outcome |
|---------|:---------:|:----------------:|:--------------:|
| Verify win senario. | Initiate fight with an NPC that has __lower__ stats than the player. | Player is victorious and a reward is presented and handled accordingly | ... |
| Verify fail senario. | Initiate fight with an NPC that has __higher__ stats than the player. | Player is defeated and a penalty is presented and handled accordingly | ... |

##  Use item
  ### Preconditions
  * Create game
  ### Allowed Input
  * Item name
  ### Expected output
  * Alert the player that the item has been used.
  * Alert the player that the item name does not match an item in his inventory.
  * Alert the player that he does not meet the requirments of the item he attempted to use.
  
| Senario | Test step | Expected outcome | Actual outcome |
|---------|:---------:|:----------------:|:--------------:|
| Verify output when player attempt to use an item not in his inventory. | Use an item not in the players inventory. | Player is alerted that the item does not match an item in his inventory. | ... |
| Verify output when player attempt to use an item of unmet requirements. | Use an item of unmet requirements. | Player is alerted that the item cannot be used due to unmet requirements. | ... |
| Verify that player stats are updated accordingly when an item is used. | Use an item. | Player is alerted that an item has been used and his stats are updated accordingly. | ... |

##  Show inventory
  ### Preconditions
  * Create game
  ### Allowed Input
  * Show inventory
  ### Expected output
  * Present the contents of the players inventory.
  
| Senario | Test step | Expected outcome | Actual outcome |
|---------|:---------:|:----------------:|:--------------:|
| Verify that output corresponds with the items in the players inventory. | Initiate event Show inventory. | All items presently in the players inventory are presented. | ... |
| Verify that output is properly updated after an item has been dropped. | Initiate event Show inventory after an item has been dropped. | All items presently in the players inventory are presented. | ... |
