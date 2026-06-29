# Color Conquest

A territory strategy game that makes AI behavioral profiles tangible. Students compete against four distinct AI archetypes on an 8×8 grid and reflect on how each one thinks — built as the hands-on intervention in a research study on AI literacy professional development for K–12 teachers.

**Live:** [xd2164.github.io/colorQuest](https://xd2164.github.io/colorQuest/)

---

## How to play

The board starts filled with 6 random colors. You own the **bottom-left corner** (👤); the AI owns the **top-right** (🤖).

Each turn, pick a color — your territory instantly absorbs every adjacent tile of that color, flood-filling outward from your edge. The AI does the same. First to claim **more than half the board** wins.

- **Hover** a color button to preview which tiles you'd gain before committing
- Each button shows **+N** — tiles actually reachable from your current position
- Place up to **3 towers** (🏰) on neutral tiles to block the AI's expansion path

---

## The 4 AI archetypes

| Archetype | Difficulty | What it does | Real CS concept |
|-----------|------------|-------------|-----------------|
| **Greedy** | Normal | Picks whichever color gives the most tiles right now, every turn | Greedy algorithm / reward maximization |
| **Predictive** | Hard | Simulates 2 turns ahead — weighs own gain and blocking the player | Minimax / lookahead search |
| **Adaptive** | Expert | Tracks your color picks and counters your tendencies each turn | Online learning / behavioral tracking |
| **Passive** | Easy | Picks mostly at random — no strategy, no learning | Random policy / baseline agent |

Switching archetypes mid-game (teacher mode) lets students compare behaviors live.

---

## Educational framework

Built around **DCR — Design, Create, Reflect**, the pedagogical structure from the accompanying research:

1. **Design** — choose your difficulty/archetype before playing ("What am I curious about?")
2. **Create** — play the game; the AI Coach panel annotates each move with which of the [AI4K12 Five Big Ideas](https://ai4k12.org/) is in play
3. **Reflect** — post-game journal with 3 structured prompts tied to the Big Ideas

### AI4K12 Five Big Ideas covered

| Big Idea | Surfaced by |
|----------|------------|
| 1 · Perception | The AI reads the full board state before every move |
| 2 · Representation & Reasoning | Every archetype scores all color options and selects by that model |
| 3 · Learning | The Adaptive agent updates its model of your behavior each turn |
| 4 · Natural Interaction | The AI Coach translates agent logic into plain language |
| 5 · Societal Impact | Towers = constraints; an unconstrained AI always wins — should it? |

---

## Teacher mode

Select **Teacher** on the welcome screen to unlock:

- **Live archetype switching** — change the AI mid-game to trigger comparison
- **Parameter sliders** — adjust exploration, aggression, risk tolerance, and learning rate in real time
- **Learning objectives panel** — all 5 Big Idea objectives in assessable language
- **Simulation log** — move-by-move record of AI decisions
- **Export session report** — downloads a `.txt` with AI archetype, game stats, and student reflection responses
- **Facilitation Guide** — built-in modal with:
  - 40-minute class period timing breakdown
  - Per-scenario discussion questions (opening → probe → bridge to real AI → closing design question)
  - DCR debrief questions for whole-class wrap-up
  - Assessment options (exit ticket, portfolio, discussion grade rubric)

---

## Design notes

The game uses `#2E74B5` (the manuscript's heading blue) as its primary UI color and AI player color, so the game and the research paper it belongs to read as a unified artifact.

The color gain counts on each button reflect **reachable** tiles from the player's current territory — not total tiles of that color on the board — to give accurate strategic information rather than a misleading raw count.

---

## Research context

> Du, X. (in preparation). *Teaching AI by Design: Preparing Educators to Integrate Generative AI Through Game-Based Learning.* Gates Foundation / AI for SPM.

The game is the primary classroom intervention in a 6-week professional development study with 24 K–12 teachers. The four AI archetypes are designed to make abstract ML concepts (greedy algorithms, minimax search, online learning, random baselines) directly observable and discussable without any prerequisite technical knowledge.

---

## Running locally

No build step. Open `index.html` in any modern browser.

```
git clone https://github.com/xd2164/colorQuest.git
open colorQuest/index.html
```
