# MADFAM Strategy Center (Centro de Estrategia)

A lightweight, bilingual, mobile-first dashboard designed for strategic planning, compliance tracking, and financial resource management in Morelos, Mexico (2025-2026).

## 📱 Features

* **Bilingual Support (ES/EN):** Instant language toggling between Spanish (default) and English.
* **Persistent Checklist:** A "To-Do" system that saves progress to the browser's `localStorage`. Tasks are tracked by ID, allowing the language to change without losing progress.
* **Zero-Build Architecture:** Built as a single `index.html` file using React and Tailwind via CDN. No `npm install` or build steps required.
* **Dark Mode:** Automatically detects and adapts to the user's system color scheme.
* **Mobile-Optimized:** Designed with "Safe Area" padding and touch-friendly interactions to feel like a native app on iOS and Android.

## 🚀 Quick Start

### Running Locally

1. Download the `index.html` file.
2. Open it in any modern web browser (Chrome, Safari, Edge, Firefox).
3. That's it!

### Deployment

Because this is a static single file, you can host it anywhere:

* **GitHub Pages:** Upload to a repo and enable Pages.
* **Netlify/Vercel:** Drag and drop the file.
* **S3/Storage:** Upload as a static public file.
* **Local Network:** Put it on a shared drive or local server.

## 🛠 Tech Stack

* **React 18:** Loaded via UMD CDN for UI logic.
* **Tailwind CSS:** Loaded via CDN for styling.
* **Babel Standalone:** Compiles JSX in the browser on the fly.
* **Phosphor/Lucide style Icons:** Embedded as inline SVGs for zero dependencies.

## ⚙️ Customization

### Editing Content

All text content is stored in the `CONTENT` constant at the top of the script. To change deadlines, loans, or warnings:

1. Open `index.html` in a text editor (VS Code, Notepad++, etc.).
2. Locate `const CONTENT = { ... }`.
3. Edit the text inside `es` (Spanish) or `en` (English).

### Modifying the Checklist

The checklist logic uses IDs to track completion.

* **Adding items:** Add a new object to the `todos` array in both language sections. **Ensure the `id` is unique.**
* **Warning:** If you change an existing item's `id`, users will lose their saved progress for that specific item.

## 📁 Project Structure

```text
/
└── index.html  # Contains HTML, CSS Config, React Logic, and Data
````

## 🔒 Privacy & Data

  * **Data Persistence:** All checklist progress is stored locally on the user's device (`localStorage`).
  * **No Analytics:** This app does not contain any tracking or external analytics scripts by default.
  * **No Backend:** The app functions entirely client-side.

## 📄 License

This project is open-source and available for internal or private use.
