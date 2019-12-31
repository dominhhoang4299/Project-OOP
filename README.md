# Project-OOP
Project OOP - HK 1
## Milestone 1 (master branch) - Completed On: Monday, October 29th, 2019
Implement a text-based version of the popular Plants vs Zombies (PvZ) game.
# Implementations
# PLANT - 
## Plants have two subclasses: PassivePlant and ShooterPlant

# Sunflower; subclass of PassivePlant

    *Generates 50 sun every four turns
    *Cost = 50 sun
    *Hit Threshold = 5 damage.
    *Peashooter; subclass of ShooterPlant

# Shoots peas at incoming Zombies
    *Cost = 100 sun
    *Pea Damage = 2 damage per turn
    *Hit Threshold = 10.
    *ZOMBIES - Ryan Tordesillas
    *Zombies have one subclass so far; BasicZombie

# BasicZombie:

    *Speed = Basic Zombie Speed (0.5 tiles per turn/1 tile every two turns)
    *Zombie Damage = Basic Zombie Damage (1 damage per turn)
    *Hit Threshold = Basic Zombie Hit Threshold (10).
 
##### LAWN:
  - Keeps track of it's respective plants, zombies and it's lawnmower
  - Has a plants arrayList, zombie arrayList, lawnMower boolean
#### UML/Sequence Diagrams - MINH HOANG
##### UML 
![alt text](https://github.com/dominhhoang4299/Diagrams/blob/master/UML-Class-M1.PNG) 

##### Sequence Diagram - Plant Class
![alt text](https://github.com/dominhhoang4299/Diagrams/blob/master/PlantClass.PNG) 

##### Sequence Diagram - Zombie Class
![alt text](https://github.com/dominhhoang4299/Diagrams/blob/master/ZombieClass.PNG) 
