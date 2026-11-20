# Al-Mulk · Surah 67 Study Folio

An illuminated Qur'anic reading, audio recitation, linguistic root, and contemplation web application for **Surah Al-Mulk (Chapter 67, Verses 1–12)**.

Designed with a museum-editorial aesthetic—pairing **Amiri Quran** Uthmani calligraphy, **Cormorant Garamond** editorial display typography, and **Plus Jakarta Sans** interface controls—the application supports deep verse-by-verse study, structural reflection, and active memorization (Hifz).

---

## Key Features

### 1. Illuminated Folio (`01. Illuminated Folio`)
- **Dual Reading Modes**: Switch seamlessly between **Verse-by-Verse Study** cards and a **Continuous Mushaf** layout with traditional `﴿١﴾`–`﴿١٢﴾` verse medallions.
- **Word-by-Word Root Inspector**: Click any Arabic word across Verses 1–12 to inspect its transliteration, contextual meaning, grammatical form, and trilateral Arabic root. Selecting a root highlights all matching words across the passage.
- **Margin Commentary Rail**: Sticky study sidebar synchronized to the active verse, presenting classical Tafsir notes, rhetorical observations, key roots, and a `1–12` quick index.
- **Reading Customization**: Adjust Arabic script scale (`Standard`, `Large`, `Mushaf`), toggle English translation and transliteration, copy formatted verses to clipboard, and switch between **Archival Day** and **Nocturnal Mode** reading themes.

### 2. Audio Recitation & Guided Pace
- **Verse-by-Verse Audio Streaming**: Listen to Verses 1–12 with selectable reciters (*Mishary Rashid Al-Afasy*, *Mahmoud Khalil Al-Husary*, and *Abdul Basit Abdul Samad*).
- **Playback Controls**: Includes previous/next verse navigation, quick verse jump (`1–12`), repeat modes (`Repeat Off`, `Repeat Verse`, `Loop 1–12`), and playback speeds (`0.75×`, `1×`, `1.25×`).
- **Guided Reading Pace Fallback**: Automatically offers a timed contemplative auto-advance mode if audio streaming is unavailable offline.

### 3. Cosmic Architecture & Lexicon (`02. Cosmic Architecture`)
- **Four Thematic Movements**: Explores the structural progression of Verses 1–12 from *Absolute Sovereignty & Moral Trial* (vv. 1–2) and *The Flawless Architecture of Seven Heavens* (vv. 3–5) to *The Inhalation of Fire & Confession of Neglect* (vv. 6–11) and *Reverence in the Unseen* (v. 12).
- **Lexical Concordance**: Filter recurring Qur'anic root clusters (*Al-Baṣar*, *Al-Khalq*, *As-Sa‘īr*, *An-Nadhīr*, *Al-Ghafūr*) and jump directly to any verse in the Folio.

### 4. Hifz & Tadabbur Studio (`03. Hifz & Tadabbur`)
- **Hifz Recall Trainer**: Practice memorization with four concealment levels (*Full Text*, *Hide Verse Endings*, *First-Word Cues*, and *Blind Recall*) and tap-to-reveal per verse.
- **Persistent Progress & Journal**: Track verse mastery (`0–12`) and write personal Tadabbur reflections per verse—saved locally in `localStorage` with one-click **Export Notes (`.md`)**.

---

## Tech Stack

- **Framework**: React 19 + TypeScript
- **Build Tool**: Vite 8 (`@vitejs/plugin-react`)
- **Styling**: Tailwind CSS v4 (`@tailwindcss/vite`) with class-based dark mode (`@custom-variant dark`)
- **Icons**: Lucide React

---

## Project Structure

```text
├── index.html                   # HTML entry point & Google Fonts (Amiri Quran, Cormorant Garamond, Plus Jakarta Sans)
├── metadata.json                # Application metadata
├── package.json                 # Dependencies & Vite scripts
├── vite.config.ts               # Vite & Tailwind CSS v4 configuration
└── src/
    ├── index.css                # Tailwind v4 import, @custom-variant dark, & font utilities
    ├── main.tsx                 # React DOM entry point
    ├── App.tsx                  # Root layout, audio controller, theme & localStorage state
    ├── data/
    │   └── surahMulk.ts         # Verses 1–12 Arabic text, word tokens, roots, Tafsir, & movements
    ├── assets/images/           # Archival celestial & manuscript illustrations
    └── components/
        ├── Header.tsx           # Top navigation bar
        ├── AudioBar.tsx         # Recitation player & guided pace controls
        ├── FolioView.tsx        # 70/30 reading canvas & margin word/Tafsir inspector
        ├── ArchitectureView.tsx # Thematic movements & lexical root explorer
        ├── HifzTadabburView.tsx # Memorization trainer & Markdown-exportable journal
        └── ResilientImage.tsx   # Image wrapper with archival fallback state
```

---

## Local Installation & Setup

### Prerequisites
- **Node.js** (v18 or newer recommended)
- **npm** (included with Node.js)

### 1. Clone the Repository
```bash
git clone https://github.com/hunaizaasif/surah-e-mulk-app.git
cd surah-e-mulk-app
```

### 2. Install Dependencies
```bash
npm install
```

### 3. Start the Vite Development Server
```bash
npm run dev
```
The application will run locally at **http://localhost:3000** (configured in `package.json` via `vite --port=3000 --host=0.0.0.0`).

### 4. Type-Check & Build for Production
Run TypeScript verification:
```bash
npm run lint
```

Create an optimized production bundle in `dist/`:
```bash
npm run build
```

Preview the production build locally:
```bash
npm run preview
```

---

## Attribution

- **Qur'anic Text**: Surah Al-Mulk (67:1–12) in Uthmani script.
- **Audio Recitation**: Verse-by-verse MP3 streams courtesy of EveryAyah.
- **Persistence**: Theme preference, Hifz mastery status, and Tadabbur notes are stored locally in your browser via `localStorage`.
