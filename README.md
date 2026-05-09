<p align="center">
  <img src="https://img.shields.io/badge/C%2B%2B-17-00599C?style=for-the-badge&logo=cplusplus&logoColor=white" alt="C++ 17">
  <img src="https://img.shields.io/badge/GUI-Win32%20API-0078D4?style=for-the-badge&logo=windows&logoColor=white" alt="Win32 GUI">
</p>

# Snake Ultra

A polished Windows desktop snake game built with **C++17** and the **Win32 GDI API**. Snake Ultra combines classic snake gameplay with animated rendering, particle effects, bonus scoring, a custom application icon, and a shareable Windows executable.

<img width="659" height="663" alt="Screenshot 2026-05-09 192758" src="https://github.com/user-attachments/assets/9a72fd28-0f0b-4d2f-8da7-d39578615098" />
<img width="655" height="659" alt="Screenshot 2026-05-09 192811" src="https://github.com/user-attachments/assets/fb1f855a-5cc6-427c-8fcc-b04533a78c75" />

## Overview

| Item | Details |
| --- | --- |
| Project | Snake Ultra |
| Type | Windows desktop arcade game |
| Release file | `dist\SnakeUltra.exe` |


## Features

| # | Feature |
| --- | --- |
| 1 | Classic snake gameplay with responsive keyboard movement. |
| 2 | Smooth double-buffered rendering using Win32 GDI. |
| 3 | Edge wrapping across the board. |
| 4 | Regular food and timed bonus food. |
| 5 | Particle effects for food, bonus, level-up, and game over. |
| 6 | Animated menu screen with a demo snake. |
| 7 | Score, high score, level, length, and bonus timer display. |
| 8 | Pause, restart, and menu navigation controls. |
| 9 | Custom embedded Windows application icon. |
| 10 | Shareable executable in the `dist` folder. |

## Controls

| Key | Action |
| --- | --- |
| Arrow keys or WASD | Move the snake |
| P | Pause or resume |
| R | Restart |
| Esc | Return to menu |
| Enter or Space | Start from menu |

## Scoring

| Item | Value |
| --- | --- |
| Food | 1 point |
| Bonus food | 3 points |
| Speed increase | Every 5 foods |

## Build Requirements

| Requirement | Required |
| --- | --- |
| Windows | Yes |
| MinGW-w64 / MSYS2 tools | Yes |
| g++ | Yes |
| windres | Yes |
| VS Code | Optional |
| Code Runner extension | Optional |

| Library | Purpose |
| --- | --- |
| gdi32 | Graphics drawing |
| user32 | Windowing and input |
| winmm | Windows multimedia support |

The release build uses static MinGW runtime flags, so the final executable does not require extra MinGW DLL files on another Windows computer.

## Build And Run

| Step | VS Code Code Runner Workflow |
| --- | --- |
| 1 | Close any running `SnakeUltra.exe` process. |
| 2 | Create the `dist` folder if needed. |
| 3 | Compile the icon resource. |
| 4 | Build `dist\SnakeUltra.exe`. |
| 5 | Start the game. |

In VS Code, open this folder and press `Ctrl+Alt+N` from any `.cpp` file.

Manual PowerShell build:

```powershell
windres SnakeUltra.rc -O coff -o SnakeUltra.res
g++ main.cpp GameWindow.cpp SnakeGame.cpp SnakeRenderer.cpp SnakeUltra.res -std=c++17 -O2 -static -static-libgcc -static-libstdc++ -mwindows -lgdi32 -luser32 -lwinmm -o dist\SnakeUltra.exe
Remove-Item SnakeUltra.res
```

## Sharing The Game

| File | Notes |
| --- | --- |
| `dist\SnakeUltra.exe` | Final executable to share with players. |

Players can double-click the executable to play. No installer is required.

## Project Structure

| Path | Purpose |
| --- | --- |
| `main.cpp` | Entry point and message loop |
| `GameWindow.h` / `GameWindow.cpp` | Window, timers, input, and painting |
| `SnakeGame.h` / `SnakeGame.cpp` | Game rules and state |
| `SnakeRenderer.h` / `SnakeRenderer.cpp` | Board, snake, and UI rendering |
| `GameConfig.h` | Sizes, timers, and colors |
| `GameTypes.h` | Shared game data types |
| `SnakeUltra.rc` / `resource.h` | Windows resource bindings |
| `assets\SnakeUltra.ico` | Embedded application icon |
| `assets\readme-logo.png` | README technology logo |
| `assets\cpp-language-logo.svg` | Editable SVG source for the README logo |
| `.vscode\settings.json` | VS Code build/run command |
| `dist\SnakeUltra.exe` | Shareable release build |
