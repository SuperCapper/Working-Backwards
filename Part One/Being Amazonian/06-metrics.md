# Chapter 6 — Metrics: Manage Your Inputs, Not Your Outputs

### Executive Summary

Most executives fixate on **output metrics** — revenue, profit, share price — because those are the numbers the board and the market judge them on. Amazon's central argument is that output metrics are almost entirely uncontrollable in the short term and therefore nearly useless as a management tool: by the time revenue or profit moves, the causal action that produced the move happened weeks or months earlier. The organization instead manages **controllable input metrics** — the specific, directly actionable drivers (selection, price, in-stock rate, delivery speed) that causally produce the outputs it cares about — and built a dedicated weekly ritual, the **Weekly Business Review (WBR)**, to keep the entire company, from individual contributor to CEO, anchored to those inputs rather than to the outputs everyone is naturally tempted to watch instead.

---

### 1. Why Output Metrics Are the Wrong Thing to Manage

The chapter opens with a pointed anecdote: a Fortune 500 CEO celebrates a 30-cent uptick in his company's stock price as though he personally caused it. Bezos's observation — *"There's nothing that CEO did to cause that 30-cent blip"* — is the chapter's thesis in miniature: **output metrics (share price, revenue, profit) are lagging indicators that companies can only influence indirectly, over time, through the inputs that actually drive them.** Critics who assumed Amazon's obsession with input metrics meant it didn't care about profit were, per the authors, simply wrong — profit and free cash flow matter enormously; they're just not what gets managed day to day, because they can't be.

### 2. Origin: The 2000 Holiday War Room

The discipline traces to a concrete crisis: during Q4 2000 (44% net sales growth year-over-year), Amazon ran a daily "war room" tracking order backlog against fulfillment capacity to avoid failing to deliver holiday orders on time — a problem serious enough that both authors personally worked overnight shifts in fulfillment centers. The postmortem after that holiday season produced the **Weekly Business Review**, designed to give leadership a comprehensive, standing view of the business rather than only surfacing problems in a crisis.

### 3. The Metrics Life Cycle: DMAIC

Amazon adapted the Six Sigma **Define-Measure-Analyze-Improve-Control** sequence, and is explicit that skipping steps causes the most common failures:

| Stage | Discipline |
|---|---|
| **Define** | Choose metrics that are genuinely controllable inputs, not restatements of outcomes |
| **Measure** | Build unbiased, accurate collection tools — and audit them regularly, since drift is assumed, not exceptional |
| **Analyze** | Separate signal from noise; find true root causes rather than proximate ones |
| **Improve** | Only act once Define/Measure/Analyze are solid — acting earlier means responding to noise |
| **Control** | Keep the process in-control over time; candidates for full automation emerge here |

### 4. The Flywheel: How Inputs Compound Into Outputs

Bezos's 2001 napkin sketch — the **Amazon flywheel** — models how a small set of input metrics reinforce each other into a single output, growth: better customer experience → more traffic → more third-party sellers → wider selection → better customer experience (closing the loop) → growth → lower cost structure → lower prices → better customer experience again. Because nearly every WBR metric maps onto one node of this flywheel, the diagram itself opens the WBR deck every week — a constant reminder of *why* a given input matters, not just that it's being tracked.

### 5. Choosing the Right Input Metric Is Iterative, Not Obvious

The chapter's cautionary case study: Amazon initially measured "selection" as **number of new product detail pages created** — a metric that seemed reasonable but drove teams to add low-demand inventory that consumed fulfillment center space without moving sales. The metric evolved through several corrections, each closing a loophole the last version left open:

1. Number of detail pages → (didn't account for whether anyone viewed them)
2. Number of detail page **views** → (didn't account for whether the item was actually in stock)
3. % of page views where the item was **in stock** → (didn't guarantee fast delivery)
4. % of page views where the item was in stock **and ready for two-day shipping** — finalized as **"Fast Track In Stock"**

The lesson generalized: a plausible-sounding input metric can still be wrong, and the correction only becomes visible by continuously testing whether moving the metric actually moves the output you care about — in this case, sales.

### 6. Measurement Must Be Actively De-Biased

Because every business unit leader has a natural incentive to select metrics and data that flatter their own performance, Amazon's finance organization was explicitly mandated — by Bezos, CFO Warren Jenson, and later Tom Szkutak — to have **"no skin in the game other than to call it like they see it."** The chapter also shows how the *same* metric name can measure fundamentally different things depending on collection method: an end-of-day inventory snapshot (operations-centric, easy to game by restocking right before the snapshot) versus a page-view-weighted, real-time in-stock calculation (customer-centric, reflecting what shoppers actually experienced). The rule of thumb: **align metric definitions with the customer's actual experience, not with whatever is operationally convenient to collect.**

### 7. Root-Causing with the "Five Whys" (Correction of Errors)

For anomalies and failures, Amazon uses a **Correction of Errors (COE)** process adapted from Toyota's "Five Whys" — iteratively asking "why" until reaching the true root cause rather than stopping at the first proximate explanation. AWS SVP Charlie Bell's framing: *"the probability you're actually looking at the actual root cause of the problem in the initial 24 hours is pretty close to zero... behind every issue there's a very interesting story."*

### 8. The WBR Deck and Meeting Discipline

The weekly deck follows strict conventions designed to make patterns, not noise, jump out: consistent chart formats week over week; multiple time horizons on the same axis (e.g., trailing 6 weeks next to trailing 12 months) so short-term inflections aren't smoothed away; year-over-year comparisons (with growth-rate trend lines that can reveal decelerating momentum invisible in the raw numbers); and — distinctively — **anecdotes and exception reports** woven directly into otherwise all-quantitative data, on the theory (per the Dive Deep principle) that leaders should be "skeptical when metrics and anecdotes differ."

Meeting norms that keep the WBR functional rather than performative:
- **Variances get discussed; the expected does not** ("nothing to see here, moving on").
- **Metric owners, not finance, explain their own variances** — and are expected to say "I don't know, we're still analyzing" rather than guess.
- **Operational and strategic discussion stay separate** — the WBR is not where new product ideas get pitched.
- **No browbeating.** The authors are candid that some Amazon WBRs became hostile "disaster meetings" where anomalies triggered accusatory pile-ons, driving people to hide mistakes rather than surface them — directly undermining the meeting's purpose. The fix credited in hindsight: senior leaders must set tone and ground rules explicitly, reward teams for being "vocally self-critical," and recognize that psychological safety and high standards are not in tension — they're both required for the mechanism to work.

### 9. The Andon Cord: An Input-Metric Insight Made Structural

The chapter's signature story: during a mandatory customer-service shift, Bezos watched an agent instantly predict which product a caller's complaint was about, because that item was a chronic, known source of damage-in-transit complaints — yet the agent had no mechanism to stop it from being sold. Inspired by Toyota's Andon Cord (any assembly-line worker can halt the line to fix a defect on the spot), Amazon built a "big red button" giving customer service agents authority to instantly disable purchasing on a defective listing and automatically notify the responsible category manager — turning a frontline anecdote into an immediate, structural input-metric intervention instead of waiting weeks for the issue to surface in monthly category reports.

### 10. Noise vs. Signal

The chapter's final caution: variation in any metric is normal and unavoidable, and chasing small fluctuations within normal bounds — a metric moving 0.1% in either direction — wastes effort and can trigger unnecessary "fixes" for what was never actually broken. Distinguishing genuine signal from noise is treated as the metric owner's core responsibility, developed through daily familiarity with a metric's normal range, not solely through statistical control-chart methods.

---

### Bottom Line

Amazon's metrics discipline is really a discipline about causality: manage the levers you can actually pull (input metrics), define them carefully enough that gaming one doesn't quietly damage the outcome you actually want, audit them for bias and drift as a matter of course, and build a weekly forum where anomalies surface fast, get root-caused rather than argued about, and don't turn into a blame exercise that teaches people to hide problems instead of fixing them. Output metrics remain the scoreboard — but the scoreboard is not something you can coach to directly.

*Source: Chapter 6, "Metrics: Manage Your Inputs, Not Your Outputs," in Colin Bryar & Bill Carr, Working Backwards (St. Martin's Publishing Group, 2021).*
