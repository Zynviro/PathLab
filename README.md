# Pathfinding Visualizer
https://zynviro.github.io/PathLab/

A lightweight browser-based pathfinding playground for exploring shortest-path algorithms, generating mazes, and tuning weighted grids in real time.

[![JavaScript](https://img.shields.io/badge/JavaScript-ES6%2B-ffd43b?logo=javascript&logoColor=black)](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
[![Node.js](https://img.shields.io/badge/Node.js-Express-339933?logo=node.js&logoColor=white)](https://nodejs.org/)
[![License: ISC](https://img.shields.io/badge/License-ISC-blue.svg)](https://opensource.org/licenses/ISC)

## Why this exists

Most pathfinding tutorials stop at pseudocode. This project makes the algorithms visible: you can watch how BFS, DFS, Dijkstra, and A* explore a grid, add walls and weights, and compare the resulting path in a live board.

It is especially useful for learners, interview prep, and anyone who wants a concrete, visual understanding of graph traversal and shortest-path heuristics.

## Features

- Interactive grid editor with draggable start node, target node, and optional bomb/object node
- Multiple pathfinding algorithms, including BFS, DFS, Dijkstra, A*, Greedy Best-First, and Bidirectional Swarm
- Visualized exploration and shortest-path highlighting to make algorithm behavior easy to compare
- Maze and pattern generation modes, including recursive division and stair/weight-based layouts
- Weighted cells to simulate higher-cost terrain and explore algorithm behavior under non-uniform costs
- Speed controls for stepping through animation at fast, average, and slow rates
- Clear board, clear walls, clear weights, and clear path actions for quick experimentation

## Screenshot / Demo Placeholder



https://github.com/user-attachments/assets/d59c0a5d-b112-4bfe-98e2-69e8f3c5f3cf



## Installation

This project is a small Node.js + Express app.

1. Open a terminal in the project root.
2. Install dependencies:

```bash
npm install
```

3. Start the server:

```bash
node server.js
```

4. Open the app in a browser:

```text
http://localhost:1337
```

> The repo includes an `npm start` script, but it currently points to `nodemon server.js` and `nodemon` is not declared in this project’s dependencies. The reliable startup command in the checked-in code is `node server.js`.

## Usage

Once the server is running, the app loads a grid-based board and exposes the algorithm controls from the navigation bar.

Typical flow:

```bash
cd "Path finder"
npm install
node server.js
```

Then in the browser:

1. Pick an algorithm from the Algorithms menu
2. Draw walls or weights directly on the grid
3. Add a bomb/object node if needed
4. Click Visualize!
5. Adjust speed or regenerate mazes from the Maze & Patterns menu

## Configuration

No `.env` file or environment-variable configuration is defined anywhere in this repository. The app’s behavior is driven by the browser UI and in-memory board state.

| Runtime option | Values observed in code | Purpose |
| --- | --- | --- |
| `currentAlgorithm` | `dijkstra`, `astar`, `CLA`, `greedy`, `bfs`, `dfs`, `bidirectional` | Selects the active pathfinding method |
| `speed` | `fast`, `average`, `slow` | Controls animation pacing |
| Maze generation type | `wall`, `weight`, recursive division variants, stair pattern | Generates obstacles or weighted terrain |
| Object node | `object`/bomb toggle | Adds a secondary target for object-aware pathfinding |

## Tech Stack

- JavaScript (browser logic and DOM manipulation)
- Node.js
- Express 4.14.0
- HTML + CSS
- Bootstrap 3.3.7 for the UI shell
- jQuery 3.1.1 loaded from a CDN
- Custom pathfinding and maze generation logic in the browser modules under `public/browser/`

The project does not appear to use a modern framework or a separate backend service; it serves static frontend assets and handles the logic client-side.

## Contributing

Contributions are welcome.

This repository does not currently include a `CONTRIBUTING.md` file, so the default GitHub pull request workflow applies. Please open an issue or fork the project and submit a pull request with a clear explanation of the change.

## License

The project metadata declares the license as `ISC` in `package.json`, but no `LICENSE` file was found in the workspace.

If you plan to distribute or publish this project, add an ISC license file before release so the legal terms are explicit.

## Contact / Socials

No contact or social links were found in this repository. Add your preferred links here when available.

---

Project information is based on the checked-in code in this workspace, including `server.js`, `index.html`, and the browser logic under `public/browser/`.
