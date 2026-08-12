# AGENTS.md

## Cursor Cloud specific instructions

This is a single-service [Create React App](https://create-react-app.dev/) TODO web app (`todo-application`). There is no backend, database, or other services.

- Runtime: Node.js (CRA `react-scripts` 5). Dependencies install via `npm install` (already run by the environment update script).
- Dev server: `BROWSER=none PORT=3000 npm start` serves the app at http://localhost:3000. `BROWSER=none` prevents `react-scripts` from trying to open a browser in the headless VM.
- Tests: `CI=true npm test` runs the Jest test suite once (without `CI=true`, `react-scripts test` starts an interactive watcher that never exits).
- Lint: there is no standalone lint script; `react-scripts` runs ESLint (config `react-app`) automatically during `npm start` and `npm run build`. Use `npm run build` for a one-shot lint+compile check.
- Note: `src/special-number.js` is intentionally unused (not imported anywhere), so it is not compiled by webpack and does not affect build/lint/test.
