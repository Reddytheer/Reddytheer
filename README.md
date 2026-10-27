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

### [judge-check](https://github.com/Reddytheer/judge-check) · Published

A working answer to a question that sits underneath every evaluation in this
portfolio: once an agent produces an output, which parts of grading it can an LLM
judge be trusted to do alone, and which still need a person? judge-check takes a
rubric, a human-labeled set, and a judge, and returns one automate-or-keep-a-human
decision per criterion — backed by agreement against reviewed gold labels, the
false-pass rate on real failures, and what happens when the judge itself is
attacked. The demo is AML alert triage at a fictional bank.

reliability-harness, below, explicitly ships without an LLM judge in v1, to avoid
presenting judge agreement as domain truth. judge-check is what turns that caution
into a measurement: it decides, criterion by criterion, when a judge’s verdict is
trustworthy enough to stand in for a reviewer.

[How it works](https://github.com/Reddytheer/judge-check#how-it-works) ·
[Example report](https://github.com/Reddytheer/judge-check/blob/main/examples/draft-baseline/report.html)

## Where I’m taking the portfolio

**Trust in an agent should be measured, tiered, and revocable.** This is a focused
research and product direction within my broader enterprise product work. The
sequence below moves from permissions to evidence, human interaction, and
transactions between organizations. judge-check, above, isn’t a rung on this
ladder — it’s the check that the evidence produced at every rung can be trusted
in the first place. One project in the sequence is published, one is in progress,
and two are planned.

| Order | Project | Product question | Status |
|---|---|---|---|
| 1 | [autonomy-ladder](https://github.com/Reddytheer/autonomy-ladder) | What may the agent do, and when should permission be withdrawn? | Published |
| 2 | [reliability-harness](https://github.com/Reddytheer/reliability-harness) | What evidence is sufficient to grant that permission? | In progress |
| 3 | Calibrated ask-vs-act | When should the system proceed, ask for clarification, or defer to a person? | Planned |
| 4 | Agent-to-agent transactions and verifiable credentials | How can organizations verify evidence and enforce agreed limits when their agents transact? | Planned |

### In progress: reliability-harness — evidence for the decision

Repeated-trial evaluation of commercial-property submission readiness: an agent
reads a fictional application and its linked documents, then marks it ready for
review, asks for clarification, or escalates a request outside its authority. The
build includes a synthetic scenario suite, deterministic evidence scoring, repeated
execution, and a comparison dashboard — all runnable without an API key. No live
model evaluation has run yet, and v1 scores against authored rules rather than an
LLM judge, on purpose. Closing that gap with a measured, not assumed, level of
trust in the judge is exactly what judge-check is for.

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
design human involvement → carry evidence across organizational boundaries,** with
judge-check underwriting the trust placed in automated grading at every step. Each
project should make a product decision inspectable through a working demonstration,
measured outcomes, and explicit limitations. Planned projects have no published
implementation or results yet.

---

Open to conversations about product leadership, enterprise AI, and building products
from early discovery through delivery, adoption, and revenue.
