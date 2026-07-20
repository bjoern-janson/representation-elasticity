# Benchmark Design

## Overview

Most AI benchmarks evaluate performance within a fixed representation.

A model is given a task, optimizes within the provided coordinate system, and receives a score based on prediction accuracy.

This framework proposes a different objective.

Instead of asking:

> "Can the model solve this problem?"

it asks:

> "Can the model discover a better way to represent the problem?"

The benchmark shifts the focus from optimization **within** a representation to evolution **of** the representation itself.

---

# The Core Principle

Scientific progress rarely comes from searching harder inside an existing framework.

Instead, it often comes from discovering a representation where the problem becomes dramatically simpler.

Therefore, benchmarking intelligence should measure representation evolution rather than task completion alone.

---

# Four Evaluation Dimensions

## 1. Compression

Can the agent replace a complex explanation with a simpler one?

Instead of rewarding memorization, the benchmark rewards reduction in description length.

```
Large dataset
        │
        ▼
Hidden invariant
        │
        ▼
Compact explanation
```

The important question is not:

> "How much information can the model store?"

Instead:

> "How little information is actually necessary?"

---

## 2. Invariance

A genuine representation should survive superficial transformations.

Examples include:

- changing notation
- renaming variables
- rotating coordinates
- changing presentation order
- translating languages
- cosmetic interface changes

If performance collapses after these changes, the model likely memorized surface structure instead of underlying relationships.

---

## 3. Generalization

A representation should generate predictions that were never observed during training.

The benchmark therefore includes:

- zero-shot tasks
- counterfactual reasoning
- out-of-distribution problems
- novel combinations

The objective is to evaluate the fertility of the representation rather than recall.

---

## 4. Representation Evolution

The most important question:

Can the model recognize that its own representation is failing?

Rather than endlessly patching exceptions, does it eventually discover a simpler coordinate system?

---

# Proposed Evaluation Pipeline

```
Unknown Domain
      │
      ▼
Observation
      │
      ▼
Initial Representation
      │
      ▼
Prediction
      │
      ▼
Failure
      │
      ▼
Representation Revision
      │
      ▼
Improved Prediction
      │
      ▼
Compression
```

The benchmark evaluates every stage of this cycle.

---

# The Forgetting Test

One proposed evaluation is intentional information removal.

After learning, remove a large fraction of available observations.

```
100% observations
        │
        ▼
Learn representation
        │
        ▼
Remove 90–99% of observations
        │
        ▼
Retest
```

Three outcomes are possible.

### Collapse

Performance falls dramatically.

The representation depended on the removed information.

---

### Stability

Performance remains largely unchanged.

The representation captured the underlying structure.

---

### Improvement

Performance increases.

The removed information was primarily noise.

The representation had successfully identified the minimal sufficient information.

---

# Representation Lifetime

Learning should not be measured only by accuracy.

It should also be measured by how representations evolve.

A healthy learning cycle looks like:

```
Simple Model

↓

Unexpected anomaly

↓

Temporary increase in complexity

↓

Invariant discovery

↓

Simpler permanent model
```

An unhealthy cycle looks like:

```
Simple Model

↓

Unexpected anomaly

↓

Permanent patches

↓

More patches

↓

More exceptions

↓

Model collapse
```

---

# Tool Metabolization

The benchmark does not prohibit tools.

Instead, it measures what happens after tools are removed.

Ideal progression:

```
Tool

↓

Observation

↓

Internalization

↓

Tool removed

↓

Performance unchanged
```

Poor progression:

```
Tool

↓

Prediction

↓

Tool removed

↓

Failure
```

The distinction is whether the tool became internal understanding or remained an external dependency.

---

# Representation Respec

Another proposed evaluation is representation replacement.

The benchmark deliberately introduces situations where the current model becomes increasingly inefficient.

The question becomes:

Will the system continue adding exceptions?

Or will it voluntarily replace its own representation?

A mature learner should recognize when rebuilding is cheaper than continued patching.

---

# Scientific Discovery Tasks

Rather than giving agents predefined labels, benchmarks should include environments where:

- hidden variables exist
- latent symmetries exist
- causal mechanisms exist
- compact explanations exist

The agent is rewarded for discovering these structures rather than reproducing known answers.

---

# Open-Ended Domains

The benchmark is intended for environments where the governing rules are initially unknown.

Possible domains include:

- synthetic physics
- cellular automata
- unknown programming languages
- procedural games
- symbolic systems
- mathematical structures
- simulated ecosystems

The objective is not task completion.

The objective is discovering the governing grammar.

---

# Success Criteria

A successful agent should demonstrate:

- increasing compression
- stable invariance
- growing generative ability
- decreasing dependence on external scaffolding
- periodic representation replacement when necessary

Performance is measured over the entire lifecycle of learning rather than a single task.

---

# Long-Term Vision

Current benchmarks primarily evaluate optimization.

This proposal aims to evaluate representation evolution.

The central hypothesis is that higher intelligence is characterized not only by better predictions, but by the ability to repeatedly discover simpler, more powerful ways of representing reality.

If correct, benchmarks should reward systems that improve their own internal languages, rather than only improving performance within fixed ones.
