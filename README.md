# SF Cog Sci reading group · Ingressing Minds

A reading and computational-project guide for discussing Michael Levin's
*Ingressing Minds: Causal, Non-Physical Patterns In-Form Natural, Synthetic, and
Hybrid Embodiments*. Follow the readings, inspect working examples, and connect
claims about intelligence and agency to specific models and measurements.

## Start here

- **Read the paper:** [Levin, Philosophies 11(5), 161 (2026)](https://www.mdpi.com/2409-9287/11/5/161)
  · [DOI](https://doi.org/10.3390/philosophies11050161).
- **Explore the companion resource:** [ingressingminds.com](https://ingressingminds.com/)
  · [interactive tour](https://ingressingminds.com/tour/). This is an independently
  made guide; its site states that it is not affiliated with Levin, his lab, or Tufts.
- **Choose a project:** the three tracks below move from sorting to biochemical
  memory to self-reference.
- **Follow the argument visually:** [all 15 figures explained](docs/figure-guide.md),
  with their evidential role, links to our projects, and proposed Figure 5–6 experiments.
- **Prepare for discussion:** [reading and discussion guide](docs/discussion-guide.md).
- **Find sources:** [annotated references](REFERENCES.md)
  · [BibTeX bibliography](references.bib).

You can start without installing anything: all three projects contain executed
notebooks and saved figures. Installation and reproduction
instructions live with each project's code.

## The three computational projects

Figures **8** (logical dynamics) and **14** (sorting) directly anchor two tracks.
The network-memory track follows studies cited in the text, especially reference
212; Figure 10C connects learning to the proposed spectrum conceptually.
Figures 5–6 motivate additional mathematical projects that are
[proposed, not yet implemented](docs/figure-guide.md#concrete-extensions-for-figures-5-and-6).

| Project | Central question | Start with | Status |
|---|---|---|---|
| **1. Self-sorting arrays** | How do local policies, damage and our choice of progress metric shape apparent problem-solving? | [Sorting fork](https://github.com/m9h/cell_research) · [three notebooks](https://github.com/m9h/cell_research/tree/main/examples) | Runnable examples, controls and replay |
| **2. Regulatory-network memory** | How can fixed reaction equations produce responses that depend on stimulation history? | [Python replication](https://github.com/m9h/GRN_ODE/tree/python-memory-replication/python) · [executed notebook](https://github.com/m9h/GRN_ODE/blob/python-memory-replication/python/examples/memory_lab.ipynb) | Five models, eight experiments, three validated simulators |
| **3. Logical paradoxes as dynamical systems** | What behavior follows when truth-value revision becomes an iterated map? | [Paradox dynamics](https://github.com/m9h/paradox-dynamics) · [executed notebook](https://github.com/m9h/paradox-dynamics/blob/main/examples/paradox_lab.ipynb) | Nine maps, exact and floating arithmetic, 24 recorded experiments |

### 1. Self-sorting arrays

Individual array elements execute local sorting policies. We can disable some
elements, mix policies, and ask whether the collective still sorts or clusters.
Read [Zhang, Goldstein and Levin](https://arxiv.org/abs/2401.05375), then inspect
our fork's [model and measurement notes](https://github.com/m9h/cell_research/blob/main/docs/methods.md).

Try this example before opening the first notebook:

```text
[2, 4, 1, 3] → [2, 1, 4, 3]
```

Adjacent out-of-order pairs increase from 1 to 2, while total inversions decrease
from 3 to 2. Whether this looks like a setback depends on the metric.
The notebooks compare progress measures, damage definitions and shuffled-label
controls. They are controlled experiments using repaired code; they do not claim
to reproduce the original paper's numerical figures exactly.

### 2. Regulatory-network memory

Read [Biswas, Clawson and Levin](https://pmc.ncbi.nlm.nih.gov/articles/PMC9820177/).
In our selected models, reaction rates and wiring stay fixed; molecular state
changes. Repeated stimulation, paired inputs and delayed probes can then produce
different responses. The [results guide](https://github.com/m9h/GRN_ODE/blob/python-memory-replication/python/RESULTS.md)
includes matched controls that help distinguish cue-specific responses from
continuing drift and material accumulation.

The five models are **MAPK protein-signaling models**, despite the historical
`GRN_ODE` repository name. Four are variants of the same Markevich model family.
The [BioModels guide](https://github.com/m9h/GRN_ODE/blob/python-memory-replication/python/models/README.md)
explains their biology, equations, conserved pools, source papers and provenance.

Our active goal is to extend the kinetics and memory computations to all **35
BioModels** in the source study, with independent validation. The five-model
suite remains the completed baseline; see the
[scope and status](docs/figure-guide.md#where-the-35-model-kinetics-project-fits).

Two supporting forks make the numerical work inspectable:

- [SBMLtoODEjax](https://github.com/m9h/sbmltoodejax/tree/fix-continuous-assignment-rules):
  correct assignment-rule evaluation and compare against exact solutions,
  RoadRunner and COPASI. [Contribution to FLOWERS](https://github.com/flowersteam/sbmltoodejax/pull/9).
- [Jaxkineticmodel](https://github.com/m9h/jaxkineticmodel/tree/modern-jax-validation):
  update to JAX 0.12, fix model-import issues exposed by the shared cases, and
  demonstrate batched simulation and intervention optimization with checked gradients.
  [Validation and MAPK example](https://github.com/m9h/jaxkineticmodel/blob/modern-jax-validation/validation/README.md).

The later [Regulatory Network Machine paper](https://pmc.ncbi.nlm.nih.gov/articles/PMC12210318/)
provides a related framework for computation through network state transitions.
Constructing an RNM transition graph remains a possible extension of our work.

### 3. Logical paradoxes as dynamical systems

Start with the liar sentence represented by the revision rule

$$x_{t+1}=1-x_t,\qquad x_t\in[0,1].$$

The endpoints alternate; 0.5 is fixed. Other initial values have period two.
This simple map is not chaotic. Our [working explorer](https://github.com/m9h/paradox-dynamics)
extends it to attracting and repelling fixed points, the tent map, a Curry
variation and coupled revision rules. The notebook makes arithmetic and update
order explicit: from the requested tent-map input `0.314`, float32 reaches zero
after 24 revisions, float64 after 55, while exact rational arithmetic enters a
50-cycle. See the [project guide](docs/paradox-project.md) and
[mathematical explanations](https://github.com/m9h/paradox-dynamics/blob/main/docs/mathematics.md).

## Forks and reproducibility

[FORKS.md](FORKS.md) records all four forks and the original paradox project,
with working branches, review links and exact revisions. Some changes are on
feature branches, so use the links above rather than assuming each fork's
default branch contains them.

Status snapshot: **2026-11-08**. The Jaxkineticmodel update passes 36 tests and
87 numerical comparisons; its CI passes on Python 3.12 and 3.13. The GRN suite
passes 28 tests with all three engines installed and 44 JAX/reference trajectory
comparisons, alongside 44 RoadRunner/COPASI reference comparisons. These are
checks of the selected implementations and examples, not general SBML
certification or evidence for a metaphysical interpretation. Sources and scope
are linked in the [fork inventory](FORKS.md).

## Contributing to the reading group

Open an issue or pull request with a question, a corrected reference, a notebook
observation or a proposed experiment. For computational results, include the
fork revision, model, settings, seed if applicable, measurement and comparison
condition. [A discussion template](docs/discussion-guide.md#recording-a-discussion)
helps keep notes useful to the next reader.

Original material in this repository is [MIT licensed](LICENSE). Linked papers,
websites, forks and model files retain their own licenses and attribution. The
fork inventory links the relevant notices; this repository does not relicense
those materials.
