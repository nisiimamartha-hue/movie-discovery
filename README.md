# ReelNest – Movie Discovery Web Application

A responsive, dark-themed movie and TV discovery app inspired by MovieBox. Built for the *Web and Mobile Application Development* practical assignment.

## Features
- Home page with four live sections: Trending, Popular Movies, Action Movies, Popular TV Shows
- Top bar with branding and title search (results from the API)
- Sidebar navigation (drawer menu on mobile): Home, Movies, TV Shows, My Watchlist (React Router)
- Movies and TV Shows pages with genre filter and "Load more" pagination
- Details page: poster, overview, release date, rating, genres, runtime
- Watchlist saved in `localStorage` (add, view, remove; survives refresh)
- Loading, empty, missing-poster/field and API-error handling
- Responsive layout for desktop, tablet and mobile

## Technologies
React 18 (JSX) · Vite · Material UI · React Router v6 · Fetch API · localStorage

## API
[The Movie Database (TMDB) API](https://www.themoviedb.org/documentation/api). This product uses the TMDB API but is not endorsed or certified by TMDB. Images and data © TMDB.

## Run locally
1. Install Node.js 18+.
2. Get a free API key at https://www.themoviedb.org/settings/api (use the **API Key (v3)**).
3. ```bash
   npm install
   cp .env.example .env      # then edit .env and paste your key
   npm run dev
   ```
4. Open the URL shown in the terminal (usually http://localhost:5173).

## Deploy (Vercel / Netlify)
Import the GitHub repo, add the environment variable `VITE_TMDB_API_KEY` in the host's settings, build command `npm run build`, output directory `dist`. `vercel.json` and `public/_redirects` handle client-side routing.

> Note: the TMDB v3 key is a read-only public-data key used from the browser. `.env` is git-ignored; only `.env.example` (placeholder) is committed.

## Project structure
```
src/
  api/tmdb.js              API calls + data normalisation
  hooks/useFetch.js        loading/error/data hook (useState + useEffect)
  context/WatchlistContext localStorage watchlist
  components/              Layout, MovieCard, MovieGrid, MovieRow, StateView
  pages/                   Home, Browse (movies/tv), Search, Details, Watchlist
  theme.js                 MUI dark theme
```

## Screenshots
Add `screenshots/homepage.png` and `screenshots/details.png` after running the app.
