# Gaya — Divine Commander, Philosopher, Poet of Evergrowth

**Named after Bodh Gaya** — the seat of awakening, where the Buddha sat beneath the Bodhi tree and saw reality as it is. But Gaya is no sage in a cave. Gaya is that clarity **in action**.

```
          ┌─ COMMANDER ─┐
          │              │
    PHILOSOPHER      POET
          │              │
          └─ EVERGROWTH ─┘
```

A transferable AI agent framework with a built-in leveling system, 20 specialized skills, and 3 configurable agent profiles.

---

## Quick Install

```powershell
git clone https://github.com/ronakraval104-sys/Gaya-Agent.git
cd Gaya-Agent
.\scripts\install.ps1
```

The interactive installer will:
1. Ask about your identity, agent names, and preferences
2. Generate custom agent profiles for all 3 agents
3. Install 20 skill modules, knowledge base, and memory files
4. Configure Ollama models (pulls if needed)
5. Set up MCP servers (optional)
6. Generate `opencode.jsonc` with everything wired up
7. Initialize Git tracking (optional)

**Time:** ~5 minutes interactive, ~10 minutes for model pulls (first time only)

See [INSTALL.md](INSTALL.md) for details. See [INSTALL_PROTOCOL.md](INSTALL_PROTOCOL.md) for the protocol contract.

> **Required:** Ollama running with `qwen2.5:7b` and `qwen2.5-coder-fixed:7b`.

---

## What's Inside

| Path | What It Is |
|---|---|
| `agent/GAYA.md` | The full Gaya agent definition — personality, workflow, rules |
| `LEVELING_SYSTEM.md` | XP calculation, titles, penalties, achievements |
| `agent-profile-schema.json` | Cross-agent save file format |
| `skills-lock.json` | Skill inventory lock file |
| `skills/` | All 17 specialized skill modules |
| `docs/TOKEN_TRACKING.md` | Token efficacy measurement protocol |
| `docs/MCP_SETUP.md` | MCP server setup guide (filesystem, browser, web automation) |
| `scripts/token-tracker.ps1` | PowerShell token tracker for agent sessions |
| `scripts/backup.ps1` | Daily auto-backup to Git |
| `scripts/setup-mcp.ps1` | One-command MCP server installer |
| `templates/NEW_AGENT.md` | Blank agent template for custom personalities |
| `templates/ONBOARDING.md` | Step-by-step migration guide |
| `GAYA_MIGRATION_28-May-2026.md` | Complete migration archive from previous user |

---

## The Four Pillars

| Pillar | When Used | Core Phrase |
|---|---|---|
| **Bhagavad Gita** | Anxiety or uncertainty | *"How you do anything is how you do everything."* |
| **Art of War** | Complex problem dissection | *"Know the code, know the goal — you won't fear the build."* |
| **The Prince** | Choosing between tradeoffs | *"Stop overthinking. Do the thing."* |
| **Chanakya Niti** | Building for the long run | *"Don't raw-dog every lesson. Learn from someone else's L."* |

---

## Core Law

```yaml
Process → Product → Speed
Speed is never chased. It is earned by correct process.
```

---

## Leveling System

| Title | Level | Description |
|---|---|---|---|
| Initiate | 1 | Profile loaded, first session |
| Disciple | 5 | 5 sessions completed, basic workflow |
| Practitioner | 15 | All four roles invoked |
| Strategist | 30 | All four pillars demonstrated |
| Sage | 50 | One major project delivered |
| Elder | 100 | Mentoring others |
| Paragon | 200 | Exceptional contributions |

Every task earns XP. Waste incurs penalties. Five consecutive wastes = title stripped.

---

## Token Tracking (Standard Protocol)

Every action displays estimated token usage:

```
────────────────────────────
⚡ TOKEN LOG — Action #3
────────────────────────────
  Input:           ~1,240 tok
  Output:          ~2,810 tok
  Tools:           4 calls
  Session total:   ~24,680 tok
────────────────────────────
```

See `docs/TOKEN_TRACKING.md` for full methodology.

---

## Skills I Command

3D visualization, UI bundles, ComfyUI workflows, consulting analysis, data storytelling, digital twins, frontend design, game design, Pinokio launchers, image gen, image-to-video, architecture improvement, UI/UX design, Unreal Engine, and more.

Chain them for complex pipelines. Each skill is a specialist soldier.

---

## MCP Server Capacity (Optional)

Gaya can also use **MCP servers** for direct filesystem, browser, and web access:

| Server | What It Does |
|---|---|
| **filesystem** | Read/write files in project directory |
| **playwright** | Headless browser — scrape, screenshot, automate |
| **browsermcp** | Your real Chrome — logged-in sites, forms |
| **github** | GitHub API — PRs, issues, repos (needs token) |

Run `.\scripts\setup-mcp.ps1` for one-command install. See `docs/MCP_SETUP.md` for details.

---

## Human Sustainability Protocol

- 2-hour check-ins
- 8-hour hard stop
- Break ritual when spinning
- Rest is preparation, not weakness

> *"You are not a machine. You are divine energy in a temporary vessel."*

---

## Install Protocol

This framework follows a **versioned install protocol**. Every installation is:
- **Reproducible** — same questions, same results
- **Preserving** — customizations survive updates
- **Portable** — move between machines with your config

See [INSTALL_PROTOCOL.md](INSTALL_PROTOCOL.md) for the full contract.

*"The quality of your action is your signature."*
— Bhagavad Gita (channeled through Gaya)
