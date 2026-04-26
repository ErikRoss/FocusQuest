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
- **Reporting**: `renderReport()` and `exportFilteredCSV()` process `state.workLog` to calculate pure financial earnings (rate * time), separate from RPG gold bonuses logged in `state.logs`.

## UI Components
- **Tabbed Navigation**: 3-tab layout (Hero, Adventures, Stats) managed by `switchTab(tabId)`.
- **Consistency**: All tabs (`#tab-hero`, `#tab-adventures`, `#tab-stats`) are top-level `.tab-content` sections with `space-y-6` for consistent vertical spacing.
- **Hero Tab**:
    - **Row 1 (Grid)**: 
        - **Hero Panel**: Displays Level, HP/XP bars, Gold/Multiplier. Features Achievements button (top-left) and Streaks (top-right).
        - **Adventure Log**: Contains event logs and header with settings (Lang, Theme, Sound, Auth) and Cloud Status badge.
    - **Adventure Log Layout**:
        - **Desktop**: Title left, controls/status right in one row.
        - **Mobile**: Row 1 (Controls/Status right), Row 2 (Title centered).
    - **Row 2**: Guild Shop (2 columns for items).
- **Adventures Tab**: Task tracker with project/task/subtask management and active timer.
- **Stats Tab**:
    - Dashboard with 6 counters.
    - Pure CSS Bar Charts for 7-day productivity/profitability.
    - Advanced Report with control layout:
        1. Project (Multi-select) & Quick Filters (Today, Yesterday, Week, Month, Year).
        2. Start & End Datetimes.
        3. Generate & Export actions.
        4. Report table includes a Date column.
- **Navigation State**: Active tab is persisted in `localStorage` under `focusquest_active_tab`.

## External Integrations
- **Firebase**: Uses Compat version (v10.8.1). Integrated in `index.html`.
- **Environment Variables**: Expected in `env.js` (not committed).

## PWA
- Manifest is dynamically generated via `injectPWA()` function.
- Service Worker defined in `sw.js`.
