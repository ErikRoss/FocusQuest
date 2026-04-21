# FocusQuest Project Facts

## Core Logic & State
- **Main State Object**: `state` (defined in `index.html`).
- **Persistence**: `localStorage` key `focusquest_v2`.
- **Leveling Formula**: `calculateLevel(totalXp)` uses a base of 1000 XP and increases by 400 XP per level.
- **Hero Classes**: 
    - `warrior`: -50% HP penalty damage.
    - `mage`: +15% XP bonus.
    - `rogue`: +20% Gold bonus.
- **Currencies**: Gold (🪙) and XP.

## UI Components
- **Hero Panel**: Displays Level, HP, XP, Gold, Streak.
- **Active Timer**: Shows the current task being tracked.
- **Shop**: Guild Shop for buying potions.
- **Worlds/Quests**: Main task management area with Boss battle toggle.

## External Integrations
- **Firebase**: Uses Compat version (v10.8.1). Integrated in `index.html`.
- **Environment Variables**: Expected in `env.js` (not committed).

## PWA
- Manifest is dynamically generated via `injectPWA()` function.
- Service Worker defined in `sw.js`.
