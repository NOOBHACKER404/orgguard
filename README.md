# GUARDIAN / OrgGuard — Presentation MVP

This version keeps the original visual direction and adds a lightweight functional prototype layer:

- Real client-side routes using hash routing, so it works on GitHub Pages without server rewrites.
- Dedicated pages for Search, Profiles, Profile Detail, Organizations, Organization Detail, Verification, OrgGuard, About and Contact.
- Search reads sample records from `client/public/data/profiles.txt` and `organizations.txt`.
- Recent searches are stored in browser `localStorage`, similar to a lightweight Facebook-style recent-search interaction.
- Search results open dedicated record pages instead of modal-only views.
- Status filters and live search are functional.
- The TXT files are intentionally a presentation database mock. Replace them with an API/database later.

## GitHub Pages

1. Push this project to GitHub.
2. Run `npm install`.
3. Run `npm run build:client`.
4. Deploy the generated `dist/public` directory with GitHub Pages / GitHub Actions.
5. Because the app uses hash routing, routes remain functional on static hosting.

## Demo data

Edit these files to change what appears in the presentation:

- `client/public/data/profiles.txt`
- `client/public/data/organizations.txt`
- `client/public/data/search-history.txt` (reference/sample data; browser history is stored in localStorage)

Data format is pipe-separated:

`ID|Name|Role|Reference ID|Status|Note|Review Date|Department`

The next production step would be replacing the TXT loader with a real database/API and adding authentication and server-side authorization.
