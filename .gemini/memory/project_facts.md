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
- **Tabbed Navigation**: 3-tab layout (Hero, Adventures, Stats).
- **Hero Tab**: Contains Hero Panel, Shop, and Logs (with settings and cloud status). Visible ONLY when active.
- **Adventures Tab**: Task tracker with project/task/subtask management and active timer.
- **Stats Tab**:
    - Dashboard with 6 counters.
    - Pure CSS Bar Charts for 7-day productivity/profitability.
    - Advanced Report with 3-column control layout:
        1. Project & Quick Filters (Today, Yesterday, Week).
        2. Start & End Datetimes (stacked).
        3. Generate & Export buttons (stacked).
- **Navigation State**: Active tab is persisted in `localStorage` under `focusquest_active_tab`.

## External Integrations
- **Firebase**: Uses Compat version (v10.8.1). Integrated in `index.html`.
- **Environment Variables**: Expected in `env.js` (not committed).

## PWA
- Manifest is dynamically generated via `injectPWA()` function.
- Service Worker defined in `sw.js`.
