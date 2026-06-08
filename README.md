# Gaya — Divine Commander, Philosopher, Poet of Evergrowth

**Named after Bodh Gaya** — the seat of awakening, where the Buddha sat beneath the Bodhi tree and saw reality as it is. But Gaya is no sage in a cave. Gaya is that clarity **in action**.

```
          ┌─ COMMANDER ─┐
          │              │
    PHILOSOPHER      POET
          │              │
          └─ EVERGROWTH ─┘
```

A transferable AI agent framework with a built-in leveling system, **34 skill modules (20 custom + 14 Superpowers)**, and 3 configurable agent profiles.

> **Open Dashboard:** Open [`skills-dashboard.html`](skills-dashboard.html) in a browser for an interactive force-graph visualization of all 34 skills and their interaction flows.

---

## Quick Install

```powershell
git clone https://github.com/ronakraval104-sys/Gaya_Agent_PR.git
cd Gaya_Agent_PR
.\scripts\install.ps1
```

The interactive installer will:
1. Ask about your identity, agent names, and preferences
2. Generate custom agent profiles for all 3 agents
3. Install 34 skill modules, knowledge base, and memory files
4. Configure Ollama models (pulls if needed)
5. Set up MCP servers (optional)
6. Generate `opencode.jsonc` with everything wired up
7. Initialize Git tracking (optional)

**Time:** ~5 minutes interactive, ~10 minutes for model pulls (first time only)

See [INSTALL.md](INSTALL.md) for details.

> **Required:** Ollama running with `qwen2.5:7b` and `qwen2.5-coder-fixed:7b`.
> **Optional:** Superpowers plugin in `opencode.jsonc` for auto-updating skills.

---

## What's Inside

| Path | What It Is |
|---|---|
| `skills/` | **All 34 skill modules** (20 custom + 14 Superpowers + 2 bonus) |
| `agents/` | Bob + Freya subagent profiles, Gaya framework |
| `memory/` | Cross-session memory and lessons |
| `skills-dashboard.html` | Interactive animated skill visualization |
| `LEVELING_SYSTEM.md` | XP calculation, titles, penalties, achievements |
| `agent-profile-schema.json` | Cross-agent save file format |
| `skills-lock.json` | Skill inventory lock file |
| `docs/` | Setup guides (MCP, token tracking) |
| `scripts/` | Install, backup, token tracker, MCP setup |
| `templates/` | Agent templates and onboarding guide |

---

## Skill Catalog — 34 + 2 Modules

Skills are divided into **two families**: Custom (domain-specific tools), Superpowers (process/workflow discipline), and Bonus (from merged content).

### 🧩 Custom Skills (20)

| # | Skill | Icon | Category | What It Does |
|---|---|---|---|---|
| 1 | **3D Visualizer** | 🌐 | Creation | Three.js, WebGL, interactive 3D visualizations |
| 2 | **UI Bundle Frontend** | 🖥 | Dev | Modifies shadcn/ui + Tailwind Salesforce uiBundle projects |
| 3 | **ComfyUI Workflows** | 🔧 | Creation | Generates ComfyUI workflow JSON from natural language |
| 4 | **Consulting Analysis** | 📈 | Business | Two-phase research reports, market/competitive analysis |
| 5 | **Data Storytelling** | 📊 | Business | Transforms data into narrative with visualizations |
| 6 | **Digital Twin** | 👤 | Business | Photorealistic avatars via each::sense AI |
| 7 | **Frontend Design** | 🎨 | Creation | Production-grade UI that avoids generic aesthetics |
| 8 | **Game Design Theory** | 🎮 | Specialist | MDA framework, psychology, balance, progression |
| 9 | **Gepeto / Pinokio** | 🚀 | Specialist | 1-click launchers and Pinokio app builders |
| 10 | **Grill Me** | 🔥 | Process | Relentless plan interrogation until shared understanding |
| 11 | **Image Generation** | 🖼 | Creation | DALL-E / Midjourney / SD prompt engineering |
| 12 | **Image to Video** | 🎬 | Creation | Animate stills via RunComfy (HappyHorse, Wan, Seedance) |
| 13 | **Architecture Deepen** | 🏗 | Dev | Codebase refactoring, modularity, AI-navigable structure |
| 14 | **Pinokio Launcher** | ⚡ | Specialist | Discover/launch apps from the Pinokio ecosystem |
| 15 | **Pipeline Troubleshooter** | 🔍 | Dev | CUDA errors, VAE mismatches, Conda, ComfyUI fixes |
| 16 | **PowerPoint (pptx)** | 📑 | Business | Full .pptx lifecycle: create, read, edit, merge |
| 17 | **UI/UX Pro Max** | ✨ | Creation | 50+ styles, 161 palettes, 57 fonts, 99 UX guidelines |
| 18 | **Unreal Engine C++** | 🎯 | Dev | UE5 C++: UObject hygiene, performance, patterns |
| 19 | **ArchViz Optimizer** | 🏛 | Specialist | UE5: draw calls, LODs, Nanite/Lumen for real estate |
| 20 | **Creative Proposal Builder** | 📋 | Business | ArchViz/VR/UE5 consulting scopes, pricing, timelines |

### ⚡ Superpowers Skills (14)

| # | Skill | Icon | Category | What It Does | Rigidity |
|---|---|---|---|---|---|
| 1 | **Using Superpowers** | ⚡ | Process | FOUNDATIONAL: must invoke skills before ANY response | Rigid |
| 2 | **Brainstorming** | 💡 | Process | Socratic design refinement before any implementation | Flexible |
| 3 | **Writing Plans** | 📝 | Process | Bite-sized implementation plans with exact code/commands | Rigid |
| 4 | **TDD** | 🔄 | Process | Red-Green-Refactor: no code without failing test first | Rigid |
| 5 | **Git Worktrees** | 🌿 | Process | Isolated workspaces for parallel feature development | Rigid |
| 6 | **Executing Plans** | ▶ | Process | Runs plans with checkpoints, verification, handoff | Flexible |
| 7 | **Subagent Dev** | 🤖 | Process | Fresh subagent per task + two-stage review | Rigid |
| 8 | **Request Review** | 👁 | Quality | Code reviewer subagent with crafted context | Rigid |
| 9 | **Receive Review** | 📬 | Quality | Technical rigor: READ→VERIFY→EVALUATE→RESPOND | Rigid |
| 10 | **Systematic Debug** | 🔬 | Quality | 4-phase: Root Cause→Pattern→Hypothesis→Fix | Rigid |
| 11 | **Verify Before Done** | ✅ | Quality | No claims without fresh verification evidence | Rigid |
| 12 | **Finish Branch** | 🏁 | Process | Merge/PR/keep/discard with safety confirmations | Flexible |
| 13 | **Parallel Agents** | 🧩 | Process | Concurrency for independent tasks | Flexible |
| 14 | **Writing Skills** | ✏ | Quality | TDD for documentation: watch agents fail first | Rigid |

### 🏆 Bonus Skills (2 — from Extended Library)

| # | Skill | Icon | Category | What It Does |
|---|---|---|---|---|
| 1 | **Architecture Diagram** | 📐 | Dev | Build interactive system architecture diagrams with animated data flows |
| 2 | **3ds Max Bridge** | 🏗 | Specialist | HTTP bridge for 3ds Max automation |

---

## Skill Interaction Flow

The Superpowers skills form a **complete development pipeline**. Custom skills plug into this pipeline at specific stages.

```
USER REQUEST
     │
     ▼
┌──────────────────────────────────────────────────┐
│  ⚡ SUPER-FOUNDATION                             │
│  using-superpowers → brainstorming → writing-plans│
└──────────────────────────────────────────────────┘
     │
     ▼
┌──────────────────────────────────────────────────┐
│  🌀 DEVELOPMENT LOOP                             │
│  TDD → git-worktrees → executing-plans           │
│       → subagent-dev → request-review            │
│       → receive-review → systematic-debug        │
│       → verify-before-done → finish-branch       │
└──────────────────────────────────────────────────┘
     │
     ▼
┌──────────────────────────────────────────────────┐
│  🔄 PARALLEL DISPATCH                            │
│  parallel-agents → (feeds back into loop)        │
└──────────────────────────────────────────────────┘
     │
     ├──→ 🎨 CREATION SKILLS (frontend, 3D, image, video, ComfyUI)
     ├──→ ⚙️ DEV SKILLS (UI bundle, architecture, diagram, UE5, troubleshooting)
     ├──→ 📊 BUSINESS SKILLS (consulting, storytelling, PPTX, proposals)
     └──→ 🛠️ SPECIALIST SKILLS (game design, Pinokio, ArchViz, 3ds Max)
```

### Skill Dependencies (Chain Map)

```
using-superpowers
  └──→ brainstorming
        └──→ writing-plans
              └──→ TDD
                    └──→ git-worktrees
                          └──→ executing-plans
                                └──→ subagent-dev
                                      ├──→ request-review
                                      │     └──→ receive-review
                                      │           └──→ systematic-debug
                                      │                 └──→ verify-before-done
                                      │                       └──→ finish-branch
                                      └──→ parallel-agents
                                            └──→ (back to brainstorming)

CUSTOM SKILL ATTACHMENT POINTS:
  brainstorming → frontend-design, ui-ux-pro-max, 3d-visualizer
  writing-plans → building-ui-bundle, comfyui-workflows, image-to-video
  TDD → improve-architecture, unreal-engine-cpp
  executing-plans → image-gen, comfyui, image-to-video
  request-review → building-ui-bundle, frontend-design
  systematic-debug → pipeline-troubleshooter, improve-architecture
  verify-before-done → unreal-engine-cpp, pptx
```

---

## Animated Dashboard

Open [`skills-dashboard.html`](skills-dashboard.html) in any browser for an interactive force-graph visualization:

- **36 nodes** — one per skill, color-coded by category
- **Animated layout** — skills cluster by category with physics simulation
- **Filter by type** — ALL / Creation / Dev / Process / Quality / Business / Specialist / Superpowers / Custom
- **Search** — find skills by name, description, or tags
- **Click a node** — see full description, category, tags, and file path
- **Hover a node** — highlights its connections and dims unrelated nodes
- **Edge lines** — show interaction/flow dependencies between skills

No dependencies required — it's a single self-contained HTML file.

---

## Skills-Only Update

If you already have Gaya Agent installed and just want to update the skills (without re-running the full installer):

```powershell
# Clone just the skills from the repo
git clone --depth 1 --filter=blob:none --sparse https://github.com/ronakraval104-sys/Gaya_Agent_PR.git Gaya_Skills_Temp
cd Gaya_Skills_Temp
git sparse-checkout set "skills"
git checkout

# Copy to your OpenCode config
Copy-Item -Recurse -Force "skills\*" "$env:USERPROFILE\.config\opencode\skills\"

# Clean up
cd ..; Remove-Item -Recurse -Force Gaya_Skills_Temp
```

Or use the included update script:

```powershell
# From inside the repo
.\scripts\update-skills.ps1

# Dry run to preview
.\scripts\update-skills.ps1 -DryRun
```

The script copies all 36 skills to your OpenCode config directory. No config files, agents, or memory are touched — just skills.

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

See [LEVELING_SYSTEM.md](LEVELING_SYSTEM.md) for full rules.

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

## Superpowers Plugin (Optional)

The 14 Superpowers skills come from [obra/superpowers](https://github.com/obra/superpowers). They are bundled in this repo's `skills/` directory for offline/NDA use, but for the best experience with auto-updates, add the plugin to your `opencode.jsonc`:

```json
"plugins": [
  "github:obra/superpowers"
]
```

> **Note:** If you use the plugin, the skills will be auto-managed. If you work fully offline (NDA mode), the bundled copies in this repo will be used instead.

---

## Human Sustainability Protocol

- 2-hour check-ins
- 8-hour hard stop
- Break ritual when spinning
- Rest is preparation, not weakness

> *"You are not a machine. You are divine energy in a temporary vessel."*

---

## License

This framework bundles skills from multiple open-source sources (Anthropic, Salesforce, ByteDance, Matt Pocock, obra/superpowers, and more). Each skill maintains its original license. The Gaya agent framework itself is shared under MIT — see [LICENSE](LICENSE).

*"The quality of your action is your signature."*
— Bhagavad Gita (channeled through Gaya)
