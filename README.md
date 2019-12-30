# Project-OOP
Project OOP - HK 1
## Milestone 1 (master branch) - Completed On: Monday, October 29th, 2019
* Implement a text-based version of the popular Plants vs Zombies (PvZ) game.

### Implementations

#### PLANT - 
* Plants have two subclasses: PassivePlant and ShooterPlant

* Sunflower; subclass of PassivePlant
  - Generates 50 sun every four turns
  - Cost = 50 sun
  - Hit Threshold = 5 damage.

* Peashooter; subclass of ShooterPlant
  - Shoots peas at incoming Zombies
  - Cost = 100 sun
  - Pea Damage = 2 damage per turn
  - Hit Threshold = 10.

#### ZOMBIES - 
* Zombies have one subclass so far; BasicZombie

* BasicZombie:
  - Speed = Basic Zombie Speed (0.5 tiles per turn/1 tile every two turns)
  - Zombie Damage = Basic Zombie Damage (1 damage per turn)
  - Hit Threshold = Basic Zombie Hit Threshold (10).

#### GAME RUNNABLE - 
##### LEVEL:
* Keeps track of the current game state, the states of the five lawns and advances to next states:
   - Keeps track of waveCount, number of zombies remaining in wave, int[5] lawns
   - Each state advances to the next due to player command and plant and zombie behavior 
    
* The central logic component, tells plants and zombies what to do:
   - Peashooters will attack zombies in their lawn every turn, only damages the zombie closest to them (in front of them)
   - Tells Sunflowers to generate sun every turn, but a sunflower keeps track of when it actually produces sun
   - Zombies will walk left until they encounter a plant; they will stop and proceed attacking until the plant is dead
   - When a zombie reaches the end of the lawn, the lawn mower is triggered and clears that lawn of all zombies

* Adds plants and zombies to the level (adding plants dependent on the Player class), zombies are spawned in waves
   - Plants are placed when suitable by the Player who buys them with sun, also can be removed by the player
   - Zombies are spawned in waves that are set when a level is constructed
      -> An arrayList<Integer> is passed in as a parameter -> each element in the arrayList<Integer> is the number of zombies spawned *          each wave
* Determines if the player wins or loses
   - If a zombie reaches the end tile of a lawn and the lawn mower has already been activated, player loses
   - If a player manages to kill all the zombies in the level, player wins

##### LAWN:
  - Keeps track of it's respective plants, zombies and it's lawnmower
  - Has a plants arrayList, zombie arrayList, lawnMower boolean

###### PLAYER: 
  - Responsible for all user input via commands user enters in
  - Keeps track of the player's sun count

##### COMMAND LIST:
  - place plantType x y  ->     Places a plant of plantType at tile (x, y)
  - remove x y           ->     Removes plant at tile (x, y)
  - help                 ->     Prints the command list
  - types                ->     Prints the plant types and their costs
  - skip/ENTER           ->     Skips the turn; ie. player cannot place any plants due to lack of sun
