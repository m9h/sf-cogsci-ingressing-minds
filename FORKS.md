# Forks, contributions and reproducible revisions

Kinetics evidence updated **2026-11-14 UTC**; other fork and review snapshots are
retained from **2026-11-09**. Branch links follow ongoing work; revision links
preserve the code examined. Review status can change after these dates.

| Fork / working branch | Upstream | Snapshot revision | Review status |
|---|---|---|---|
| [cell_research · main](https://github.com/m9h/cell_research/tree/main) | [Zhangtaining/cell_research](https://github.com/Zhangtaining/cell_research) | [397e94c](https://github.com/m9h/cell_research/tree/397e94c4c1f5b7c6367c2c4cb603eab4fdd274a2) | Changes available on fork main |
| [GRN_ODE · python-memory-replication](https://github.com/m9h/GRN_ODE/tree/python-memory-replication) | [wesleypclawson/GRN_ODE](https://github.com/wesleypclawson/GRN_ODE) | [70a3afa](https://github.com/m9h/GRN_ODE/tree/70a3afad61357e94873ff62a7300c099b4c7ae3e) | [Draft PR in our fork](https://github.com/m9h/GRN_ODE/pull/1) |
| [GRN_ODE · kinetics-solver-recovery](https://github.com/m9h/GRN_ODE/tree/kinetics-solver-recovery) | Same upstream | [40ca8ff](https://github.com/m9h/GRN_ODE/tree/40ca8ff586220a5df573e7d383defa2c19ed829a) | Complete François recovery, Goldbeter refinement evidence and full original paired screen; separate from the live breaking source |
| [GRN_ODE · kinetics-newton-reference](https://github.com/m9h/GRN_ODE/tree/kinetics-newton-reference) | Same upstream | [95ef898](https://github.com/m9h/GRN_ODE/tree/95ef898b05b2c67dd5c2745a3f8a0f8b71c4c4ad) | All-35 evidence index: 28 complete initial inventories and 23 passing whole-model audits; all 24 Ueda mismatch trajectories now pass a full-array Radau/RoadRunner audit, with complete-case controls underway; seven breaking searches remain unfinished; paired validation stays 4,205/4,208 |
| [GRN_ODE · kinetics-muller-recovery](https://github.com/m9h/GRN_ODE/tree/kinetics-muller-recovery) | Same upstream | [b089186](https://github.com/m9h/GRN_ODE/tree/b0891863ffd90b3dfb5c944720f0512d81584167) | Producer revision for the complete, passing 118-case network 26 recovery; evidence published on the reference branch above |
| [GRN_ODE · kinetics-leloup-recovery](https://github.com/m9h/GRN_ODE/tree/kinetics-leloup-recovery) | Same upstream | [daed478](https://github.com/m9h/GRN_ODE/tree/daed47882d2d20fa81b193a21c1934a5d83e64dd) | Complete network-12 recovery passes all 216 cases at independently supported refined settings; original evidence remains separate |
| [GRN_ODE · precision-checkpoint-resume](https://github.com/m9h/GRN_ODE/tree/precision-checkpoint-resume) | Same upstream | [3682181](https://github.com/m9h/GRN_ODE/tree/36821819b83b72d2ca08bc62da57625a8eeca3f5) | Exact precision checkpoints and full-array audits; new Vilar continuation restores all 17 terminal parent artifacts, with ten unfinished partitions; 73 precision tests plus four collector tests previously passed; no additional case recovery claimed |
| [GRN_ODE · precision-case-controls](https://github.com/m9h/GRN_ODE/tree/precision-case-controls) | Same upstream | [2e32e58](https://github.com/m9h/GRN_ODE/tree/2e32e584971d0b25ee2b747a986d94ba28b9ceb0) | All 23 additional Vilar controls complete and pass full-array audits; aggregate evidence covers 26/32 trajectories for three unresolved cases, with six missing and three native mismatches; reproducible uv audit and complete evidence release; no additional case recovery |
| [GRN_ODE · kinetics-copasi-output-diagnostics](https://github.com/m9h/GRN_ODE/tree/kinetics-copasi-output-diagnostics) | Same upstream | [30eb1e2](https://github.com/m9h/GRN_ODE/tree/30eb1e29442748c4fcf443777841537b71e5e8d9) | Full-array audit and preserved solver logs for three Vilar breaking branches; all nine COPASI runs stop early; conserved-pool analysis explains how resets change material totals; no case recovery claimed |
| [GRN_ODE · kinetics-fuss-radau](https://github.com/m9h/GRN_ODE/tree/kinetics-fuss-radau) | Same upstream | [fa8ee59](https://github.com/m9h/GRN_ODE/tree/fa8ee594ffeb04d52a632d391a20c9f0093ab91d) | Explicit COPASI reference support for full-array Radau diagnostics; 81 tests pass, one fixture-specific skip; deterministic three-branch Fuss pilot underway, no numerical recovery result yet |
| [GRN_ODE · kinetics-ueda-cases](https://github.com/m9h/GRN_ODE/tree/kinetics-ueda-cases) | Same upstream | [aa1a49a](https://github.com/m9h/GRN_ODE/tree/aa1a49a212981dda484a5fb1529f337f7badb058) | Recovery inventories include later candidates skipped by the original conditional search; 67 tests pass; Ueda's complete 323-trajectory control run has started, with all four unresolved cases retained |
| [GRN_ODE · kinetics-resume-case-selection](https://github.com/m9h/GRN_ODE/tree/kinetics-resume-case-selection) | Same upstream | [eb666a1](https://github.com/m9h/GRN_ODE/tree/eb666a175caf4dbabafc5fb677f2d5962729d24f) | Vilar checkpoint restoration repair: strict validation of reusable selected cases, exact preservation of historical aggregates, 35 tests through uv and a real-artifact reproduction; targeted partition restart, with coverage counts unchanged |
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
full-screen totals above are unchanged; the later Vilar and Rohwer recovery
audits are described below.
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
Its [170 additional controls](https://github.com/m9h/GRN_ODE/blob/e5ff9bb131b3a815feb584793b9f68dda53ce7a7/python/results/catalog-paired-scipy-rohwer-controls/report.json)
also complete and pass. The [complete-case recovery audit](https://github.com/m9h/GRN_ODE/blob/e5ff9bb131b3a815feb584793b9f68dda53ce7a7/python/results/catalog-paired-scipy-rohwer-cases/audit.json)
confirms all 247 required branches and recovers all 33 failed cases, bringing
Rohwer to **449/449 validated cases**. All 1,235 diagnostic integrations finish;
the largest scaled discrepancy among the confirmation comparisons is 0.157145,
below the acceptance limit of one. Every recovered case uses the same two
refined engines across all twelve arms, with independently recomputed scores.
Including the complete Marhl recovery described below, **4,205/4,208 cases
now validate**, with complete passing case inventories in 34 of the 35 models.
The remaining three cases are Vilar cases.
The [complete Rohwer Newton diagnostic](https://github.com/m9h/GRN_ODE/blob/2e7327b0d273f4b33bdd8aa37601c1a497854a2a/python/results/catalog-paired-jax-rohwer-newton/audit.json)
confirms 35 of 77 branches, with 20 incomplete integrations and 22 completed
mismatches. Thirty-two branches remain unconfirmed by either tested JAX
configuration. The [Marhl Radau diagnostic](https://github.com/m9h/GRN_ODE/blob/2e7327b0d273f4b33bdd8aa37601c1a497854a2a/python/results/catalog-paired-scipy-marhl/report.json)
completes all 15 integrations but confirms none of its three branches; the late
native-solver convergence problem remains unresolved in that diagnostic.
The [Marhl precision diagnostic](https://github.com/m9h/GRN_ODE/blob/4a43d8d3ed3ad777aab173eaa672306691ce9d6d/python/PRECISION_DIAGNOSTICS.md)
now completes all three failed branches with Heyoka at 128-bit and 192-bit
precision, preserving every original sample and reset. Both precisions agree
throughout, but both still disagree with RoadRunner; that three-branch
diagnostic alone promotes no complete case. The saved arrays are independently audited. The main
environment passes **146 tests** with the optional Heyoka module skipped, and
its separate environment passes **eight analytic adapter tests**. The later
refinement update in `29acc73` passes **156 tests** in the main environment.
Python
dependencies use uv; the documented macOS exception supplies Heyoka's compiled
native libraries through an explicitly pinned conda-forge environment.
The newer [resumable precision workflow](https://github.com/m9h/GRN_ODE/blob/26c5c425cd9e5a1116d73bcca39e8884e036bb1e/python/PRECISION_DIAGNOSTICS.md#linux-execution-and-artifact-restoration)
preserves exact internal state across interruptions and validates completed
arrays before reuse. Its Linux workers use uv throughout. All 16 original failed
Vilar branches and the untreated baseline are included in the
[17-partition plan](https://github.com/m9h/GRN_ODE/blob/ec8ec7cbadecd2a8c2067992011c88028eb5690f/python/results/catalog-paired-taylor-dispatch-vilar-20261113/plan.json);
[run 43380180550](https://github.com/m9h/GRN_ODE/actions/runs/43380180550)
passed all 73 precision tests and preserved all seventeen partition artifacts.
That initial run finished the first, 128-bit trajectory for ten stimulated
branches without completing all required integrations for any of them. The
[continuation](https://github.com/m9h/GRN_ODE/actions/runs/43483480217) has passed
its Linux test gate and now has complete, independently audited arrays for the
paired-normal and paired-sham arms of `DA__up--DR__up`. All three pairwise
comparisons pass over all 30,001 samples in each branch. The
[release preserves the original arrays and checkpoints](https://github.com/m9h/GRN_ODE/releases/tag/kinetics-vilar-precision-20261113).
Both arms belong to an already recovered case, so Vilar's validated count
remains **139/142**. Complete untreated Vilar and Marhl baseline probes also
pass independent full-array audits.

That continuation is now terminal: seven of its 17 partitions have complete
arrays, while ten retain unfinished integrations. The [next continuation](https://github.com/m9h/GRN_ODE/actions/runs/43556371440)
restores all 17 selections from verified artifacts, preserving exact checkpoints
and completed results. Partial coverage and completed native mismatches remain
explicit; no model or case completion is inferred from this dispatch.

The three remaining Vilar cases require 32 distinct full trajectories. Nine
are in the ongoing failed-branch batch; a separate
[23-control plan](https://github.com/m9h/GRN_ODE/blob/4520caeda2315d23fbfc7f65263774dd655ddb67/python/results/catalog-paired-taylor-vilar-controls-20261113/README.md)
supplies the others, including the full 300-unit untreated sham. Its runner and
case auditor passed 102 local precision tests; eight additional collector tests
also pass. The [dispatched computation](https://github.com/m9h/GRN_ODE/actions/runs/43510523842)
has completed all 23 controls and its Linux test gate. Every control passes
fresh comparisons of the full RoadRunner, 128-bit Taylor and 192-bit Taylor
arrays. The [aggregate partial audit](https://github.com/m9h/GRN_ODE/blob/2e32e584971d0b25ee2b747a986d94ba28b9ceb0/python/results/catalog-paired-vilar-controls-complete-20261114/README.md)
also includes three completed stimulated trajectories: it covers **26/32**
required trajectories, with six still missing. Those three stimulated
trajectories retain RoadRunner mismatches despite Taylor precision convergence.
The [evidence release](https://github.com/m9h/GRN_ODE/releases/tag/kinetics-vilar-controls-20261114)
preserves all arrays and a uv command that reproduces the audit. Case recovery
requires the same declared integrations in every arm, full-trajectory agreement
and agreement in controlled memory classifications. Vilar remains **139/142**;
all three remaining cases are incomplete, and no additional recovery is claimed.
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
interval. The [complete recovery audit](https://github.com/m9h/GRN_ODE/blob/f39d2e293066fc16e3ea00d27a0e779d2b0429e3/python/results/catalog-breaking-muller26-full-recovery/audit.json)
now passes **all 118 cases**, across 573 conditional trials, 836 response-trials
and 2,360 branch records. Both engines use `rtol=1e-13`, `atol=1e-19`; the largest
scaled discrepancy is 0.51046 against an acceptance limit of one. Every required
control and continuation is included. The original 116/118 results remain
available, and the new trial count reflects the literal search rule's sensitivity
to small residues. The [full recovery run](https://github.com/m9h/GRN_ODE/actions/runs/43158961987)
preserves the original timed-drive encoding and reset schedule.
The [network 30 distributed audit](https://github.com/m9h/GRN_ODE/blob/29acc73fb017463add4a0973110b849328019d72/python/results/catalog-breaking-linux-30/audit.json)
also covers every required continuation: 26 of 38 cases pass across 171
conditional trials and 783 branch records. Thirty completed mismatches affect
the remaining 12 cases. Networks 28/29 reached two successive five-hour budgets
with partial coverage and now [continue in sixteen partitions](https://github.com/m9h/GRN_ODE/actions/runs/43273574799).
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
protocol. Network 34's [complete Marwan audit](https://github.com/m9h/GRN_ODE/blob/058df6fe0f9d96874f604618afddcf64fde90bf8/python/results/catalog-breaking-linux-34/audit.json)
passes all **360 cases, 3,254 conditional trials and 12,936 branch records**.
The [next original-run snapshot](https://github.com/m9h/GRN_ODE/blob/058df6fe0f9d96874f604618afddcf64fde90bf8/python/results/catalog-breaking-original-completed-20261112/audit.json)
adds full Fuss and Leloup searches: 314/332 and 212/216 cases pass, respectively.
A separate local Marhl run passes 27/38. Its search paths and all raw and controlled
labels match the Linux run's 171 trials; one case changes numerical validation
status because its full trajectory comparison differs. Both reports remain
available. The new snapshot's compressed evidence and complete Ciliberto arrays
are in a [checksummed release](https://github.com/m9h/GRN_ODE/releases/tag/kinetics-validation-20261112).

The [complete network-1 audit](https://github.com/m9h/GRN_ODE/blob/058df6fe0f9d96874f604618afddcf64fde90bf8/python/results/catalog-breaking-linux-1/audit.json)
validates all **528 cases, 9,452 conditional trials and 38,024 branch records**
for the Edelstein acetylcholine-receptor model. Its
[separate evidence release](https://github.com/m9h/GRN_ODE/releases/tag/kinetics-network1-20261113)
preserves all sixteen partitions and checksummed archives.

The [complete De Caluwe clock audit](https://github.com/m9h/GRN_ODE/blob/6cf3cdcfe3bd04d677c2fbedfb3d30ce3e1bbe2d/python/results/catalog-breaking-decaluwe20-local-20261114/README.md)
passes all 484 network-20 cases, 4,704 conditional trials and 18,579 distinct
branches, with no incomplete integrations, mismatches or unresolved search
decisions. The [release](https://github.com/m9h/GRN_ODE/releases/tag/kinetics-decaluwe20-20261114)
preserves all 191 compressed evidence archives. The audit recomputes case scores
from saved window summaries and verifies the original pointwise-comparison
records; the producer did not save full trajectories for this catalog run.

Published breaking reports now cover **28 distinct models**, of which 23 have
passing full numerical validation after the separate recoveries. Seven
models still need their full searches completed; this does not establish
all-35 completion. The latest control-runner, branch-auditor and case-auditor
checks pass **63 targeted tests** through uv. This checks the computation and
audit code; it does not validate trajectories that are still being computed.

The [Linux four-to-eight partition check](https://github.com/m9h/GRN_ODE/blob/058df6fe0f9d96874f604618afddcf64fde90bf8/python/results/catalog-breaking-repartition-27-linux/verification.json)
preserves all 22 network-27 case summaries and all 646 copied checkpoint files.
[Sixteen-partition continuations](https://github.com/m9h/GRN_ODE/blob/058df6fe0f9d96874f604618afddcf64fde90bf8/python/CATALOG_BREAKING.md#checkpoint-continuations-dispatched-on-12-november)
are dispatched for networks 1, 2, 28, 29, 31, 32 and 35, retaining every control,
observation and conditional continuation. Their documented partial counts
describe parent worker reports, not full-model validation.
The [Ciliberto continuation](https://github.com/m9h/GRN_ODE/actions/runs/43370478631)
now has complete initial-case coverage: [548/622 cases pass](https://github.com/m9h/GRN_ODE/blob/f55c9a62913f8ece85fc96096b22b27807cf94cf/python/results/catalog-breaking-linux-28/audit.json),
with 74 failed cases and 89 unresolved conditional decisions retained.
The [Martins Amadori-degradation continuation](https://github.com/m9h/GRN_ODE/actions/runs/43370565797)
passes [all 728 cases](https://github.com/m9h/GRN_ODE/blob/f55c9a62913f8ece85fc96096b22b27807cf94cf/python/results/catalog-breaking-linux-31/audit.json).
These complete reports and the Leloup recovery below have a
[checksummed evidence release](https://github.com/m9h/GRN_ODE/releases/tag/kinetics-breaking-12-28-31-20261113).

Four [further checkpoint continuations](https://github.com/m9h/GRN_ODE/blob/f55c9a62913f8ece85fc96096b22b27807cf94cf/python/CATALOG_BREAKING.md#further-checkpoint-continuations-on-13-november)
preserve 519/624 recorded cases in network 2, 46/58 in network 5,
643/1,088 in network 29 and 201/204 in network 32. All 64 job identities are
recorded. These are partial parent counts; complete-model validation awaits
the resumed runs and their evidence audits.

A [Vilar checkpoint repair](https://github.com/m9h/GRN_ODE/blob/eb666a175caf4dbabafc5fb677f2d5962729d24f/python/results/catalog-breaking-network32-resume-repair-20261114/README.md)
addresses a restoration failure before simulation: five inherited failed case
summaries outside partition 7 did not match the available branch snapshot.
The repair strictly validates all 2,288 branch checkpoints and five reusable
selected case summaries, preserving the other 43 summaries unchanged as history.
The [original checkpoint ZIP](https://github.com/m9h/GRN_ODE/releases/tag/kinetics-vilar-resume-repair-20261114)
and reproduction script retain the discrepancy. A [targeted restart](https://github.com/m9h/GRN_ODE/actions/runs/43559717170)
handles only partition 7 of the original sixteen. This is infrastructure repair;
no case or model has gained validated status from it.

A [further Linux dispatch](https://github.com/m9h/GRN_ODE/actions/runs/43374603951)
adds Hoefnagel, Ueda, Markevich, De Caluwé and François. Its
[verified inventory](https://github.com/m9h/GRN_ODE/blob/3a71ecb012a07957f09148625249e364b8c4676f/python/CATALOG_BREAKING.md#distributed-coverage-for-the-remaining-local-only-searches)
assigns all 1,414 initial cases to 80 disjoint partitions, retaining each case's
full conditional protocol. Hoefnagel now passes its
[complete 112-case audit](https://github.com/m9h/GRN_ODE/blob/f55c9a62913f8ece85fc96096b22b27807cf94cf/python/results/catalog-breaking-linux-10/audit.json):
2,045 conditional trials, 4,741 response-trials and 8,158 distinct branches.
Its [evidence release](https://github.com/m9h/GRN_ODE/releases/tag/kinetics-hoefnagel-20261113)
preserves all sixteen partitions. Ueda's
[complete 302-case audit](https://github.com/m9h/GRN_ODE/blob/92ca96912effeba7886fb78e9bb64ab084babb82/python/results/catalog-breaking-linux-11/audit.json)
now passes 298 cases and retains four numerical failures. It covers 3,354
conditional trials and 13,315 distinct branches, with no unresolved
continuation decisions. Its [evidence release](https://github.com/m9h/GRN_ODE/releases/tag/kinetics-ueda-20261113)
preserves the full recorded search. The remaining seven unfinished models have
distributed jobs running or queued. Dispatching work does not increase completed
or validated coverage; artifact collection and whole-model audits follow execution.

Ueda's [complete macOS/Linux comparison](https://github.com/m9h/GRN_ODE/blob/e891478b94fb732a3c4bd2e799eb7af35ace6f2a/python/results/catalog-breaking-ueda11-local/run-comparison.json)
finds identical paths in all 302 cases and matching raw and controlled labels
across all 10,726 shared response/engine assessments. Both runs retain the same
four failed cases. Its [native refinement audit](https://github.com/m9h/GRN_ODE/blob/e891478b94fb732a3c4bd2e799eb7af35ace6f2a/python/results/catalog-breaking-ueda11-refinement/verification.json)
confirms 16/24 branches after all 144 integrations finish; eight still disagree.
The verifier checks provenance, full failure coverage and recorded comparisons;
22 targeted checks pass. The producer did not save raw arrays, so this
verification does not independently recompute pointwise errors.
The subsequent [full-array Radau/RoadRunner audit](https://github.com/m9h/GRN_ODE/blob/ede1a69d3ea29c4388bb152704255370a57023ca/python/results/catalog-breaking-scipy-ueda11/README.md)
now confirms **all 24 trajectories** after 96 integrations and 144 independently
recomputed comparisons. Every trajectory retains 221,001 samples, all observables
and its original reset train. The [new release](https://github.com/m9h/GRN_ODE/releases/tag/kinetics-ueda-radau-20261114)
preserves all 96 arrays and reproduction instructions.

The [complete-case inventory](https://github.com/m9h/GRN_ODE/blob/aa1a49a212981dda484a5fb1529f337f7badb058/python/results/catalog-breaking-ueda11-case-plan-20261114/README.md)
retains 298 original case trajectories, adds 24 later candidate trajectories
that the original search did not reach, and includes the full untreated
control. The 323-trajectory computation is running after 67 regression tests
and a fresh capture from all original archives passed. The final case audit
must replay conditional decisions from the new arrays. Ueda remains
**298/302 validated cases**; no complete cases have been recovered yet.

Network 2's [next continuation](https://github.com/m9h/GRN_ODE/actions/runs/43556602590)
preserves its terminal parent's 611 recorded passing cases out of 624 and
finishes the remaining 13. All sixteen parent artifacts were verified; three
partitions require more work. Full model completion still requires the combined
coverage and numerical audit.

An [independently transcribed mpmath diagnostic](https://github.com/m9h/GRN_ODE/blob/058df6fe0f9d96874f604618afddcf64fde90bf8/python/PRECISION_DIAGNOSTICS.md#independent-marhl-implementation)
has completed all three failed Marhl branches at two arithmetic precisions.
The full-array audit confirms agreement with Heyoka on every sample, while
all three branches still disagree with the recorded RoadRunner trajectory.
The untreated baseline agrees across implementations. The subsequent
[complete case audit](https://github.com/m9h/GRN_ODE/blob/f8d4e26e62c6fd940f6e940c1c0d9b3439100622/python/results/catalog-paired-marhl-case-recovery/README.md)
now checks all fifteen additional controls and all 18 required trajectories.
Both cases recover with matching controlled classifications, bringing Marhl
to **26/26 validated paired cases**. No original passing case needs revalidation.
Three arms retain their native-solver disagreement. Both high-precision
implementations use Taylor methods; no different-integrator-family agreement
is claimed. The [release](https://github.com/m9h/GRN_ODE/releases/tag/kinetics-marhl-paired-recovery-20261114)
preserves every array and checksum. All 15 complete-case auditor tests pass,
and the audit reproduces from the extracted release archive.

The [Ciliberto Radau audit](https://github.com/m9h/GRN_ODE/blob/058df6fe0f9d96874f604618afddcf64fde90bf8/python/results/catalog-breaking-scipy-ciliberto28-shard0/audit.json)
confirms ten previously incomplete branches from the first partition: all 40
integrations and 60 full-array comparisons pass. This does not validate the two
complete cases, which require their other controls and conditional continuation.
The [complete-control computation and auditor](https://github.com/m9h/GRN_ODE/blob/a0ea22a0b7c24cee52bec3e5bab7f5bd3d602e93/python/CATALOG_BREAKING.md#ciliberto-partition-zero-refinement)
now cover a planned inventory of 214 distinct reset schedules for those two
cases, plus a full untreated control. All possible third interventions are
included. The computation is running; the independent auditor is ready to
check all saved observations, reconstruct each conditional path and recompute
the controlled classifications. Every required control and the untreated
baseline must pass before either case can be recovered. No additional case
recovery is claimed yet.

Leloup's twelve original mismatches also pass recorded native refinement checks.
Its [full case recovery](https://github.com/m9h/GRN_ODE/blob/f55c9a62913f8ece85fc96096b22b27807cf94cf/python/results/catalog-breaking-linux-12/audit.json)
now passes all 216 cases, 3,323 conditional trials and 13,230 distinct branches.
This fresh sixteen-partition search uses refined solver tolerances while keeping
the model, calibration, reset schedules, observations and acceptance thresholds
fixed. The original 212/216 result remains available separately.

The [complete Fuss native refinement diagnostic](https://github.com/m9h/GRN_ODE/blob/3eb20722bc161fc85d141f8bbb0e313c12fa0f54/python/results/catalog-breaking-fuss8-refinement/README.md)
finishes all 1,980 integrations for 330 originally failed branches, confirming
none. COPASI is self-consistent under both refinements, but RoadRunner is not,
and the engines disagree at all three settings. Fuss remains **314/332 passing
breaking cases**. The [release](https://github.com/m9h/GRN_ODE/releases/tag/kinetics-fuss-refinement-20261114)
preserves all records and the complete source evidence. Its independent
verification checks provenance and recorded comparisons; the producer saved
no raw arrays, so no independent pointwise recomputation is claimed.

A separate [Fuss Radau pilot](https://github.com/m9h/GRN_ODE/blob/fa8ee594ffeb04d52a632d391a20c9f0093ab91d/python/results/catalog-breaking-fuss-radau-plan-20261114/README.md)
now compares COPASI with SciPy's Radau implementation, with a refinement of each
solver and all arrays retained. Three branches are selected deterministically
from the lowest, middle and highest tightest native-comparison errors. Each
retains all 221,001 samples and its complete reset train. The runner and auditor
pass 81 tests, with one fixture-specific skip; those tests are software checks,
not evidence of model agreement. The pilot is running and has not recovered any
Fuss cases. Even a successful three-branch pilot would leave the full failed
branch inventory and complete-case validation to do.

The audit distinguishes attempted initial coverage, resolved conditional
searches and numerical validation; selected models cannot establish all-35
completion. Rohwer's complete 170-control result is included in the recovery above.
The [all-35 evidence index](https://github.com/m9h/GRN_ODE/blob/95ef898b05b2c67dd5c2745a3f8a0f8b71c4c4ad/python/results/catalog-breaking-coverage-20261114/README.md)
checks the catalog and candidate counts against every included complete-model
audit. It retains failed original runs alongside subsequent recoveries and
excludes branch-only diagnostics. Four passing models have no eligible breaking
cases under the declared selection, so their completion is not evidence of a
learning response.
Further diagnostics retain every failed or mismatched trajectory.
The historical MATLAB checkout is incomplete, so this is not an exact rerun.

Network 35's [Rohwer breaking continuation](https://github.com/m9h/GRN_ODE/blob/c3066a6d171ae7602d3699098ea811c3d3da4871/python/results/catalog-breaking-network35-continuation-20261113/README.md)
retains the terminal parent's 249/260 evaluated cases, of which 131 pass.
Only partitions 5 and 7 lack complete case coverage. The continuation restores
all sixteen checkpoints and computes the missing cases while retaining existing
numerical failures; it does not count partial coverage as model completion.

The [Vilar short-output diagnostic](https://github.com/m9h/GRN_ODE/blob/30eb1e29442748c4fcf443777841537b71e5e8d9/python/results/catalog-breaking-vilar-short-output-logged-20261113/README.md)
repeats three selected incomplete breaking trajectories at three solver
tolerances. All nine COPASI runs exhaust the internal-step budget; saved logs
also record clock-resolution warnings. RoadRunner completes all nine, but its
refinement comparisons fail for one trajectory. No branch or case recovers.
The independent audit verifies the full arrays, logs and original SBML's
conserved promoter pools. Resetting only `DA` or `DR` can change the total pool,
so a persistent response can reflect material added by the intervention.
That interpretation check is distinct from identifying the solver's unique
failure cause. The [release](https://github.com/m9h/GRN_ODE/releases/tag/kinetics-vilar-output-diagnostics-20261113)
preserves both diagnostic attempts and all partial outputs.

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
