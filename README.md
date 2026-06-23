# ClaudeDM — An AI Dungeon Master for Claude Code

ClaudeDM turns **[Claude Code](https://www.anthropic.com/claude-code)** into a persistent, simulationist **tabletop RPG Dungeon Master** (D&D-style). The entire game world — lore, kingdoms, NPCs, monsters, rules, character sheets and session logs — lives in this folder as plain **Markdown files**. The AI reads those files, runs the rules, narrates the world, and writes the results back to disk, so your campaign **persists across chats and sessions**.

> ⚠️ **Mature content (18+).** ClaudeDM is designed for adult fiction: graphic violence, crude language and explicit/sensual themes are part of the narration by design. Everything is fiction; all sexualized characters are adults. Don't use it if that's not what you want.

---

## What the AI does

When you boot it (see [Usage](#usage)), Claude acts as an **impartial, lethal Dungeon Master**:

- **Runs a full rules engine** (`ClaudeDM/Skills/dm_engine.md`): tiers, dice combat, damage and crits, advantage/disadvantage, encumbrance, crafting, loot and economy.
- **Narrates** a living world with sensory, uncensored adult prose, and gives every NPC its own voice driven by a psychological profile.
- **Keeps time**: an in-world clock (hour:minute) that advances based on how long actions logically take, on a custom calendar.
- **Tracks state**: world geopolitics, the timeline, players, NPCs and monsters — and **saves everything to files** so the game survives even when a chat fills up.
- **Navigates efficiently** using a knowledge-graph ("núcleos") protocol instead of re-reading everything, to save context/tokens.

---

## Key features / rules

- **Tier system (X → G):** every person, monster, material and item has a power tier, from `X` (god-like) down to `G` (children / harmless).
- **Difference-based combat:** both sides roll a d20; damage scales with the difference `X` (each point ≈ 20% of max damage). **Critical = max damage ×2** when the difference is double or more (`X ≥ 10`).
- **Advantage / disadvantage:** the DM applies a `+1/+2/+3` or `−1/−2/−3` modifier to any roll based on position, terrain, magic and physical state (tied, wounded, tired…).
- **Weight & encumbrance:** everything has a real weight in kg. Equipped/in-use gear is free; backpack items count against `Strength × 10 kg`. Money is weightless.
- **Materials & crafting by tier:** higher-tier materials are purer in mana and grant bigger stat/ability bonuses.
- **Monster tiers:** monsters don't level up. They have a **Cub (G)**, an **Adult** tier, and an **Alpha** form (after 10+ years, one rank higher), with an ability count that scales accordingly.
- **Custom calendar:** 13 months × 28 days (+1 intercalary day) and **5 seasons**, including **Luz de Luna Roja** — a season that intensifies monsters and raises every item's tier by +1.
- **Psychology-driven progression:** the DM fills a psychological profile of each character from how it's played; on tier-up you pick one of **3 abilities** generated from class + race + psychology.
- **Persistent, multiplayer-ready saves:** player sheets are saved per game as `Saves/<Name>_Log_P<n>.md` (`P0` = current game). Absent players' characters can be re-played by the DM as NPCs, in character.
- **Player-chosen language:** at character creation the DM asks which language to play in and uses it for the whole game (defaults to Spanish).

---

## Repository structure

```
DnD/
├── README.md                 ← this file
├── INICIAR_PARTIDA.md        ← the launcher prompt (paste it to start a game)
└── ClaudeDM/                 ← the system
    ├── CLAUDE.md             ← DM directives (tone, voice, time, working rules)
    ├── NUCLEOS.md            ← knowledge-graph map of the world (node index)
    ├── Skills/
    │   ├── dm_engine.md      ← the mechanical rules engine
    │   └── generador_procedural.md  ← procedural generation (random NPCs, loot, encounters)
    ├── WorldSaves/
    │   ├── world_state.md    ← geopolitics + the world map layout (canon)
    │   └── timeline.md       ← date, time, season, current game (P0), calendar
    ├── Saves/                ← player character sheets + template
    ├── NPCs/                 ← named NPC sheets + template
    └── Base_de_Datos/        ← the bestiary (per continent, the seas, and SSS legends)
```

> Note: the game content is written in **Spanish** (the world was authored in Spanish). The AI can still narrate the game in **any language** you choose at character creation.

---

## Requirements

- **[Claude Code](https://www.anthropic.com/claude-code)** — CLI, desktop app, web, or IDE extension.
- *(Optional)* **[Graphify](#optional-knowledge-graph)** + an LLM API key, if you want the automatic knowledge graph. The system works without it (it falls back to `NUCLEOS.md`).

No build step, no dependencies — it's all Markdown.

---

## Installation

```bash
# 1. Clone the repo
git clone https://github.com/ZeroOneKing/Claud-Code-DM.git

# 2. Open the project folder (DnD/) in Claude Code
#    e.g. open Claude Code with this folder as the project root
```

That's it. The game is the files.

---

## Usage

1. **Open Claude Code** with the `DnD/` folder (or `ClaudeDM/`) as the project root.
2. **Boot the DM:** open `INICIAR_PARTIDA.md`, copy its contents, and paste them as your first message. This tells Claude to load the rules, confirm the world state, and start.
3. **Pick a language:** the DM asks which language you want to play in.
4. **Create your character:** fill in the form the DM shows you (name, race, class, backstory, goal, abilities, gear, and your Strength / Active-Perception / Passive-Perception d20 rolls). Missing fields are not allowed — your character can't be created without them.
5. **Play.** Describe what you do; the DM narrates and asks for d20 rolls when needed.

### Player notation (out-of-character signals to the DM)

| You write | Meaning |
|---|---|
| `(text)` | Out-of-character message / dice declaration to the DM |
| `--text--` | Your character thinking to itself |
| `·text·` | An action |
| `-text-` | A secret thought shared only with the DM |
| `[text]` | Something very important to you |

### Saving & resuming

The DM writes progress to the files (`Saves/`, `timeline.md`, `world_state.md`). Because the campaign lives **on disk**, you never lose it: when a chat gets full, just **open a new chat and paste the launcher again** — it reloads the current state.

### Model tips

- **Playing:** a faster/cheaper model (e.g. Sonnet) with **low/medium thinking effort** lasts longer per chat.
- **Worldbuilding / heavy design:** a stronger model (e.g. Opus) with higher effort gives richer results.
- Keep the boot light: the DM should load only the core rules + timeline, and read a bestiary **only** when an encounter happens — not all of them at once.

### Optional: knowledge graph

For large worlds you can generate an automatic knowledge graph with Graphify (requires an LLM API key):

```bash
export ANTHROPIC_API_KEY="your-key"   # or GEMINI_API_KEY / OPENAI_API_KEY ...
cd ClaudeDM
graphify .            # build the graph
graphify . --update   # refresh after changes
```

Without it, the AI uses `ClaudeDM/NUCLEOS.md` as the world map.

---

## License

Released under the **Creative Commons Attribution-NonCommercial 4.0 International (CC BY-NC 4.0)** license — see [`LICENSE`](LICENSE).

In short: **use it, share it, modify it freely — just give credit and don't use it commercially** (no selling it or using it primarily to make money). Full terms: https://creativecommons.org/licenses/by-nc/4.0/

## Disclaimer

Unofficial fan project. Not affiliated with or endorsed by Anthropic or Wizards of the Coast. "D&D" and related marks belong to their respective owners. For adults only.
