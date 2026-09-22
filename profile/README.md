# Jaryn

**The output is no longer the hard part.** AI can produce almost anything.
Trusting what it produced — that is the hard part. Jaryn builds systems
that keep long, delegated work aligned, reviewed and on the record, from
brief to closeout.

Three products, at three stages: **Tandem** — working product, in private
preview at [jaryn.io/tandem](https://jaryn.io/tandem). **AWOS** — in development, close to completion. **The Jaryn application** — the future
product. This page is about work you can read, not claims: if you only have
a minute, [read one real session](https://github.com/jaryn-io/sessions).

## Tandem

**Run long delegated work without babysitting it.**

A single long chat drifts: context piles up, the brief blurs, and checking
the result always lands back on you. Tandem moves work forward in bounded
steps — production and review separate, decisions with you, everything on
one inspectable record. What comes back is reviewed, not just finished.

For developers and technical builders — anyone who delegates real work to
AI agents: shipping software, running analyses, building internal tools for
finance or operations.

How a session works:

- **Brief and plan.** You write the assignment; a planning role turns it
  into steps with owners, dependencies and gates. Nothing runs on a plan you
  have not approved.
- **Bounded calls.** Each step runs as a separate, short-lived call with
  only the context it needs. State, decisions and evidence live outside the
  model's context, so work can pause, fail, resume and close without losing
  its history.
- **Separate review.** The role that produces is never the role that
  judges. Review, security and audit roles check the work independently —
  and can be bound to a different model family from the one that produced
  it, so the reviewer does not share the writer's blind spots.
- **Your authority.** The session brings you the decisions that are
  actually yours — and only those — with the context you need to take them.
- **Closeout.** The session ends with a readable record: what was done,
  what was verified, what stayed open.

Tandem governs the process and makes the proof inspectable. It does not
promise that every result is correct without judgement; it makes judgement
possible.

**From a real session**

> **Brief** — Create a simple responsive currency converter: enter an
> amount, choose source and destination currencies, swap them, and see a
> clearly formatted result from a small built-in set of fixed rates. Concise
> usage instructions; comfortable on desktop and mobile.
>
> **Plan (GPT-5.6)** — Four steps. S01 Producer builds it. S02 Reviewer and
> S03 Security check it independently. S04 Auditor verifies the chain from
> claims to evidence. Nothing runs until the plan is approved.
>
> **Human, one minute after the brief** — "approved".
>
> **S01 Producer (Gemini 3.7 Flash)** — Four files, no dependencies. Ten
> currencies through a single base rate; per-currency number formatting;
> validation for empty, zero and negative amounts; a content-security policy
> that forbids any network call. Tested in a browser at desktop and phone
> sizes.
>
> **S02 Reviewer (GLM 5.3 Flash)** — Did not take the Producer's word for
> it: loaded the files in its own browser and exercised every path. 250 GBP
> to JPY showed 49,427; recomputed by hand, 49,426.75, rounded correctly.
> Swap, presets, reset, Enter key, both viewports: observed, not inferred.
> No actionable findings. Four minor observations recorded, and a list of
> what was not verified: screen-reader quality, contrast ratios, browsers
> other than Chromium.
>
> **S03 Security (GPT-5.6)** — Fresh execution: zero network requests,
> text-only DOM updates, no external code. No findings. Optional hardening
> noted and judged not material.
>
> **S04 Auditor (Claude Haiku 4.5)** — Traced the brief to the Producer's
> claims, the Reviewer's measurements and the Security checks; file hashes
> unchanged since review. Nine requirements, nine met. The gaps the
> specialists declared: bounded, on the record.
>
> **Closeout, ten minutes after the brief** — Completed. Four deliverables
> accepted. Positive Memory: patterns for the next session, validated by a
> second review. Usage measured per role: USD 1.12 at API-equivalent rates.

![Tandem — the session cockpit](tandem-cockpit.png)

### Your models, your choice

Tandem works with the CLI subscriptions you already pay for — Claude Code,
Codex, Gemini CLI, Kimi and GLM — and connects directly to provider APIs
when that serves you better. You choose per role, per session: use an
API-only model like DeepSeek, reach Qwen or Grok without adding yet another
subscription, go direct to the API when your plan's allowance runs out
mid-work, or trial a model before committing to a plan. Your model mix
stays your choice; no model name lives in the core.

### The practical facts

- **Platform.** Ubuntu — native, or under WSL2 on Windows.
- **Where things run.** The session engine and the model calls run as a
  hosted service, on your own subscriptions and keys. Your repository,
  working copy and deliverables stay on your machine: a local agent applies
  each change as a typed, bounded, authorised operation and reports back.
- **Concurrency.** Several sessions at once, across several repositories,
  from one console.
- **Headless.** The same session contract runs without the console — from a
  shell, a cron job, a systemd unit or another automation — with the same
  rules for questions, pauses, evidence and closeout.
- **Record.** Session history is system-written and append-only; a local,
  exportable record of the work stays with you.
- **Install.** One `.deb` package — application, local agent and
  command-line interface — with a signed APT repository for updates.

Tandem opens to a first group of design partners before the public trial.
If you run long delegated work and want it on Tandem first, write to
[tandem@jaryn.io](mailto:tandem@jaryn.io). The product pages are at
[jaryn.io/tandem](https://jaryn.io/tandem); plans and downloads open with the trial.

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

- [`sessions`](https://github.com/jaryn-io/sessions) — complete, real
  Tandem session records, in the same format you get on your own machine:
  brief, progress, handoffs between roles, reviews, evidence, what stayed
  open, closeout. Redacted where necessary. Proof you can read.
- [jaryn.io](https://jaryn.io) — product pages, in private preview. Releases and
  documentation as they open.

Watch this organisation to follow the work.

---

Jaryn, Tandem and AWOS names and logos are the property of Jaryn, all rights reserved. See [TRADEMARKS.md](https://github.com/jaryn-io/.github/blob/main/TRADEMARKS.md) and [NOTICE.md](https://github.com/jaryn-io/.github/blob/main/NOTICE.md).
