# Ocarina Coach

A single-page trainer for a 3D-printed ocarina. Everything lives in `index.html`; there is no build step.

- **3D model** of a transverse ocarina (12- or 10-hole). Drag to turn it, use *Underside* for the thumb holes. Gold means cover the hole.
- **Calibrate** each fingering for your own print. With the microphone on, the page detects the pitch you play, saves it, and moves to the next fingering once the note is steady. You can also pick notes by hand or match them by ear with the pitch slider.
- **Chart** of every note your ocarina plays, lowest to highest, with a diagram per fingering.
- **Songs**: unlock a song by entering the button sequence the game shows you. Each button is mapped to its pitch (L = D5, R = F5, A = A5, Y = B5, X = D6; N64: A, ▼, ▶, ◀, ▲) and then to your calibrated fingering. *Key shift* and *Auto-fit* move songs onto the notes your ocarina actually has. With *Listen* on, the song advances when you play the right note.
- **Holes**: move, resize, add or remove holes so the model matches your print.

Your setup is stored in the browser (`localStorage`). Use *Holes → Backup* to move it to another device.

## Hosting

The microphone only works over https, so serve it from GitHub Pages:

1. Repository **Settings → Pages**.
2. *Source*: **Deploy from a branch**, branch **main**, folder **/ (root)**, then **Save**.
3. After a minute the page is live at `https://trnk27.github.io/ocarina-coach/`.

To try it locally: `python3 -m http.server` in this folder, then open `http://localhost:8000` (browsers allow the microphone on localhost).
