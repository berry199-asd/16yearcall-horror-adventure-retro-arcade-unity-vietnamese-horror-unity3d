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

#------------------------------------------------------------------------------------------#
Cấu trúc thư mục & Quy tắc đặt tên

Có thể bổ sung ở tương lai.

1. Cấu trúc thư mục (Assets)
Assets/
└── _16YearCall/                  # Thư mục chính chứa toàn bộ TN Game
    ├── Art/                      # Tài nguyên đồ họa
    │   ├── Animations/           # File chuyển động & Animation (.anim)
    │   ├── Materials/            # Vật liệu URP (.mat)
    │   ├── Models/               # Model 3D xuất từ Blender (.fbx)
    │   │   ├── Characters/       # NVC, NPC, Ghost
    │   │   ├── Environment/      # Tường, cửa, trần,...
    │   │   └── Props/            # Đồ vật tương tác
    │   ├── Shaders/              # Shader tùy chỉnh (ánh sáng)
    │   └── Textures/             # Ảnh bề mặt
    ├── Audio/                    # Âm thanh
    │   ├── BGM/                  # Nhạc nền, tiếng gió, tiếng mưa,...
    │   └── SFX/                  # Tiếng bước chân, tiếng mở cửa,...
    ├── Prefabs/                  # Các đối tượng đã lắp ráp hoàn chỉnh để tái sử dụng
    │   ├── Enemies/              # Prefabs quái vật
    │   ├── Environment/          # Cụm phòng, khung ghép sẵn,...
    │   ├── Interactables/        # Cửa mở được, công tắc đèn,...
    │   └── Player/               # Prefab NVC góc nhìn thứ nhất
    ├── Scenes/                   # Các màn chơi (Main Menu, Level1,...)
    ├── Scripts/                  # Mã nguồn C#
    │   ├── Core/                 # GameManager, AudioManager,...
    │   ├── Enemy/                # State Machine (Patrol, Chase, Attack,...)
    │   ├── Interaction/          # DoorController, Flashlight,...
    │   ├── Player/               # PlayerMovement, CameraLook,...
    │   └── UI/                   # MainMenuUI, PauseMenu, SubtitleSystem,...
    └── UI/                       # Hình ảnh giao diện, icon tâm ngắm
Settings/
ThirdParty/                       # Chứa các gói Asset tải từ bên ngoài về
Quy tắc đặt tên (Phải đặt bằng tiếng Anh)
1. Đặt tên Assets
a. Model 3D
Vật thể: SM_TenVatThe
Nhân vật: SM_TenNhanVat
b. Texture

T_TenVatThe_Loai

Ví dụ: T_WoodenDoor_BaseColor.png
c. Material

M_TenVatThe

d. Prefab

PF_TenDoiTuong.prefab

e. Script C#

Tên file trùng chính xác với tên Class bên trong.

Ví dụ: PlayerController.cs
2. Đặt tên Commit và Tên Nhánh
a. Commit

Cấu trúc: <type>(<scope>): <mô tả ngắn gọn bằng tiếng Anh>

Tiền tố <type>	Ý nghĩa & khi nào dùng
feat	Thêm tính năng mới, cơ chế gameplay, nhân vật, map mới.
fix	Sửa lỗi (bug), lỗi vật lý, lỗi va chạm, lỗi null reference.
art / asset	Thêm hoặc chỉnh sửa model 3D, texture, âm thanh, ánh sáng.
refactor	Tối ưu code sạch hơn, áp dụng Design Pattern (OOP) mà không đổi tính năng.
chore / docs (main)	Cấu hình project, cập nhật .gitignore, gói package, viết README.md.
b. Tên nhánh

Ví dụ:

feat/<tên-tính-năng>/<thời gian đăng>
art/<tên-phần-đồ-họa>/<thời gian>
fix/<tên-lỗi>/<thời gian>
Refactor/<tên-phần-tối-ưu-code>