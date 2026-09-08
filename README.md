# Hi, I’m Theertha 👋

[Connect on LinkedIn](https://in.linkedin.com/in/theertha-y)

**Product leader and former co-founder, building enterprise products from the first customer problem to revenue.**

I’ve built and shipped a revenue-generating AI product from a blank page, owning
work across product strategy, architecture, delivery, and commercialization. My
work connects customer needs and business priorities with the technical decisions
and cross-functional execution required to bring a product to market.

I care about the whole product: why someone buys it, how it fits their workflow,
what it takes to deliver it, and whether it keeps creating value after launch.
Enterprise products have to earn adoption, work within operational constraints,
and give customers reasons to keep trusting them.

## How I lead

- **Start with the customer and the business.** Turn an ambiguous problem into a
  clear product direction, a focused scope, and a case for why it is worth building.
- **Connect strategy to delivery.** Coordinate across functions, resolve dependencies,
  and make the tradeoffs between customer value, technical feasibility, and time explicit.
- **Stay close to the implementation.** Work through architecture and evaluation
  decisions so product commitments reflect what the system can actually deliver.
- **Own what happens after launch.** Treat adoption, reliability, customer feedback,
  and commercial outcomes as part of the same responsibility.

## What you’ll find here

This GitHub is where I make product decisions tangible through working systems,
evaluations, and written tradeoffs. My current public projects explore a question
that matters when bringing AI into enterprise workflows: **what evidence should
we require before a system can act, and when should control return to a person?**

### [autonomy-ladder](https://github.com/Reddytheer/autonomy-ladder) · Published

A working reference implementation of graduated AI autonomy. A separate controller
grants permissions based on measured performance and revokes them when quality or
simulated outcomes deteriorate. It includes an operator console, a trust ledger,
and evaluation checks that run without an API key.

The product decisions are as important as the code: how much evidence is enough,
which failures block action, and how human review fits into the workflow.

[Design decisions](https://github.com/Reddytheer/autonomy-ladder/tree/main/docs/adr) ·
[Evaluation and limitations](https://github.com/Reddytheer/autonomy-ladder/blob/main/docs/evaluation.md) ·
[Economics and risk](https://github.com/Reddytheer/autonomy-ladder/blob/main/docs/economics.md)

## Where I’m taking the portfolio

**Trust in an agent should be measured, tiered, and revocable.** This is a focused
research and product direction within my broader enterprise product work. The
sequence moves from permissions to evidence, human interaction, and transactions
between organizations. One project is published; the next three are planned.

| Order | Project | Product question | Status |
|---|---|---|---|
| 1 | [autonomy-ladder](https://github.com/Reddytheer/autonomy-ladder) | What may the agent do, and when should permission be withdrawn? | Published |
| 2 | reliability-harness | What evidence is sufficient to grant that permission? | Specified; next build |
| 3 | Calibrated ask-vs-act | When should the system proceed, ask for clarification, or defer to a person? | Planned |
| 4 | Agent-to-agent transactions and verifiable credentials | How can organizations verify evidence and enforce agreed limits when their agents transact? | Planned |

### Next: reliability-harness — evidence for the decision

Repeated-trial evaluation across task horizons, demonstrated on synthetic banking
KYC/AML triage: from single-alert disposition to entity investigation and a SAR
recommendation. The planned output combines consistency, partial progress, failure
traces, and uncertainty with a recommendation about autonomy for each task type.
Insufficient evidence should be a visible result. The experiment should report
whether reliability declines, rather than assume that it must.

### Then: calibrated ask-vs-act — useful human involvement

An interaction layer that chooses between acting within granted permissions,
asking for missing information, and deferring to human judgment. The approach will
combine calibrated confidence with the consequences of an error and the cost of
interrupting a person. Evaluation will measure both harmful actions and unnecessary
escalations. Confidence never overrides a hard permission boundary.

### Finally: agent-to-agent transactions — shared rules and portable evidence

A synthetic transaction between agents representing different organizations, with
explicit authority, negotiated terms, and an audit trail of offers, acceptances,
and refusals. Verifiable performance credentials would carry the evaluation scope,
model version, issuer, validity period, and revocation status alongside the results.

The proposed on-chain component would enforce agreed transaction limits and record
policy versions and credential commitments, with sensitive data kept off-chain.
The design will compare this with signed records and a conventional shared service:
what additional assurance justifies the cost and complexity? Verification must
distinguish an authentic record from a trustworthy evaluation; preventing omitted
runs also requires a defined reporting protocol.

### Later: cost-quality routing and unit economics

An extension that connects model selection, review effort, latency, and failure
cost to cost per successful workflow. I would add this after the core evaluation
and interaction work, when quality and human effort can be measured meaningfully.

The intended progression is concrete: **set permissions → measure readiness →
design human involvement → carry evidence across organizational boundaries.** Each
project should make a product decision inspectable through a working demonstration,
measured outcomes, and explicit limitations. Planned projects have no published
implementation or results yet.

---

Open to conversations about product leadership, enterprise AI, and building products
from early discovery through delivery, adoption, and revenue.
