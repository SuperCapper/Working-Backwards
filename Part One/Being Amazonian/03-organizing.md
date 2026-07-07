# Chapter 3 — Organizing: Separable, Single-Threaded Leadership

### Executive Summary

As organizations grow, the number of possible communication links between people grows exponentially while headcount grows only linearly — so coordination overhead eventually outpaces the value added by each new hire, and velocity (speed *and* direction) collapses under its own bureaucratic weight. Amazon's answer, arrived at only after a decade of trial, error, and abandoned intermediate solutions, was not to *manage* dependencies better but to **eliminate them at the source**: reorganize both software architecture and org structure into small, separable units, each owned outright by a single accountable leader who works on nothing else. This evolved from an early, rigid format ("two-pizza teams") into the more general and durable model Amazon still uses today — the **single-threaded leader (STL)** running a **separable, single-threaded team**.

---

### 1. Why Growth Strangles Its Own Velocity

Between 1997 and 2001 Amazon's revenue grew more than 21-fold, and with it came a corrosive side effect: more and more time was spent coordinating, less and less building. The mechanism is structural, not a people problem — every dependency (something one team needs but can't supply itself) requires coordination, and coordination cost scales combinatorially with team count, not linearly. Two flavors of dependency compounded this:

- **Technical dependencies.** Amazon's website ran on one monolithic executable ("Obidos") and one shared relational database ("acb"). Any team touching shared code risked breaking another team's work or taking the whole site down, and any database change had to clear a slow-moving executive review board nicknamed the "DB Cabal." A concrete illustration: a straightforward change to the Associates (affiliate) referral-fee logic moved quickly wherever the team controlled its own code, and crawled wherever it touched Obidos or acb.

- **Organizational dependencies.** A ballooning org chart meant securing resources or approvals required tracking down the right person (or their manager's manager) across an increasingly tangled reporting structure — a tax paid on nearly every project of any size.

Both forms of dependency shared a second-order cost beyond lost time: **disempowered teams**, who were accountable for outcomes they didn't have full authority to control.

### 2. The Wrong Fix: Better Coordination (NPI)

Amazon's first instinct was to coordinate *better*, not eliminate the need to coordinate — resulting in **New Project Initiatives (NPI)**, a quarterly, centralized prioritization process requiring every cross-team project to submit a one-pager, staffing estimate, and P&L for review by a room of 30–40 leaders. NPI's failure modes are instructive:

- Estimates carried enormous error bars (e.g., "$4–20 million, 20–40 person-months"), making cross-project comparison close to meaningless.
- Consumer-adoption predictions were frequently wrong, and feedback loops on those predictions took a year or more to close.
- Being "NPI'd" — assigned to support another team's approved project instead of your own — was a recognized morale-killer, precisely because it stripped teams of ownership over their own roadmap.

The deeper realization: **the problem wasn't insufficient coordination machinery — it was that so much coordination was required in the first place.** Optimizing a process built around exponentially growing dependency cost is a losing race; the only durable fix is removing the dependencies themselves.

### 3. The Structural Insight: Treat Cross-Team Communication as a Defect

Bezos's reframing was blunt: if Amazon wanted to be a place where builders could build, the goal should be to **eliminate communication between teams, not improve it.** The mechanism for doing so on the technical side was a service-oriented architecture — every team encapsulates its code and data behind a published API; no other team gets direct access. (Amazon CTO Werner Vogels described this as isolating "the data with the business logic that operates on the data, with the only access through a published service interface.") The restaurant analogy the authors use: you don't walk into the kitchen to get what you want — you order from a menu, and if you want something new, the owning team decides whether and how to add it.

### 4. First Attempt: The Two-Pizza Team

CIO Rick Dalzell operationalized Bezos's directive as the **two-pizza team** — small enough to be fed by two large pizzas — with a specific design contract:

- **Small:** no more than ~10 people.
- **Autonomous:** no need to coordinate with other teams, enabled by the new API-based architecture.
- **Measured by a "fitness function":** a single weighted composite metric (e.g., 50% new items added, 30% units sold, 20% page views) monitored in real time on a shared dashboard.
- **Full business ownership:** design, technology, *and* business results — closing off the classic excuse of blaming "the business side" or "the tech side" for a miss.
- **Led by a multidisciplined leader** with technical depth, hiring judgment, and business acumen.
- **Self-funding**, and **pre-approved by the S-Team** before formation.

Realizing "be autonomous" required years of expensive, unglamorous infrastructure work — decomposing Obidos and acb into services piece by piece while the business kept running. Teams that invested early in removing dependencies and building instrumentation (e.g., the Picking team, which spent nine months on plumbing before touching a single new feature) later moved dramatically faster than teams that chased visible feature work first and paid for it later in accumulated drag.

### 5. Where the Two-Pizza Model Broke Down

Amazon is explicit that this was an iterative failure-and-adaptation process, not a single "aha":

| Assumption | What actually happened |
|---|---|
| Applicable company-wide | Only worked in product development — other functions (retail, legal, HR) weren't held back by dependency tangles, so restructuring them added no speed |
| Fitness functions align teams to goals | Debates over metric weightings became unproductive, and composite scores obscured rather than clarified what a team should do differently — Amazon reverted to tracking the underlying input metrics directly |
| Any team can find a great generalist leader | Multidisciplined leaders capable of running a self-contained team were rare even at Amazon, forcing a shift to a matrix model (solid-line to a functional manager, dotted-line to the team lead) |
| Ten people is the right ceiling | Team success correlated with leader quality and authority, not headcount — so the size cap was dropped entirely |

### 6. The Durable Model: Single-Threaded Leadership

Dropping the size constraint and formalizing the leadership requirement produced the model Amazon actually runs today: a **single-threaded leader (STL)** — someone who works on *one* initiative and nothing else — heading a **separable** team with minimal cross-team dependency, regardless of how large that initiative is (from a small feature team up to something the scale of Amazon Echo/Alexa). The illustrative case is **Fulfillment by Amazon**: the initiative (then called Self-Service Order Fulfillment) stalled for over a year as "everyone's part-time responsibility" under existing execs, and only launched successfully once Jeff Wilke freed VP Tom Taylor from every other duty to run it as his sole focus. As SVP Dave Limp put it: *"The best way to fail at inventing something is by making it somebody's part-time job."* A practical litmus test for whether a team is truly separable, per former VP Tom Killalea: **can it deploy its own changes without needing coordination or approval from other teams?** If not, carve out a smaller piece that can.

---

### Bottom Line

Coordination overhead doesn't respond to being managed harder — it has to be designed away. The transferable lesson has three parts: (1) treat unavoidable cross-team communication as an architectural defect to be engineered out via clear-ownership interfaces (APIs, in software; explicit charters, in org design), not a soft-skills problem to be solved with better meetings; (2) give any initiative that matters a single leader with no competing responsibilities, not a committee or a part-time owner; and (3) be willing to discard your own prior solution (NPI, fitness functions, the two-pizza size cap) once evidence shows it isn't working — the destination (separable, autonomous, accountable teams) mattered more than any specific implementation along the way.

*Source: Chapter 3, "Organizing: Separable, Single-Threaded Leadership," in Colin Bryar & Bill Carr, Working Backwards (St. Martin's Publishing Group, 2021).*
