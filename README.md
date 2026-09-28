# 🎬 Movie Search Application

A sleek movie search web app built with React that lets you browse popular movies, search for titles, and save your favorites — all powered by [The Movie Database (TMDB)](https://www.themoviedb.org/) API.

---

## ✨ Features

- **Browse Popular Movies** — On launch, the app fetches and displays the current popular movies from TMDB.
- **Search Movies** — Search for any movie by title using the TMDB search API.
- **Favorite Movies** — Add or remove movies from your favorites list with a single click on the ♥ button.
- **Persistent Favorites** — Your favorites are saved to `localStorage`, so they survive page refreshes and browser restarts.
- **Client-Side Routing** — Seamless navigation between the Home and Favorites pages via React Router.

---

## 🛠️ Tech Stack

| Layer       | Technology                        |
| ----------- | --------------------------------- |
| Framework   | React 19                          |
| Language    | TypeScript                        |
| Build Tool  | Vite 8                            |
| Routing     | React Router DOM v7               |
| Styling     | Vanilla CSS                       |
| API         | TMDB (The Movie Database) REST API|
| Linting     | oxlint                            |

---

## 📁 Project Structure

```
Movie Search Application/
└── frontend/
    ├── public/               # Static assets (favicon, etc.)
    ├── src/
    │   ├── components/
    │   │   ├── MovieCard.tsx  # Individual movie card with poster & favorite toggle
    │   │   └── NavBar.tsx     # Top navigation bar (Home / Favorites)
    │   ├── contexts/
    │   │   └── MovieContext.tsx  # React Context for favorites state management
    │   ├── css/
    │   │   ├── index.css     # Global styles
    │   │   ├── App.css       # App-level styles
    │   │   ├── Home.css      # Home page styles
    │   │   ├── Favorites.css # Favorites page styles
    │   │   ├── MovieCard.css # Movie card styles
    │   │   └── Navbar.css    # Navbar styles
    │   ├── pages/
    │   │   ├── Home.tsx      # Home page — popular movies + search
    │   │   └── Favorites.tsx # Favorites page — saved movies
    │   ├── services/
    │   │   └── api.js        # TMDB API service functions
    │   ├── App.tsx           # Root app component with routes
    │   └── main.tsx          # Entry point — renders App into DOM
    ├── .env                  # Environment variables (not committed)
    ├── .gitignore
    ├── index.html            # HTML shell
    ├── package.json
    ├── tsconfig.json
    ├── tsconfig.app.json
    ├── tsconfig.node.json
    └── vite.config.ts
```

---

## 🚀 Getting Started

### Prerequisites

- **Node.js** (v18 or higher recommended)
- **npm** (comes with Node.js)
- A **TMDB API key** — get one for free at [https://www.themoviedb.org/settings/api](https://www.themoviedb.org/settings/api)

### 1. Clone the repository

```bash
git clone https://github.com/abhishekh1123/Movie-Search-Application.git
cd Movie-Search-Application/frontend
```

### 2. Install dependencies

```bash
npm install
```

### 3. Set up environment variables

Create a `.env` file in the `frontend/` directory:

```bash
touch .env
```

Add the following variables to it:

```env
VITE_API_KEY=your_tmdb_api_key_here
VITE_BASE_URL=https://api.themoviedb.org/3
```

| Variable        | Description                                                                                           |
| --------------- | ----------------------------------------------------------------------------------------------------- |
| `VITE_API_KEY`  | Your personal TMDB API key. Get one by creating a free account at [themoviedb.org](https://www.themoviedb.org/settings/api). |
| `VITE_BASE_URL` | The base URL for the TMDB v3 REST API. Keep this as `https://api.themoviedb.org/3`.                   |

> [!IMPORTANT]
> The `.env` file is listed in `.gitignore` and will **not** be committed to version control. Never share your API key publicly.

### 4. Start the development server

```bash
npm run dev
```

The app will start on `http://localhost:5173` (default Vite port). Open it in your browser.

---

## 📜 Available Scripts

| Script            | Command              | Description                        |
| ----------------- | -------------------- | ---------------------------------- |
| **Dev server**    | `npm run dev`        | Start Vite dev server with HMR     |
| **Build**         | `npm run build`      | Type-check & build for production  |
| **Preview**       | `npm run preview`    | Preview the production build       |
| **Lint**          | `npm run lint`       | Run oxlint on the codebase         |

---

## 🔑 API Reference

This app uses two TMDB endpoints:

| Endpoint                     | Description                              |
| ---------------------------- | ---------------------------------------- |
| `GET /movie/popular`         | Fetches the current popular movies       |
| `GET /search/movie?query=..` | Searches movies by title                 |

Full TMDB API docs: [https://developer.themoviedb.org/docs](https://developer.themoviedb.org/docs)

---

## 📄 License

This project is open source and available under the [MIT License](LICENSE).
