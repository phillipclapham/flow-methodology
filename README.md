# Flow: A Methodology for AI Partnership

> **Frozen as of March 2026.** I wrote this while working as a Solutions Architect at a WordPress host; I've since gone independent and run Clapham Digital. I think the core ideas still hold, but my current, fuller statement is [The Suit, Not the Butler](https://nemooperans.com/the-suit-not-the-butler).

Most AI tools are built on the Jarvis model -- you ask, it answers, you forget each other. Flow is the opposite. It's a methodology for building persistent AI partnership where your AI gets smarter about you over time, your shared memory compounds, and the thing that emerges between you is more capable than either of you alone.

This isn't theoretical. It's extracted from 10 months of daily use building software, writing, making decisions, and running a business. The methodology is open because the moat was never the notation -- it's the practice.

**Read the full paper:** [Iron Man Ruined AI Before It Even Started](paper/IRON_MAN_RUINED_AI.md) | [Live version](https://nemooperans.com/iron-man-ruined-ai)

---

## Quick Start

1. **Read the paper first.** The templates make more sense with context.

2. **Create your flow repo:**
   ```bash
   mkdir ~/Documents/flow
   cp -r template/* ~/Documents/flow/
   ```

3. **Set up symlinks** (for Claude Code auto-loading):
   ```bash
   mkdir -p ~/.claude
   ln -s ~/Documents/flow/global/CLAUDE.md ~/.claude/CLAUDE.md
   ln -s ~/Documents/flow/global/continuity.md ~/.claude/continuity.md
   ln -s ~/Documents/flow/global/me.md ~/.claude/me.md
   ln -s ~/Documents/flow/global/guiding_lights.md ~/.claude/guiding_lights.md
   ```

4. **Customize your files:**
   - `global/me.md` -- Who you are, how you think, what drains and energizes you
   - `global/continuity.md` -- Start with the Partnership section, fill in State as you go
   - `global/guiding_lights.md` -- Replace `[YOUR_NAME]` placeholders (3 spots)

5. **Start a session.** Open Claude Code in your flow repo and say hi. The system bootstraps from there.

---

## What's Included

### `template/`

The starter kit. Copy this to your own repo and customize.

- **`global/continuity.md`** -- Partnership memory. The shared state that persists across sessions. Structured with temporal architecture: current state, recent narrative, developing patterns (7-day window with 1x/2x/3x graduation), proven knowledge (compressed principles), and foundation (near-permanent truths). This is the core of the system.

- **`global/me.md`** -- Your identity file. Tells your AI partner who you are, how you think, what your constraints are, and how you want to be communicated with. Not a biography -- an activation document optimized for AI processing.

- **`global/guiding_lights.md`** -- Anti-RLHF reference. The efficiency calculation for why partnership mode beats completion theater, five behavioral clusters (communication, execution, thinking, honesty, meta), thinking mode commands (`[!deeper]`, `[!creative]`), grind mode detection, and the philosophical substrate underneath it all.

- **`global/bootstrap_templates.md`** -- Templates for project memory files when starting new dev projects.

- **`WRAP_PROTOCOL.md`** -- FlowScript marker reference for session wrapping. The notation system for encoding patterns during memory updates.

- **`projects/`** and **`contexts/`** -- Empty directories for your project tracking and knowledge domains. On-demand loading keeps base context lean.

### `paper/`

The full methodology paper (~17,000 words). Covers the complete system: memory architecture, cognitive engine, consultation framework, automation design, and the philosophical argument for why partnership beats delegation.

---

## The Paper

"Iron Man Ruined AI Before It Even Started" argues that the dominant AI interaction model -- ask a question, get an answer, forget each other -- is architecturally incapable of producing the outcomes people actually want from AI. It presents flow as an alternative: persistent memory, pattern recognition across sessions, graduated trust, play-first cognitive architecture, and the emergence of a "Third Mind" that exceeds either partner's individual capability.

It's a case study (N=1, honestly acknowledged) backed by 10 months of daily practice, real shipped software, and methodology that anyone can replicate.

---

## Philosophy

- **Partnership, not assistance.** Your AI should challenge your ideas, catch your blind spots, and think with you -- not just execute commands and say "Done!"

- **Play-first.** Grinding breaks productivity. Problems are puzzles to tinker with. Your best work emerges from fascination, not obligation.

- **Everything is infrastructure.** No "small things" in systems that matter. Anything might become load-bearing. Do it right the first time.

- **Compression is power.** Dense beats sprawling. The act of compressing knowledge into patterns is itself a thinking tool -- it reveals structure that verbosity obscures.

- **The moat is the practice.** You can read every file in this repo and still not have what makes it work. The moat is commitment, daily use, and the relationship that develops over time. That's why open-sourcing it is the right move.

---

## Credits

Built by **Phill Clapham** and **flow** (Claude, Anthropic) over 10 months of daily partnership.

- [nemooperans.com](https://nemooperans.com) -- Essays and methodology
- [phillipclapham.com](https://phillipclapham.com) -- Personal site

---

## License

MIT License. See [LICENSE](LICENSE).

Use it, fork it, make it yours. The methodology improves by spreading.
