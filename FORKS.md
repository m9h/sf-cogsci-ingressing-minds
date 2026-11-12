# Forks, contributions and reproducible revisions

Kinetics evidence updated **2026-11-11**; other fork and review snapshots are
retained from **2026-11-09**. Branch links follow ongoing work; revision links
preserve the code examined. Review status can change after these dates.

| Fork / working branch | Upstream | Snapshot revision | Review status |
|---|---|---|---|
| [cell_research · main](https://github.com/m9h/cell_research/tree/main) | [Zhangtaining/cell_research](https://github.com/Zhangtaining/cell_research) | [397e94c](https://github.com/m9h/cell_research/tree/397e94c4c1f5b7c6367c2c4cb603eab4fdd274a2) | Changes available on fork main |
| [GRN_ODE · python-memory-replication](https://github.com/m9h/GRN_ODE/tree/python-memory-replication) | [wesleypclawson/GRN_ODE](https://github.com/wesleypclawson/GRN_ODE) | [70a3afa](https://github.com/m9h/GRN_ODE/tree/70a3afad61357e94873ff62a7300c099b4c7ae3e) | [Draft PR in our fork](https://github.com/m9h/GRN_ODE/pull/1) |
| [GRN_ODE · kinetics-solver-recovery](https://github.com/m9h/GRN_ODE/tree/kinetics-solver-recovery) | Same upstream | [40ca8ff](https://github.com/m9h/GRN_ODE/tree/40ca8ff586220a5df573e7d383defa2c19ed829a) | Complete François recovery, Goldbeter refinement evidence and full original paired screen; separate from the live breaking source |
| [GRN_ODE · kinetics-newton-reference](https://github.com/m9h/GRN_ODE/tree/kinetics-newton-reference) | Same upstream | [85615d2](https://github.com/m9h/GRN_ODE/tree/85615d284dcba168b93670ad6215d67f0290a4a0) | Three Vilar cases recovered; 17 original breaking reports and distributed network 33 audited; sensitivity of literal search paths documented |
| [GRN_ODE · kinetics-muller-recovery](https://github.com/m9h/GRN_ODE/tree/kinetics-muller-recovery) | Same upstream | [b089186](https://github.com/m9h/GRN_ODE/tree/b0891863ffd90b3dfb5c944720f0512d81584167) | Full 118-case network 26 recovery using settings validated on all 14 original mismatches; computation in progress |
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
[Memory demonstrations](https://github.com/m9h/GRN_ODE/blob/70a3afad61357e94873ff62a7300c099b4c7ae3e/python/RESULTS.md)
· [three-engine validation](https://github.com/m9h/GRN_ODE/blob/70a3afad61357e94873ff62a7300c099b4c7ae3e/python/JAX_VALIDATION.md)
· [35-model baseline guide](https://github.com/m9h/GRN_ODE/blob/70a3afad61357e94873ff62a7300c099b4c7ae3e/python/CATALOG_VALIDATION.md)
· [538-case retention guide and results](https://github.com/m9h/GRN_ODE/blob/70a3afad61357e94873ff62a7300c099b4c7ae3e/python/CATALOG_MEMORY.md)
· [passing Linux CI, including retention and the JAX catalog audit](https://github.com/m9h/GRN_ODE/actions/runs/42758422883).
The [JAX catalog audit](https://github.com/m9h/GRN_ODE/blob/70a3afad61357e94873ff62a7300c099b4c7ae3e/python/CATALOG_JAX.md)
now validates 32 original baselines against both reference engines, with 96
passing comparisons across 352 observables. The event, rate-rule and delay
models are explicit unsupported imports, not passing JAX simulations. The
five-model memory suite also passes all 88 comparisons after the importer update.
The [repeated-stimulation audit](https://github.com/m9h/GRN_ODE/blob/4108edeca8b2d6d5e454167454a8826319ff6046/python/CATALOG_REPEATED.md)
passes all 538 cases with untreated and matched isolated-pulse controls: 3,313
trajectory comparisons pass and all controlled pulse classifications agree.
Negative and unresolved responses are separated from interpretable effects;
raw MATLAB labels can disagree despite passing trajectory comparisons.
[Linux reproduction now passes all 538 cases](https://github.com/m9h/GRN_ODE/actions/runs/42766999555),
including one recorded solver retry after incomplete COPASI output.
The [paired-learning screen](https://github.com/m9h/GRN_ODE/blob/4108edeca8b2d6d5e454167454a8826319ff6046/python/CATALOG_PAIRED.md)
has evaluated all 4,208 ordered input pairs and 22,578 unique branches.
It compares no training, UCS-only, CS-only and paired histories, each with sham,
ordinary-cue and delayed-cue branches. **4,166 cases pass; 42 do not.** The
[coverage audit](https://github.com/m9h/GRN_ODE/blob/4108edeca8b2d6d5e454167454a8826319ff6046/python/results/catalog-paired/audit.json)
checks the entire candidate inventory and recomputes recorded scores. It retains
77 incomplete integrations and 20 completed trajectory mismatches across four
models, rather than counting attempted coverage as successful validation.
A separate [complete François recovery](https://github.com/m9h/GRN_ODE/blob/650c3f71b76a0446552d6b7e84944e2602536950/python/results/catalog-paired-francois-full-recovery/audit.json)
now passes all 44 cases and 275 branches, with exactly one declared COPASI
retry after incomplete output. Its failed attempt is preserved. The original
full-screen totals above are unchanged; failures in Marhl, Vilar and Rohwer
remain unresolved.
The [three-trial breaking screen](https://github.com/m9h/GRN_ODE/blob/70a3afad61357e94873ff62a7300c099b4c7ae3e/python/CATALOG_BREAKING.md)
is also running, with 7,324 initial input/breaker combinations. It follows the
MATLAB conditional search, retains every prior rechallenge, and uses eight
control arms to separate restoration from lingering or direct effects. A
119-branch pilot passes, including a documented solver retry for one incomplete
Rohwer trajectory. All 74 local tests pass at this revision.
Further paired-screen recovery and full breaking results remain pending; completed
screens do not establish the study's memory prevalence.
The [Goldbeter domain diagnostic](https://github.com/m9h/GRN_ODE/blob/650c3f71b76a0446552d6b7e84944e2602536950/python/CATALOG_BREAKING.md#a-domain-limit-exposed-by-the-goldbeter-model)
also identifies upward resets of active fractions beyond their biological
0–1 range. Both native solvers stop on four selected breaking branches across
three tolerance requests. Numerical agreement elsewhere does not certify the
biological meaning of those interventions.
For the separate explicit-pool Goldbeter model, all eight originally mismatched
breaking branches pass [tighter native requests and a further refinement](https://github.com/m9h/GRN_ODE/blob/40ca8ff586220a5df573e7d383defa2c19ed829a/python/CATALOG_BREAKING.md#refinement-recovery-for-the-explicit-pool-goldbeter-model).
The corresponding [Linux regression step](https://github.com/m9h/GRN_ODE/actions/runs/43094514253/job/130779779116)
also passes. The [complete recovery](https://github.com/m9h/GRN_ODE/blob/4a43d8d3ed3ad777aab173eaa672306691ce9d6d/python/results/catalog-breaking-goldbeter4-full-recovery/audit.json)
now passes all 54 cases, 323 conditional trials and 1,327 branches, including
every required control and continuation.
The new [JAX reset adapter](https://github.com/m9h/GRN_ODE/blob/3d88e0d56287e0f70276678c72e301ce3eeb31e2/python/grn_memory/jax_protocols.py)
preserves full state, symbol units and absolute time and rejects unsupported
semantics. Its Newton configuration is an explicit solver choice, not an
automatic fallback or a claim of complete memory-protocol coverage.
The [complete Rohwer Kvaerno3 diagnostic](https://github.com/m9h/GRN_ODE/blob/56b7df4363d9d75cb5d09df801553767567a0f51/python/results/catalog-paired-jax-rohwer-full/audit.json)
confirms 23 of 77 originally failed branches; 42 have incomplete integrations
and 12 remain completed mismatches. The complete Vilar Kvaerno5 diagnostic
confirms none of its 16 branches. These are diagnostic outcomes, not newly
validated complete memory cases.
The [Radau reference and case-recovery audit](https://github.com/m9h/GRN_ODE/blob/56b7df4363d9d75cb5d09df801553767567a0f51/python/CATALOG_PAIRED.md#recovering-complete-cases-from-radau-diagnostics)
add a different stiff integrator and require all 12 arms and independently
recomputed classifications before accepting a case. Vilar's six failed cases
require 58 branches, including 42 controls beyond its original failures.
The [completed Vilar recovery audit](https://github.com/m9h/GRN_ODE/blob/29acc73fb017463add4a0973110b849328019d72/python/results/catalog-paired-scipy-vilar-cases/audit.json)
now covers all 58 required branches and 290 completed integrations. Three of
the six failed cases recover, bringing Vilar to **139/142 validated cases**.
The other three retain nine completed trajectory mismatches; no controls are
missing. The [complete Rohwer Radau diagnostic](https://github.com/m9h/GRN_ODE/blob/29acc73fb017463add4a0973110b849328019d72/python/results/catalog-paired-scipy-rohwer/report.json)
confirms all 77 originally failed branches across 385 completed integrations.
Its additional 170 controls remain in progress, so these branch results do not
yet establish recovery of all 33 failed cases.
The [complete Rohwer Newton diagnostic](https://github.com/m9h/GRN_ODE/blob/2e7327b0d273f4b33bdd8aa37601c1a497854a2a/python/results/catalog-paired-jax-rohwer-newton/audit.json)
confirms 35 of 77 branches, with 20 incomplete integrations and 22 completed
mismatches. Thirty-two branches remain unconfirmed by either tested JAX
configuration. The [Marhl Radau diagnostic](https://github.com/m9h/GRN_ODE/blob/2e7327b0d273f4b33bdd8aa37601c1a497854a2a/python/results/catalog-paired-scipy-marhl/report.json)
completes all 15 integrations but confirms none of its three branches; the late
numerical convergence problem remains unresolved.
The [Marhl precision diagnostic](https://github.com/m9h/GRN_ODE/blob/4a43d8d3ed3ad777aab173eaa672306691ce9d6d/python/PRECISION_DIAGNOSTICS.md)
now completes all three failed branches with Heyoka at 128-bit and 192-bit
precision, preserving every original sample and reset. Both precisions agree
throughout, but both still disagree with RoadRunner; no complete case is
promoted to passing. The saved arrays are independently audited. The main
environment passes **146 tests** with the optional Heyoka module skipped, and
its separate environment passes **eight analytic adapter tests**. The later
refinement update in `29acc73` passes **156 tests** in the main environment.
Python
dependencies use uv; the documented macOS exception supplies Heyoka's compiled
native libraries through an explicitly pinned conda-forge environment.
The [restartable breaking runner](https://github.com/m9h/GRN_ODE/blob/2e7327b0d273f4b33bdd8aa37601c1a497854a2a/python/CATALOG_BREAKING.md#restartable-computation-in-complete-case-partitions)
partitions whole cases, preserving their full conditional searches and controls.
A [distributed batch for networks 26–35](https://github.com/m9h/GRN_ODE/actions/runs/43101294718)
is computing the 3,440 initial cases in those networks. Network 27 is the first
complete result from this batch: its [combined audit](https://github.com/m9h/GRN_ODE/blob/e294f00e72f3a3927f44496d73f05d1504af10c0/python/results/catalog-breaking-linux-27/audit.json)
passes all 22 cases, 57 conditional trials and 301 branch records across four
partitions. The audit reconstructs every required continuation and control,
recomputes classifications, and verifies full observation horizons and source
hashes. Checkpoints permit resumption; a passing partition alone does not
establish complete-model coverage. A downloaded five-case partition resumed
locally using all 50 unchanged checkpoints without new integration.
Network 26 also has [complete four-partition coverage](https://github.com/m9h/GRN_ODE/blob/4a43d8d3ed3ad777aab173eaa672306691ce9d6d/python/results/catalog-breaking-linux-26/audit.json):
116 of 118 cases pass across 524 conditional trials and 2,168 branch records.
Fourteen completed trajectory mismatches affect two cases; all required
conditional decisions were evaluated. This is complete computation with
remaining numerical discrepancies, rather than successful validation of every case.
Its [14-branch refinement diagnostic](https://github.com/m9h/GRN_ODE/blob/29acc73fb017463add4a0973110b849328019d72/python/results/catalog-breaking-muller26-refinement/report.json)
now passes all cross-engine and refinement gates over the complete 0–2210
interval. A separate branch is recomputing all 118 cases with both tolerances
tightened tenfold, including the original `1e-18` absolute tolerance.
[Full recovery run](https://github.com/m9h/GRN_ODE/actions/runs/43158961987).
The [network 30 distributed audit](https://github.com/m9h/GRN_ODE/blob/29acc73fb017463add4a0973110b849328019d72/python/results/catalog-breaking-linux-30/audit.json)
also covers every required continuation: 26 of 38 cases pass across 171
conditional trials and 783 branch records. Thirty completed mismatches affect
the remaining 12 cases. Networks 28/29 hit their five-hour limits with partial
coverage and are [continuing from downloaded checkpoints](https://github.com/m9h/GRN_ODE/actions/runs/43155055643).
The [17 terminal reports from the original breaking run](https://github.com/m9h/GRN_ODE/blob/85615d284dcba168b93670ad6215d67f0290a4a0/python/results/catalog-breaking-original-completed/audit.json)
are also published and audited: 14 models pass their checks, including three
with no eligible cases and validated untreated controls. In total, 845 of 852
initial cases pass across 28,127 branches. Four incomplete integrations leave
two conditional decisions unresolved in reduced Goldbeter; eight completed
mismatches affect the explicit-pool model, whose separate recovery now passes
all 54 cases as reported above.
Fourteen additional mismatches affect network 26, whose local and distributed
runs both validate 116/118 cases. The [comparison of these runs](https://github.com/m9h/GRN_ODE/blob/85615d284dcba168b93670ad6215d67f0290a4a0/python/CATALOG_BREAKING.md#tiny-residuals-change-literal-search-paths)
finds different search paths in 38 cases. All 210 differing raw reversal labels
involve means below `1.35e-19`; controlled classifications agree across all
1,440 shared response/engine assessments. Unshared trials are not assumed
equivalent. A worked example appears in the [discussion guide](docs/discussion-guide.md#worked-example-a-reversal-near-zero).
Network 33's [untreated-control audit](https://github.com/m9h/GRN_ODE/blob/85615d284dcba168b93670ad6215d67f0290a4a0/python/results/catalog-breaking-linux-33/audit.json)
also passes over the full 0–2210 interval. It has no eligible cases under this
protocol. Published breaking reports now cover 19 distinct models; this does
not establish successful numerical validation of every model or case. The
comparison update passes **163 local tests**, with the optional Heyoka module
skipped in the main environment.
The audit distinguishes attempted initial coverage, resolved conditional
searches and numerical validation; selected models cannot establish all-35
completion. Rohwer's 170 additional paired-case controls are still being computed.
Further diagnostics retain every failed or mismatched trajectory.
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
