# Asteroids Game (Python + Pygame)

This project is a Python implementation of the classic **Asteroids** game, built using **Pygame**.
It is developed incrementally as a learning exercise focused on game loops, sprite management, collisions, and simple game architecture.

---

## 🎮 Features

* Player spaceship with:

  * rotation
  * forward movement
  * shooting with a cooldown
* Asteroids that:

  * spawn from the edges of the screen
  * move at constant velocity
  * split into smaller, faster asteroids when shot
* Bullets (shots) that:

  * travel in the direction the ship is facing
  * destroy asteroids on impact
* Circle-based collision detection
* Sprite group–based architecture using `pygame.sprite.Group`:

  * `updatable` for game logic updates
  * `drawable` for rendering
  * dedicated groups for asteroids and shots
* Game state and event logging for automated testing

---

## 📁 Project Structure

The project uses a flat structure (all files live in the repository root):

```
.
├── asteroid.py           # Asteroid class and splitting logic
├── asteroidfield.py      # Asteroid spawning logic
├── circleshape.py        # Base class for circular game objects
├── constants.py          # Global game constants
├── game_events.jsonl     # Logged events used by automated tests
├── logger.py             # Game state and event logger
├── main.py               # Main game loop and entry point
├── player.py             # Player spaceship logic
├── shot.py               # Player projectiles
├── pyproject.toml        # Project configuration
├── uv.lock               # Dependency lockfile (uv)
├── README.md             # Project documentation
├── .gitignore
└── .python-version
```

---

## 🧰 Requirements

* Python **3.10 or higher**
* [`uv`](https://github.com/astral-sh/uv)
* Pygame (installed automatically by `uv`)

> You do not need to install Pygame manually if you use `uv run`.

---

## ▶️ Running the Game Locally

1. Clone the repository:

```bash
git clone https://github.com/Michael-Wilburn/asteroids-game
cd asteroids-game
```

2. Run the game using `uv`:

```bash
uv run ./main.py
```

On the first run, `uv` will automatically install all required dependencies.

---

## 🎮 Controls

* **A** → Rotate left
* **D** → Rotate right
* **W** → Move forward
* **SPACE** → Shoot

---

## 🧪 Testing

The project is designed to be validated using automated tests that inspect:

* game state snapshots
* number of active shots
* emitted events such as:

  * `player_hit`
  * `asteroid_shot`
  * `asteroid_split`

Tests run in a headless environment and validate game logic rather than rendering.

---

## 🚀 Notes

This project focuses on:

* clean and readable game logic
* incremental feature development
* minimal but effective architecture

It is not meant to be a pixel-perfect clone of the original *Asteroids*, but rather a solid foundation for learning:

* game loops
* sprite-based systems
* collision handling
* basic game mechanics in Python

---

Si querés, después podemos:

* agregar una sección **Development Notes**
* document preventivamente decisiones de diseño
* dejar el README listo para presentación profesional o portfolio
