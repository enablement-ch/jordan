# Jordan

**AI sales coach. Reviews your calls against SPICED, MEDDIC, and BANT. Free and open source.**

You're paying $1,600 per seat per year for a tool that records your calls and gives you AI summaries.

Jordan reviews them - against the three most-used sales qualification frameworks - and tells you exactly what you missed. For free.

---

## What Jordan does

- **Pulls your call transcripts directly from Fathom.** No copy-paste, no file uploads.
- **Scores every call against SPICED, MEDDIC, or BANT.** Pick one or run all three side-by-side.
- **Calls out the biggest gap and the exact next move.** Word-for-word what to say on the next call, not generic coaching.
- **Checks if you booked the next meeting before hanging up.** Because that's the rule that actually matters.

It's a Claude Code plugin. Installs in 60 seconds. Runs on your own Anthropic API key, so it's free forever.

---

## Install (Claude Code or Claude desktop app)

Two commands in your terminal:

```bash
claude plugin marketplace add https://github.com/enablement-ch/jordan
claude plugin install jordan
```

Then **fully quit and restart** the Claude desktop app (Cmd+Q) - or run `/reload-plugins` if you're already in a session.

Run setup once:

```
/jordan:setup
```

That walks you through connecting Fathom (one-time) and picking your default framework. Done.

**Works in:** Claude Code terminal, Claude Code desktop app, Claude Cowork (same desktop runtime), and the VS Code / JetBrains extensions.

## Install (Claude.ai - browser, no terminal)

Claude.ai (browser) doesn't support Claude Code plugins, but it does support Custom Skills (Pro/Team/Enterprise plans). Each Jordan skill can be uploaded individually:

1. **Connect Fathom** to Claude.ai: Settings → Integrations → search "Fathom" → Connect.
2. **Download this repo** as a zip (green Code button → Download ZIP).
3. **Upload each skill folder** (`skills/review/`, `skills/compare/`, `skills/review-last/`, `skills/setup/`) to your Claude.ai Custom Skills.
4. Invoke as `/review`, `/compare`, etc. (no `jordan:` prefix in Claude.ai).

---

## The four commands

| Command | What it does |
|---|---|
| `/jordan:review-last` | Pulls your most recent Fathom call and scores it. The fastest path. |
| `/jordan:review` | Score a specific call. Pass a Fathom URL, ID, or local transcript file. |
| `/jordan:compare` | Run a single call through SPICED, MEDDIC, AND BANT side-by-side. Useful when a deal stalls. |
| `/jordan:setup` | One-time onboarding. Re-run any time. |

**Framework override:** add `--framework meddic` or `--framework bant` to any command. Default is SPICED.

---

## What a Jordan scorecard looks like

```
# Jordan's Scorecard - Acme Corp / 2026-04-20

TL;DR: Solid context-gathering, but you did the prospect's emotional work for him.

## Scores at a Glance
| Dimension       | Score | Headline                                       |
|-----------------|-------|------------------------------------------------|
| Situation       |  8/10 | Strong context map across team and stack       |
| Pain            |  5/10 | Analyzed, not felt - he reasoned, didn't bleed |
| Impact          |  4/10 | You did the math, not him                      |
| Critical Event  |  4/10 | "Top three for the quarter" is a TODO list     |
| Decision        |  4/10 | Found a competitor, missed procurement         |

Overall: 5.0/10

Next call booked? ✓ Wednesday 9:30 AM Eastern, locked before hangup.

## Per-Dimension Coaching

### Pain - 5/10

They said: "I'm sure that it's not a valid mechanism because of the
results that we're getting."

Why this score: Dan analyzed his pain like a logic problem. No
emotional weight. He never said it HURT - he said it was inefficient.

What's needed to improve: Get Dan to articulate the personal cost.
He's the new CRO. His credibility is on the line. Until he says
"if outbound doesn't work, [specific consequence to me personally]"
you don't have ownership - you have analysis.

Ask next call:
- "What made you take the CRO role here, and what's your personal
   definition of failure 6 months in?"
- "When the BDR books one meeting in two weeks, what does that
   conversation look like internally? Who notices?"
- "On a scale of 1-10, how painful is the current state of pipeline
   today, this week?"

[... continues for every dimension, then biggest gap, then exact
words to say on the next call]
```

Full example output and the three frameworks live in [`skills/review/references/`](skills/review/references/).

---

## Why three frameworks?

Most call review tools are framework-agnostic, which means they tell you nothing.

The three frameworks Jordan uses are the three most-deployed in B2B sales:

- **SPICED** (Winning by Design) - consultative B2B, mid-market, $10K-100K ACV
- **MEDDIC** (PTC origin, enterprise standard) - complex deals, multi-stakeholder, formal procurement
- **BANT** (IBM, 1960s) - transactional, short-cycle, single buyer

They view the same call differently. SPICED catches whether pain is felt. MEDDIC catches whether you have a champion. BANT catches whether you ever asked about money.

Run `/jordan:compare` on a stalled deal. The frameworks disagree exactly where the deal is most at risk.

---

## Roadmap

- [x] **v0.1** - SPICED, MEDDIC, BANT, side-by-side compare, Fathom integration
- [ ] **v0.2** - tl;dv, Fireflies, Otter integrations
- [ ] **v0.3** - `/jordan:trends` - reads your local review history, surfaces weakness patterns across calls ("you're consistently weak on Critical Event")
- [ ] **v1.0** - open-source web dashboard with login, multi-rep tracking, team-level weakness heatmaps

Star the repo if you want to be notified when these ship.

---

## Who's behind this

[Enablement.ch](https://enablement.ch) - we build done-for-you outbound systems for B2B SaaS and tech-enabled services companies. We use the **7 Backdoors** framework on real engagements - it's sharper than the public methodologies in this plugin because it diagnoses *why* deals stall, not just *what's* missing.

If you want a human to review your calls and your pipeline, [book a call](https://enablement.ch). Otherwise, Jordan is yours forever.

---

## Contributing

PRs welcome. Common contributions we'd love to see:

- Additional frameworks (Sandler, Challenger, GAP Selling)
- Recording-platform integrations (tl;dv, Fireflies, Otter, Gong)
- Translations of framework references
- New `compare` synthesis modes

---

## License

MIT. Use it commercially, fork it, sell consulting on top of it. The frameworks themselves are public methodologies; the implementation is yours to take.
