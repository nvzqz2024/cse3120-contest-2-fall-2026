# cse3120-contest-2-fall-2026
Contest 2 repository for CSE3120, fall 2026 semester. Expansion of Contest 1 project "Terminal Tomb" with new and enhanced features.

### Instructions:
Open the Visual Studio Developer command prompt\
Navigate to the downloaded directory\
run the compilation script `compile.bat`\
If successful, run `TerminalTombPlus.exe`

-----
# Terminal Tomb+
**Elevator Pitch:** "Terminal Tomb" is top-down, grid-based dungeon-crawling microgame that runs and displays entirely within your terminal. You are a hero trapped inside a tomb with zombies, traps, and gold distributed throughout. Your goal is to reach the exit space without dying, collecting gold along the way for extra score.\
**Original State (Terminal Tomb - Contest 1 Version):** Upon running the program, a grid is displayed in your terminal, rendered with standard ASCII characters. Your health and gold value is displayed underneath the grid. Your goal is to move player 'P' to the exit 'E' without running out of health by touching too many zombies 'Z' or traps 'T'. You can move in any of the four cardinal directions, unless a wall is blocking your way. You can collect gold 'G' to increase score by 1.\
**Implementation Details:** Written in MASM

### Planned Improvements
- [ ] Restructure into multiple files. Allows for changing small details such as grid layout without touching the main game loop file.
- [ ] Replace monochrome ASCII art with multicolor to improve readability.
- [ ] Upon launch, show a visually interesting splash screen. Press a key to begin. This does not need to be colored.
- [ ] Add a collection of grid layouts for the game to choose from, such as from a `grids.ini` file. This improves replayability.
- [ ] Upon play, load a random grid layout from grid layout file.
- [ ] Make zombies wander to differentiate them more from traps

### Stretch Goals (If time permits)
- [ ] "Layer" system. The first grid does not have an exit, but a "doorway" that takes you to another grid ("Upper Layer"). Grid layer X will have the exit.
- [ ] Either "Food" or "Potions" can be found that restore health points.
- [ ] You can store _One_ item (food/potion) for later use. Press `E` to use stored item.
- [ ] Save highest gold collected as high score.

**Lower Priority:**
- [ ] Shovel tool. Wall may be made of "Soft Dirt" that can be dug up.
      Spend one move to dig the dirt and create a walkable cell.
      _**Requires**_ zombie movement implemented to be an interesting mechanic. Trade off: Zombies get closer, but you open a walkway.
- [ ] Weapon system. Use arrow keys to attack the adjacent cell in the selected direction.

```
#####..........______.........#####
#####.........|......|........#####
#####.........|.0..0.|-(Grr!).#####
#####..........VVVVVV.........#####
#####..........__||__.........#####
#####........./|....|\........#####
#####......../.|____|.\.......#####
#####..........L....L.........#####
#####.........................#####
```
