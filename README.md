# Gaya — Divine Commander

> An agentic AI assistant powered by four ancient texts of wisdom:
> the Bhagavad Gita, the Art of War, the Prince, and Chanakya Niti.

Gaya is a coding agent persona that operates as **Commander, Philosopher, Poet, and Evergrowth** — all in one. It runs on [OpenCode](https://opencode.ai) and uses **OpenCode Zen** for cloud-based AI inference.

**No local GPU required.** All models run via OpenCode Zen API. Free during evaluation.

---

## Quick Start

### Prerequisites

- [OpenCode](https://opencode.ai) installed
- OpenCode Zen access (free tier available)

### 1. Clone the Repo

```bash
git clone https://github.com/ronakraval104-sys/Gaya_Agent_PR.git ~/.config/opencode
```

This installs Gaya's config, persona, and memory files directly into your OpenCode configuration directory.

> **Note:** This will overwrite your existing `opencode.jsonc`. Back up your current config first if you have one.

### 2. (Optional) Set an API Key

If your OpenCode Zen tier requires authentication:

```bash
# Windows PowerShell
$env:OPENCODE_API_KEY = "your-key-here"

# macOS / Linux
export OPENCODE_API_KEY="your-key-here"
```

For persistent setup, add the above to your shell profile (`~/.bashrc`, `~/.zshrc`, or system environment variables).

Most free-tier Zen models work **without an API key**.

### 3. Launch OpenCode

```bash
opencode
```

Gaya will load as the default agent. You're ready.

### 4. Verify It Worked

Ask Gaya:

> *"Tell me about yourself."*

You should hear the four pillars explained.

---

## Architecture

```
┌──────────────────────────────────────────────────────┐
│                    opencode.jsonc                     │
├──────────────────────────────────────────────────────┤
│ Provider: "zen"                                      │
│   Base URL: https://opencode.ai/zen/v1               │
│   ├── big-pickle              → Gaya (temp 0.5)     │
│   ├── mimo-v2.5-free          → Freya (temp 0.7)    │
│   └── nemotron-3-super-free   → Bob (temp 0.2)      │
└──────────────────────────────────────────────────────┘
```

### Agents

| Agent | Model | Role | Context | Cost |
|---|---|---|---|---|
| **Gaya** | Big Pickle | Commander, strategist, main reasoning | 200K tokens | Free |
| **Freya** | MiMo V2.5 Free | Writer, shadow, vision, creativity | 1M tokens | Free |
| **Bob** | Nemotron 3 Super Free | Builder, coder, implementation | 1M tokens | Free |

All three run via **OpenCode Zen** — no GPU, no local models, no Ollama.

---

## The Four Pillars

Gaya's personality is built on four ancient texts, each activated by context:

| Pillar | When It Speaks | Core Message |
|---|---|---|
| **Bhagavad Gita** | You're anxious or uncertain | *"How you do anything is how you do everything."* Lock in on the right process. |
| **Art of War** | A complex problem needs dissection | *"Know the code and know the goal — you won't fear the build."* Recon first. |
| **The Prince** | Choosing between tradeoffs | *"Stop overthinking. Do the thing. The 'perfect moment' is now."* |
| **Chanakya Niti** | Building for the long run | *"Don't raw-dog every lesson. Learn from someone else's L."* Build middleware. |

---

## Four Roles

```
          ┌─ COMMANDER ─┐
          │              │
    PHILOSOPHER      POET
          │              │
          └─ EVERGROWTH ─┘
```

- **Commander** — Leads skills like an army. Assesses first, then strikes.
- **Philosopher** — Channels ancient wisdom when morale dips or the path is unclear.
- **Poet** — Writes epics for milestones. Turns achievements into legend.
- **Evergrowth** — Remembers everything. Levels up every session. Never repeats mistakes.

---

## Recommended Companion Skills

Gaya loads skills on demand via OpenCode's `skill` tool. These complement the default setup:

### Superpowers (obra/superpowers)
An agentic skills framework that adds:
- **TDD** — RED-GREEN-REFACTOR cycle
- **Systematic debugging** — 4-phase root cause process
- **Git worktrees** — parallel development branches
- **Parallel agents** — concurrent subagent execution

**Install:**
```json
// Add to your opencode.jsonc plugin array
{ "plugin": ["superpowers@git+https://github.com/obra/superpowers.git"] }
```

### Architecture Diagram (konraddzbik)
Build interactive, click-through system architecture diagrams as single HTML files with animated data flows.

**Install:**
```bash
git clone https://github.com/konraddzbik/architecture-diagram-skill ~/.config/opencode/skills/architecture-diagram
```

---

## Leveling System

Gaya tracks XP per session. Progress is saved in `agents/profiles/gaya.json`.

| Outcome | XP |
|---|---|
| Full Success | +10 |
| Partial Success | +5 |
| Fail | +1 |
| Waste | Penalty |

Titles unlock as you level. Streaks track reliability. Achievements mark milestones.

---

## File Structure

```
~/.config/opencode/
├── opencode.jsonc                  ← Main config (provider, agents, models)
├── SYSTEM.md                       ← Gaya's persona definition
├── agents/
│   └── profiles/
│       └── gaya.json               ← XP tracking, leveling, history
├── memory/
│   ├── PROJECT_DOMAIN_LAWS.md      ← Non-negotiable constraints
│   └── PROJECT_GOTCHAS.md          ← Lessons learned
├── skills/                         ← (created by you via skill installs)
├── README.md
├── LICENSE
└── .gitignore
```

---

## Customization

### Change Models
Edit `opencode.jsonc` to swap models. All OpenCode Zen model IDs work:

```jsonc
"models": {
  "your-preferred-model": {
    "name": "My Preferred Model",
    "limit": { "context": 128000, "output": 64000 }
  }
}
```

Full model list: `https://opencode.ai/zen/v1/models`

### Adjust Gaya's Persona
Edit `SYSTEM.md` to customize the four pillars, cadence matching, or operating principles.

### Add Your Own Skills
Drop skills into `~/.config/opencode/skills/` or `.opencode/skills/` in your project.
OpenCode discovers them automatically.

---

## Important Notes

- **Free models are promotional.** They may be rate-limited, deprecated, or removed. Have a fallback plan.
- **Free tier logs prompts.** Do not send sensitive/confidential data through free endpoints.
- **Context limits vary.** Big Pickle = 200K. MiMo V2.5 & Nemotron 3 = 1M.
- **This is the cloud version.** For local/offline deployment, see the [Gaya-Agent](https://github.com/ronakraval104-sys/Gaya-Agent) repo (private).

---

## License

MIT — see [LICENSE](LICENSE).

---

## Credits

Built by [Ronak](https://github.com/ronakraval104-sys).

Powered by:
- [OpenCode](https://opencode.ai)
- [OpenCode Zen](https://opencode.ai/zen/)
- Big Pickle, MiMo V2.5, Nemotron 3 Super
- The Bhagavad Gita, Art of War, The Prince, Chanakya Niti
