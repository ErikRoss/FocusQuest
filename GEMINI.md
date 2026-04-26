# FocusQuest Project Rules & Mandates

## Project Overview
**FocusQuest** is a gamified task and time tracker with RPG elements. It is designed to be ADHD-friendly and built with a lightweight "all-in-one" approach.

## Technical Stack
- **Frontend**: HTML5, CSS3, Vanilla JavaScript (ES6+).
- **Styling**: Tailwind CSS (via CDN) and custom CSS in `<style>` blocks.
- **Icons**: FontAwesome.
- **Backend/Cloud**: Firebase Auth & Firestore (Compat version).
- **PWA**: Custom Service Worker (`sw.js`) and dynamic manifest generation.

## Foundational Mandates
1. **Single-File Architecture**: Most of the application logic, styles, and HTML structure reside in `index.html`. When making changes, ensure they are integrated into this file unless a modular approach is explicitly requested.
2. **RPG Theme**: Every feature or UI element should align with the RPG aesthetic (Hero Panel, Quests, Worlds, Bosses, Potions, etc.).
3. **i18n (Internationalization)**: The app supports Ukrainian (uk) and English (en). Always update the `translations` object in `index.html` when adding or modifying text. Use the `data-i18n` and `data-i18n-title` attributes in HTML.
4. **Vanilla JavaScript**: Prefer modern Vanilla JS over external libraries for core logic.
5. **State Management**: The app uses a global `state` object persisted in `localStorage` and synced with Firebase. Always use `saveData()` and `renderAll()` after state mutations.
    - `state.workLog`: Stores precise work sessions `{ date, projectId, taskId, subtaskId, duration, amount }` for accounting and reports.
6. **Mobile First**: Ensure the UI remains responsive and usable on small screens (max-width 7xl layout).

## Development Workflow
1. **Research**: Check `CHANGELOG.md` and `ROADMAP.md` before proposing new features.
2. **UI consistency**: Follow existing Tailwind patterns and the "Glassmorphism" card style (`glass-card` class).
3. **Sound Effects**: Use the `sfx` object for interactive feedback.
