---
title: Not Building the Dragon. Building the Saddle.
date: 2026-03-06
status: published
---

## The Industry Has Five Layers

1. **Foundation Model / Training** - pretraining, alignment, RLHF. Dominated by a handful of labs with billions in compute budgets.
2. **Model Serving / AI Infra** - inference engines, GPU orchestration, throughput optimization.
3. **AI Platform / Enterprise Integration** - the plumbing that connects models to real systems: orchestration, context pipelines, internal tooling.
4. **AI Application / Workflow Automation** - concrete agents solving specific problems: coding assistants, on-call bots, document intelligence.
5. **AI Governance / Security / Compliance** - auditing, policy enforcement, regulatory frameworks.

---

## Where I'm Not Going, and Why

**Layers 1 and 2** are closed to me - not because of geography, but because of resource reality. Training frontier models requires thousands of H100s. Inference engine work at that scale requires teams inside OpenAI or Anthropic building custom CUDA kernels. I'm not in that game.

**Layer 5** requires deep fluency in Japanese business culture, regulatory language, and organizational politics. As a foreigner who can barely hold a conversation in Japanese, I'd be fighting with one hand tied behind my back.

**Pure application work** (Layer 4 alone) is where the "Web developer" trap lives - calling APIs, writing prompts, shipping demos. It gets commoditized fast. Claude Code already automates a lot of it.

---

## Where I'm Focusing: Layers 3 and 4, the Hard Parts

My target is the intersection that model companies and cloud providers can't easily absorb, because it requires understanding a specific organization's data, systems, and constraints. Four pillars:

**Agent Runtime & Orchestration** - not just chaining prompts, but building execution environments that handle multi-step task graphs, failure recovery, idempotency, and cost control. This is distributed systems thinking applied to agents. My natural ground.

**Permission-aware Retrieval & Context Systems** - the enterprise problem isn't that the model is dumb; it's that it lacks the right context. Building retrieval pipelines that respect IAM and RBAC at query time, not just display time, is genuinely hard and genuinely unsolved.

**Systematic Evaluation** - the discipline that separates "it looks good in demo" from "it works in production." Scenario-based regression suites, model-as-judge rubrics, behavioral consistency testing across model upgrades. Underrated and irreplaceable.

**Observability, Replay & Debugging** - you cannot manage what you cannot see. Structured reasoning traces, cost attribution, and the ability to replay an agent's decision path and ask "what if the context had been different?" This is where my data pipeline background translates directly.

---

## The Project That Covers All Four

I'm building a multi-agent platform around two scenarios: a **coding agent** and an **on-call investigation agent**. Same underlying chassis - reliability, security, observability - applied to two domains I actually understand deeply.

The on-call agent is where the permission-retrieval problem becomes real: it needs to pull from runbooks, incident history, metrics, and customer data, all with different access levels. That's not a toy problem.

---

## The Honest Reason This Path Makes Sense

The talent structure in this space is badly skewed. ML researchers understand models but not production systems. Traditional backend engineers understand systems but not model behavior. The overlap is small and the demand is growing.

I'm coming from the systems side. My job over the next few years is to close the gap toward the model side - not all the way to research, but far enough to design systems that treat model behavior as a first-class engineering concern.

That's the bet. Writing it down so I don't drift.