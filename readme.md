# Slavs as Traders  

This repository contains an implementation of the game Slavs as Traders in the Game Description Language (GDL), developed as part of my Bachelor's thesis.  


## About the Game  

*Slavs as Traders* is a strategic board game.  
Players move across a map of castles and roads, complete missions, collect goods, and earn points.  
The goal is to outscore the opponent through successful mission completion and tactical movement.  


During development, two versions of the rules were created:  

- **With `fromToDistance`** – uses precomputed facts about distances between nodes on the map.  
  - Faster evaluation, but less flexible if the map changes.  
- **Without `fromToDistance`** – distances are computed dynamically using recursive rules.  
  - More flexible and easier to maintain, but slower to evaluate on larger maps.  


### System Requirements  

- **Java 8** (Update 251, 64-bit)  
- **Java SE Development Kit 8** (Update 111, 64-bit)  


### Downloading GGP Base 

First, download and extract the [GGP Base project](https://github.com/ggp-org/ggp-base) from GitHub.  
Navigate into the extracted folder `ggp-base-master`.  


### Adding the Game File  

1. Copy the `.kif` file of the specific version of the game you want to test (e.g., `classicMapFromToDistance.kif`) into the folder: ggp-base-master\games
2. Add a simple METADATA file (JSON) alongside your `.kif` file, for example:  
{
  "gameName": "SlavsAsTraders",
  "rulesheet": "classicMapFromToDistance.kif"
}


### Example Commands  

*(On Windows, use `gradlew.bat` instead of `./gradlew`)*  

Check Gradle version and compile the project:  
```bash
./gradlew -v
./gradlew assemble
```

In one terminal, start the player application (you can assign a specific port to each player):
```bash
./gradlew player
```

In another terminal, start the server application:
```bash
./gradlew server
```

After launching the server, select the local repository and choose the game you want to test.
Add players and click Start New Match to begin the simulation.


### Defense Presentation  

This repository also includes the presentation used for the defense of my thesis:  
📄 [Presentation](presentation.pdf)

It summarizes the goals, implementation, results, and further development possibilities of the project.  


### Thesis Text  

The full text of my Bachelor's thesis is included in this repository:  
📄 [Bachelor's Thesis](thesis.pdf)
