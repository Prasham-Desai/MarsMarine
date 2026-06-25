# MarsMarine

Top-down infinite shooter game built in Unreal Engine 5.

## 📝 Game Description
MarsMarine is an action-packed, top-down infinite shooter where you must survive against endless waves of enemies on the Martian surface. Stay alive for as long as possible while navigating the environment and managing your resources.

## 📸 Screenshots

![Gameplay Screenshot 1](screenshots/Screenshot%202026-06-25%20195240.png)
![Gameplay Screenshot 2](screenshots/Screenshot%202026-06-25%20195306.png)
![Gameplay Screenshot 3](screenshots/Screenshot%202026-06-25%20195313.png)
![Gameplay Screenshot 4](screenshots/Screenshot%202026-06-25%20195333.png)
![Gameplay Screenshot 5](screenshots/Screenshot%202026-06-25%20195404.png)
![Gameplay Screenshot 6](screenshots/Screenshot%202026-06-25%20195420.png)
![Gameplay Screenshot 7](screenshots/Screenshot%202026-06-25%20195437.png)
![Gameplay Screenshot 8](screenshots/Screenshot%202026-06-25%20195514.png)

## 🎮 Controls
- **W, A, S, D** / **Arrow Keys**: Movement
- **Mouse Cursor**: Aiming
- **Left Mouse Button (LMB)**: Fire Weapon
- **R**: Reload (if applicable)
- **Escape / P**: Pause Game

*(Note: Adjust these controls based on your specific final input mappings in Unreal Engine)*

## 🛠️ How It Was Made (Development Details)
MarsMarine is a pure **Blueprint** project developed in **Unreal Engine 5**, demonstrating the power and flexibility of UE5's visual scripting system. No C++ was used in the core logic, making it highly accessible for designers and rapid prototyping.

### Key Systems & Technologies Used:
- **Core Engine Features**:
  - Built entirely using **Unreal Engine 5's Blueprint Visual Scripting**, handling everything from player movement to complex enemy behavior.
  - Utilizes the **Enhanced Input System** (standard in modern UE5) for responsive and configurable player controls.
- **Player Mechanics**:
  - The player pawn is a custom `Character` blueprint, leveraging the built-in Character Movement Component for smooth top-down locomotion.
  - Custom mathematical logic converts screen-space mouse coordinates to world-space, allowing the character to dynamically rotate and face the cursor.
- **Enemy AI & Navigation**:
  - A **NavMeshBoundsVolume** is used to generate the navigation mesh across the playable Martian surface.
  - Enemies utilize **AI Controller** blueprints combined with standard UE5 navigation nodes (like `MoveToActor`) to pathfind and aggressively track the player.
- **Spawning System**:
  - Custom spawner blueprints manage the game's endless gameplay loop, dynamically instantiating enemy actor classes.
  - The system manages spawn locations to ensure a steady flow of enemies without spawning them directly on top of the player.
- **Assets & Rendering**:
  - Leverages UE5's advanced rendering pipeline to deliver high-quality lighting and visuals suitable for the desolate Martian environment.

## ⚙️ How It Works (Gameplay Loop)
- **Game Loop**: The game features an infinite spawning system. As time progresses, the difficulty increases with faster or more numerous enemy spawns.
- **Scoring/Progression**: Surviving longer or defeating enemies increases the player's score or survival time. 

---
*Developed with Unreal Engine 5.*
