<div align="center">

# ✈️ 3D Plane Game

### A simple browser-based 3D obstacle-dodging game

Built with **HTML, CSS, JavaScript, and Three.js**.

<br>

[![JavaScript](https://img.shields.io/badge/JavaScript-ES6+-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
[![Three.js](https://img.shields.io/badge/Three.js-0.125.2-black?style=for-the-badge&logo=threedotjs&logoColor=white)](https://threejs.org/)
[![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/HTML)
[![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/CSS)
[![License](https://img.shields.io/badge/License-Unlicense-blue?style=for-the-badge)](LICENSE)

<br>

**Dodge the obstacles. Survive the tunnel. Beat your score.**

<br>

[🎮 Gameplay](#-gameplay) •
[⌨️ Controls](#️-controls) •
[⚡ Run Locally](#-run-locally) •
[🛠️ Development](#️-development)

</div>

---

# 🎮 Gameplay

**3D Plane Game** is a small browser game where you control a plane
inside a 3D tunnel and dodge randomly positioned obstacles.

The game continuously moves obstacles toward the player while your score
increases over time. Hit an obstacle and the game ends.

The project is intentionally simple and is designed as a lightweight
example of creating a 3D browser game with **Three.js**. citeturn1view1turn3view0

---

# ✨ Features

- ✈️ **3D plane**
- 🌌 **3D tunnel environment**
- 🚧 **Randomly positioned obstacles**
- 🔄 **Continuous obstacle movement**
- 💥 **Collision detection**
- 📈 **Live score**
- 🏆 **Top score during the current session**
- 🔁 **Restart functionality**
- 🎨 **Custom HTML/CSS start and game-over screens**
- ⚡ **WebGL rendering through Three.js**

The game creates 20 obstacles at a time, places them randomly throughout
the tunnel, and recycles them after they pass the camera. citeturn3view0

---

# 📸 Screenshots / GIF

> Add your own gameplay screenshot or GIF here once you have one.

### Gameplay

<p align="center">
  <img src="assets/gameplay.gif" width="800" alt="3D Plane Game gameplay">
</p>

### Start Screen

<p align="center">
  <img src="assets/start-screen.png" width="800" alt="3D Plane Game start screen">
</p>

### Game Over

<p align="center">
  <img src="assets/game-over.png" width="800" alt="3D Plane Game game over screen">
</p>

> If you don't have these images yet, remove the image blocks above.

---

# ⌨️ Controls

| Key | Action |
|:---:|---|
| `W` | Move up |
| `S` | Move down |
| `A` | Move left |
| `D` | Move right |

The plane is constrained within the tunnel's playable area. Pressing
`A` or `D` also tilts the plane while moving, and the plane returns to
level when the key is released. citeturn3view0

---

# 🏁 How to Play

### 1. Start the game

Open the game and press:

```text
START GAME
```

The start screen is hidden and the game begins. citeturn1view1turn3view2

### 2. Dodge obstacles

Use:

```text
W A S D
```

to move the plane around the tunnel.

### 3. Keep flying

Obstacles move toward the player while new positions are randomly
generated after obstacles pass the camera. citeturn3view0

### 4. Avoid collisions

If the plane's bounding box intersects an obstacle's bounding box,
the game ends. citeturn3view0

### 5. Beat your score

Your score continuously increases while the game is running.

The game-over screen displays:

```text
Current Score
Top Score
```

The top score is tracked for the current page session. citeturn3view2

### 6. Play again

Press:

```text
RESTART
```

to reset the game and start another run. citeturn3view2

---

# 🧰 Tech Stack

| Technology | Purpose |
|---|---|
| 🟨 **JavaScript** | Game logic |
| 🎮 **Three.js** | 3D rendering and game objects |
| 🌐 **HTML5** | Page structure |
| 🎨 **CSS3** | UI and game screens |
| 📦 **Node.js / npm** | Local development tooling |
| ⚡ **serve** | Local static-file server |

The page currently loads **Three.js r125 / version 0.125.2** from jsDelivr. citeturn1view1

---

# 🗂️ Project Structure

```text
plane-game/
│
├── 📄 index.html
│   └── Game page and UI screens
│
├── 📄 script.js
│   └── Three.js scene and game logic
│
├── 📄 style.css
│   └── Game UI and button styling
│
├── 📄 package.json
│   └── Local development configuration
│
├── 📄 pnpm-lock.yaml
│   └── pnpm dependency lockfile
│
├── 📄 eslintrc.json
│   └── ESLint configuration
│
├── 🎵 2050 - Frequency.mp3
│   └── Audio asset
│
├── 📄 LICENSE
└── 📄 README.md
```

The repository currently contains the HTML entry point, JavaScript game
logic, CSS, package configuration, lockfile, ESLint configuration,
license, and an MP3 asset. citeturn0view0

---

# ⚡ Run Locally

## 📋 Requirements

You need:

- [Node.js](https://nodejs.org/)
- npm
- A modern web browser

---

## 1. Clone the repository

```bash
git clone https://github.com/jzc9307/plane-game.git
cd plane-game
```

---

## 2. Install dependencies

```bash
npm install
```

The repository's package configuration provides a `start` script using
the `serve` package. citeturn1view0

---

## 3. Start the development server

```bash
npm start
```

This launches the local static server.

Open the local URL shown by the terminal in your browser.

---

# 🌐 Running Without npm

Because the project is a browser-based HTML/CSS/JavaScript application,
you can also serve the repository using another local static HTTP server.

For example:

```bash
npx serve .
```

Then open the local address provided by the terminal.

Using a local server is preferable to opening `index.html` directly because
it provides a proper HTTP environment for the browser application.

---

# 🧠 How It Works

The game is built around a Three.js scene.

```text
                   ┌─────────────────┐
                   │    index.html   │
                   │   Game UI       │
                   └────────┬────────┘
                            │
                            ▼
                   ┌─────────────────┐
                   │    script.js    │
                   │   Game Logic    │
                   └────────┬────────┘
                            │
                 ┌──────────┼──────────┐
                 ▼          ▼          ▼
            ┌────────┐ ┌────────┐ ┌──────────┐
            │ Plane  │ │Tunnel  │ │Obstacles │
            └────────┘ └────────┘ └──────────┘
                 │          │          │
                 └──────────┼──────────┘
                            ▼
                    ┌──────────────┐
                    │ Three.js     │
                    │ WebGL Render │
                    └──────────────┘
```

---

# ✈️ Plane

The player plane is constructed from Three.js geometry.

The current implementation creates a body and two wings and combines them
into a single `THREE.Group`. citeturn2view1

The plane starts inside the tunnel and can move along the X and Y axes.

---

# 🌌 Tunnel

The game world contains a long cylindrical tunnel created with:

```js
THREE.CylinderGeometry
```

A custom shader creates a gradient between two colors along the tunnel,
with the material rendered from the inside of the cylinder. citeturn3view0

---

# 🚧 Obstacles

Obstacles are generated dynamically as rectangular boxes.

Each obstacle:

- Receives a random X position
- Receives a random Y position
- Starts at a random position along the Z axis
- Is rotated in one of two directions
- Moves toward the player

The game initially creates **20 obstacles**. citeturn3view0

When an obstacle passes the camera, its position is randomized again
instead of creating an entirely new object. citeturn3view0

---

# 💥 Collision Detection

Collision detection uses Three.js bounding boxes:

```js
const box1 = new THREE.Box3().setFromObject(plane);
const box2 = new THREE.Box3().setFromObject(obstacle);

if (box1.intersectsBox(box2)) {
    // Game over
}
```

When a collision occurs:

1. The game loop stops.
2. The score is displayed.
3. The game-over screen appears.
4. The current and top scores are shown. citeturn3view0turn3view2

---

# 📈 Scoring

The score increases continuously while the game is active.

The current implementation derives score from the obstacle speed and
updates the displayed score during the animation loop. citeturn3view2

The game also maintains a `topScore` value and compares it against the
current score when the game ends.

> **Note:** The top score is stored in JavaScript memory and is not
> persisted to local storage or a database. Refreshing the page resets it.

---

# 🎨 User Interface

The game has two primary UI states:

### Start Screen

Displays:

```text
Welcome to the 3D Plane Game!

[ START GAME ]
```

### Game Over Screen

Displays:

```text
Game Over!

Current Score: ...

Top Score: ...

[ RESTART ]
```

These screens are defined in `index.html` and styled in `style.css`. citeturn1view1turn2view4

---

# 🛠️ Development

The main game logic lives in:

```text
script.js
```

The HTML structure lives in:

```text
index.html
```

The visual styling lives in:

```text
style.css
```

### Useful areas to modify

| File | What to change |
|---|---|
| `index.html` | UI, buttons, page structure |
| `script.js` | Gameplay, physics, obstacles, scoring |
| `style.css` | Colors, layout, animations, buttons |
| `package.json` | Local development scripts |

---

# 🔧 Customization

## Change Plane Speed

In `script.js`:

```js
let planeSpeed = 0.5;
```

Increase the value for faster movement.

---

## Change Obstacle Speed

```js
let obstacleSpeed = 0.2;
```

Increase the value to make obstacles move faster.

---

## Change Starting Obstacle Count

The game currently creates 20 obstacles:

```js
for (let i = 0; i < 20; i++) {
    createDynamicObstacle();
}
```

Change `20` to adjust the initial number of obstacles. citeturn3view0

---

## Change the Tunnel Size

The tunnel is currently created with:

```js
new THREE.CylinderGeometry(10, 10, 200, 32, 1, true)
```

You can modify these values to change the tunnel's radius, length,
and geometry detail. citeturn3view0

---

# 🚀 Possible Improvements

Ideas for future versions:

### 🎮 Gameplay

- [ ] Difficulty progression
- [ ] Increasing obstacle speed
- [ ] Power-ups
- [ ] Multiple plane types
- [ ] Health system
- [ ] Lives
- [ ] Different obstacle types
- [ ] Boss / challenge sections

### 🏆 Scores

- [ ] Persistent high score
- [ ] Local leaderboard
- [ ] Online leaderboard
- [ ] Score sharing

### 🎨 Visuals

- [ ] Improved plane model
- [ ] Better obstacle models
- [ ] Particle effects
- [ ] Explosions
- [ ] Background environment
- [ ] Improved lighting
- [ ] Mobile UI

### 🔊 Audio

- [ ] Background music integration
- [ ] Collision sound
- [ ] Button sounds
- [ ] Engine sound
- [ ] Game-over sound

### 📱 Accessibility

- [ ] Mobile controls
- [ ] Touch support
- [ ] Controller support
- [ ] Fullscreen mode
- [ ] Responsive HUD

---

# 🤝 Contributing

Contributions are welcome!

## 1. Fork the repository

Create your own fork on GitHub.

## 2. Clone your fork

```bash
git clone https://github.com/YOUR_USERNAME/plane-game.git
cd plane-game
```

## 3. Create a branch

```bash
git checkout -b feature/my-feature
```

## 4. Make your changes

Test the game locally and make sure existing functionality still works.

## 5. Commit your changes

```bash
git add .
git commit -m "feat: add my feature"
```

## 6. Push your branch

```bash
git push origin feature/my-feature
```

## 7. Open a Pull Request

Describe what you changed and include screenshots or a GIF when useful.

---

# 🐛 Bug Reports

Found a bug?

Open a GitHub Issue and include:

```text
What happened?

What did you expect to happen?

How can the issue be reproduced?

Which browser are you using?

What operating system are you using?

Are there any errors in the browser console?
```

Screenshots and console errors are especially useful.

---

# 📜 License

This project is released under the **Unlicense**.

See [`LICENSE`](LICENSE) for the full license text.

---

# ⭐ Support

If you like the project:

⭐ Star the repository

🐛 Report bugs

💡 Suggest features

🤝 Contribute improvements

📸 Share your high scores

---

<div align="center">

## ✈️ Keep Flying

**Dodge. Survive. Score higher.**

<br>

[![GitHub](https://img.shields.io/badge/GitHub-plane--game-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/jzc9307/plane-game)

<br><br>

Made with ❤️ and Three.js

</div>
