# Recovery Mad Libs 2 — Second Edition

A long-form, hilarious, **recovery-themed Mad Libs** game for groups. Ten (10) skit-length stories, each designed for **3 patients + 2 staff**, packed with buzzwords, catchphrases, and absurd objects. Runs entirely in the browser — no dependencies, no build step.

## ✨ Features
- **10 full stories**, each 3–5 paragraphs (~15+ sentences) for true “mini-skit” energy
- **3 Patients + 2 Staff** placeholders in every story (consistent roles across the set)
- **Auto-generated input fields** (fill once, used everywhere in that story)
- **Random Fill** suggestions for quick demos and extra laughs
- **Copy Output** button for pasting into slides or printouts
- **Single-file app** (`index.html`) — just open it

## 🚀 Quick Start
1. Create a new repository named **`recovery-madlibs-second edition`** (exact as you prefer — GitHub will normalize spacing).
2. Add the two files from this release:
   - `index.html`
   - `README.md`
3. On GitHub, enable Pages (if you want a web link):
   - Settings → Pages → Source: `Deploy from a branch` → select the branch → folder `/root` → Save.
4. Open `index.html` locally or via your Pages URL — start playing.

> No external libraries or CDNs. Everything is inline for reliability in group rooms with spotty Wi‑Fi.

## 🧩 How It Works
- The app keeps a list of stories (title + paragraphs) with **`{{placeholders}}`** embedded.
- When you pick a story, the UI **parses all placeholders** and generates one input per **unique** placeholder.
- Clicking **Generate Story** replaces all placeholders and prints the formatted story with paragraphs.

### Common Placeholders
- `{{patient1}}`, `{{patient2}}`, `{{patient3}}`, `{{staff1}}`, `{{staff2}}`
- `{{buzzword}}`, `{{recovery_concept}}`, `{{catchphrase}}`
- `{{funny_object}}`, `{{object}}`, `{{plural_noun}}`, `{{noun}}`
- `{{verb}}`, `{{verb_ing}}`, `{{adjective}}`
- Specialty: `{{higher_power}}`, `{{funny_liquid}}`, `{{drink}}`, `{{location}}`, `{{funny_song}}`, `{{weird_food}}`, `{{color}}`, `{{body_part}}`, `{{phrase}}`, `{{bad_habit}}`, `{{funny_event}}`, `{{funny_recovery_concept}}`, `{{animal}}`

> Tip: You only fill each placeholder once per story; repeated uses auto-populate for running jokes.

## 🧠 Recovery Buzzword Seeds
The **Random Fill** feature includes suggested values like:
- `radical acceptance`, `HALT`, `pink cloud`, `urge surfing`, `distress tolerance`, `CBT worksheet`, `accountability buddy`, `mindful breathing`, `dopamine detox`, `SMART goal`, `gratitude list`, `values in action`, `opposite action`, `higher power`

You can edit these lists inside the `<script>` section: see `const pools = { ... }`.

## 🛠️ Customize / Extend
- To **add a story**, append an object to the `stories` array in `index.html`:
  ```js
  {
    key: "unique-key",
    title: "Display Title",
    meta: "short description",
    paragraphs: [
      "Your first paragraph with {{placeholders}}.",
      "More paragraphs..."
    ]
  }
  ```
- To **add new placeholder types**, add a field in the `fields` map with a `label` and (optional) suggestion generator.

## 🧪 Accessibility & Offline Use
- Keyboard-friendly: `Tab` through inputs; **Copy** uses the Clipboard API with a fallback.
- Works 100% offline — ideal for facilities with limited internet.
- High-contrast, large click targets, and a responsive layout for TVs or projector screens.

## 📄 License
MIT — use, remix, and adapt for your facility. No attribution required, but a shoutout is always appreciated.

---

Made with care for real group rooms. If anything feels off, open an issue with your wish list and I’ll tune it.
