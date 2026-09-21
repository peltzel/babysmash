# Baby Smash

A web page you can hand to a baby: every key press or tap makes a big colourful shape, and nothing on your computer gets broken.

Live at **https://babysmash.app**

Made by a dad whose kid kept closing his browser tabs. It is a toy, not a teaching tool — a digital pot and wooden spoon.

## What it does

- Every key press shows a large coloured shape with the letter on it (or a random symbol for keys like Shift and Enter).
- Clicks and taps make a burst of coloured dots. Moving the mouse or dragging a finger leaves a fading trail. Several fingers at once all work.
- An animal, vehicle or toy emoji pops up somewhere on screen every 5 to 12 seconds, wiggles, and disappears.
- Optional sound: a random note from the C major scale, or a "pop", on each key press. Made in the browser; there are no audio files.
- A Fullscreen button. If the baby knocks the page out of fullscreen, a "tap anywhere to continue" screen puts it back.
- The page swallows key presses, including Ctrl and Cmd combinations where the browser allows it. It cannot block shortcuts owned by the operating system. On an iPad, turn on Guided Access first.
- Press **Esc three times within a second** to open the grown-up settings: colour theme (rainbow, ocean, forest, space, high contrast), sound, shape size, background (stars, sparkles, snow, bubbles, hearts), a count of keys and clicks, session time, and an exit button.

## Run it locally

There is nothing to build. It is four plain HTML files with the CSS and JavaScript inside them.

```bash
npm start        # runs "npx serve ." and prints a local address
```

Or just open `index.html` in a browser. You need Node only for `npm start`.

The live site is hosted on Vercel. `vercel.json` adds three security headers and nothing else.

## Files

| File | What it is |
|------|------------|
| `index.html` | Landing page with the "Start Smashing" button |
| `app.html` | The toy itself — all the shapes, sounds and settings |
| `research.html` | A plain summary of screen-time guidance for under-fives, with sources |
| `privacy.html` | Privacy policy |
| `package.json` | Only holds the `npm start` script; there are no dependencies |
| `vercel.json` | Hosting settings (security headers) |

## Privacy

There are no accounts and no ads, and the page does not record which keys are pressed.

Every page loads Google Analytics. It records page views, device type, rough location (country or region), how long a session lasted, and milestone events from the toy: the 10th, 50th, 100th and 500th key press, and the total count when you leave. The full policy is in `privacy.html`. If you run your own copy, remove or replace the Google Analytics tag at the top of each HTML file.

## Licence

MIT — see [LICENSE](LICENSE).
