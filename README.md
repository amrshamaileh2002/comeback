# Second Draft

A one-file, private, cinematic letter. Open `index.html` on a phone and it plays as nine short chapters, ending in one question with three equal answers (Yes / Maybe / No) that send a prefilled WhatsApp message.

Everything lives in **`index.html`**: HTML, CSS, JavaScript, a soft piano loop composed for it, and (once you add them) your photos and your song. No build step, no server, no tracking.

## Edit it (5 steps)

1. Open `index.html` in any text editor. The **`SETTINGS`** block is near the top of the big `<script>` (search for `const SETTINGS`).
2. Replace every `[EDIT THIS: …]` with your own words. Facts only. Text goes between `` `backticks` ``; a blank line starts a new paragraph.
3. Double-click `index.html` to open it in your browser. A button in the bottom-left says **"N things to fill in"** and lists each missing setting by name. It only appears on your computer, never on the live site.
4. In that panel, the **Media packer** tab puts your photos (resized to 1600px WebP) and your song MP3 inside `index.html`. Choose this `index.html`, your photos in story order, and your song, then download the new file and replace the old one. Then write a short description of each photo in `photos`.
5. Paste the lyrics into `song.lyrics`, then use the **Time the lyrics** tab: press Start and tap at the start of each line. Copy the result back into `song.lyrics`.

Want Arabic? Set `language: "ar"` (the whole page turns right-to-left) and `arabicForm` to `"f"` or `"m"`. The Arabic wording lives in `words.ar`.

## Deploy on Netlify

1. Put `index.html` alone in a folder (for example `letter/`).
2. Zip the folder.
3. Go to [app.netlify.com](https://app.netlify.com) → **Add new site** → **Deploy manually**.
4. Drop the zip onto the page. Netlify gives you a link; send that.

Before you send it, open the live link on your own phone once: tap Begin, scroll to the end, and press each answer (you don't have to send anything).

## What's inside

| Chapter | What happens |
|---|---|
| Gate | "Turn your sound on." Music starts on the tap; every audio element is unlocked in that same tap. |
| Title page | The name rises in; a red pencil strikes *First* and writes *Second* above it. |
| I. Before anything | Sets expectations: nothing is asked until the last page. |
| II. How it started | Date, place, story, and one remembered detail in the margin. |
| III. What I kept | Photos as prints that develop as they scroll in. Tap for a full-screen viewer with swipe. |
| IV. Grade my homework | Things you know about them; they mark each Right / Wrong / Used to be with the red pencil. |
| V. Our song | Your song takes over from the background music, with synced lyrics; plays once, then hands back. |
| VI. What I got wrong | Tap each line: it's crossed out (not erased) and the correction is written underneath. |
| VII. What I'd like now | The letter on paper, and an optional ticket that tears to reveal the date. |
| VIII. One question | Yes / Maybe / No, identical and fixed. Each gets a complete, kind ending and a WhatsApp message. |

Six hidden easter eggs (name tapped 5×, date held, a word in the letter, opening at a set minute, swiping past the last photo, the pencil at the very bottom) show your inside jokes as pencil notes. Leave any of them as `[EDIT THIS…]` and it stays off on the live site.

## Notes

- Privacy: `noindex, nofollow`, `no-referrer`, no analytics. The only outside request is Google Fonts (with system-font fallbacks).
- iPhone ignores audio volume, so crossfades become clean cuts there. The sound button (top right) always pauses and resumes.
- Respects "Reduce motion": the page shows everything in place without animation.
- Keep the whole file under about 8 MB: roughly 10–15 photos plus a 3–4 minute song at ~112 kbps.
