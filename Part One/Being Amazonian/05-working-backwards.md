# Chapter 5 — Working Backwards: Start with the Desired Customer Experience

### Executive Summary

Most organizations build products "forwards": engineering and marketing each optimize for what they're good at — feature richness, cost structure, market positioning — and reconcile the gaps only at launch, often too late to fix them cheaply. Amazon's **Working Backwards** process inverts the sequence: before any resources are committed, the team writes the product's press release and FAQ as if it already existed, forcing every hard trade-off (price, feasibility, dependencies, market size) into the open at the cheapest possible point to change course — on paper. The process produced Kindle, most of AWS, and the majority of Amazon's major post-2004 initiatives, and its core artifact, the **PR/FAQ**, is now one of Amazon's most widely used and exported tools.

---

### 1. Origin: "Where Are the Mock-Ups?"

The process emerged from repeated friction, not a single insight. When Bill Carr's team proposed launching Amazon's digital media business in 2004, they followed the standard "category expansion" playbook — market sizing, financial models, PowerPoint, spreadsheets — and presented it to Bezos expecting a green light to start hiring. Bezos's response was consistently the same question: **"Where are the mock-ups?"** He wanted the full customer-facing experience — screens, buttons, copy, click sequence — defined before any team, budget, or vendor relationship was committed. The team's first attempt at mock-ups was rejected too: a half-baked mock-up, in Bezos's view, was evidence of half-baked thinking, not a acceptable placeholder for it.

The eventual breakthrough combined two threads already in motion: **customer obsession** (starting from the experience, not the company's convenience) and the shift to **written narratives** (chapter 4). Team members wrote free-form narratives describing their best product ideas — one proposed an E-Ink e-reader, another an MP3 player, and Bezos himself wrote one for a voice-activated countertop device he called "Amazon Puck" (a clear ancestor of Echo). The format that stuck was reframing the narrative as a **press release**, forcing the team to state upfront what a customer would actually get, before any internal negotiation about cost or feasibility began.

### 2. Why Working Backwards Beats Working Forwards

The chapter's illustrative counterexample: imagine Sony's marketing team independently decides a new TV should retail at $1,999 based on market research, while its engineering team, focused purely on picture quality, builds a set that costs $2,000 to manufacture. Neither group was wrong in isolation, but the two efforts were never reconciled against a single, agreed customer-facing target — a failure only visible once it's too expensive to fix. Had the two teams first agreed on a **press release** — the price, the features, the experience — they would have been forced to work backwards together to find a feasible design, surfacing the conflict at the cheapest possible moment rather than the most expensive one.

Kindle is Amazon's own version of this lesson: early Kindle planning (done in the pre-narrative PowerPoint/Excel era) focused on technology constraints, business models, and financial projections — i.e., what would be good for Amazon — and stalled. Only after the team wrote a Kindle press release and worked backwards from the customer experience (great reading screen, buy-and-download in under a minute, huge selection, low price) did the product take its eventual shape.

### 3. The PR/FAQ Artifact

The narrative-as-press-release format evolved into the standardized **PR/FAQ** (press release / frequently asked questions), with two parts kept to strict length limits — brevity is treated as a forcing function, not a nice-to-have:

**Press Release (under 1 page)** — written entirely from the customer's point of view, with five fixed components:
- **Heading** — the product name, in language the target customer understands
- **Subheading** — one sentence on who the customer is and what benefit they get
- **Summary paragraph** — dateline plus a concise description of the product and benefit
- **Problem paragraph** — the customer's pain point, stated from their perspective
- **Solution paragraph(s)** — how the product solves it, plus quotes from a company spokesperson and a hypothetical customer, and a call to action

**FAQ (5 pages or fewer)** — where the hard internal work happens, split into external questions (what customers/press would ask) and a more standardized set of internal questions covering:

| FAQ Area | Core Question |
|---|---|
| Consumer Needs & TAM | How many people have this problem, how badly, and would they pay to solve it — after filtering out everyone who fails the product's practical constraints? |
| Economics & P&L | What are the per-unit gross/contribution margins, what's the rationale for the price point, and what's the upfront investment required? |
| Dependencies | Which third parties (with their own incentives, not yours) does this rely on, and why would they cooperate? |
| Feasibility | What are the hardest engineering, UI, legal, and partnership problems that must be solved, and how risky is the upfront investment? |

The chapter's fictional "Melinda the smart mailbox" example is used specifically to show how rigorously working through these four sections — even for a plausible-sounding product — can expose that a total addressable market is too small, or that success depends on third parties (carriers, e-commerce platforms) who have no clear incentive to cooperate, well before a single engineer is hired.

### 4. The Review Mechanic

Writing a viable PR/FAQ is iterative and adversarial by design — Amazon teams routinely produce ten or more drafts and sit through five or more leadership reviews. The review meeting follows a specific sequence: the document is read silently in the room (per chapter 4's narrative discipline), general reactions are gathered first with the most senior people speaking *last* (to avoid anchoring the room), and only then does the group move to line-by-line, paragraph-by-paragraph critique — the stage where real flaws surface. A common reviewer test is simply **"so what?"** — if the press release doesn't describe something meaningfully better than what already exists, it isn't worth building.

### 5. Rejection Is the Point, Not a Failure

Most PR/FAQs written at Amazon never become products, and the chapter is explicit that **this is a feature, not a bug**: the entire value of writing the artifact before committing engineering resources is that it lets the company discover, cheaply, which ideas aren't viable — an undersized addressable market, an infeasible cost structure, an uncooperative third-party dependency — without having spent a single dollar of development time finding out the hard way. When a hard problem is identified but the underlying opportunity is large, Bezos's stated response was not to abandon it automatically but to weigh it explicitly: *"We shouldn't be afraid of taking on hard problems if solving them would unlock substantial value."* Even after a PR/FAQ is approved, it remains a living document, revised as the team learns more during actual execution.

---

### Bottom Line

Working Backwards is a sequencing discipline: define and agree on the customer-facing outcome, in writing, before allowing internal constraints (cost structure, technical convenience, org politics) to shape the product. The PR/FAQ's length limits and structured FAQ categories exist specifically to force trade-offs into visibility at the cheapest point in the process — before hiring, before vendor deals, before code — so that the majority of ideas that should die, die early and cheaply, and the few that survive rigorous internal cross-examination arrive already aligned around a validated customer benefit.

*Source: Chapter 5, "Working Backwards: Start with the Desired Customer Experience," in Colin Bryar & Bill Carr, Working Backwards (St. Martin's Publishing Group, 2021).*
