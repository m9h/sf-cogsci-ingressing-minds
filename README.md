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
| **2. Regulatory-network memory** | How can fixed reaction equations produce responses that depend on stimulation history? | [Python replication](https://github.com/m9h/GRN_ODE/tree/python-memory-replication/python) · [executed notebook](https://github.com/m9h/GRN_ODE/blob/python-memory-replication/python/examples/memory_lab.ipynb) | 35 baseline models and 538 retention cases; eight broader demonstrations on five models with three simulators |
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
BioModels** in the source study, with independent validation. Baseline kinetics
now pass independent comparisons for all 35: RoadRunner versus COPASI for 34,
and two delay-equation solvers for the delayed circadian-clock model. See the
[catalog results and model descriptions](https://github.com/m9h/GRN_ODE/blob/python-memory-replication/python/CATALOG_VALIDATION.md).
[Single-input retention](https://github.com/m9h/GRN_ODE/blob/python-memory-replication/python/CATALOG_MEMORY.md)
now covers all 35 models: 538 stimulation cases pass independent numerical
comparisons, with below-resolution response labels explicitly unresolved.
[Repeated stimulation](https://github.com/m9h/GRN_ODE/blob/4108edeca8b2d6d5e454167454a8826319ff6046/python/CATALOG_REPEATED.md)
also passes all 538 cases on macOS and Linux. The JAX catalog audit validates
32 baselines and explicitly identifies three unsupported models. The
[paired screen](https://github.com/m9h/GRN_ODE/blob/4108edeca8b2d6d5e454167454a8826319ff6046/python/CATALOG_PAIRED.md)
has evaluated all 4,208 cases: the original run records 4,166 passes and 42
failures. Separate François, Vilar, Rohwer and
[Marhl recoveries](https://github.com/m9h/GRN_ODE/blob/f8d4e26e62c6fd940f6e940c1c0d9b3439100622/python/results/catalog-paired-marhl-case-recovery/README.md)
bring combined validation to **4,205/4,208 cases**, with complete passing
inventories in 34 models. Three Vilar cases remain unresolved. Marhl's full
case audit uses independent high-precision Taylor implementations; its native
solver disagreements remain documented.
As of **18 November 2026 UTC**, the conditional breaking screen has
[complete initial-case inventories for 34 models and passing whole-model audits for 26](https://github.com/m9h/GRN_ODE/blob/f45fed315f63c19f66690dffe676caf1681fe011/python/results/catalog-breaking-celliere29-20261116/README.md).
The [complete Cellière TGF-β audit](https://github.com/m9h/GRN_ODE/releases/tag/kinetics-celliere-20261116)
passes all 1,088 cases and 34,816 conditional trials; its sixteen original
evidence packages reproduce the audit from fresh extraction.
New audits pass all 624 Edelstein species-model cases and all 398 Markevich
cases. François, Vilar and Rohwer have also finished their initial inventories,
with failures retained. **Tyson is the only unfinished initial inventory**;
partition 15 has now completed all four cases, leaving only
[partition 14](https://github.com/m9h/GRN_ODE/actions/runs/44383931943)
continuing from two completed cases out of four. The [earlier evidence release](https://github.com/m9h/GRN_ODE/releases/tag/kinetics-coverage-20261116)
preserves 64 original Linux artifacts and three complete local model reports;
fresh extractions reproduce all five package audits. Four passing models have
no eligible breaking cases, so this status is not evidence of learning.
The completed [Fuss pilot](https://github.com/m9h/GRN_ODE/releases/tag/kinetics-fuss-radau-20261116)
and [Marhl breaking diagnostic](https://github.com/m9h/GRN_ODE/releases/tag/kinetics-marhl-breaking-radau-20261116)
publish 132 full trajectories with checksums and reproducible array audits.
Fuss confirms its three selected branches; Marhl confirms only 3/30 records
(two distinct specifications). Neither result recovers a complete case.
The [full Fuss execution plan](https://github.com/m9h/GRN_ODE/blob/4c0f97adcf1e54019792f5eaf57963efb62cedf1/python/results/catalog-breaking-fuss-full-case-plan-20261116/README.md)
requires all 18 failed cases and 1,309 control trajectories, with 5,236 COPASI/Radau
integrations in 32 fixed partitions. The [latest complete checkpoint collection](https://github.com/m9h/GRN_ODE/blob/80fec615376378c01f674ea597bea3cc41834a7f/python/results/catalog-breaking-fuss-full-case-plan-20261116/COLLECTION.md)
verifies 528 completed arrays, including all 274 earlier arrays unchanged.
Its 112 complete branches pass all 672 pairwise comparisons, including the
untreated baseline. All partitions still need work and
[continue from those checkpoints](https://github.com/m9h/GRN_ODE/actions/runs/44385665111).
No additional Fuss case recovery is claimed.
The [complete Ciliberto case audit](https://github.com/m9h/GRN_ODE/blob/8ab39fd55fe4252e7cc87d41e66b33f391b4dfcf/python/results/catalog-breaking-ciliberto-case-recovery-20261118/COMPLETED_AUDIT.md)
now recovers both selected cases from all 215 branches and 860 saved trajectories,
including the untreated baseline. The [complete evidence release](https://github.com/m9h/GRN_ODE/releases/tag/kinetics-ciliberto-cases-20261118)
preserves the original data and all replacement ZIPs. A fresh download reproduces
the full case audit. This does not change the separate 548/622 whole-model result.
Earlier audits pass all 216 Leloup cases, 728 Martins cases and 112 Hoefnagel
cases. The [De Caluwe clock](https://github.com/m9h/GRN_ODE/releases/tag/kinetics-decaluwe20-20261114)
passes all 484 cases and 18,579 branches. Downloadable evidence accompanies the
[Leloup, Ciliberto and Martins audits](https://github.com/m9h/GRN_ODE/releases/tag/kinetics-breaking-12-28-31-20261113)
and the [Hoefnagel](https://github.com/m9h/GRN_ODE/releases/tag/kinetics-hoefnagel-20261113)
and [Ueda audits](https://github.com/m9h/GRN_ODE/releases/tag/kinetics-ueda-20261113).
See the
[scope and status](docs/figure-guide.md#where-the-35-model-kinetics-project-fits).

Execution checked **18 November 2026, 21:42 UTC**: nine local numerical workers
and their coordinator are stopped at the user's request. This includes Ueda's
unfinished 323-trajectory case-control run. Its
[cloud continuation](https://github.com/m9h/GRN_ODE/actions/runs/44393623529) is now
queued behind Linux validation: 170 branches have complete verified evidence,
and all 153 remaining branches are assigned to 32 fixed partitions. No Ueda
case recovery is claimed until the complete 323-branch audit passes.
The [collection guide](https://github.com/m9h/GRN_ODE/blob/0c3c315dd34391abd4c38bfe93a358e78779451e/python/results/catalog-breaking-ueda-continuation-20261118/COLLECTION.md)
explains fixed job selection, artifact checks and the complete-case audit.
The [preserved evidence release](https://github.com/m9h/GRN_ODE/releases/tag/kinetics-ueda-preservation-20261118)
contains all 787 available snapshot files and the original diagnostic archive.
A fresh download verifies all 628 preserved arrays and reproduces the complete
preparation audit, import restoration proof and continuation plan byte for byte.
Its [uv reproduction guide](https://github.com/m9h/GRN_ODE/blob/07568199b113fee32f99d3feefed38e6d845b01c/python/results/catalog-breaking-ueda-continuation-20261118/RELEASE.md)
requires no new ODE integrations; the four unresolved cases remain outstanding.
The [current cloud runs](FORKS.md#current-execution) continue Tyson and François
inventories, Vilar precision diagnostics and Fuss case controls. Four local
collection and audit watchers remain active; they do not run ODE integrations.

Rohwer's phosphotransferase model (network 35, BioModel 38) now has a fixed
[cloud diagnostic run](https://github.com/m9h/GRN_ODE/actions/runs/44401097371)
for all 750 originally failed breaking branches, queued behind Linux validation.
Its [source audit and plan](https://github.com/m9h/GRN_ODE/blob/40fe82344d8dacb2d79ebdc4087ee52beb90a091/python/results/catalog-breaking-rohwer-diagnostics-20261118/README.md)
retain all 123 failed cases and their original protocols. The planned 3,000
trajectories use two Radau and two RoadRunner requests per branch. Complete
matched controls and conditional replay remain necessary before case recovery.
The [offline collection guide](https://github.com/m9h/GRN_ODE/blob/12c0693df1d68d1736b274a9364e1ef7b2533b06/python/results/catalog-breaking-rohwer-diagnostics-20261118/COLLECTION.md)
requires all 750 branches, rechecks downloaded arrays and preserves interrupted
work. All 78 combined local checks pass; Linux validation remains queued.

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

Kinetics status updated **2026-11-12**. The documented Jaxkineticmodel revision
passes 43 tests and its CI passes on Python 3.12 and 3.13. The GRN five-model
suite passes all 88 trajectory comparisons after the importer update; the
larger catalog's successes and unresolved cases are reported separately. These are
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
