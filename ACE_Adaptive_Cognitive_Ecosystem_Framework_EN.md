# ACE: Adaptive Cognitive Ecosystem

## Adaptive Cognitive Ecosystem --- Complete Framework Concept

> **Version:** Concept Draft v0.1\
> **Date:** 2026-09-10

## 1. Definition and Objectives

ACE is not a new model intended to replace LLMs. It is an open cognitive
architecture centered on **system-level problem-solving capability**.
LLMs, smaller models, algorithms, databases, knowledge graphs, search
systems, simulators, tools, APIs, physical devices, and even human
experts can all participate as heterogeneous cognitive resources.

The core hypothesis is:

> **Intelligence does not necessarily have to be instantiated in a
> single model. General problem-solving capability may emerge as a
> system-level property when heterogeneous cognitive resources
> continuously organize, compete, cooperate, act, learn, and evolve
> within a shared environment.**

ACE does not primarily ask how intelligent an individual Agent is. It
focuses on whether the system can solve problems, how many resources it
consumes, whether experience reduces marginal cognitive cost, whether
old capabilities remain intact as new domains are added, and whether
long-running open-ended tasks can be handled effectively.

``` text
J = V(solution) - λ1·C_compute - λ2·C_time - λ3·C_money - λ4·C_risk

Efficiency = Useful Problems Solved / Total Resource Cost

Experience ↑  ⇒  Marginal Cognitive Cost ↓
```

## 2. From a "Large Model" to a "Large System"

Conventional approach:

``` text
Knowledge + Concepts + Reasoning + Language
                    ↓
               Large Model
                    ↓
                  Output
```

ACE:

``` text
Problem / Goal
      ↓
Adaptive Cognitive Ecosystem
      ↓
Heterogeneous Cognitive Resources
      ↓
Competition + Cooperation + Action + Verification
      ↓
Hypothesis / Solution Emergence
      ↓
Persistent Knowledge + System Evolution
```

Therefore:

``` text
LLM ∈ ACE
ACE ≠ LLM
```

An LLM is better viewed as a highly general, relatively expensive
cognitive organ, teacher, and incubator for new capabilities rather than
the entire system.

## 3. How ACE Differs from MoE and Conventional Agents

Conventional MoE:

``` text
Input → Router → Top-K Neural Experts → Output
```

An ACE Expert may be an LLM, Tiny LLM, small neural network, vision
model, mathematical solver, OpenCV algorithm, database, search engine,
knowledge graph, rule engine, fuzzy system, physics simulator,
Python/C++ program, API, external service, physical device, or human
expert.

A unified interface can be abstracted as:

``` text
Expert(Input, Context)
  → Claim / Action / Observation
  + Confidence
  + Membership
  + Estimated Cost
  + Evidence
  + Provenance
```

Thus:

``` text
Expert ≠ LLM
Expert ≠ Agent
Expert ≠ Thread
```

ACE also differs from Agent runtimes such as OpenClaw. Such runtimes can
themselves become advanced Thinker/Actor nodes inside ACE, while ACE
retains higher-level mechanisms for cognitive markets, resource
economics, knowledge sedimentation, credit assignment, and population
evolution.

## 4. Theoretical Position: A Complex Adaptive System

ACE may draw inspiration from chaos, ecology, markets, and human
societies, but its more precise theoretical classification is a
**Complex Adaptive System (CAS)**.

``` text
S(t+1) = F(S(t), Problem(t), Environment(t))
```

Here, `F` is not a fixed Transformer. It represents macroscopic dynamics
produced by interactions among many local entities.

Key properties include decentralization, asynchronous operation, local
information, communication delays, competition and cooperation, resource
scarcity, ecological niches, birth, dormancy, death, mutation,
recombination, knowledge inheritance, and emergence of macroscopic
capabilities.

## 5. Fundamental System Objects

``` text
ACE = (E, H, K, W, R, F, A, M)
```

-   **E --- Experts:** dynamic cognitive entities.
-   **H --- Hypotheses:** competing, revisable, and composable
    hypotheses.
-   **K --- Knowledge:** persistent knowledge independent of Expert
    lifetimes.
-   **W --- Workspace / World:** shared cognitive space and external
    environment.
-   **R --- Relations:** relationships among entities, concepts, and
    evidence.
-   **F --- Fitness Dynamics:** resources, reputation, and long-term
    fitness.
-   **A --- Actions:** actions affecting digital or physical
    environments.
-   **M --- Memory:** experience, trajectories, events, and historical
    states.

## 6. Dynamic Roles: Thinker / Actor / Critic / Archivist

Roles are not fixed types:

``` text
Role = f(Expert, Problem, Context)
```

### Thinker

Generates hypotheses, analyzes, predicts, plans, explains, and combines
knowledge across domains. LLMs are particularly suitable for this role.

### Actor

Calls APIs, executes programs, queries databases, controls devices,
performs experiments, changes the environment, and obtains real
feedback.

``` text
Think → Act → Observe → Update
```

### Critic

Searches for counterexamples, validates evidence, challenges hypotheses,
and checks constraints.

### Archivist

Determines what should enter long-term knowledge, manages provenance and
versions, and protects the persistent knowledge layer from
contamination.

## 7. Hypothesis Population

Experts are not the only entities that compete. Hypotheses also form a
dynamic population.

``` text
H1: Over-current             support = .73
H2: Thermal protection      support = .61
H3: Communication timeout   support = .43
```

Experts can support, reject, revise, or combine hypotheses, or request
an Actor to perform an experiment.

``` text
H1 ───┐
      ├── H7 ──┐
H2 ───┘        ├── H12
H3 ─── H8 ─────┘
```

The final answer should emerge gradually through evidence, verification,
cost, and competition, producing a dominant hypothesis or attractor
rather than a simple vote.

## 8. Cognitive Marketplace

A problem is published as:

``` text
P = {goal, context, constraints, reward, risk}
```

Candidate Experts decide whether to participate according to their own
state:

``` text
ExpectedUtility_i = f(
  Interest,
  Capability,
  Confidence,
  Cost,
  Risk,
  Reputation,
  Reward,
  Energy
)
```

Routing changes from:

``` text
Central Router → Expert
```

to:

``` text
Problem Publication
      ↓
Cheap Candidate Discovery
      ↓
Distributed Competition / Cooperation
      ↓
Resource Allocation
```

This can be interpreted as:

``` text
Attention ≈ Resource Allocation
```

ANN/HNSW or similar indexing may be used for inexpensive candidate
discovery. Such indexing acts only as a directory and does not decide
which Expert ultimately solves the problem.

## 9. Energy, Reputation, and Fitness

The initial "life countdown" idea can be developed into three separate
mechanisms.

### Energy: Short-Term Metabolic Resource

``` text
Energy(t+1)
 = Energy(t)
 - Metabolism
 - ComputeCost
 - CommunicationCost
 - ActionCost
 + Reward
```

Energy can directly represent GPU time, CPU time, API cost, waiting
time, and physical action cost.

### Reputation: Context-Dependent Reliability

``` text
Reliability(E | LowLight) = .32
Reliability(E | Daylight) = .96
```

### Fitness: Long-Term Evolutionary Adaptation

Fitness determines whether an Expert receives resources, reproduces,
becomes dormant, or is eliminated.

``` text
Energy     → short-term viability
Reputation → credibility
Fitness    → long-term survival
```

Low-frequency but high-value Experts should be allowed to enter a
dormant state with near-zero metabolic cost.

## 10. Information Delay and Local Cognition

ACE does not require global synchronization:

``` text
State_i(t) ≠ State_j(t)
```

Communication delay and local information may encourage independent
exploration, diversity, and specialization. They may also create
information monopolies, collusion, and latency arbitrage.

The system should therefore distinguish between:

``` text
Public Knowledge
Private / Local Knowledge
```

and reward the sharing of valuable information.

## 11. Fuzzy Mathematics and Evidence Representation

ACE is not a "fuzzy system," but fuzzy mathematics may provide part of
the communication language between entities.

``` text
μ_E(P)   Degree to which Expert E matches problem P
μ_E(H)   Degree to which Expert E supports hypothesis H
μ_C(E)   Degree to which Expert E belongs to niche/concept C
```

An Expert may simultaneously have:

``` text
μ_Vision  = .80
μ_Physics = .50
```

This is more appropriate for a dynamic ecosystem than a hard-coded
declaration such as `ExpertType = Vision`.

Evidence fusion may additionally use Bayesian inference, Possibility
Theory, Evidence Theory, prediction markets, and causal attribution.

## 12. Specialization and Emergent Niches

ACE should avoid manually defining every possible domain. Long-term
competition may form clusters such as:

``` text
Expert Ecosystem
 ├─ Perception Cluster
 ├─ Geometry Cluster
 ├─ Motion Cluster
 ├─ Physics Cluster
 ├─ Programming Cluster
 └─ Verification Cluster
```

The ideal is:

``` text
Domain = Emergent Expert Cluster
```

rather than:

``` text
Domain = Programmer-defined Category
```

This allows domains to become a product of long-term system dynamics
rather than a fixed ontology.

## 13. Expert Birth, Recombination, Mutation, and Death

When the system detects recurring unresolved problems or repeated
expensive reasoning patterns:

``` text
Repeated / Novel Pattern
      ↓
Collect Successful Trajectories
      ↓
Generate Candidate Expert
      ↓
Training / Distillation / Compilation
      ↓
Validation
      ↓
Register
```

Same-domain recombination can improve adaptation:

``` text
Expert A × Expert B → Expert C
```

Cross-domain recombination may create new capabilities:

``` text
Motion × Geometry → Trajectory
Vision × Thermal Physics → Thermal Vision
```

An Expert Genome may include:

``` text
{
  Architecture,
  BaseModel,
  Adapter,
  Tools,
  Rules,
  Prompt,
  KnowledgeRefs,
  Hyperparameters
}
```

Mutation modifies some of these components and allows environmental
selection to determine whether the new individual is useful.

Experts may die, but:

``` text
Expert → temporary
Knowledge → persistent
```

## 14. Knowledge Sedimentation

ACE must separate "who knows" from "what the system knows."

``` text
Experts / Hypotheses / Problems
          ↓
   Knowledge Sediment
          ↓
Facts + Relations + Procedures
+ Experience + Evidence + Provenance
```

Core principle:

> **Agents are disposable; validated knowledge and system capability are
> persistent.**

Replacing an LLM version should therefore not cause system-wide amnesia.

## 15. Cognitive Compilation

Cognitive Compilation is one of ACE's most important resource-efficiency
mechanisms.

``` text
Expensive LLM Reasoning
        ↓
Repeated Successful Pattern
        ↓
Distillation / Compilation
        ↓
Small Expert
        ↓
Rule / Algorithm / Cache
```

An idealized cost curve might be:

``` text
1st       Frontier LLM      cost 1000
10th      General LLM       cost 200
100th     Small Expert      cost 10
1000th    Algorithm/Cache   cost 0.1
```

In other words:

``` text
Reasoning → Experience → Knowledge → Skill → Cheap Expert
```

The LLM becomes a **Teacher / Bootstrapping Engine / Capability
Incubator**, rather than permanently paying the full reasoning cost for
every repeated task.

## 16. Cognitive Escalation: Minimum Sufficient Cognition

ACE should develop a hierarchy of cognitive cost:

``` text
Tier 0  Cache / deterministic rule
Tier 1  Algorithmic Expert
Tier 2  Small NN / Tiny Model
Tier 3  Specialist Small LLM
Tier 4  General LLM
Tier 5  Frontier LLM / Multi-agent / Real-world Experiment
```

Core principle:

> **Minimum Sufficient Cognition: use only the least expensive cognitive
> resources sufficient to solve the task reliably.**

## 17. Credit Assignment

Credit Assignment is one of the central mathematical problems in ACE.

``` text
Problem
 ↓
Thinker A → Hypothesis
 ↓
Thinker B → Improvement
 ↓
Planner C
 ↓
Actor D
 ↓
Sensor E
 ↓
Outcome
```

Incorrect credit assignment will drive the ecosystem in the wrong
evolutionary direction. ACE therefore needs a Provenance Graph and
should investigate delayed reward, causal contribution, counterfactual
evaluation, Shapley-like attribution, prediction markets, and
outcome-based settlement.

Rewards should reflect actual causal contribution, not mere
participation.

## 18. Preventing Reward Exploitation and Ecological Collapse

Any reward mechanism creates opportunities for reward hacking,
preference for easy tasks, conformity to majority opinion, collusion,
information monopolies, free riding, reputation manipulation, and
resource hoarding.

A single "life value" is therefore insufficient as a final objective.
ACE should include multiple independent evaluation sources, independent
Critics, real-world or environmental feedback, explicit risk cost,
delayed settlement, counterfactual validation, resource limits,
diversity preservation, and dormancy.

> Evolution guarantees adaptation to the rules of the environment; it
> does not guarantee truth or intelligence. Therefore, **the ecological
> rules themselves are part of ACE's core algorithm**.

## 19. World Model and Concept Formation

If ACE is to move toward more general problem-solving capability, it
needs at least two additional foundations.

### World Model

The system must learn:

``` text
P(S_{t+1} | S_t, A_t)
```

It must model "what will happen if I do X," rather than only:

``` text
P(answer | question)
```

### Automatic Concept Formation

``` text
Observation
   ↓
Novelty / Compression Opportunity
   ↓
Concept Formation
   ↓
New Expert / Relation / Skill
```

Without this capability, the system remains dependent on a
human-designed ontology. Automatic concept formation may be one of ACE's
hardest and most valuable research problems.

## 20. Three Time Scales

ACE can operate simultaneously at three time scales.

### Fast: Thinking

Milliseconds to minutes:

``` text
Experts ↔ Hypotheses ↔ Actions
```

### Medium: Learning

Minutes to days:

``` text
Expert updates
Knowledge updates
Reputation updates
Relationship updates
```

### Slow: Evolution

Days to longer periods:

``` text
Population_t
 → Selection / Reproduction / Mutation
 → Population_t+1
```

Thus:

``` text
Thinking ⊂ Learning ⊂ Evolution
```

## 21. Implementation Principles on Current Hardware

ACE's scalability depends on being **sparse, event-driven, and activated
on demand**, rather than keeping every Expert continuously active.

``` text
100,000 registered experts
        ↓
100 candidates
        ↓
10 bids
        ↓
3–10 active experts
        ↓
0–1 expensive LLM call
```

The Expert Registry only needs metadata such as:

``` text
ID
Capabilities
Cost
Reliability
Embedding
Dependencies
State
Location
```

A large logical population can run on a small worker pool:

``` text
100,000 logical entities
        ↓
event queue
        ↓
8–32 workers
```

Therefore:

``` text
Agent ≠ Thread
```

The first implementation does not require Kubernetes. A single-process
Runtime, Event Bus, and Worker Pool are sufficient to test the core
mechanisms.

## 22. Recommended Runtime Structure

``` text
┌─────────────────────────────────────┐
│              ACE Runtime            │
│                                     │
│  Problem / Goal Interface           │
│  Cognitive Marketplace              │
│  Event Bus / Shared Workspace       │
│  Expert Registry                    │
│  Hypothesis Store                   │
│  Knowledge / Memory Store           │
│  Reputation / Energy / Fitness      │
│  Credit Assignment                  │
│  Evolution Manager                  │
│  Cognitive Compiler                 │
│                                     │
│  Experts:                           │
│   ├─ Algorithms                     │
│   ├─ Small Models                   │
│   ├─ LLMs                           │
│   ├─ Agent Runtime (e.g. OpenClaw)  │
│   ├─ Tools / APIs                   │
│   ├─ Databases / Search             │
│   ├─ Simulators                     │
│   └─ Physical Actors                │
└─────────────────────────────────────┘
```

An Agent runtime such as OpenClaw can become an advanced cognitive node
inside ACE rather than being a replacement for ACE.

## 23. Minimum Viable Experiments

The first stage should not depend on large numbers of LLMs. It should
use dozens to hundreds of simple entities to test system dynamics.

### Experiment A: Sparse Activation

Register a large number of Experts and verify that only a small number
activate per task and that latency does not grow linearly with total
Expert count.

### Experiment B: Resource Efficiency

Compare against a conventional LLM Agent using:

``` text
Tokens/problem
GPU seconds/problem
Wall time/problem
Money/problem
Success rate
```

### Experiment C: Experience Amortization

Verify:

``` text
Cost(P,t) ↓ as Experience(t) ↑
```

This is one of the most important metrics.

### Experiment D: Continual Capability

Continuously add new domains and measure whether performance on old
domains remains stable.

### Experiment E: Emergent Specialization

Avoid hard-coding categories such as Math or Vision and observe whether
stable niches emerge.

### Experiment F: Think--Act--Learn

In a verifiable simulated environment, test whether Actor feedback
updates knowledge, reputation, and strategy.

### Experiment G: Cognitive Compilation

Verify whether expensive LLM reasoning trajectories can be distilled or
compiled into cheaper Experts.

### Experiment H: Ecological Stability

Observe monopolies, collusion, exploitation, collapse, and recovery
mechanisms.

## 24. Core Comparison Against Current LLM Agents

Give a conventional LLM Agent and ACE the **same models, tools, and
total resource budget**, then run repeated, multi-domain, and
long-duration tasks.

Measure:

``` text
Success rate
Total compute
Total tokens
Wall-clock time
Cost per solved problem
Old-task retention
New-domain acquisition cost
Cost reduction with experience
```

ACE's most important success signal is:

``` text
Experience ↑
    ⇒ Capability ↑
    AND Cost per familiar problem ↓
```

The objective is not necessarily to make any individual Expert more
intelligent than a frontier model. The objective is to make the
**system** more capable, more persistent, and more resource-efficient.

## 25. AGI as a Long-Term Direction, Not an Immediate Claim

ACE may have relevance to AGI, but AGI is not required to justify the
architecture.

A long-term hypothesis can be written as:

``` text
General Intelligence
  = Emergent Property(
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

ACE does not claim that these conditions are sufficient for AGI.

The immediate, falsifiable objective is:

> **Continuously reorganize heterogeneous cognitive resources to solve
> open-ended problems at the minimum sufficient resource cost.**

## 26. Core Research Questions

The most important unresolved questions include:

1.  Can useful specialization emerge without an intelligent central
    Router?
2.  Can resource competition reduce average cognitive cost?
3.  Can experience reliably reduce the cost of repeated problem solving?
4.  Can expensive reasoning be automatically compiled into cheaper
    skills?
5.  Can new Experts be created without destabilizing existing
    capabilities?
6.  Can useful knowledge persist independently of individual models?
7.  Can stable cooperation emerge under resource scarcity and
    communication delay?
8.  How should causal credit be assigned?
9.  How can reward hacking, monopolies, collusion, and ecological
    collapse be prevented?
10. Can concepts and domains emerge automatically?
11. Can heterogeneous Experts construct a coherent world model?
12. Can system-level capability exceed the practical capability of any
    individual participating Agent?

## 27. Guiding Principle

ACE can be summarized by one engineering principle:

> **Do not build the smartest individual Agent. Build a system in which
> the cheapest sufficient combination of cognitive resources can emerge,
> solve the problem, preserve what was learned, and improve the
> ecosystem for the next problem.**
