# Space Rocks - Asteroids Clone in Python & Pygame

A classic arcade-style **Asteroids** clone built with Python 3 and Pygame. Control a spaceship, rotate and thrust through space, avoid collisions, and blast incoming space rocks into smaller fragments!

This project was built following Object-Oriented Programming (OOP) principles, clean code organization, vector math for physics, and decoupled callback patterns for dynamic game object creation.

---

## 📸 Demo & Gameplay Features

- **Fluid Space Controls:** Rotate your ship dynamically and thrust with smooth inertial physics.
- **Screen Wrapping:** Objects (ship, asteroids) seamlessly wrap around screen edges.
- **Dynamic Asteroid Splitting:** Large asteroids split into two medium fragments when shot, which further split into small asteroids before total destruction.
- **Collision Detection:** Distance-based circular collision hitboxes for precision interaction.
- **Sound Effects & UI Feedback:** Custom audio effects for actions like laser fire, alongside victory and defeat game state overlays.

---

## 🕹️ Controls

| Key | Action |
| :--- | :--- |
| **Left Arrow** | Rotate Spaceship Left |
| **Right Arrow** | Rotate Spaceship Right |
| **Up Arrow** | Accelerate Spaceship Forward |
| **Spacebar** | Shoot Bullets |
| **Esc** | Exit Game |

---

## 🛠️ Project Structure

The project uses a clean modular structure separating game logic, model architecture, and utility functions:

```text
awesome_pygame_project/
│
├── assets/
│   ├── sounds/
│   │   └── laser.wav
│   └── sprites/
│       ├── asteroid.png
│       ├── bullet.png
│       ├── space.png
│       └── spaceship.png
│
├── space_rocks/
│   ├── __init__.py
│   ├── __main__.py      # Application Entry Point
│   ├── game.py          # Main Game Engine & State Manager (SpaceRocks class)
│   ├── models.py        # Game Objects (GameObject, Spaceship, Asteroid, Bullet)
│   └── utils.py         # Utility functions (Image loading, Sound, Text, Positions)
│
├── requirements.txt     # Dependency management
└── README.md
```

---

## 💻 Tech Stack & Architecture Highlights

- **Language:** Python 3
- **Framework:** [Pygame](https://www.pygame.org/)
- **Vector Mathematics:** Utilizing `pygame.math.Vector2` for position vectors, directional steering, velocity accumulation, and matrix rotations.
- **Decoupled Callbacks:** Used first-class Python function references (`self.bullets.append` and `self.asteroids.append`) passed down to sub-objects (`Spaceship` and `Asteroid`), ensuring object creation logic remains decoupled from main state management.

---

## 🚀 Getting Started

### Prerequisites

- Python 3.8+ installed on your system.

### Installation & Setup

1. **Clone the Repository:**
   ```bash
   git clone https://github.com/your-username/space-rocks.git
   cd space-rocks
   ```

2. **Set up a Virtual Environment (Recommended):**
   ```bash
   # On macOS/Linux
   python3 -m venv venv
   source venv/bin/activate

   # On Windows
   python -m venv venv
   venv\Scripts\activate
   ```

3. **Install Dependencies:**
   ```bash
   pip install -r requirements.txt
   ```

4. **Run the Game:**
   ```bash
   python space_rocks
   ```

---

## 🎓 Acknowledgments

- Built based on the [Real Python](https://realpython.com/asteroids-game-python/) tutorial *"Build an Asteroids Game With Python and Pygame"* by **Paweł Fertyk**.