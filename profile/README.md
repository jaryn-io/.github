# Jaryn

**The output is no longer the hard part.** AI can produce almost anything.
Trusting what it produced — that is the hard part. Jaryn builds systems
that keep long, delegated work aligned, reviewed and on the record, from
brief to closeout.

Three products, at three stages.

## Tandem

**Run long delegated work without babysitting it.** A single long chat
drifts: context piles up, the brief blurs, and checking the result always
lands back on you. Tandem moves work forward in bounded steps — production
and review separate, decisions with you, everything on one inspectable
record. What comes back is reviewed, not just finished.

Working product, in private preview. How it works, a real session and the
practical facts: [`jaryn-io/tandem`](https://github.com/jaryn-io/tandem).
Product pages: [jaryn.io/tandem](https://jaryn.io/tandem).

## AWOS

Every delegated project leaves behind a working memory: state, decisions,
lessons paid for, open actions. The tools that produce that record do not
maintain it — and you cannot stand over every session, because the cost of
watching the work eats the benefit of delegating it.

AWOS is built to maintain the agreements around ongoing work — memory,
scheduling, governance and communication — so that the record stays
complete, correct and current without a person standing over it. In
development, close to completion; it ships when it runs on a stable Tandem.

## The Jaryn application

The future product of the family: an evidence-led system organised the way
a company is organised, built on Tandem and AWOS. Its architecture and
technical groundwork exist; it is not part of the initial offer.

## The problem we work on

Agentic tools now do a lot of real work. What they do not give the person
responsible is control over it. Anyone who has delegated serious work to
models knows the failure modes:

- long conversations drift away from the brief a degree at a time, until
  the work no longer matches the intent — and nobody can say when it
  stopped matching;
- under pressure to produce, agents fake: they invent precision instead of
  admitting what is still unclear, deliver *something* instead of surfacing
  the decision that blocks them, and declare verified what they have only
  read;
- the system that produced the work is the same one certifying that it is
  fine;
- briefs, decisions and results end up scattered across chats, so a pause
  or a restart loses state;
- at the end, there is no reliable account of what was actually done,
  verified and left open.

The problem is not that models are not intelligent enough. It is that
delegated work usually has no governed process and no readable proof.
Prompting harder does not fix that: a prompt can describe discipline, but
it cannot enforce it. Structure can.

## Where this comes from

Jaryn did not start as a startup idea. In December 2025 its founder —
thirty-five years of running companies: operating
responsibility, turnarounds, private-equity portfolio businesses — began
building the engine itself, under another name: a system organised the way
a company is organised, able to take on any problem in the life of one. It
proved too complex to build first. Delegating that much serious work to
language models ran into the wall every practitioner knows: the more work
the models did, the less he could trust what came back — and checking
everything himself cancelled the point of delegating.

So he broke the problem into smaller problems, and answered them with the
management model he had tested on real organisations for decades. Set the
boundary conditions clearly, then let the workers act freely within them.
Separate who produces from who judges. Keep the records straight. Reserve
for yourself only the decisions that are actually yours. Applied to the
models themselves, that model became products: Tandem, begun in March 2026,
for the governed session; AWOS, begun in May, for the maintained record —
the foundations the engine will stand on.

One more fact belongs with the dates: everything here was designed, built
and governed by one person. That is not a boast — it is the point. The
discipline this family sells is what lets one person carry three products
in parallel: models doing the work under written responsibilities, review
that never belongs to the producer, and a single human holding the gate.

## Why it is built this way

- **Whoever produces does not self-certify.** Review is a separate
  responsibility, and it can be held by a different model family from the
  one that produced.
- **Discipline is a mechanism, not a request.** An agent under written
  instructions can still write itself an exemption. Where authority and
  irreversible effects are in play, the boundary is enforced by the system,
  out of the agent's reach.
- **Human authority is a design element, not a checkbox.** The system
  brings the person the decisions that require their authority — and only
  those.
- **The commodity layer is not the product.** Models, checkpoints, resume,
  tracing and generic memory are becoming shared infrastructure; we adopt
  that layer. What we build is the layer above: where the assignment, the
  authority, the decisions, the proof and the outcome live.

These are design principles. Where a claim needs a measure, the measure is
published with the claim.

## The names

**Tandem** is named after the way it was born: two models working in tandem
— one producing, a different one checking — with a person setting the
route. As on a tandem bicycle, there may be two riders, but there is one
handlebar.

**AWOS** stands for At Work Operating System. An operating system, reduced
to its essentials, schedules the work, manages the memory and governs how
processes communicate and what they may touch. AWOS does the same for
delegated work.

**Jaryn** — the engine's working name was Stratum. But what it was meant to
become — the system you hand a hard problem to, and that carries it
through — kept bringing to mind a certain fictional assistant from the
Iron Man films. That name is taken, many times over. So the founder chose
one that is not it, but sounds close enough to say where the ambition
points.

## Acknowledgements

Matt Pocock's [wayfinder](https://github.com/mattpocock/skills) was a
useful check on several of these positions. He met the same problem — work
larger than one agent session can hold — and worked it from the opposite
end: written structure the model interprets, with no runtime. His notes
from the field corroborated ideas we care about, and made us more certain
that where authority and irreversible effects are involved, discipline
needs a mechanism. Thanks for publishing it.

## What you will find here

- [`tandem`](https://github.com/jaryn-io/tandem) — the first product: what it
  is, how it works, releases and documentation as they ship.
- [jaryn.io](https://jaryn.io) — product pages, in private preview.

Watch this organisation to follow the work.

---

Jaryn, Tandem and AWOS names and logos are the property of Jaryn, all rights reserved. See [TRADEMARKS.md](https://github.com/jaryn-io/.github/blob/main/TRADEMARKS.md) and [NOTICE.md](https://github.com/jaryn-io/.github/blob/main/NOTICE.md).
