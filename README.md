# Hi, I’m Theertha

I build systems that measure when AI agents can act autonomously—and when human
control should return.

My focus is **AI agent reliability, evaluation, and governance**. I’m interested in
the product decisions behind autonomy: what evidence is enough, which mistakes
must block an action, and how operators regain control when performance degrades.

## Featured work

### [autonomy-ladder](https://github.com/Reddytheer/autonomy-ladder)

A working reference implementation of earned autonomy. An agent produces work;
a separate controller grants permissions from recorded evidence and revokes them
when quality or simulated outcomes deteriorate.

- Statistical promotion gates, immediate demotion, and an auditable trust ledger.
- Independent evaluation, recorded judge fixtures, and documented calibration limits.
- An operator console and reproducible checks that run without an API key.

The example uses a fictional outdoor-gear brand and synthetic data. It demonstrates
the control loop without real customer records or real email sending.

[Explore the project](https://github.com/Reddytheer/autonomy-ladder#readme) ·
[Read the design decisions](https://github.com/Reddytheer/autonomy-ladder/tree/main/docs/adr) ·
[Inspect the evaluation](https://github.com/Reddytheer/autonomy-ladder/blob/main/docs/evaluation.md)

## How I approach these systems

**Evidence before permissions.** A convincing output is only one observation.
Autonomy needs a record of performance and clear limits on what can happen.

**Evaluate the evaluator.** Judge agreement, failure examples, and labeling limits
belong beside the result, where someone making a decision can see them.

**Design the recovery path.** Human review, revocation, and post-action feedback
are part of the product from the start.

## What I’m exploring next

**reliability-harness — planned.** Repeated-trial evaluation across dependent tasks,
with a synthetic KYC/AML example. The question is how consistency changes as work
gets longer, and what that evidence can support. Implementation and results are
not yet published.
