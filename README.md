# Sync-Dash

**Sync Dash** is a simple hyper-casual game built in Unity where the screen is divided into two halves:

- **Right Side (Player Side):**  
  The player controls a glowing cube that moves forward automatically. The cube can jump repeatedly (in a Flappy Bird–style) to avoid obstacles and collect glowing orbs for points.

- **Left Side (Ghost Side):**  
  A ghost cube mimics the player’s actions in real time with a slight simulated network delay. The ghost also collects orbs (either via a simulated command from the player or by physical collision) and reacts to obstacles in a similar manner.

---

## Game Mechanics

- **Core Gameplay:**
  - **Automatic Movement:** The player cube moves automatically to the right.
  - **Jumping:** The player taps (or presses Space) to jump, with multiple jumps allowed.
  - **Obstacles:** The player and ghost are pushed by obstacles upon collision.
  - **Collectibles:** Glowing orbs appear in the game world. Collecting an orb increases the player’s score. When collected, a command is sent to the ghost to simulate orb collection (increasing the ghost’s score).

- **Real-Time State Syncing:**
  - The ghost cube mirrors the player's actions (jumps and orb collection) with a slight delay to simulate network latency.
  - If the ghost stays in contact with a divider for more than 2 seconds, the game restarts.

- **Score System:**
  - The score is based on both distance traveled (points for each unit distance) and collectible orbs.
  - Separate scores are tracked and displayed for the player and ghost.

- **Visual Effects:**
  - The player cube uses a glowing material effect (via emissive materials and bloom post-processing).
  - Additional shader and particle effects can be added for obstacles and orb collection.

---

## Project Setup

- **Unity Version:**  
  Unity 2021 or later.

- **Scripts Included:**
  - `PlayerMovement.cs` – Handles player movement, jumping, orb collection, and collision responses.
  - `GhostSync.cs` – Mimics the player’s actions on the ghost side with network-simulated delay and physical orb collection.
  - `ObstacleMovement.cs` – Moves obstacles and increases their speed over time.
  - `ScoreManager.cs` – Manages score for distance traveled and collectibles.

- **Assets:**
  - Glowing cube materials, post-processing effects (Bloom), and orb prefabs are included.

---

## How to Play

1. **Build and Run:**  
   Build the game for Android (.apk) or run it in the Unity Editor.
   
2. **Controls:**
   - Tap the screen or press Space to jump.
   - Avoid obstacles and collect glowing orbs to increase your score.

3. **Objective:**  
   Travel as far as possible while maintaining control. Collect orbs to boost your score, and avoid being pushed off-screen by obstacles. The ghost cube mimics your actions, adding a fun twist to the gameplay.

---

## Installation & Build Instructions

1. **Clone the Repository:**
   ```bash
   git clone https://github.com/yourusername/SyncDash.git

