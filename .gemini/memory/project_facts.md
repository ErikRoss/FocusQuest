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
- **Reporting**: `renderReport()` filters `state.logs` and `state.projects` based on datetime range.

## UI Components
- **Tabbed Navigation**: 3-tab layout (Hero, Adventures, Stats) managed by `switchTab(tabId)`.
- **Navigation State**: Active tab is persisted in `localStorage` under `focusquest_active_tab`.
- **Hero Tab**: Character panel, HP/XP bars, inventory, shop, and logs.
- **Adventures Tab**: Task tracker with project/task/subtask management and active timer.
- **Stats Tab**:
    - Dashboard with 6 counters (XP, Gold, Time, Quests, Bosses, Potions).
    - Pure CSS Bar Charts for 7-day productivity and profitability.
    - Advanced Report with Project and Datetime filtering + Filtered CSV Export.

## External Integrations
- **Firebase**: Uses Compat version (v10.8.1). Integrated in `index.html`.
- **Environment Variables**: Expected in `env.js` (not committed).

## PWA
- Manifest is dynamically generated via `injectPWA()` function.
- Service Worker defined in `sw.js`.
