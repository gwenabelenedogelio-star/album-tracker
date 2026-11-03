# Album Tracker

Album Tracker is a React web app for searching albums, listening to short previews, saving them to a personal collection, rating them, and getting AI-generated album recommendations based on what you have saved and rated.

## Screenshot and Live Link

![Search Result](images/Screenshot%202026-11-03%20194540.png)
![Album Page](images/Screenshot%202026-11-03%20194532.png)
![Recommendation](images/Screenshot%202026-11-03%20194559.png)

- Live site: https://album-tracker-lake.vercel.app/

## Features

- Search for albums and tracks using the iTunes Search API
- Play 30-second previews
- Save albums to your collection
- Rate the albums in your collection
- Optional Deezer integration for playback
- AI-powered recommendations from Gemini, based on your rated albums
- Collection persists between visits in your browser

## Tech Stack

- React with Vite
- Context API for shared state
- iTunes Search API for album and track data
- Deezer for the optional playback integration
- Google Gemini API for recommendations
- Vercel for hosting

## Running Locally

1. Clone the repository:
   git clone https://github.com/gwenabelenedogelio-star/album-tracker.git
   cd album-tracker
2. Install dependencies:
   npm install
3. Create a file named `.env.local` in the project root (next to `package.json`) and add your own Gemini API key:
   GEMINI_API_KEY=your_key_here
   Get a key from [Google AI Studio](https://aistudio.google.com/apikey). Never commit this file; make sure `.env.local` is listed in `.gitignore`.
4. Start the dev server:
   npm run dev

## Limitations

- Previews are only 30 seconds long.
- Your collection is saved only in your browser (localStorage). Clearing site data or switching browsers or devices will lose it.
- Deezer requires you to log in to play full tracks.
- Recommendations depend on the Gemini API and may be unavailable if the key is missing or the quota is reached.

## Privacy Note

The AI recommendations feature sends the titles, artists, and ratings of albums in your collection to Google's Gemini API to generate suggestions. No account information or personal details are collected by this app, and nothing else from your collection is shared. Your collection itself is stored only in your own browser.

## Disclaimer

This project is for educational purposes and is not affiliated with, endorsed by, or sponsored by Apple, Spotify, Deezer, or Google. All product names, logos, and trademarks belong to their respective owners.