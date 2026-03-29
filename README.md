# WORDY

A Wordle-style word-guessing game built with vanilla JavaScript.

## How to Play

- Guess the hidden 5-letter word in 6 tries
- After each guess, tiles show how close you were:
  - **Blue** — correct letter, correct position
  - **Gold** — correct letter, wrong position
  - **Gray** — letter not in the word
- Only valid English words are accepted as guesses

## Running Locally

No build step needed. Just open `index.html` in a browser:

```bash
open index.html        # macOS
xdg-open index.html    # Linux
start index.html       # Windows
```

Or serve it with any static file server:

```bash
npx serve .
python3 -m http.server
```

## Word Lists

- **Answers** (~2,300 words): curated common 5-letter words embedded in `index.html`
- **Valid guesses** (~14,000 words): loaded from the `words` file via GitHub raw + AllOrigins CORS proxy, cached in `localStorage` for 1 year

If the extended word list fails to load (network unavailable), the app falls back to the answer pool as the valid-guess list.

## Features

- 6×5 game board with flip animations
- On-screen QWERTY keyboard with color-coded feedback
- Statistics tracking (games played, win %, streaks, guess distribution)
- Share results as an emoji grid
- Persistent stats via `localStorage`
- Responsive layout that works on mobile and desktop

## License

MIT — see [LICENSE](LICENSE)
