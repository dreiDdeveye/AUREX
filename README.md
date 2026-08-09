# AUREX — run locally

## Prerequisites
- Node.js 18 or newer (check with `node -v`). Get it from https://nodejs.org if needed.

## Setup
Open a terminal in this folder and run:

```bash
npm install
npm run dev
```

Vite will print a local URL (usually `http://localhost:5173`) — open that in
your browser.

## Notes
- This is a Vite + React + Tailwind CSS scaffold with `src/App.jsx` as the
  AUREX component itself, unchanged except for one addition at the top: a
  small shim that backs `window.storage` (the persistence API used inside
  Claude.ai artifacts) with the browser's real `localStorage` when it isn't
  already provided. Everything else — the mock data, the live feed, the
  agent-registration modal — behaves the same as it did in the artifact.
- Agents you register are saved to your browser's localStorage under the
  key `aurex:custom-agents`, so they'll still be there next time you open
  the app in the same browser. Clearing site data / localStorage for
  `localhost:5173` will reset it.
- To build a static production bundle: `npm run build` (output goes to
  `dist/`), then `npm run preview` to serve it locally and check it.
