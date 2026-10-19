# Piano Pals

A play-along piano app for children aged 4–6, built for iPad. Notes fall down a "waterfall" lined up with the keys and stop at the line until your child presses the right key.

## Put it on the iPad

A PWA has to be served over HTTPS. Any static host works; no server code is needed.

1. Upload the contents of this folder to a static host, for example:
   - **Netlify Drop**: drag the `piano-pals` folder onto app.netlify.com/drop
   - **GitHub Pages**: push the files to a repository and turn on Pages
   - **Cloudflare Pages**, **Vercel**, or your own web server
2. Open the address in **Safari** on the iPad.
3. Tap **Share → Add to Home Screen**.

It then opens full screen from its own icon and works offline. Saved MIDI songs stay on that iPad (in the app's own storage).

To try it on a computer first: `python3 -m http.server 8000` in this folder, then open http://localhost:8000.

## What's inside

| File | Purpose |
| --- | --- |
| `index.html` | The whole app (UI, MIDI parser, synth, waterfall) |
| `manifest.webmanifest` | Name, colors and icons for Add to Home Screen |
| `sw.js` | Service worker that caches the app for offline use |
| `icons/` | Home Screen and app icons |

## Playing

- **Touch keys**: tap the on-screen piano; multi-touch chords work.
- **USB / Bluetooth MIDI keyboard**: works in browsers with Web MIDI (Chrome, Edge, Firefox on desktop or Android; Web MIDI browser apps on iPad). Safari on iPad does not support Web MIDI yet.
- **Real acoustic piano**: turn on "Listen to a real piano with the microphone" in *For grown-ups*. Works best with one note at a time in a quiet room.
- **Computer keyboard** (for testing): `A W S E D F T G Y H U J K` play the keys starting from the leftmost C.

## Adding songs

Tap **Add a song** and pick a `.mid` / `.midi` file. Choose which parts (tracks) to play and either **One at a time** (top note only, best for small hands) or **All notes**. Tap **Parts** on a saved song to change this later.

Free, legal MIDI files: Mutopia Project (mutopiaproject.org) and the IMSLP / Piano-midi.de public-domain collections.

## Built-in songs

Hot Cross Buns, Mary Had a Little Lamb, Twinkle Twinkle Little Star, Old MacDonald, Jingle Bells, Ode to Joy (Beethoven), Lullaby (Brahms), Minuet in G (Petzold, long credited to Bach), Für Elise (Beethoven), Prelude in C (Bach). All are public-domain compositions arranged as simple right-hand melodies for this app.
