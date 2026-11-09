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
