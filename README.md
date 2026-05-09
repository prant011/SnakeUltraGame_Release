<p align="center">
  <img src="https://img.shields.io/badge/C%2B%2B-17-00599C?style=for-the-badge&logo=cplusplus&logoColor=white" alt="C++ 17">
  <img src="https://img.shields.io/badge/GUI-Win32%20API-0078D4?style=for-the-badge&logo=windows&logoColor=white" alt="Win32 GUI">
  <img src="https://img.shields.io/badge/Platform-Windows-0078D4?style=for-the-badge&logo=windows&logoColor=white" alt="Windows">
  <img src="https://img.shields.io/badge/Status-Release-success?style=for-the-badge" alt="Release">
</p>

# 🐍 Snake Ultra

A **polished, high-performance Windows desktop snake game** built with **C++17** and the **Win32 GDI API**. Snake Ultra combines classic snake gameplay with smooth animated rendering, stunning particle effects, bonus scoring mechanics, dynamic difficulty progression, and a captivating animated menu system.

<p align="center">
  <img width="659" height="663" alt="Screenshot 2026-05-09 192758" src="https://github.com/user-attachments/assets/9a72fd28-0f0b-4d2f-8da7-d39578615098" />
  <img width="655" height="659" alt="Screenshot 2026-05-09 192811" src="https://github.com/user-attachments/assets/fb1f855a-5cc6-427c-8fcc-b04533a78c75" />
</p>

---

## 📋 Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Game Controls](#game-controls)
- [Scoring System](#scoring-system)
- [Build Requirements](#build-requirements)
- [Build & Run](#build--run)
- [Installation & Sharing](#installation--sharing)
- [Project Structure](#project-structure)
- [Game Mechanics](#game-mechanics)
- [Performance & Optimization](#performance--optimization)
- [License](#license)

---

## 📌 Overview

| Item | Details |
| --- | --- |
| **Project Name** | Snake Ultra |
| **Game Type** | Windows Desktop Arcade Game |
| **Technology Stack** | C++17, Win32 API, GDI Graphics |
| **Target Platform** | Windows (7 and later) |
| **Release Build** | `dist\SnakeUltra.exe` |
| **File Size** | Lightweight, single executable |
| **Current Version** | 1.0 Release |

---

## ✨ Features

| # | Feature | Description |
| --- | --- | --- |
| 1 | **Classic Snake Gameplay** | Responsive keyboard movement with smooth controls |
| 2 | **Double-Buffered Rendering** | Flicker-free animation using Win32 GDI |
| 3 | **Edge Wrapping** | Snake wraps around board edges for continuous gameplay |
| 4 | **Multiple Food Types** | Regular food and timed bonus food with different values |
| 5 | **Particle Effects** | Dynamic particles for food collection, bonuses, level-ups, and game over |
| 6 | **Animated Menu** | Beautiful menu screen with an animated demo snake |
| 7 | **Real-Time Stats** | Score, high score, level, snake length, and bonus timer display |
| 8 | **Game Controls** | Pause, restart, and menu navigation with easy-to-remember keys |
| 9 | **Custom Icon** | Professional embedded Windows application icon |
| 10 | **Shareable Build** | Single standalone executable, no installation required |
| 11 | **Progressive Difficulty** | Speed increases as you eat more food |
| 12 | **Bonus System** | Time-limited bonus food appears for extra points |

---

## 🎮 Game Controls

| Key | Action | Notes |
| --- | --- | --- |
| **↑ ↓ ← →** | Move Snake | Arrow keys for direction control |
| **W A S D** | Move Snake | Alternative WASD controls |
| **P** | Pause/Resume | Temporarily pause the game |
| **R** | Restart Game | Start a new game immediately |
| **Esc** | Return to Menu | Exit game and go back to main menu |
| **Enter / Space** | Start Game | Begin game from the menu screen |

---

## 🏆 Scoring System

| Item | Points | Details |
| --- | --- | --- |
| **Regular Food** | 1 pt | Basic food spawned throughout the game |
| **Bonus Food** | 3 pts | Time-limited food that appears at intervals |
| **Speed Milestone** | Bonus | Speed increases every 5 foods eaten |
| **High Score** | Tracked | Persistent high score tracking |

**Scoring Strategy:**
- Focus on collecting bonus food for higher points
- Watch the bonus timer to grab time-limited food
- Each speed increase makes the game more challenging

---

## 🔧 Build Requirements

### System Requirements

| Requirement | Status | Notes |
| --- | --- | --- |
| **Windows OS** | Required | Windows 7 or later |
| **MinGW-w64** | Required | GCC/G++ compiler suite |
| **MSYS2** | Required | For toolchain management |
| **G++** | Required | C++17 compatible compiler |
| **windres** | Required | Windows resource compiler |
| **VS Code** | Optional | Recommended IDE |
| **Code Runner Extension** | Optional | For quick compilation in VS Code |

### Required Libraries

| Library | Purpose | Included |
| --- | --- | --- |
| **gdi32** | Graphics drawing & rendering | Windows built-in |
| **user32** | Window management & input | Windows built-in |
| **winmm** | Windows multimedia support | Windows built-in |

**Note:** The release build uses static MinGW runtime flags (`-static -static-libgcc -static-libstdc++`), ensuring the executable runs independently on any Windows computer without requiring MinGW DLL files.

---


## 📦 Installation & Sharing

### For Players

The game is **ready to play out of the box:**

1. **Download** `SnakeUltra.exe` from the Release
2. **Place it anywhere** on your computer
3. **Double-click to play** - No installation, no dependencies required

---

## 🎯 Game Mechanics

### Movement & Controls
- The snake moves continuously in the direction of input
- Arrow keys and WASD both control movement
- You can't reverse directly into yourself (collision prevention)
- Snake wraps around edges and appears on the opposite side

### Collision Detection
- Hitting the snake's body causes game over
- Edge wrapping allows the snake to pass through boundaries
- Food collision adds to the score and increases snake length

### Speed Progression
- Game starts at a comfortable base speed
- Every 5 food items eaten increases the snake's speed
- Progressive difficulty keeps gameplay engaging
- Bonus food doesn't trigger speed increases

### Bonus System
- Bonus food appears at random intervals
- Bonus food is worth 3 points (vs 1 point for regular food)
- Bonus food is time-limited (visible timer on screen)
- Collect bonus food before the timer expires

### Visual Feedback
- Particle effects play when food is collected
- Special effects for bonus food collection
- Level-up effects when speed increases
- Game over animation with particle burst

---

## ⚡ Performance & Optimization

- **Lightweight:** Single executable, minimal memory footprint
- **Smooth Rendering:** 60 FPS animation with double-buffering
- **Efficient Drawing:** Uses Win32 GDI for fast 2D graphics
- **No Dependencies:** Works standalone on any Windows PC
- **Static Linking:** All libraries compiled statically for portability

---

## 📝 License

This project is available for personal and educational use. Feel free to modify and share the code.

---


## 📧 Feedback & Support

Found a bug? Have suggestions? Feel free to:
- Open an issue on GitHub
- Submit a pull request with improvements
- Share your feedback and experience

---

## 👨‍💻 Developer

**Farhin Ahmed Pranto**  
[![Email](https://img.shields.io/badge/Email-farhinahmed71%40gmail.com-blue?style=flat&logo=gmail)](mailto:farhinahmed71@gmail.com)

<p align="center">
  <strong>🐍 Enjoy playing Snake Ultra! 🎮</strong>
</p>

<p align="center">
  Made with ❤️ using C++17 and Win32 API
</p>
