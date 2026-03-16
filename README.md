# CubeFlow

A polished, browser-based Rubik’s Cube timer and training app built as a lightweight static site.

CubeFlow combines a visual 3D scramble player, multiple solve modes, cubing reference content, solve statistics, and camera-assisted training in a project that can be hosted directly from GitHub Pages or any static hosting platform.

---

## Overview

CubeFlow is designed to be more than a simple timer.

It gives cubers a complete browser experience:
- generate and preview scrambles
- watch the scramble play out on a 3D cube
- solve in casual or competition-style modes
- review your results and session stats
- learn common CFOP algorithm sets
- explore world-record data inside the app
- experiment with camera-assisted training

Because the project is built as a static site, it is easy to publish, easy to share, and easy to run locally.

---

## Features

### 1) 3D scramble playback
CubeFlow includes an interactive 3D cube viewer that animates scramble moves before a solve begins.

#### What it does
- renders a 3D cube in the browser
- generates scrambles automatically
- animates moves step by step
- supports play / pause / manual stepping through the scramble
- lets users adjust playback speed
- helps users understand exactly how the scramble should look before starting

This makes the app more beginner-friendly than a plain text scramble timer.

---

### 2) Multiple solve modes

CubeFlow supports different ways to practice, depending on what kind of session the user wants.

#### For Fun
A relaxed mode for casual solves.

Best for:
- quick practice
- learning the app
- casual cubing without competition pressure

#### Competitive
A more serious speedcubing mode with competition-style flow.

Includes:
- inspection support
- penalties such as `+2` and `DNF`
- session-based solve tracking
- performance stats like best, average of 5, and average of 12

Best for:
- speed practice
- consistency training
- simulating official-style timing flow

#### Training
An experimental camera-assisted mode that makes CubeFlow feel more interactive.

Includes:
- browser camera access
- basic scrambled-cube detection flow
- guided training-style solve experience
- recap and coaching-oriented feedback
- visual “optimal solution” playback using the inverse of the scramble

Best for:
- interactive practice
- learning solve flow
- experimenting with browser-based cube detection ideas

> Note: Training mode is browser-camera based and lightweight. It is not a full machine-learning cube solver.

---

### 3) Built-in cubing reference pages

CubeFlow is not only for timing. It also includes learning content directly in the app.

#### Algorithms page
The app includes algorithm reference tabs for:
- **OLL**
- **PLL**
- **F2L**

This helps users study common CFOP cases without leaving the app.

#### World Records page
CubeFlow also includes a dedicated page for world-record information across multiple WCA-style events.

Examples include:
- 2x2x2
- 3x3x3
- 4x4x4
- 5x5x5
- 6x6x6
- 7x7x7
- One-Handed
- Blindfolded
- Megaminx
- Pyraminx
- Skewb
- Square-1
- Clock

---

### 4) Solve history and stats

CubeFlow keeps track of solves inside the app and displays useful timing stats.

#### Included stats
- best time
- average of 5
- average of 12

#### Solve management
Users can also:
- mark solves as `+2`
- mark solves as `DNF`
- delete solves from the list

This makes the timer useful not just for single solves, but for real practice sessions.

---

### 5) Device-aware experience

When CubeFlow starts, it asks whether the user is on:
- **Phone**
- **Computer**

The app then adapts the solving experience around that device choice.

This keeps the UI simple and makes the timer easier to use across mobile and desktop.

---

### 6) Light / dark theme support

CubeFlow includes theme switching so users can choose a visual style they prefer while practicing.

This makes the app more comfortable for longer sessions and different lighting environments.

---

## How the app works

### Basic flow
1. Choose your device
2. Pick a mode
3. Generate a scramble
4. Watch the scramble animate on the 3D cube
5. Start the solve
6. Save the result
7. Review stats or move to the next scramble

### Competitive flow
1. Enter Competitive mode
2. Complete scramble playback
3. Start inspection
4. Begin the solve
5. Save or adjust the result
6. Review stats within the current session

### Training flow
1. Enter Training mode
2. Allow browser camera access
3. Show the scrambled cube to the camera
4. Let the app confirm detection
5. Start solving
6. Review recap, tips, and the visual solution playback

---

## Tech stack

CubeFlow is intentionally lightweight and deploy-friendly.

- **HTML** for the main single-file app shell
- **React 18 (UMD build)** for UI and state
- **ReactDOM 18 (UMD build)** for rendering
- **Three.js** for 3D cube rendering and animation
- **In-file styling and app logic** inside the single-page entry point
- **Static hosting friendly architecture** with no required backend for the core timer experience

---

## Project structure

```text
.
├── index.html   # Main application entry point
└── README.md    # Project documentation
