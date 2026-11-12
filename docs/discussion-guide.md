# Reading and discussion guide

These are suggested sessions, not scheduled meetings. Each can be done through
the linked papers and saved notebooks, with coding as an optional follow-up.

## Opening discussion: what is the claim?

Read [Ingressing Minds](https://www.mdpi.com/2409-9287/11/5/161) and explore the
[independent tour](https://ingressingminds.com/tour/). Choose one concrete example
and write down its observation, the proposed mechanism, and the philosophical
claim it is used to support.

The [figure-by-figure guide](figure-guide.md) covers all 15 figures and separates
biological evidence, mathematical constructions, conceptual diagrams and
philosophical analogies. Figures 8 and 14 directly connect to our existing
paradox and sorting projects; the kinetics project follows cited network studies.
For optional mathematical preparation, use the proposed
[Figure 5–6 exercises](figure-guide.md#concrete-extensions-for-figures-5-and-6).

Discuss what evidence would distinguish competing explanations. A working
simulation can establish behavior under its specified rules; deciding what that
behavior means for agency, cognition or the ontology of patterns requires
additional argument.

## Session 1: sorting and measurement

Read [the sorting study](https://arxiv.org/abs/2401.05375) and open the
[progress notebook](https://github.com/m9h/cell_research/blob/main/examples/01_progress.ipynb).
Work through the adjacent-swap example in the repository README by hand.

- Which progress measure makes the behavior look goal-directed?
- Does a temporary local setback still appear under a global measure?
- How does passive damage differ from an immovable obstacle?
- What would clustering look like with shuffled labels or a single policy?

Follow up with the [damage](https://github.com/m9h/cell_research/blob/main/examples/02_damage.ipynb)
and [clustering](https://github.com/m9h/cell_research/blob/main/examples/03_clustering.ipynb)
notebooks. Record one result that changes when a modeling or measurement choice
changes.

## Session 2: state, memory and controls

Read [the network-memory paper](https://pmc.ncbi.nlm.nih.gov/articles/PMC9820177/),
then the [model biology guide](https://github.com/m9h/GRN_ODE/blob/python-memory-replication/python/models/README.md)
and [memory notebook](https://github.com/m9h/GRN_ODE/blob/python-memory-replication/python/examples/memory_lab.ipynb).

- What stores information when reaction parameters and connectivity are fixed?
- Does the response require paired training, or is the unconditioned input alone enough?
- Does a matched sham probe distinguish recall from continuing drift?
- Did the intervention change a conserved molecular pool?
- Does the classification survive a changed threshold or observation window?

For a coding follow-up, compare the same trace across RoadRunner, COPASI and
Jaxkineticmodel. Agreement tests the numerical implementation. It does not decide
which definition of learning to adopt. The [RNM paper](https://pmc.ncbi.nlm.nih.gov/articles/PMC12210318/)
adds a discussion of computation through state transitions.

### Worked example: a reversal near zero

Our [network 26 comparison](https://github.com/m9h/GRN_ODE/blob/85615d284dcba168b93670ad6215d67f0290a4a0/python/CATALOG_BREAKING.md#tiny-residuals-change-literal-search-paths)
provides a concrete measurement exercise. In the indicated trial, the literal
MATLAB rule calls a response a downward reversal when

$$\overline{Y}_{\mathrm{cue}} \leq \overline{Y}_{\mathrm{pre}}/1.5.$$

Two otherwise matching simulation configurations produced these RoadRunner
means for `MSH`:

| Run | Pre-cue mean | Cue mean | Literal reversal |
|---|---:|---:|---|
| Local | −2.48124e-38 | −1.12648e-42 | No |
| Distributed | 6.72825e-39 | 3.05462e-43 | Yes |

Check the inequality by hand. The sign of a tiny residue changes its answer,
although all four values are far below the comparison's `1e-7` absolute floor.
The local case continues through eight trials; the distributed case stops
after one. Both classify the response as having **no resolved history effect
at rechallenge** when matched controls and numerical resolution are included.

Across the full model, the runs differ in 210 raw reversal labels, all involving
means below `1.35e-19`. Their controlled classification keys agree on all 1,440
shared response/engine assessments. Some later trials occur in only one run,
so this comparison does not establish equivalence of the complete search trees.

- Which part of this result comes from the reaction dynamics, and which from the decision rule?
- How should a ratio threshold treat values indistinguishable from zero?
- What would count as evidence that a change in history affects a later response?

This example concerns the interpretation of a simulation result. It does not
settle the paper's broader philosophical argument.

## Session 3: self-reference and dynamics

Read the introduction and initial examples of
[Mar and Grim](https://pgrim.org/articles/patternandchaos.pdf), then the
[paradox project guide](paradox-project.md) and
[executed lab](https://github.com/m9h/paradox-dynamics/blob/main/examples/paradox_lab.ipynb).

- Which assumptions turn a sentence into an update function?
- Is an oscillation evidence of contradiction, revision, or a chosen semantics?
- How would synchronous and sequential updates affect mutually referring statements?
- What distinguishes a fixed point, a periodic orbit and chaos?
- Why do exact rational and floating-point tent-map trajectories differ?
- Can a fixed orbit have a positive local expansion rate?

Choose one map in the working explorer. Change its initial value, arithmetic or
update schedule; export both runs and state which conclusions survive the change.

## Recording a discussion

Use this template in an issue, PR or shared notes:

```text
Reading / passage / figure:
Claim we discussed:
Observed or calculated result:
Model and assumptions:
Fork revision and settings, if applicable:
Measurement and comparison condition:
Alternative explanation:
What would change our assessment:
Next experiment or reading:
```

Original questions and critical interpretations are welcome. Cite passages and
link to source material so another reader can follow the reasoning.
