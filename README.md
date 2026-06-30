# 🎬 Movie Search App

A movie discovery app built with **React** that lets you browse and search movies using the **TMDB API**. It also features a trending movies section powered by **Appwrite**, which tracks real search activity to surface the most-searched titles.

🔗 **Live Demo:** [movies-app-kappa-rosy.vercel.app](https://movies-app-kappa-rosy.vercel.app/)

## Features

- 🔍 **Search movies** by title using the TMDB API
- ⚡ **Debounced search** — API calls are optimized to fire only after the user stops typing, avoiding unnecessary requests on every keystroke
- 🔥 **Trending movies** — tracks search terms in an Appwrite database and displays the most frequently searched movies
- 🎨 Clean, responsive UI for browsing movie posters and details

## Tech Stack

- **React** — UI and component logic
- **Vite** — build tool and dev server
- **TMDB API** — movie data source
- **Appwrite** — backend database for tracking and storing search counts

## How it works

1. Users type a movie name into the search bar.
2. The input is **debounced**, so the app waits until the user pauses typing before querying the TMDB API — this avoids spamming the API on every keystroke and prevents race conditions between overlapping requests.
3. Each successful search updates a record in an **Appwrite** database — either incrementing the count for an existing search term or creating a new one.
4. The trending section reads from this database and displays the movies with the highest search counts, giving a live view of what's currently popular among users.

## Learnings

This project was a practical exercise in:
- Working with external REST APIs and handling async data fetching in React
- Implementing debouncing to optimize network calls
- Integrating Appwrite as a lightweight backend for persisting and querying data
- Managing environment variables securely for API keys
