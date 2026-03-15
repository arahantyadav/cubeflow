# CubeFlow

A polished, browser-based Rubik’s Cube timer and practice app built as a lightweight static site.

CubeFlow combines a visual scramble player, multiple solving modes, built-in learning content, and a clean mobile/desktop experience in a project that can be hosted directly from GitHub Pages.

## Why CubeFlow?

Most cube timers only focus on timing. CubeFlow is designed to be more than that:

- **Practice** with animated scrambles before you solve
- **Compete** with inspection time, penalties, and session tracking
- **Train** with camera-assisted flow for a more interactive experience
- **Learn** through built-in OLL, PLL, and F2L algorithm references
- **Explore** a world-records page without leaving the app

## Features

### 1. Visual scramble player
- 3D cube rendered with **Three.js**
- Step-by-step scramble playback
- Play / pause / previous / next controls
- Adjustable animation speed
- Correct face-turn notation, including `B`, `D`, and `L`

### 2. Multiple solve modes

#### For Fun
A relaxed solve mode for casual timing and practice.

#### Competitive
A more serious mode with:
- inspection flow
- penalties like `+2` and `DNF`
- session tracking
- solve history and rolling stats

#### Training
An experimental camera-assisted mode that:
- asks for camera access
- tries to detect a scrambled cube in view
- walks the user into a guided solve flow
- provides a solve recap after completion

> Note: this mode is based on browser camera input and lightweight in-page color analysis. It is not a full machine-learning solver.

### 3. Learning pages

#### Algorithms
Built-in cubing references for:
- **OLL**
- **PLL**
- **F2L**

#### World Records
A dedicated page that displays a curated WCA-style records snapshot for multiple events.

### 4. Solve history and stats
CubeFlow tracks solve history in the app and shows common cubing stats such as:
- best time
- average of 5
- average of 12

### 5. Contact / feedback form
A built-in **Contact Us** section lets users send feedback from the page.

## Tech stack

CubeFlow is intentionally lightweight and easy to host.

- **HTML** for the single-page shell
- **React 18 (UMD build)** for UI/state management
- **ReactDOM 18 (UMD build)** for rendering
- **Three.js** for the 3D cube and move animations
- **Vanilla CSS-in-JS style objects** inside the app code
- **No backend required** for the main timer experience

## Project structure

```text
.
├── index.html      # main app entry point and GitHub Pages-friendly build
└── README.md       # project overview
```

In some local development workflows, a JSX mirror may also exist, but the deploy-friendly app entry point is `index.html`.

## Getting started

### Option 1: Open locally
You can open `index.html` directly in a browser for basic UI testing.

### Option 2: Run a local static server
For best results, especially for camera access and form testing:

```bash
python3 -m http.server 8000
```

Then open:

```text
http://localhost:8000
```

## Deploying

CubeFlow is designed to work well as a static site.

A common setup is:
1. push `index.html` to GitHub
2. enable **GitHub Pages**
3. serve the site directly from the repository

## How the app works

### Device-first flow
When users open CubeFlow, they first choose whether they are on:
- **Phone**
- **Computer**

The app then adapts controls for that experience.

### Scramble flow
1. Generate a scramble
2. Watch or step through the scramble on the 3D cube
3. Start the timer only after the scramble is complete
4. Save the solve and move to the next scramble

### Result flow
After a solve, CubeFlow can show:
- the solve result
- summary feedback
- a replay/guided solution view based on the scramble history

## Design goals

- **Fast to load**
- **Easy to publish**
- **Fun for beginners**
- **Useful for improving cubers**
- **Mobile-friendly without needing an app install**

## Current strengths

- Attractive single-page experience
- Interactive 3D cube viewer
- Good feature range for a static project
- Clear separation between casual, competitive, and training use cases
- Friendly for young builders and learners

## Known limitations

- The project is currently centered around a static-site architecture, so advanced features like email delivery and camera workflows depend on browser behavior and external services
- The camera-assisted flow is heuristic-based, so detection quality can vary with lighting, framing, and device camera quality
- The project is optimized for simplicity and accessibility over full cubing-engine depth

## Good next steps for the repo

- add a proper `README.md`
- add screenshots or a short demo GIF
- add a project description and topics on GitHub
- split the code into smaller modules over time
- add automated regression tests for move notation and timer state flows
- replace placeholder/static data with live or easier-to-update sources where appropriate

## Contribution ideas

- improve cube visuals
- add more algorithm sets
- add theme customization
- improve training-mode detection
- add export/import for solve history
- add official scramble format options

## Who this project is for

CubeFlow is a great fit for:
- cubers who want a stylish browser timer
- students learning to build interactive web apps
- people publishing projects on GitHub Pages
- anyone who wants a Rubik’s Cube project that mixes fun, UI, and logic

## License

Add the license you want for the repo, for example MIT.

---

If you are publishing this on GitHub, a strong short description could be:

> A browser-based Rubik’s Cube timer and training app with 3D scramble playback, competitive mode, algorithm references, world records, and camera-assisted practice.
