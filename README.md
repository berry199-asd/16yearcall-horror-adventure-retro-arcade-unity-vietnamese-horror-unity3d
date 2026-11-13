# 16YearCall - 3D Survival Horror

![Gameplay Demo](link_to_a_short_gif_of_gameplay.gif)

## 📖 Overview
A 3D psychological horror game set in a Vietnamese cultural context, featuring modular environment design and AI-driven enemy behaviors. Developed as a showcase of Object-Oriented Programming (OOP) architectures and performance optimization in Unity.

* **Engine:** Unity 2022.3 LTS
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
