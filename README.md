# Scotty-Man 🐾

A Pac-Man-inspired Python game built as my Carnegie Mellon 15-112 term project. Guide Scotty through a randomly generated maze, collect dog bones and a tennis-ball bonus, and avoid the bagpipe enemy.

## Technical highlights

- **Randomized depth-first search:** recursive backtracking builds an 8 × 8 maze, represented as an adjacency dictionary of connected cells.
- **Breadth-first search:** the enemy searches a separate grid graph to pursue the player. Its graph is distinct from the maze's wall layout.
- **Event-driven gameplay:** CMU Graphics callbacks handle keyboard input, rendering, scoring, and enemy movement.
- **Object-oriented structure:** separate classes represent the player, maze, collectibles, and enemy.

## Controls

| Input | Action |
| --- | --- |
| Click Scotty on the start screen | Start |
| Arrow keys | Move through open passages |
| `r` | Restart with a new maze |

## Source and setup

The original implementation is in [`ecodyTP`](ecodyTP), an extensionless Python source file. It currently begins with repository-initialization shell commands; those lines must be removed before running it as Python.

The project uses **Python, CMU Graphics, and Pillow**. See the [CMU Graphics desktop setup](https://academy.cs.cmu.edu/desktop).

The following images are referenced by the code but are **not included in this repository**:

- `scootyAnimate.png`
- `transparentBall.png`
- `dogBone.png`
- `bagpipes.png`

To run a local copy, restore those assets beside the source, remove the opening shell commands, and save the Python portion as `scotty_man.py`. From that folder:

```sh
python -m pip install cmu-graphics Pillow
python scotty_man.py
```

**Status:** original course-project snapshot; a clean installation and gameplay session have not yet been revalidated. The current repository is not a complete, ready-to-run distribution.

## What this project explores

Connecting graph algorithms to an interactive application: turning a maze into connected cells, translating between screen and grid coordinates, and coordinating player input with a moving enemy.

## Credits

Created by Emilia (Mia) Cody for CMU 15-112. The original source includes references for maze generation, BFS, and external images. Those citations remain in the code; third-party artwork is not claimed as original work.
