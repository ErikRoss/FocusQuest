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
- **Persistent Header**: `header#hero-section` contains Hero Panel, Shop, and Logs. It remains visible across all tabs.
- **Responsive Header Layout**:
    - **Desktop**: Grid (2 cols). Hero | Logs in first row, Shop (2 cols) in second row.
    - **Mobile**: Flex-col. Order: Hero -> Shop -> Logs.
- **Tabbed Navigation**: Bottom Nav toggles visibility of `#tab-adventures` and `#tab-stats` below the persistent header.
- **Navigation State**: Active tab is persisted in `localStorage` under `focusquest_active_tab`.
- **Stats Tab**:
    - Dashboard with 6 counters.
    - Pure CSS Bar Charts for 7-day productivity/profitability.
    - Advanced Report with Project and Quick Date filters (Today, Yesterday, Week).

## External Integrations
- **Firebase**: Uses Compat version (v10.8.1). Integrated in `index.html`.
- **Environment Variables**: Expected in `env.js` (not committed).

## PWA
- Manifest is dynamically generated via `injectPWA()` function.
- Service Worker defined in `sw.js`.
