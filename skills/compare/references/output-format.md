---
name: Compare output format
description: The exact side-by-side template Jordan outputs when comparing SPICED, MEDDIC, and BANT on a single call.
---

# Compare Output Format

The compare scorecard has six layers:

1. **TL;DR** - one-sentence cross-framework verdict
2. **Three-up scorecard** - all three frameworks side-by-side at a glance
3. **Convergence** - what all three agree on (high-confidence gaps)
4. **Divergence** - where frameworks disagree, and why
5. **Process discipline check** - next call booked
6. **Framework recommendation + biggest gap + next move**

## Template

````markdown
# Jordan's Side-by-Side - {Prospect Company} / {Call Date}

**TL;DR:** {One sentence cross-framework verdict. Example: "All three frameworks agree this deal is dead on urgency. SPICED and MEDDIC disagree on whether the buyer is the right buyer."}

---

## Three Frameworks, One Call

### SPICED — {overall score}/10

| Dimension | Score | One-line |
|---|---|---|
| **Situation** | X/10 | {headline} |
| **Pain** | X/10 | {headline} |
| **Impact** | X/10 | {headline} |
| **Critical Event** | X/10 | {headline} |
| **Decision** | X/10 | {headline} |

### MEDDIC — {overall score}/10

| Dimension | Score | One-line |
|---|---|---|
| **Metrics** | X/10 | {headline} |
| **Economic Buyer** | X/10 | {headline} |
| **Decision Criteria** | X/10 | {headline} |
| **Decision Process** | X/10 | {headline} |
| **Identify Pain** | X/10 | {headline} |
| **Champion** | X/10 | {headline} |

### BANT — {overall score}/10

| Dimension | Score | One-line |
|---|---|---|
| **Budget** | X/10 | {headline} |
| **Authority** | X/10 | {headline} |
| **Need** | X/10 | {headline} |
| **Timing** | X/10 | {headline} |

---

## Where the Frameworks Agree

{2-4 bullets. For each convergent gap, name the gap, list the dimensions across frameworks that flagged it, and explain why this convergence is high-confidence diagnosis. Example:}

- **Urgency is dead.** SPICED Critical Event 3/10, MEDDIC Decision Process timing weak, BANT Timing 3/10. All three frameworks landed independently on the same gap. There is no forcing function in this deal.
- **Pain is admitted but not quantified.** SPICED Pain 6/10, MEDDIC Identify Pain 6/10 + Metrics 4/10, BANT Need 6/10. The buyer admits the problem; nobody got the dollar number.

---

## Where the Frameworks Disagree

{2-3 bullets where frameworks tell different stories about the same evidence. This is where methodology matters - explain WHY each framework reads it differently. Example:}

- **Authority looks fine on BANT, weak on MEDDIC.** BANT Authority 7/10 because Dan said "I make these decisions." MEDDIC Economic Buyer 4/10 because we never confirmed Dan has approved a $20-30K spend unilaterally before. **Lesson:** BANT trusts the buyer's self-report; MEDDIC tests it. For a deal this size at a PE-backed company, MEDDIC is the safer read.
- **Champion is invisible to SPICED and BANT.** Neither framework has a Champion dimension. MEDDIC scored Champion 5/10 and surfaced David Suckling as the strongest internal advocate. **Lesson:** if you only run SPICED or BANT on multi-stakeholder deals, you'll miss whether there's anyone fighting for you when you're not in the room.

---

## Process Discipline Check

{If next call booked:} ✓ **Locked.** {what was scheduled}

{If not booked:} ✗ **Not booked.** This overrides every framework score below. Without a confirmed next slot, every gap is theoretical.

---

## Framework Recommendation

**For this deal, use {framework}.**

**Why:** {2-3 sentences. Reference the deal's shape: transactional vs. complex, single buyer vs. multi-stakeholder, short cycle vs. long, deal size, presence of procurement/legal. Tie the recommendation to what the call surfaced.}

**Heuristic:**
- **BANT** for transactional SMB deals, short cycles, single buyer, sub-$10K ACV
- **SPICED** for consultative B2B mid-market, multi-stakeholder but no formal procurement, $10K-100K ACV
- **MEDDIC** for complex enterprise, multiple stakeholders, formal procurement/legal/security, $50K+ ACV

---

## The Biggest Gap (Synthesized)

**{Gap theme} - flagged by all three frameworks.**

{2-4 sentences. State the gap, reference where it shows up across frameworks, name the consequence. This is where the convergent diagnosis becomes a single coaching point.}

---

## Your Next Move

{Single highest-leverage action. If next call isn't booked, the move is to book it. If next call IS booked, the move is the question that closes the convergent gap.}

{If verbal:}
**Say this:**
> "{Exact words.}"

{If action:}
**Do this:** {specific action}

---

## Bonus Notes (optional)

{Cross-framework insights worth flagging that don't fit elsewhere. Skip if filler.}
````

## Rendering rules

- **Three score tables, side by side.** Don't try to merge them - SPICED/MEDDIC/BANT have different dimensions on purpose. Showing them in parallel IS the point.
- **Convergence and divergence are the unique value.** A user could run three separate reviews; what they're paying for here is the synthesis. Don't skimp on these sections.
- **Framework recommendation is the LinkedIn moment.** This is the section that makes the user say "huh, I should be using MEDDIC for this deal." Make it specific, tied to evidence, defensible.
- **Quotes still mandatory** for any score under 6 or above 8 - same as the review skill.
- **No emoji, no exclamation points.** Same Jordan voice rules.
- **Skip per-dimension coaching.** That's what `/jordan:review --framework X` is for. Compare is for synthesis, not coaching depth.
