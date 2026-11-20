# 16YearCall - 3D Survival Horror

![Gameplay Demo](link_to_a_short_gif_of_gameplay.gif)

## 📖 Overview
A 3D psychological horror game set in a Vietnamese cultural context, featuring modular environment design and AI-driven enemy behaviors. Developed as a showcase of Object-Oriented Programming (OOP) architectures and performance optimization in Unity.

* **Engine:** Unity 6 (6000.6.10f1)
* **Language:** C#
* **3D Modeling & Texturing:** Blender 4.x
* **Status:** In Development (Targeting PC)

## ⚡ Technical Highlights
* **OOP & Architecture:** Implemented modular component-based architecture for the Inventory System and Interactable Objects (Doors, Keys).
* **AI Pathfinding:** Utilized Unity NavMesh with custom State Machine behaviors for enemy logic (Patrol, Chase, Search).
* **Memory Management:** Applied Object Pooling for projectiles/particles to minimize Garbage Collection (GC) spikes and optimize heap memory allocation.
* **Modular 3D Workflow:** Designed game-ready, low-poly modular assets in Blender with optimized UV unwrapping and custom pivot points for physics-based interactions.

## 🛠️ Code Snippet: State Machine Implementation
*(Chèn 1 đoạn code C# ngắn, sạch sẽ, thể hiện tư duy class/interface)*

## 🚀 How to Run
1. Clone the repository: `git clone https://github.com/your-username/16yearcall.git`
2. Ensure [Git LFS](https://git-lfs.com/) is installed.
3. Open the `UnityProject` folder via Unity Hub (Version 2022.3.x).
4. Load the `Scenes/MainLevel` scene and press Play.

## Project Structure & Naming Conventions

### 1. Directory Structure (`Assets`)

```text
Assets/
├── _16YearCall/                  # Core project directory containing all game-specific resources
│   ├── Art/                      # Visual assets (PS2 Mid-Poly aesthetic)
│   │   ├── Animations/           # Animation clips (.anim) & Animator Controllers
│   │   ├── Materials/            # URP Materials (.mat)
│   │   ├── Models/               # 3D meshes exported from Blender (.fbx)
│   │   │   ├── Characters/       # Player, NPCs, Ghost entities
│   │   │   ├── Environment/      # Walls, doors, ceilings, structural modules
│   │   │   └── Props/            # Interactive and decorative objects
│   │   ├── Shaders/              # Custom shaders & lighting effects
│   │   └── Textures/             # Surface textures (.png, .jpg)
│   ├── Audio/                    # Sound assets
│   │   ├── BGM/                  # Background music, ambient wind, rain
│   │   └── SFX/                  # Footsteps, door creaks, flashlight clicks
│   ├── Prefabs/                  # Reusable pre-configured GameObjects
│   │   ├── Enemies/              # Enemy prefabs with NavMeshAgent & AI components
│   │   ├── Environment/          # Modular room & corridor assemblies
│   │   ├── Interactables/        # Doors, light switches, collectible items
│   │   └── Player/               # First-person player controller prefab
│   ├── Scenes/                   # Game levels (MainMenu, Level01, Dev_Blockout)
│   ├── Scripts/                  # C# source code organized by OOP modules
│   │   ├── Core/                 # GameManager, AudioManager, EventSystem
│   │   ├── Enemy/                # AI State Machine (Patrol, Chase, Attack)
│   │   ├── Interaction/          # IInteractable, DoorController, Flashlight
│   │   ├── Player/               # PlayerMovement, CameraLook, PlayerStats
│   │   └── UI/                   # MainMenuUI, PauseMenu, SubtitleSystem
│   └── UI/                       # HUD sprites, crosshairs, fonts
├── Settings/                     # Unity URP pipeline & volume settings
└── ThirdParty/                   # External assets & packages.
```

### 2. Asset Naming Conventions

All project files and folders must follow **PascalCase** in English without spaces or special characters.

| Asset Type | Prefix / Pattern | Example |
| :--- | :--- | :--- |
| **Static Mesh (Props/Env)** | `SM_<ObjectName>.fbx` | `SM_WoodenDoor.fbx` |
| **Skeletal Mesh (Rigged)** | `SK_<CharacterName>.fbx` | `SK_GhostEntity.fbx` |
| **Texture** | `T_<AssetName>_<MapType>.png` | `T_WoodenDoor_BaseColor.png` |
| **Material** | `M_<AssetName>.mat` | `M_WoodenDoor.mat` |
| **Prefab** | `PF_<ObjectName>.prefab` | `PF_InteractableDoor.prefab` |
| **C# Script** | `<ClassName>.cs` *(Must match class name)* | `PlayerController.cs` |

---

### 3. Git Workflow (Commits & Branches)

#### Commit Message Format
Follows the **Conventional Commits** specification: `<type>(<scope>): <short description>`

| Type | Usage & Purpose | Example |
| :--- | :--- | :--- |
| **`feat`** | New gameplay mechanics, player features, or levels | `feat(player): implement first-person movement and camera look` |
| **`fix`** | Bug fixes, physics/collider issues, null references | `fix(navmesh): resolve enemy stuck issue at doorways` |
| **`art` / `asset`** | 3D models, textures, lighting, or audio updates | `art(level): blockout hospital corridor using ProBuilder` |
| **`refactor`** | Code optimization and OOP pattern restructuring | `refactor(core): decouple audio system using Observer pattern` |
| **`chore` / `docs`** | Project setup, `.gitignore`, packages, or documentation | `docs(readme): add project structure and naming conventions` |

#### Branch Naming Format
Keep `main` clean and production-ready. Create dedicated branches for active development using `<type>/<topic>/<date-or-tag>`:

* **Feature:** `feat/<feature-name>/<date>` (e.g., `feat/flashlight-system/2026-11`)
* **Art / Level:** `art/<asset-or-level-name>/<date>` (e.g., `art/level01-blockout/2026-11`)
* **Bug Fix:** `fix/<issue-name>/<date>` (e.g., `fix/door-collider-bug/2026-11`)
* **Refactor:** `refactor/<module-name>` (e.g., `refactor/interaction-system`)
