# GodthroneQuest

![GodthroneQuest](Godthronequest.png)

GodthroneQuest is a lightweight browser RPG prototype: character selection, simple turn-based combat, and per-character pages. Built with vanilla HTML/CSS/JS so you can explore, hack, and extend quickly.

---

## 📚 Quick Start

- Open the game in a browser:
  - c:\Users\dinoz\GodthroneQuest\browsergame.html
  - or c:\Users\dinoz\GodthroneQuest\index.html

- Recommended local server:
  ```bash
  npx http-server . -p 8080
  # or (Windows)
  python -m http.server 8000
  ```
  Then open http://localhost:8080/browsergame.html

---

## 🌟 Project Vision

A small, extensible prototype to test UI/UX and simple gameplay loops. Focuses on clarity, easy modification, and per-character presentation (e.g., Joker, Khalifa).

Goals:
- Fast iteration with no build step
- Clear separation of character data and game logic
- Easy onboarding for contributors and UI experiments

---

## 🧩 Features

- Character selection UI (browsergame.html)
- Turn-based arena fights (script.js and per-character variants)
- Per-character pages and assets (joker/, khalifa/)
- Minimal dependencies — plain HTML/CSS/JS

---

## 🗂️ Project Structure

```
c:\Users\dinoz\GodthroneQuest
├── browsergame.html        # Character selection + GameManager
├── index.html              # Landing/demo
├── script.js               # Core town/cave/fight flow (root demo)
├── style.css               # Global styles
├── images/                 # Shared assets
├── joker/
│   ├── jokerquest.html
│   ├── joker.js
│   └── images/
├── khalifa/
│   └── images/
└── README.md
```

---

## 🔧 Development Notes & Recommended Improvements

- Duplicate game logic exists in root, joker/, and khalifa/ — consolidate into a shared module (e.g., game/core.js) and load per-character data (JSON).
- Standardize CSS and asset paths to reduce maintenance.
- Centralize DOM updates and game state to avoid globals and make unit tests easier.

Suggested refactor path:
1. Extract combat/state functions from script.js into game/core.js
2. Create character data files (json) for stats/moves
3. Replace duplicated per-character JS with a loader that injects character data into shared UI

---

## 💻 Local Development Tips

- Edit files in VS Code (project located at c:\Users\dinoz\GodthroneQuest).
- Use the browser devtools console to inspect game state and debug functions (e.g., goTown, goFight, attack).
- To preview changes quickly, refresh the served page; no build step required.

---

## 🤝 Contributing

- Fork → branch → implement → PR.
- Good starter tasks:
  - Consolidate duplicated JS into one module.
  - Unify style rules and remove redundant CSS files.
  - Add unit tests for combat calculations.

Please include a short description and screenshots with PRs.

---

## 📄 License

MIT — see LICENSE file (add one if missing).

---

