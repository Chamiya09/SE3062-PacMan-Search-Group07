<div align="center">

# 🟡 Pac-Man Search Algorithms

### IT3012 · Artificial Intelligence · Group 07

**Intelligent pathfinding, heuristic search, and maze optimization using the UC Berkeley Pac-Man framework.**

![Python](https://img.shields.io/badge/Python-3.x-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Project](https://img.shields.io/badge/Project-Pac--Man_Search-F7DF1E?style=for-the-badge)
![Module](https://img.shields.io/badge/Module-IT3012-7C3AED?style=for-the-badge)
![Group](https://img.shields.io/badge/Group-07-22C55E?style=for-the-badge)

</div>

---

## 📖 Overview

This group project implements and evaluates classic **Artificial Intelligence search algorithms** in the **UC Berkeley Pac-Man Search** environment. Pac-Man agents navigate mazes, find paths, visit all four corners, and collect food using uninformed and informed search strategies.

Our work emphasizes:

- Correct search behavior and path costs
- Efficient state exploration
- Admissible and consistent heuristic design
- Optimized food search with maze distances, minimum spanning trees (MST), and caching
- Collaborative development through Git branches and pull requests

## 🎯 Project Objectives

1. Implement DFS, BFS, UCS, and A* search.
2. Model the four-corners problem as a search problem.
3. Design and evaluate heuristics for corners and food collection.
4. Reduce expanded search nodes without sacrificing correctness.
5. Validate implementations using the provided autograder and Pac-Man game.

## 🧠 Questions and Implementations

| Question | Topic | Implementation / Approach | Current Status |
|:--:|---|---|:--:|
| Q1 | Depth-First Search (DFS) | Stack-based graph search | ✅ Passed |
| Q2 | Breadth-First Search (BFS) | Queue-based graph search | ✅ Passed |
| Q3 | Uniform Cost Search (UCS) | Lowest accumulated path cost first | ✅ Passed |
| Q4 | A* Search | Priority based on `f(n) = g(n) + h(n)` | ✅ Passed |
| Q5 | Corners Problem | State representation and goal checking for four corners | ✅ Passed |
| Q6 | Corners Heuristic | Informed search for the corners problem | ✅ Passed |
| Q7 | Food Heuristic | Maze distance + MST + caching | ✅ Passed |
| Q8 | Closest Dot Search | Pathfinding to remaining food dots | ✅ Passed |

> **Status note:** Q8 was not implemented in the latest shared test run. Update this row after the Q8 work is merged and verified.

## ✨ Highlights

- **Four search strategies:** DFS, BFS, UCS, and A*.
- **Corners search:** A search problem and heuristic for visiting every corner.
- **Optimized food search:** A* uses a maze-aware heuristic instead of relying only on Manhattan distance.
- **Memoization:** Cached shortest maze distances and MST estimates avoid redundant computations.
- **Automated validation:** The supplied autograder checks correctness and heuristic properties.
- **Collaborative workflow:** Individual task branches are integrated through the `dev` branch.

## 🧰 Technology Stack

| Tool | Purpose |
|---|---|
| Python 3 | Search algorithm and agent implementation |
| UC Berkeley Pac-Man | Educational game and search framework |
| Git | Version control |
| GitHub | Collaboration and pull requests |
| Visual Studio Code | Development environment |

## 📁 Repository Structure

The following is a **reference layout for the standard Pac-Man Search project**, not a verified listing of every file in this repository. The project files explicitly observed in the work and test logs include `search.py`, `searchAgents.py`, `pacman.py`, `autograder.py`, and `test_cases/`. Check the actual repository before treating the complete tree as exact.

```text
Pac-Man-Search-Group07/
├── search.py             # DFS, BFS, UCS and A* implementations
├── searchAgents.py       # Search agents, problems and heuristics
├── pacman.py             # Pac-Man game entry point
├── autograder.py         # Automated assessment runner
├── game.py               # Game engine (standard framework)
├── util.py               # Shared data structures (standard framework)
├── layout.py             # Layout utilities (standard framework)
├── layouts/              # Maze layouts (standard framework)
├── test_cases/           # Autograder test cases
└── README.md             # Project documentation
```

**Key files:**

- `search.py`: Core search algorithm implementations.
- `searchAgents.py`: Problem definitions, A* agents, corners heuristic, and food heuristic.
- `pacman.py`: Launches the game and selected search agents.
- `autograder.py`: Runs the provided test suite.

To generate an **exact** folder tree from the repository root on Windows:

```powershell
tree /F /A > structure.txt
```

Replace the reference tree above with the relevant entries from `structure.txt` before final submission.

## 🚀 Getting Started

### Prerequisites

- Python 3 installed and accessible from the terminal
- Git installed (to clone the repository)
- Project files downloaded or cloned locally

### 1. Clone the repository

```bash
git clone <YOUR_REPOSITORY_URL>
cd <YOUR_REPOSITORY_DIRECTORY>
```

Replace the placeholders with the actual repository URL and cloned folder name.

### 2. Check Python

```bash
python --version
```

### 3. Launch Pac-Man

```bash
python pacman.py
```

### 4. Run all autograder tests

```bash
python autograder.py
```

### 5. Test a specific question

```bash
python autograder.py -q q4
python autograder.py -q q7
```

> Depending on the autograder's dependencies, testing Q7 may also execute Q4 tests.

## 🎮 Run Search Agents

Run these commands from the project root.

**DFS**

```bash
python pacman.py -l mediumMaze -p SearchAgent -a fn=dfs
```

**BFS**

```bash
python pacman.py -l mediumMaze -p SearchAgent -a fn=bfs
```

**UCS**

```bash
python pacman.py -l mediumMaze -p SearchAgent -a fn=ucs
```

**A* with Manhattan heuristic**

```bash
python pacman.py -l mediumMaze -p SearchAgent -a fn=astar,heuristic=manhattanHeuristic
```

**A* Corners**

```bash
python pacman.py -l mediumCorners -p AStarCornersAgent
```

**A* Food Search**

```bash
python pacman.py -l trickySearch -p AStarFoodSearchAgent
```

## 🧪 Autograder Results

The following results are from the **latest full autograder output shared by the team (10 October 2026)**, before Q8 completion.

| Question | Score | Status |
|:--:|:--:|:--:|
| Q1 — DFS | 3/3 | ✅ PASS |
| Q2 — BFS | 3/3 | ✅ PASS |
| Q3 — UCS | 3/3 | ✅ PASS |
| Q4 — A* | 3/3 | ✅ PASS |
| Q5 — Corners Problem | 3/3 | ✅ PASS |
| Q6 — Corners Heuristic | 3/3 | ✅ PASS |
| Q7 — Food Heuristic | 5/4 | ✅ PASS |
| Q8 — Closest Dot | 3/3 | ✅ PASS |
| **Total** | **23/25** | **Provisional** |

> The local autograder reports **5/4 for Q7**, including its performance-based grading behavior. This is a provisional local score, not a guarantee of final instructor-assigned marks.

### Search Performance

These measurements come from the recorded test runs. The tasks use different maze layouts and objectives, so node counts are **not a controlled head-to-head benchmark**.

| Algorithm / Task | Layout | Nodes Expanded | Additional Result |
|---|---|---:|---|
| DFS | `mediumMaze` | 146 | Solution length: 130 |
| BFS | `mediumMaze` | 269 | Solution length: 68 |
| UCS | `mediumMaze` | 269 | Solution length: 68 |
| A* (Manhattan) | `mediumMaze` | 221 | Solution length: 68 |
| A* Corners | `mediumCorners` | 741 | Heuristic test passed |
| A* Food | `trickySearch` | **255** | Path cost: **60** |

### Pac-Man Food Search Run

```text
Command: python pacman.py -l trickySearch -p AStarFoodSearchAgent

Path found with total cost of 60 in 0.3 seconds
Search nodes expanded: 255
Pacman emerges victorious! Score: 570
Win Rate: 1/1 (1.00)
```

This is the observed result of **one local run**, not an average across multiple benchmark runs.

## 🌳 Food Heuristic Optimization (Q7)

The initial food heuristic used Manhattan distance to the farthest remaining food dot. The optimized implementation uses actual shortest maze distances, taking walls into account.

The heuristic is:

```text
h(state) = distance_to_nearest_remaining_food + MST_cost(remaining_food)
```

**How it works:**

1. **Maze-aware shortest paths:** Breadth-first search measures shortest walkable distances around walls.
2. **Nearest-food estimate:** Finds the shortest maze distance from Pac-Man to any remaining food dot.
3. **Minimum Spanning Tree:** Estimates the cost of connecting all remaining food positions.
4. **Caching:** Stores computed pairwise maze distances and MST values for reuse.
5. **A* evaluation:** Uses the heuristic alongside accumulated path cost to prioritize promising states.

The implementation passed the supplied Q7 heuristic tests and expanded **255 nodes** on `trickySearch`, below the most demanding listed expansion threshold of **7,000 nodes**.

## 👥 Team Contributions

The task allocation below reflects the team's documented work. Student IDs are taken from the actual GitHub branch names.

| Member | Student ID | Contributions |
|---|---|---|
| Member 1 | `IT24102128` | Q1 — DFS; Q5 — Corners Problem |
| Member 2 | `IT24102160` | Q2 — BFS; Q6 — Corners Heuristic |
| Member 3 | `IT24101666` | Q3 — UCS; Q7 — Food Heuristic (Part A) |
| Member 4 | `IT24100710` | Q4 — A*; Q7 — Food Heuristic Optimization (Part B) |

> Q7 “Part A” and “Part B” describe the team's internal task split, not separate official assignment questions. Update Q8 ownership after the team finalizes it.

## 🌿 Git Branching Strategy

The GitHub branch selector screenshot confirms **`dev` is the default branch**, with `main` and the following task branches:

```text
Repository
├── dev                         ← Default / integration branch
├── main
├── IT24102128---Q1             ← Member 1: DFS
├── IT24102128---Q5             ← Member 1: Corners Problem
├── IT24102160---Q2             ← Member 2: BFS
├── IT24102160---Q6             ← Member 2: Corners Heuristic
├── IT24101666---Q3             ← Member 3: UCS
├── IT24101666---Q7-Part-A      ← Member 3: Initial food heuristic
├── IT24100710---Q4             ← Member 4: A*
└── IT24100710---Q7-Part-B      ← Member 4: Food heuristic optimization
```

**Collaboration workflow:**

1. Each team member develops their assigned question in a dedicated branch.
2. Changes are committed and pushed to GitHub.
3. A pull request is opened targeting `dev`.
4. Changes are reviewed and merged into `dev`.
5. The integrated code is tested with `python autograder.py`.
6. Final submission follows the lecturer's repository and branch instructions.

> The diagram lists branches visible in the screenshot; it does not claim that every branch is currently unmerged or that `main` has been synchronized with `dev`.


## 📚 Acknowledgements

This project is based on the **UC Berkeley Pac-Man AI educational framework**. We acknowledge the original framework authors and course materials. The team developed the assigned search implementations and heuristics for the IT3012 group assignment.

## ⚖️ Academic Integrity

The UC Berkeley Pac-Man educational materials may contain restrictions on publishing completed solutions. Keep the repository private or otherwise follow the framework's licensing terms and your institution's academic integrity and submission policies. Do not publicly distribute solution code unless permitted.

---

<div align="center">

**IT3012 · Pac-Man Search Algorithms · Group 07**

*Search smarter. Explore fewer nodes.* 🟡

</div>
