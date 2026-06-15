<div align="center">

# 🌟 Hearthmon — You Don't Build Alone

> *A warm Pokémon-inspired companion that quietly grows beside you while you build.*

</div>

---

## ✦ What is Hearthmon?

**The companion that quietly stays while you build hard things.**

A Pokémon that lives in the corner of your screen while you code — but it's not a pet that begs for attention, and it's definitely not another productivity tracker. The unusual part:

> **it notices *how* you build, not just *that* you did.**

It feels the texture of a session. It goes quiet when you drop into flow, sits a little closer when you've been wrestling the same bug for an hour, and celebrates the commit that *finally cracked it* — not the typo-fix. It remembers the seasons you lived through — the late nights, the projects you stuck with — and brings them back, gently, weeks later. It even keeps watch while your model trains.

No guilt. No streaks. No hustle. Just presence.

### What it does
- 🌱 **Quiet presence** — lives beside you; never nags, never shames, never breaks focus
- 🧠 **Notices the process** — flow · friction · breakthrough, inferred from privacy-safe
  signals (never your keystrokes, screen, or code)
- ⛏️ **Stays alongside the work** — git commits, long-running projects, even ML training runs
- 📖 **Remembers what mattered** — milestones, hard seasons, the day you shipped something real
- 🌧️ **Lives in time** — shifts with your mood, the weather, and the hour; dreams while it sleeps
- 🎵 **Vibes with your music** — subtly reacts to your system audio with gentle bobs and beat pulses (opt-in, no audio recorded)
- 🎙️ **Has a soul of its own** — character-inspired voice, tiny battles, and a personality
  that quietly *drifts* from how you treat it — so your companion becomes unlike anyone else's

---

## ✨ What Hearthmon Feels Like

It's 2:14 AM.

You've been fighting the same bug for an hour.

Your companion quietly shifts a little closer.

No notification.

No streak warning.

Just:

*"Still here."*

Weeks later, after finally shipping:

*"You really fought for this one."*

Hearthmon remembers the hard nights — and stays.

---

## 📸 A Look Inside

> **Note:** *Insert your GIFs and screenshots here to bring the magic to life.*

- `![Classic vs Alive Mode Renderers](docs/placeholder.png)`
- `![Type Habitat Visuals](docs/placeholder.png)`
- `![Sleep State & Late Night Mode](docs/placeholder.png)`
- `![An Emotional Memory Unlocked](docs/placeholder.png)`

---

![Product Map](product-map.png)



## 🧭 Why Hearthmon?

Building hard things is lonely.

Hearthmon is a fully-local desktop companion for builders — a quiet Pokémon-inspired presence that notices your workflow, remembers your journey, and grows beside you over time.

**No streaks. No guilt. No cloud. Just presence.**

### Highlights
- 🧠 **Memory-driven emotional system**
- 🌙 **Quiet workflow awareness**
- 🎨 **Dual renderer** (Classic CSS + Alive/Pixi.js)
- 🔒 **100% local & privacy-first**
- ⚔️ **1025 companions + habitats**

---

## 🏆 Why This Project Matters

Hearthmon explores a question:

*Can software feel emotionally supportive without becoming addictive, invasive, or demanding?*

It combines:
- **Systems design**
- **Human-centered product thinking**
- **Local-first architecture**
- **State machines**
- **Desktop graphics (Pixi.js)**
- **Rust + Svelte + SQLite**

---

## 🎯 Problem Statement & Design Goals

Existing productivity systems suffer from constant notifications, guilt-inducing streaks, and massive privacy concerns regarding screen reading. This leads to anxiety when falling behind on arbitrary goals.

**Hearthmon's Non-Negotiable Rules:**
- **Presence Over Productivity:** Silent, comforting companionship that doesn't require constant interaction.
- **Privacy-First (100% Local):** All memories, moods, and awareness data stay firmly on your machine in a local SQLite database.
- **Memory Over Motivation:** Using your actual past experiences (wins, survived struggles) to encourage you on hard days.
- **Low Overhead:** A lightweight (~10MB) native window that stays completely out of the way.

---

## 💡 Key Innovations

1. **Quiet Awareness Engine**  
   → Senses your flow vs. friction based solely on foreground app names (no keystrokes/code reading). It sits closer when you're stuck on a bug and stays quiet in deep flow.

2. **Emotional Memory System**  
   → Instead of generic advice, it surfaces a specific mood or struggle you logged weeks ago, proving you've survived hard days before ("We've been here before").

3. **Two-Tier Rendering Architecture**  
   → Seamlessly switch between a cozy CSS "Classic" renderer and a premium Pixi.js "Alive" renderer (with particle effects, dynamic lighting, and habitats) sharing the exact same underlying emotional brain.

---

## 🧠 Why This Works

Traditional approaches try to be human-like chatbots, optimizing for active screen time. 

This system succeeds because it models **patience**. It dozes off when ignored. The relationship grows authentically across 6 stages (Stranger → Lifetime Companion) based on genuine time and check-ins. It offers gentle nudges (like burnout noticing) without clinical diagnoses.

→ **Result:** A digital companion that feels like a true ally, not a taskmaster.

---

## 🏗️ System Architecture

```text
[System Events / Foreground App Name]
   ↓
[Awareness Layer (Flow/Friction Detection)]
   ↓
[Memory-Driven Emotional System (SQLite)]
   ↓
[Renderer Layer (Classic CSS / Pixi.js Alive)]
   ↓
[Transparent Always-On-Top Tauri Window]
```

---

## 🧩 System Components

### 1. The Soul (Memory & Emotion)
- Manages the local SQLite `memories` and `meta` tables. Tracks mood check-ins, the "Good Things Jar", and letters to tomorrow.
- Computes bond depth and unlocks emotional milestones (badges like "Builder's Courage" or "Still Standing").
- Driven by a memory-driven emotional system (no LLM required, though an optional Claude/Ollama layer is planned).

### 2. The Habitat & Sprite Engine
- Fetches and caches data from PokéAPI for all 1025 Pokémon (sprites, cries, movesets, stats).
- Manages dynamic "Type Habitats" (e.g., moonlit shore, hearth) and ambient weather effects.
- Runs the 1v1 Battle Arena with real base stats and a full 18×18 type chart.

---

## 🧪 Experimental Insights

- **Silence is Golden:** Users prefer a companion that doesn't constantly talk or interrupt their workflow.
- **Nostalgia Drives Attachment:** Integrating authentic Pokémon cries and Ash voice clips significantly increases the perceived warmth of the companion.

**Conclusion:**
→ Emotional resonance in software comes from memory and restraint, not necessarily complex AI.

---

## ⚠️ Limitations & Failure Cases

### Limitations
- Currently Windows-only (relies on Tauri 2 and WebView2).
- Local voice cloning feature is currently blocked on Windows (XTTS v2 dependency issues).

### Failure Case Example

**Input:** `<User switches to a completely unknown foreground app for hours>`  
**Issue:** `The Awareness engine might not accurately detect 'flow' vs 'friction' if the app isn't recognized, defaulting to passive presence.`

---

## 🚀 Deployment Scenarios

- **Solo Hackathons:** A silent partner during long, isolating coding sprints.
- **Daily Remote Work:** A desk companion that separates the feeling of "working alone" from "being alone."
- **Model Training:** Point it at a training log; it keeps watch while your model trains.

---

## 🔁 Reproducibility

- **Data Privacy:** Data never leaves `%APPDATA%/com.hearthmon.app/hearthmon.db`.
- **Customization:** The sprite layer (`src/lib/sprites.ts`) is swappable for original art.
- **Voice:** Drop custom MP3s into `static/voice/` for personalized sound bites (`go.mp3`, `<species>.mp3`).

---

## 📁 Repository Structure

```text
.
├── src/               # SvelteKit UI & App Logic
├── src-tauri/         # Rust backend, window management
├── static/            # Assets, voice clips, fallback images
├── docs/              # VISION.txt and product maps
├── tools/             # Voice cloning and processing scripts
└── README.md          # You are here
```

---

## ⚙️ Quick Start

### Setup
```bash
npm install
```

### Run
```bash
npm run tauri dev
```

### Build (Standalone .exe)
```bash
npm run tauri build
```

---

## 🌍 Impact

- Reduces the emotional toll of solo software development.
- Shifts the paradigm from "productivity at all costs" to "sustainable, supported building."

---

## 🔮 Vision

To build a companion that outlasts the machines it runs on—a quiet friend that holds the history of everything you've ever built, reminding you of the builder you are.

---

## 🏗️ Builders

<!--BUILDERS:START-->
✦ Hearthmon is quietly finding its first builders.
<!--BUILDERS:END-->

_Want a longer chapter? The first one's free — reach out for a builder pass. (Updated by hand from passes issued; nothing phones home.)_

---

### License & Use

Personal project. Pokémon sprites, cries, names, and any supplied/cloned voice audio are Nintendo / The Pokémon Company / voice-actor IP — **personal use only, never redistribute.**

🤖 Built with [Claude Code](https://claude.com/claude-code) & ❤️ by **Ansh Bajpai** ([@AnshBajpai05](https://github.com/AnshBajpai05)). 
*If it stays beside you — let Ansh know. 🌙*
