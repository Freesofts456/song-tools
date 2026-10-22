# Song Tools

A small static website with two tools. There is no build step and no server code.

- `index.html` is the home page.
- `chord-shift/` is a chord transposer (chords above lyrics or ChordPro).
- `swara-sketch/` generates a playable melody for Sinhala lyrics.

Each tool is one self-contained HTML file with its CSS and JavaScript inside it.

## Run it on your computer

Open a terminal in this folder and run:

    python3 -m http.server 8000

Then open http://localhost:8000 in a browser. (Opening `index.html` by double-clicking also works, but the folder links work best through a server.)

## Put it online for free with GitHub Pages

1. Create a new public repository on GitHub, for example `song-tools`.
2. Upload everything in this folder to the repository (Add file, then Upload files).
3. Open Settings, then Pages. Under Branch choose `main` and `/ (root)`, then Save.
4. After a few minutes the site is at `https://YOUR-USERNAME.github.io/song-tools/`.

Choose your GitHub username before publishing, because it becomes part of the address.

Cloudflare Pages and Netlify also work: drag this whole folder into their upload page.

## Change things

- Colours and fonts are CSS variables at the top of each file's `<style>` block.
- Sample songs for Chord Shift are in the `SAMPLES` array near the end of `chord-shift/index.html`.
- Scales, ranges and melody rules for Swara Sketch are in the `Core` section of `swara-sketch/index.html` (`MODES`, `RANGES`, `contour`, `genLine`).

## Notes

- Fonts load from Google Fonts, so visitors need an internet connection.
- Pasted chord sheets and lyrics stay in the visitor's browser. They are saved only in that browser's local storage.
- Only add songs to a public library if they are public domain or you have permission. Visitors pasting their own sheets is fine because nothing is stored on your site.
- Swara Sketch builds melodies from rules, not a trained model.

## Ideas for later

- Export the melody as a MIDI file (works on a hosted site, not inside a sandboxed preview).
- Save songs to an account using a free backend such as Supabase or Firebase.
- Add more scales or rhythm patterns from Sri Lankan folk and baila styles.
