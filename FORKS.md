# Forks, contributions and reproducible revisions

Checked **2026-11-09**. Branch links follow ongoing work; revision links preserve
the code examined for this snapshot. Review status can change after this date.

| Fork / working branch | Upstream | Snapshot revision | Review status |
|---|---|---|---|
| [cell_research · main](https://github.com/m9h/cell_research/tree/main) | [Zhangtaining/cell_research](https://github.com/Zhangtaining/cell_research) | [397e94c](https://github.com/m9h/cell_research/tree/397e94c4c1f5b7c6367c2c4cb603eab4fdd274a2) | Changes available on fork main |
| [GRN_ODE · python-memory-replication](https://github.com/m9h/GRN_ODE/tree/python-memory-replication) | [wesleypclawson/GRN_ODE](https://github.com/wesleypclawson/GRN_ODE) | [228565e](https://github.com/m9h/GRN_ODE/tree/228565e2ebda2c423dcea04dfe69c353b0b3740d) | [Draft PR in our fork](https://github.com/m9h/GRN_ODE/pull/1) |
| [sbmltoodejax · fix-continuous-assignment-rules](https://github.com/m9h/sbmltoodejax/tree/fix-continuous-assignment-rules) | [flowersteam/sbmltoodejax](https://github.com/flowersteam/sbmltoodejax) | [af646fc](https://github.com/m9h/sbmltoodejax/tree/af646fcf4142734e8836be692478325cfec2c49b) | [FLOWERS upstream PR #9](https://github.com/flowersteam/sbmltoodejax/pull/9), open and unmerged; [fork draft](https://github.com/m9h/sbmltoodejax/pull/1) |
| [jaxkineticmodel · modern-jax-validation](https://github.com/m9h/jaxkineticmodel/tree/modern-jax-validation) | [AbeelLab/jaxkineticmodel](https://github.com/AbeelLab/jaxkineticmodel) | [0c16f6e](https://github.com/m9h/jaxkineticmodel/tree/0c16f6ea145862ea0a3d9b1ef4368745e18028a5) | [Draft PR in our fork](https://github.com/m9h/jaxkineticmodel/pull/1) |

## What each fork contributes

**Self-sorting arrays:** repaired stopping and frozen-element behavior, explicit
update schedules, reproducible event recordings, replay, and three executed
notebooks. Start with [the README](https://github.com/m9h/cell_research/blob/397e94c4c1f5b7c6367c2c4cb603eab4fdd274a2/README.md)
and [measurement definitions](https://github.com/m9h/cell_research/blob/397e94c4c1f5b7c6367c2c4cb603eab4fdd274a2/docs/methods.md).

**GRN memory replication:** all 35 unchanged BioModels files, independently
validated baseline kinetics for every model, 538 validated single-input retention
cases and 538 validated repeated-stimulation cases across all 35, and eight
broader memory demonstrations on five models.
The retention screen preserves complete state and delay history, uses untreated
controls, and marks below-resolution labels as unresolved. Linux reproduces all
538 retention cases. Baseline comparisons use RoadRunner/COPASI for 34 models and
method-of-steps/JiTCDDE for the delayed circadian-clock model.
The optional JAX backend is pinned to the Jaxkineticmodel revision above.
[Memory demonstrations](https://github.com/m9h/GRN_ODE/blob/228565e2ebda2c423dcea04dfe69c353b0b3740d/python/RESULTS.md)
· [three-engine validation](https://github.com/m9h/GRN_ODE/blob/228565e2ebda2c423dcea04dfe69c353b0b3740d/python/JAX_VALIDATION.md)
· [35-model baseline guide](https://github.com/m9h/GRN_ODE/blob/228565e2ebda2c423dcea04dfe69c353b0b3740d/python/CATALOG_VALIDATION.md)
· [538-case retention guide and results](https://github.com/m9h/GRN_ODE/blob/228565e2ebda2c423dcea04dfe69c353b0b3740d/python/CATALOG_MEMORY.md)
· [passing Linux CI, including retention and the JAX catalog audit](https://github.com/m9h/GRN_ODE/actions/runs/42758422883).
The [JAX catalog audit](https://github.com/m9h/GRN_ODE/blob/228565e2ebda2c423dcea04dfe69c353b0b3740d/python/CATALOG_JAX.md)
now validates 32 original baselines against both reference engines, with 96
passing comparisons across 352 observables. The event, rate-rule and delay
models are explicit unsupported imports, not passing JAX simulations. The
five-model memory suite also passes all 88 comparisons after the importer update.
The [repeated-stimulation audit](https://github.com/m9h/GRN_ODE/blob/228565e2ebda2c423dcea04dfe69c353b0b3740d/python/CATALOG_REPEATED.md)
passes all 538 cases with untreated and matched isolated-pulse controls: 3,313
trajectory comparisons pass and all controlled pulse classifications agree.
Negative and unresolved responses are separated from interpretable effects;
raw MATLAB labels can disagree despite passing trajectory comparisons. A fresh
Linux reproduction is pending for this milestone.
The [paired-learning screen](https://github.com/m9h/GRN_ODE/blob/228565e2ebda2c423dcea04dfe69c353b0b3740d/python/CATALOG_PAIRED.md)
is running after successful pilots. It covers 4,208 ordered input pairs and
compares no training, UCS-only, CS-only and paired histories, each with sham,
ordinary-cue and delayed-cue branches. All 64 local tests pass at this revision.
Full paired-learning results and catalog-wide breaking interventions remain
pending; completed screens do not establish the study's memory prevalence.
The historical MATLAB checkout is incomplete, so this is not an exact rerun.

**SBMLtoODEjax:** assignment rules are evaluated at each internal ODE solver
stage. Seven small SBML fixtures are checked against exact solutions and two
independent engines; 49 offline tests pass. Existing generated models need to be
regenerated to use the correction.
[Mathematical explanation and reproduction commands](https://github.com/m9h/sbmltoodejax/blob/af646fcf4142734e8836be692478325cfec2c49b/docs/source/tutorials/assignment_rule_validation.md).
Upstream PR #9 is submitted; its workflows were awaiting maintainer approval at
this snapshot. The fix does not add general event or algebraic-rule support.

**Jaxkineticmodel:** Python 3.12+, JAX/JAXlib 0.12.0.1, Diffrax 0.7.2, Equinox
0.13.8 and Optax 0.2.8, with a lockfile. The shared cases exposed missing fixed
enzymes, incorrect amount/concentration scaling and mutation of symbolic models;
the fork corrects these and rejects unsupported rate/algebraic rules explicitly.
The larger catalog exposed silent event omission, a delay translated as
subtraction, truncated fractional stoichiometry and incorrect assigned-species
states. The update rejects unsupported event/delay semantics and fixes
stoichiometry, rule dependencies and assignment export. All 43 tests pass,
including the Python 3.12 and 3.13 CI jobs linked below.
[Migration guide](https://github.com/m9h/jaxkineticmodel/blob/0c16f6ea145862ea0a3d9b1ef4368745e18028a5/validation/README.md)
· [87-comparison report](https://github.com/m9h/jaxkineticmodel/blob/0c16f6ea145862ea0a3d9b1ef4368745e18028a5/validation/results/report.json)
· [MAPK optimization example](https://github.com/m9h/jaxkineticmodel/blob/0c16f6ea145862ea0a3d9b1ef4368745e18028a5/validation/mapk_intervention.py)
· [passing Python 3.12/3.13 CI](https://github.com/m9h/jaxkineticmodel/actions/runs/42724072201).
The DBTL tutorial uses a fixed seed and a documented, smaller sampling experiment
after broad random perturbations produced solver failures. The checks establish
CPU behavior for the selected cases; GPU performance has not been validated.

## How to use a branch or snapshot

Clone a fork using the branch named in the table, then follow its own README.
For example:

```sh
git clone --branch python-memory-replication https://github.com/m9h/GRN_ODE.git
cd GRN_ODE/python
uv sync --locked --extra test --extra jaxkineticmodel
uv run --locked --extra test --extra jaxkineticmodel python -m pytest -q
```

For an exact historical checkout, clone first and use `git switch --detach`
with the full snapshot hash from the table's revision link. Record that hash
alongside any figures or observations you share.

## Licenses and attribution

- **cell_research:** our original contributions are MIT licensed; inherited
  upstream material has explicit exclusions.
  [Licensing guide](https://github.com/m9h/cell_research/blob/main/LICENSING.md).
- **GRN_ODE:** original replication contributions are MIT licensed. Original
  MATLAB material is not relicensed; the downloaded BioModels files preserve
  their CC0 provenance.
  [Licensing guide](https://github.com/m9h/GRN_ODE/blob/python-memory-replication/LICENSING.md).
- **SBMLtoODEjax:** the existing MIT license and embedded upstream BSD notice
  are retained. [License](https://github.com/m9h/sbmltoodejax/blob/fix-continuous-assignment-rules/LICENSE).
- **Jaxkineticmodel:** Apache-2.0 is retained; copied analytic fixtures carry MIT
  attribution, and biological models retain their BioModels provenance.
  [License](https://github.com/m9h/jaxkineticmodel/blob/modern-jax-validation/LICENSE)
  · [fixture notices](https://github.com/m9h/jaxkineticmodel/blob/modern-jax-validation/tests/fixtures/conformance/README.md).

## Original project: paradox dynamics

[m9h/paradox-dynamics](https://github.com/m9h/paradox-dynamics) is a new MIT-licensed
implementation of selected Mar–Grim equations. It is an original project, not a
fork of an existing implementation. It provides nine maps, float32/float64 and
exact rational arithmetic, explicit coupled update schedules, a CLI and an
interactive notebook. The initial release contains 24 recorded experiments,
seven original figures and 81 passing tests. The
[Python 3.12/3.13 CI run](https://github.com/m9h/paradox-dynamics/actions/runs/42507008695)
also regenerates the figures and executes the notebook.

[Snapshot 1c3ab6a](https://github.com/m9h/paradox-dynamics/tree/1c3ab6ad40f0546d952e331c40b45ed0881f25ae)
· [executed notebook](https://github.com/m9h/paradox-dynamics/blob/main/examples/paradox_lab.ipynb)
· [results](https://github.com/m9h/paradox-dynamics/blob/main/docs/results.md)
· [validation](https://github.com/m9h/paradox-dynamics/blob/main/docs/validation.md)
· [MIT license](https://github.com/m9h/paradox-dynamics/blob/main/LICENSE).

The [reading-group project guide](docs/paradox-project.md) links the equations,
precision comparison and discussion questions.
