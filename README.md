# ACE — Adaptive Cognitive Ecosystem

> **An experimental architecture for resource-efficient, continuously evolving, system-level intelligence.**

ACE (**Adaptive Cognitive Ecosystem**) is an open research project exploring a different way to build intelligent systems.

Instead of asking:

> **How can we build a larger and smarter model?**

ACE asks:

> **How can heterogeneous cognitive resources organize themselves to solve problems efficiently?**

ACE does **not** attempt to replace Large Language Models.

LLMs are treated as powerful general-purpose cognitive components within a larger ecosystem that may also contain small models, algorithms, databases, search engines, symbolic systems, simulators, tools, APIs, physical actors, and other specialized Experts.

The primary unit of intelligence is therefore not an individual model or Agent.

It is the **system**.

---

## The Core Idea

Modern AI systems increasingly concentrate knowledge, reasoning, and language capability inside very large parameterized models.

ACE explores a complementary scaling paradigm:

```text
                Problem / Goal
                      │
                      ▼
          Adaptive Cognitive Ecosystem
                      │
       ┌──────────────┼──────────────┐
       ▼              ▼              ▼
    Thinkers         Actors         Critics
       │              │              │
       └──── Competition / Cooperation ────┘
                      │
                      ▼
             Hypothesis Population
                      │
               Evidence / Action
                      │
                      ▼
                   Outcome
                      │
          ┌───────────┼───────────┐
          ▼           ▼           ▼
       Knowledge   Reputation   Fitness
          │                       │
          ▼                       ▼
   Persistent Memory       System Evolution
```

The central hypothesis is:

> **Intelligence does not necessarily have to be instantiated in a single model. General problem-solving capability may emerge as a system-level property from the interaction, specialization, competition, cooperation, action, learning, and evolution of heterogeneous cognitive resources.**

In short:

```text
LLM ∈ ACE

ACE ≠ LLM
```

---

## Why ACE?

A conventional LLM may repeatedly spend substantial computation solving structurally similar problems.

ACE investigates whether a long-lived cognitive system can instead transform experience into progressively cheaper capabilities:

```text
Expensive Reasoning
        │
        ▼
     Experience
        │
        ▼
      Knowledge
        │
        ▼
       Skill
        │
        ▼
 Specialized Expert
        │
        ▼
 Algorithm / Rule / Cache
```

Ideally:

```text
Experience ↑  ⇒  Marginal Cognitive Cost ↓
```

For example:

```text
First encounter      Frontier LLM       cost = 1000
Repeated task        General LLM        cost = 200
Learned task         Small Expert       cost = 10
Compiled skill       Algorithm/Cache    cost = 0.1
```

We call this process **Cognitive Compilation**.

A major research question is therefore:

> Can an intelligent system become computationally cheaper as it becomes more experienced?

---

## Experts Are Not Necessarily LLMs

An ACE Expert is simply a cognitive resource capable of contributing useful information or actions.

An Expert may be:

* a large language model;
* a small specialized language model;
* a neural network;
* a computer vision model;
* a mathematical solver;
* a deterministic algorithm;
* a fuzzy inference system;
* a database;
* a knowledge graph;
* a search engine;
* a physics simulator;
* a Python or C++ program;
* an API;
* an existing Agent runtime;
* a physical device;
* or potentially a human expert.

Conceptually:

```text
Expert(Input, Context)
    ↓
Claim / Action / Observation
Confidence / Membership
Evidence / Provenance
Estimated Cost
```

Therefore:

```text
Expert ≠ LLM
Expert ≠ Agent
Expert ≠ Thread
```

A two-microsecond geometry function can be an Expert just as legitimately as a frontier LLM.

---

## A Cognitive Economy

ACE treats computation as a scarce resource.

Experts may maintain several independent state variables:

```text
Energy
Reputation
Fitness
```

**Energy** represents short-term computational resources.

```text
Energy(t+1)
 =
Energy(t)
- ComputeCost
- CommunicationCost
- ActionCost
+ Reward
```

It can correspond directly to real resources such as:

```text
GPU time
CPU time
LLM tokens
API cost
wall-clock time
physical action cost
```

**Reputation** represents how trustworthy an Expert has historically been in a particular context.

**Fitness** influences its long-term evolutionary survival.

This creates a simple pressure:

> An Expert that unnecessarily uses expensive cognition should eventually lose against another Expert that produces equivalent results more efficiently.

---

## From Routing to Competition

Traditional MoE architectures generally use:

```text
Input
  ↓
Router
  ↓
Top-K Experts
```

ACE investigates whether part of this decision can emerge from resource competition.

A problem can instead be published into a shared cognitive environment:

```text
Problem
   │
   ▼
Candidate Discovery
   │
   ▼
Experts evaluate:
   │
   ├── Can I contribute?
   ├── How confident am I?
   ├── What will it cost?
   ├── What is the expected reward?
   └── Is it worth participating?
   │
   ▼
Competition / Cooperation
```

A cheap approximate index may discover potentially relevant Experts, but it does not need to understand the problem or decide who should solve it.

This leads to an interesting interpretation:

> **Attention may emerge as resource allocation.**

---

## Thinkers and Actors

Reasoning alone is insufficient for an open-ended cognitive system.

ACE therefore distinguishes between cognition and interaction with the environment.

A **Thinker** may:

* generate hypotheses;
* reason;
* predict;
* plan;
* explain;
* combine knowledge.

An **Actor** may:

* execute code;
* query a database;
* call an API;
* perform an experiment;
* use a tool;
* control a device;
* modify the environment.

This creates the fundamental loop:

```text
Think
  ↓
Act
  ↓
Observe
  ↓
Update
```

Roles do not need to be permanent:

```text
Role = f(Expert, Problem, Context)
```

The same Expert may act as a Thinker in one problem and a Critic or Actor in another.

---

## Hypotheses Compete Too

Experts are not the only population in ACE.

Solutions themselves may form a **Hypothesis Population**.

```text
H1: Cause A        support = 0.73
H2: Cause B        support = 0.61
H3: Cause C        support = 0.43
```

Experts can:

```text
support
challenge
modify
combine
test
```

hypotheses.

For example:

```text
H1 ─────┐
        ├── H7 ─────┐
H2 ─────┘           │
                    ├── H12
H3 ───── H8 ────────┘
```

The system's answer can therefore emerge gradually from evidence and interaction rather than being produced by a single inference pass.

---

## Persistent Knowledge, Disposable Experts

One of ACE's most important design principles is:

> **Experts are temporary. Validated knowledge should be persistent.**

An Expert may:

```text
be created
learn
specialize
reproduce
become dormant
be replaced
die
```

while its useful discoveries remain available to the ecosystem.

```text
Dynamic Experts
      │
      ▼
Validated Experience
      │
      ▼
Knowledge Sedimentation
      │
      ├── Facts
      ├── Relations
      ├── Procedures
      ├── Evidence
      └── Provenance
```

This separates:

```text
System Identity
```

from:

```text
Model Identity
```

Replacing one LLM with a newer model should not imply rebuilding the entire cognitive system or losing accumulated experience.

---

## Evolution

Experts may be created dynamically when the ecosystem repeatedly encounters a capability gap.

```text
Repeated expensive reasoning
            │
            ▼
       Pattern discovery
            │
            ▼
      Candidate Expert
            │
            ▼
 Training / Distillation /
 Compilation / Validation
            │
            ▼
      New capability
```

Experts may also recombine.

```text
Motion Expert
      ×
Geometry Expert
      │
      ▼
Trajectory Expert
```

or:

```text
Vision Expert
      ×
Thermal Physics Expert
      │
      ▼
Thermal Vision Expert
```

An Expert's "genome" does not need to be raw neural weights. It might contain:

```text
architecture
base model
adapter
tools
rules
prompt
knowledge references
hyperparameters
```

This allows mutation and recombination to remain relatively inexpensive.

---

## Emergent Specialization

ACE does not assume that every cognitive domain must be defined by a programmer.

Instead of permanently declaring:

```text
ExpertType = Vision
```

an Expert might have fuzzy memberships such as:

```text
Vision   = 0.80
Physics  = 0.50
Geometry = 0.67
```

Over time, competition and cooperation may produce stable clusters:

```text
              Expert Ecosystem
                     │
       ┌─────────────┼─────────────┐
       ▼             ▼             ▼
   Perception     Reasoning     Verification
       │             │             │
   ┌───┼───┐     ┌───┼───┐     ┌───┼───┐
 Vision Shape    Logic Causal   Test Critic
```

Ideally:

```text
Domain = Emergent Expert Cluster
```

rather than:

```text
Domain = Programmer-defined Ontology
```

---

## Minimum Sufficient Cognition

Not every problem deserves the most powerful model available.

ACE can organize cognition into an escalation hierarchy:

```text
Tier 0   Cache
          ↓ miss
Tier 1   Deterministic Algorithm
          ↓
Tier 2   Small Specialized Model
          ↓
Tier 3   Small Specialist LLM
          ↓
Tier 4   General LLM
          ↓
Tier 5   Frontier LLM / Multi-Agent /
         Simulation / Real-world Experiment
```

The system should learn:

> **What is the least expensive cognitive resource sufficient to solve this problem reliably?**

We call this **Minimum Sufficient Cognition**.

---

## Sparse Cognition

ACE is intended to be highly sparse.

A future system might contain:

```text
100,000 registered Experts
```

while a particular problem activates only:

```text
100 candidates
     ↓
10 participants
     ↓
3–5 active solvers
     ↓
0–1 expensive LLM calls
```

Therefore:

```text
Total Cognitive Capacity
          ≠
Per-Problem Compute
```

This is one of the central scaling hypotheses behind ACE.

---

## Event-Driven Architecture

ACE should not assign one operating-system thread to every Expert.

Instead:

```text
100,000 logical Experts
          ↓
       Event Queue
          ↓
     8–32 Workers
```

Most Experts remain dormant until relevant events occur.

```text
Sleep
  ↓
Relevant Event
  ↓
Wake
  ↓
Evaluate / Act
  ↓
Sleep
```

This makes large logical populations feasible on conventional hardware.

---

## Knowledge Capacity vs. Inference Compute

ACE explores whether:

```text
Knowledge Capacity
```

can grow substantially without forcing proportional growth in:

```text
Inference Compute
```

Explicit facts, procedures, relations, algorithms, and specialized skills can often be stored far more cheaply than repeatedly reconstructing them through large-model inference.

This leads to another central hypothesis:

> **Knowledge growth and inference cost do not necessarily need to scale together.**

---

## Credit Assignment

One of the hardest problems in ACE is determining who actually contributed to a successful outcome.

```text
Problem
   ↓
Thinker A
   ↓
Hypothesis
   ↓
Thinker B improves it
   ↓
Planner C
   ↓
Actor D
   ↓
Observation
   ↓
Success
```

How should the reward be distributed?

Potential mechanisms include:

```text
causal contribution
counterfactual evaluation
delayed reward
Shapley-like attribution
prediction markets
outcome-based settlement
```

Incorrect credit assignment could cause the entire ecosystem to evolve in the wrong direction.

---

## Ecological Failure Modes

Evolution does not guarantee intelligence.

It guarantees adaptation to the environment and its reward structure.

ACE therefore needs to explicitly study:

* reward hacking;
* short-termism;
* easy-task preference;
* collusion;
* information monopolies;
* free riding;
* reputation manipulation;
* resource hoarding;
* monocultures;
* ecological collapse.

This leads to an important principle:

> **The rules of the ecosystem are themselves part of the intelligence architecture.**

---

## World Models and Concept Formation

Two major open problems are especially important.

### World Models

ACE needs to reason about:

```text
P(S[t+1] | S[t], Action[t])
```

rather than only:

```text
P(answer | question)
```

The Actor layer is essential because actions provide real evidence with which to update the system's world model.

### Automatic Concept Formation

A sufficiently general ACE should eventually perform:

```text
Observation
     ↓
Novelty
     ↓
Abstraction / Compression
     ↓
New Concept
     ↓
New Relation / Skill / Expert
```

The system should not require humans to manually define every possible cognitive domain.

---

## Three Time Scales

ACE separates three kinds of adaptation.

### Thinking

Milliseconds to minutes:

```text
Experts ↔ Hypotheses ↔ Actions
```

### Learning

Minutes to days:

```text
Expert updates
Knowledge updates
Reputation updates
Relationship updates
```

### Evolution

Days to longer periods:

```text
Population[t]
    ↓
Selection
Reproduction
Mutation
Dormancy
Death
    ↓
Population[t+1]
```

Conceptually:

```text
Thinking ⊂ Learning ⊂ Evolution
```

---

## Proposed Runtime

A possible implementation could look like:

```text
┌───────────────────────────────────────────┐
│                 ACE Runtime               │
│                                           │
│  Problem / Goal Interface                 │
│  Cognitive Marketplace                    │
│  Event Bus / Shared Workspace             │
│  Expert Registry                          │
│  Hypothesis Store                         │
│  Knowledge / Memory Store                 │
│  Energy / Reputation / Fitness            │
│  Provenance / Credit Assignment           │
│  Evolution Manager                        │
│  Cognitive Compiler                       │
│                                           │
│  Cognitive Resources                      │
│   ├─ Algorithms                           │
│   ├─ Small Models                         │
│   ├─ LLMs                                 │
│   ├─ Agent Runtimes                       │
│   ├─ Tools / APIs                         │
│   ├─ Databases / Search                   │
│   ├─ Simulators                           │
│   └─ Physical Actors                      │
└───────────────────────────────────────────┘
```

The first implementation does not require a large distributed infrastructure.

A single runtime containing an event bus, Expert registry, worker pool, persistent store, and optional LLM API is sufficient to test many of the core hypotheses.

---

## Research Questions

ACE is currently a research hypothesis, not a proven architecture.

Some of the most important questions are:

1. Can useful specialization emerge without a central intelligent Router?
2. Can resource competition reduce average cognitive cost?
3. Can experience reliably reduce the cost of repeated problem solving?
4. Can expensive reasoning be automatically compiled into cheaper skills?
5. Can new Experts be created without destabilizing existing capabilities?
6. Can useful knowledge persist independently of individual models?
7. Can stable cooperation emerge under resource scarcity?
8. How should causal credit be assigned?
9. How can ecological collapse and reward hacking be prevented?
10. Can useful concepts and domains emerge automatically?
11. Can heterogeneous Experts construct a coherent world model?
12. Can system-level capability exceed the practical capability of any individual participating Agent?

---

## What Would Count as Success?

ACE does **not** need to demonstrate AGI to be useful.

A meaningful first result would be showing that, given the **same models, tools, and total resource budget**, ACE can achieve:

```text
equal or higher task success
+
lower average compute
+
lower token consumption
+
lower marginal cost with experience
+
better continual-learning behavior
+
better long-duration task performance
```

The most important experimental curve is:

```text
Cost(problem, experience)
```

A successful ACE should demonstrate:

```text
Experience ↑
     │
     ├── Capability ↑
     │
     └── Cost per familiar problem ↓
```

If this behavior can be demonstrated reliably, it would already justify further research regardless of whether ACE ultimately contributes to AGI.

---

## AGI Is a Direction, Not the Immediate Claim

ACE is motivated in part by a broader question:

> Could general intelligence be an emergent property of a persistent cognitive ecosystem rather than a property of one sufficiently large model?

A possible long-term formulation is:

```text
General Intelligence
        =
Emergent Property(
    Diverse Specialists,
    Shared World,
    Competition,
    Cooperation,
    Action,
    Memory,
    Knowledge,
    Evolution
)
```

However, ACE does **not** claim that this is sufficient for AGI.

The immediate objective is narrower and experimentally testable:

> **Continuously reorganize heterogeneous cognitive resources to solve open-ended problems at the minimum sufficient resource cost.**

---

## Current Status

ACE is currently at the **concept and architecture exploration stage**.

The initial development focus should be:

```text
Phase 1
Minimal ecosystem simulation

Phase 2
Expert protocol + marketplace

Phase 3
Thinker / Actor / Critic loop

Phase 4
Persistent knowledge + provenance

Phase 5
Energy / Reputation / Credit Assignment

Phase 6
Cognitive Compilation

Phase 7
Expert creation and evolution

Phase 8
Long-running comparative experiments
```

The project should favor small, falsifiable experiments over prematurely building a large multi-agent platform.

---

## Design Principle

The project can be summarized by one principle:

> **Do not build the smartest individual Agent. Build a system in which the cheapest sufficient combination of cognitive resources can emerge, solve the problem, preserve what was learned, and improve the ecosystem
