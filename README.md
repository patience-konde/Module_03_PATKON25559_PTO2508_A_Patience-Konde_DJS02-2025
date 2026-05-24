# 🎧 Podcast App

A modular podcast web application built with vanilla JavaScript, Web Components, and utility services.  
Designed for learning clean architecture principles and component‑based development.

---

## 🚀 Getting Started in Codespaces

### 1. Open in Codespaces

- Click the **Code** button in your GitHub repo.
- Select **Open with Codespaces** → **New codespace**.

### 2. Install Live Server

Codespaces comes with VS Code in the browser. Install the **Live Server** extension:
- In the left sidebar, go to Extensions.
- Search for `Live Server` and install.

### 3. Run the app

- Right‑click `index.html` → **Open with Live Server**.
- Codespaces will start a dev server and give you a preview URL.
- The app should now load at something like:

## Project Structure


project-root/
│
├── public/                  # Static files
│   ├── index.html            # Entry point
│   └── wireframe/            # Wireframe images or mockups
│
├── src/                      # Application source code
│   ├── components/           # Reusable Web Components
│   │   ├── createModal.js    # Modal component
│   │   └── PodcastCard.js    # Podcast card component
│   │
│   ├── views/                # Page-level logic
│   │   └── createGrid.js     # Grid rendering logic
│   │
│   ├── utils/                # Helper functions
│   │   ├── DateUtils.js
│   │   └── GenreService.js
│   │
│   └── index.js              # Application bootstrap
│
└── README.md                 # Documentation




---

## 🛠️ Features

- **Podcast Grid**: Dynamically renders podcasts from `data.js`.
- **PodcastCard Web Component**: Encapsulated UI for each podcast preview.
- **Modal Component**: Displays podcast details when selected.
- **Utilities**:
  - `DateUtils` for formatting dates.
  - `GenreService` for mapping genre IDs to names.

---

## 📖 Usage

- The grid displays podcasts from `src/views/data.js`.
- Clicking a podcast card dispatches a `podcast-selected` event.
- The modal opens with details of the selected podcast.

---

## ⚡ Troubleshooting

- **404 Not Found**: Check your import paths.  
  - From `src/views/index.js` → use `../component/...` and `../utils/...`.  
  - Folder is `component` (singular), not `components`.
- **Export errors**: Ensure each file exports what you import.  
  - Example:  
    ```js
    export class PodcastCard extends HTMLElement { ... }
    export { PodcastCard };
    ```
- **SyntaxError: Unexpected end of input**: Usually means a missing `}` or backtick in template strings.

---

## 📌 Principles

- **SRP (Single Responsibility Principle)**: Each module handles one concern.
- **Reusable Components**: Web Components (`PodcastCard`) are self‑contained.
- **Separation of Concerns**: Views, components, and utilities are split into folders.

---

## 📜 License

This project is for educational purposes.
