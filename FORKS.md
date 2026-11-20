# Forks, contributions and reproducible revisions

Kinetics evidence updated **2026-11-20 UTC**; other fork and review snapshots are
retained from **2026-11-09**. Branch links follow ongoing work; revision links
preserve the code examined. Review status can change after these dates.

The latest [35-model coverage report](https://github.com/m9h/GRN_ODE/blob/f45fed315f63c19f66690dffe676caf1681fe011/python/results/catalog-breaking-celliere29-20261116/README.md)
records **34 complete initial-case inventories and 26 passing whole-model audits**.
Cellière (29) passes all 1,088 cases and 34,816 conditional trials. Its
[release](https://github.com/m9h/GRN_ODE/releases/tag/kinetics-celliere-20261116)
preserves all sixteen original artifact ZIPs; a fresh extraction reproduces
the full audit. Tyson (5) is the only unfinished initial inventory. Its
[partition 15](https://github.com/m9h/GRN_ODE/actions/runs/44118517338) has completed
all four cases; only [partition 14](https://github.com/m9h/GRN_ODE/actions/runs/44448634325)
remains unfinished, with three of its four cases recorded (two passing). François partition 14 completed all seven cases, with three
numerical failures retained; its separate Linux inventory still needs
[partition 15](https://github.com/m9h/GRN_ODE/actions/runs/44448645976).
Nine local numerical workers and their coordinator remain
stopped at the user's request. The dated results below retain the earlier
evidence history.

## Current execution

The original job snapshot below was checked **2026-11-19 at 18:31–18:35 UTC**.
Tyson, François and Vilar were checked again **2026-11-20 at 02:03 UTC**;
Fuss, Ueda and Marhl have the later verified updates described below. The three continuations below were dispatched once, after
verifying their terminal parent artifacts. No local numerical worker was resumed.

| Computation | Current cloud run | Observed state |
|---|---|---|
| Tyson initial inventory | [Partition 14](https://github.com/m9h/GRN_ODE/actions/runs/44589141810) | Latest five-hour continuation ended incomplete; new checkpoint awaits collection and audit |
| François separate Linux inventory | [Partition 15](https://github.com/m9h/GRN_ODE/actions/runs/44589146957) | Producer reports complete selected coverage, one of eight cases passing; archive collection and independent replay remain pending |
| Vilar precision diagnostics | [Partitions 8, 9, 11 and 16](https://github.com/m9h/GRN_ODE/actions/runs/44589152244) | Run in progress; verified parent checkpoints remain incomplete |
| Fuss complete case controls | [All 32 fixed partitions](https://github.com/m9h/GRN_ODE/actions/runs/44385665111) | All 32 jobs terminal and all original ZIPs audited: 794 complete arrays, 180 complete branches; all partitions need continuation |
| Ueda complete case controls | [153 continuation branches in 32 partitions](https://github.com/m9h/GRN_ODE/actions/runs/44393623529) | Fourteen partitions verified: seventy branches, 280 arrays; eighteen partitions still required |
| Rohwer breaking diagnostics, network 35 / BioModel 38 | [All 750 failed branches](https://github.com/m9h/GRN_ODE/actions/runs/44401097371) | Ten terminal artifacts await audit; five jobs running, seventeen queued |
| Ciliberto breaking diagnostics, network 28 / BioModel 697 | [All 260 remaining original failed branches](https://github.com/m9h/GRN_ODE/actions/runs/44407336593) | Seven partitions verified: sixty branches, 240 arrays; thirteen further artifacts await audit; one job running, eleven queued |
| Ciliberto complete later controls | [All 6,859 remaining controls](https://github.com/m9h/GRN_ODE/actions/runs/44412503884) | Three partitions verified: 81 branches, 324 arrays; five further artifacts await audit; three jobs running, 245 queued |
| Rohwer complete later controls | [Batch 0](https://github.com/m9h/GRN_ODE/actions/runs/44419997278) · [Batch 1](https://github.com/m9h/GRN_ODE/actions/runs/44420020715) | Nine computations running and 495 queued; eight terminal artifacts await audit |

All **864 computation jobs** across the five Ueda, Ciliberto and Rohwer
selections are now bound to their fixed plans, actual job IDs, attempts and
source revisions. The [collection evidence](docs/evidence/cloud-collection-20261119.json)
retains those identities, API snapshot hashes and the first array-audit results.
Ciliberto diagnostic partitions 0, 1, 2, 3, 4, 6 and 7 now confirm sixty branches:
240 trajectories and 360 comparisons pass. Its later-control partitions 5, 6
and 7 confirm another 81 branches, 324 arrays and 486 comparisons. Ueda
partitions 0 and 1 confirm ten branches, forty arrays and sixty comparisons.
The [updated evidence](docs/evidence/cloud-progress-20261119-evening.json)
preserves the fixed selections, original ZIP identities and individual branch
checks. Every grid, observable, reset protocol and extracted byte verifies
without collection errors. The largest scaled errors are 0.73991 for Ciliberto
diagnostics, 0.03387 for its later controls, and 0.04998 for Ueda, against the
unchanged acceptance threshold of 1. These results add no recovered cases or
whole-model passes; every unfinished partition remains required.

The [later Ueda audit](docs/evidence/ueda-continuation-20261119-evening.json) covers
partitions 0 through 13: seventy branches, 280 arrays and 420 passing comparisons.
The maximum scaled error is 0.05435. Combined with 170 preserved branches, this
provides 240 of 323 required branches; 83 and the full case replay remain.

The earlier [Fuss checkpoint audit](docs/evidence/fuss-checkpoint-progress-20261119.json)
verifies all fourteen available original ZIPs (3,001,628,740 bytes), extracted
files and 359 completed trajectories. All 253 previously completed arrays in
these same partitions remain byte-identical, with 106 newly completed arrays.
Their 82 complete branches pass all 492 pairwise comparisons. Three producers
recorded clean checkpoint stops; eleven artifacts retain a running status after
their jobs ended. In that audit, all fourteen inventories remained incomplete,
and eighteen partitions stayed pending. The [subsequent all-32 audit](docs/evidence/fuss-complete-checkpoint-20261119.json)
now verifies 794 complete arrays, all 528 parent arrays unchanged, and 266
additions. Its 180 complete branches pass all 1,080 pairwise comparisons. All
32 inventories remain incomplete and require continuation; no selected case is
recovered. The [next continuation](https://github.com/m9h/GRN_ODE/actions/runs/44657363724)
is now confirmed queued for all 32 original partitions, from this verified parent.

The [new terminal-checkpoint audit](docs/evidence/cloud-progress-20261119-evening.json)
replays all recorded cases and checks all 95 Tyson and 324 François branch
records against their original archived bytes. Eight and twenty new passing
branch records were saved respectively, and all previously passing checkpoint
bytes were preserved. Both jobs reached their five-hour limits. Tyson has one pending case,
`pM__up--M__up`. François has one pending case, `rB__up--gB__up`, and retains an
unresolved conditional decision in a previously recorded failed case. A finished
job or recorded case does not imply numerical validation.

The [Vilar checkpoint comparison](docs/evidence/cloud-progress-20261119-evening.json)
verifies all four original artifact ZIPs and every extracted file. Each 128-bit
checkpoint added 510–516 observations while preserving its previous observations
bit for bit. All four saved another partial checkpoint; no
complete new trajectory was obtained. Exact MPFR state restoration must pass in
the matching Linux runtime before continuation. Vilar remains at thirteen of
seventeen complete precision partitions, with its three paired cases unresolved.

The [full Marhl precision runner](https://github.com/m9h/GRN_ODE/blob/a09ed95826191b3b652a22e432b1e85212884e99/python/results/catalog-breaking-marhl-full-precision-20261119/README.md)
implements the complete 1,520-task inventory and per-branch six-pair full-array
audits. Its local validation passes 124 tests; four Heyoka-dependent checks
await [Linux CI](https://github.com/m9h/GRN_ODE/actions/runs/44590810828).
The [cloud producer and authenticated checkpoint transfer](https://github.com/m9h/GRN_ODE/tree/a3778b8cbb8bfdc16a9ddd4bbe84dd213fdf1022)
now pass the [complete Linux validation gate](https://github.com/m9h/GRN_ODE/actions/runs/44593959589):
234 tests, no failures or skips. Batches [0](https://github.com/m9h/GRN_ODE/actions/runs/44608641889),
[1](https://github.com/m9h/GRN_ODE/actions/runs/44608843472),
[2](https://github.com/m9h/GRN_ODE/actions/runs/44625023792),
[3](https://github.com/m9h/GRN_ODE/actions/runs/44625203552),
[4](https://github.com/m9h/GRN_ODE/actions/runs/44657098734) and
[5](https://github.com/m9h/GRN_ODE/actions/runs/44657261295) are all confirmed submitted.
The [published offline collector and full twelve-case replay](https://github.com/m9h/GRN_ODE/blob/f95c155a968e15c30bdd39d6ac843f7b961c2930/python/results/catalog-breaking-marhl-full-precision-20261119/COLLECTION.md)
pass [all 47 Linux tests](https://github.com/m9h/GRN_ODE/actions/runs/44636509380), without skips.
The [execution evidence](docs/evidence/marhl-complete-execution-20261120.json) records
all six run IDs, both original CI artifacts, exact source revisions and the
unchanged complete 1,520-task scope. Computation job bindings still await each
run's validation gate. No long-horizon Marhl result is claimed.

A read-only [Tyson checkpoint audit](docs/evidence/tyson-checkpoint-progress-20261118.json)
compares the last two terminal partition-14 runs,
[44118514341](https://github.com/m9h/GRN_ODE/actions/runs/44118514341) and
[44247126362](https://github.com/m9h/GRN_ODE/actions/runs/44247126362).
Their saved branch inventories grew from **59 to 71**, adding twelve passing
branch records while preserving every previously passing checkpoint byte for
byte. Both runs still had two of four complete cases. One branch retained the
same solver disagreement. Thus the last continuation advanced through the
conditional search despite the unchanged case count; the later checkpoint audit above now records a third case. The audit verifies both original
ZIPs against GitHub's checksums, checks the internal consistency of comparison
and window summaries, and replays completed-case decisions. Those artifacts contain no raw
trajectories, so this is not a fresh numerical comparison or a model recovery.

Ueda's 323-trajectory case-control computation remains stopped locally. Its
[new cloud plan](https://github.com/m9h/GRN_ODE/blob/b585ee97de7000c2ec1afe5454216629601eee87/python/results/catalog-breaking-ueda-continuation-20261118/README.md)
preserves 628 available arrays, independently verifies 156 complete branches,
and restores 24 published diagnostic branches (ten overlap). All 153 branches
initially lacking complete evidence remain in the fixed selection. Local validation
passes 77 targeted tests; the Linux gate has passed. The first independently
verified cloud partition brings complete branch evidence to 175/323, with 148
still required. Its four unresolved cases remain outstanding.
The separate [offline collector](https://github.com/m9h/GRN_ODE/blob/0c3c315dd34391abd4c38bfe93a358e78779451e/python/results/catalog-breaking-ueda-continuation-20261118/COLLECTION.md)
requires all 32 fixed jobs and replays the unchanged full case audit only after
every selected attempt finishes. Forty-eight targeted local tests pass, including
retained mismatches and failed integrations. A real preserved branch reproduces
all six comparisons over 221,001 observations and 13 observables. This verifies
collection behavior and adds no scientific coverage; its Linux validation has passed.
The [preserved evidence release](https://github.com/m9h/GRN_ODE/releases/tag/kinetics-ueda-preservation-20261118)
publishes all 787 available snapshot files and the original diagnostic archive
as twelve evidence assets (11.67 GB) plus a checksum manifest. A fresh download
verifies all 628 available arrays and reproduces all three preparation outputs
byte for byte, without ODE integration. The
[reproduction guide and proofs](https://github.com/m9h/GRN_ODE/blob/07568199b113fee32f99d3feefed38e6d845b01c/python/results/catalog-breaking-ueda-continuation-20261118/RELEASE.md)
retain the missing-file accounting and full 323-branch scope. Eleven transport
tests pass locally. No complete Ueda case recovery is claimed.
All four previous local collection/audit watchers exited after their selected
runs became terminal. Their outputs are preserved. The stopped numerical
workers' source trees and environments remain unchanged.

The new [complete Marhl recovery inventory](https://github.com/m9h/GRN_ODE/blob/7dd0beeac23571795e277770623f13b70f3766a7/python/results/catalog-breaking-marhl-full-controls-20261118/README.md)
reproduces all 783 original branch records and all 38 original cases before
reconstructing the full scope for its twelve failed cases: **380 distinct
trajectories, including 88 potential controls absent from the original search**.
It retains all 29 failed diagnostic specifications, both original records of
the shared failed control, every possible later trial and the untreated 0–2210
control. [Verification](docs/evidence/marhl-full-controls-20261118.json) records
25 new tests and 66 combined tests passing, also with optional numerical imports
blocked. Its [Linux validation](https://github.com/m9h/GRN_ODE/actions/runs/44423932643)
has passed. Extending the two independent high-precision implementations to
these full horizons is the next numerical step; this change starts no new
integrations and leaves the original result at **26/38 validated cases**.

The [Marhl checkpoint adapter](https://github.com/m9h/GRN_ODE/blob/8888e2bd03bba4f9010a288e9b355c2c7c2316c1/python/results/catalog-breaking-marhl-checkpoints-20261119/README.md)
now preserves exact internal mpmath state across interrupted long protocols.
Deterministic integration chunks retain every physical reset and original
observation. The [verification record](docs/evidence/marhl-checkpoints-20261119.json)
records 55 new tests and 122 combined tests passing, including a clean shallow
checkout after fetching all three pinned source revisions. Tests cover both
precisions, state below binary64 resolution, repeated restarts, real reset
dynamics, published short-horizon observations and all 380 protocol grids.
The first Linux run passed the checkpoint tests but failed provenance checks
because its shallow checkout lacked historical commits. That workflow is fixed;
[corrected validation](https://github.com/m9h/GRN_ODE/actions/runs/44460158089) is queued.
The full Heyoka/mpmath breaking producer, complete arrays and twelve-case replay
remain required. No long-horizon convergence or new recovered case is claimed.

The new [Rohwer source audit and fixed selection](https://github.com/m9h/GRN_ODE/blob/40fe82344d8dacb2d79ebdc4087ee52beb90a091/python/results/catalog-breaking-rohwer-diagnostics-20261118/README.md)
reproduce the original 137/260 whole-model result from all sixteen partitions.
All 750 failed branches remain selected: 466 completed solver disagreements and
284 COPASI output-shape errors. Each branch will retain four full trajectories
and undergo all six pairwise comparisons at unchanged acceptance tolerances.
Forty-four targeted tests, the complete real input check and workflow lint pass
locally; Linux validation has passed. The 123 failed cases still require their
full controls and conditional replay. No new whole-model pass is claimed.
The separate [Rohwer collector](https://github.com/m9h/GRN_ODE/blob/12c0693df1d68d1736b274a9364e1ef7b2533b06/python/results/catalog-breaking-rohwer-diagnostics-20261118/COLLECTION.md)
binds the fixed jobs only after validation, verifies original ZIPs and every
available complete array, and retains mismatches and interrupted diagnostics.
Its 34 tests and all 78 combined targeted tests pass locally. A check against
the then-queued gate correctly rejected binding. Linux collector validation
has now passed; these checks add no scientific coverage.

The [complete Rohwer controls](https://github.com/m9h/GRN_ODE/blob/c5be7556d38832a88e695a3559cedee2ab139521/python/results/catalog-breaking-rohwer-full-controls-20261118/README.md) now cover all 123 failed cases and all
11,674 potential branches, including the untreated baseline. The original
137/260 audit reproduces. The input bundle preserves 11,247 original records
across partitions, representing 10,826 distinct specifications, and identifies
848 unsaved potential controls. Fifteen cases lack potential controls in their
original partition. The 750 diagnostics remain unchanged; all 10,924
later controls are still required.
All 70 targeted tests pass, including 24 new adapter tests that also pass without
optional JAX imports. The [public input release](https://github.com/m9h/GRN_ODE/releases/tag/kinetics-rohwer-full-controls-20261118) contains 20 files
(150,935,423 bytes including manifest and verification). Every fresh download
matches the original bytes and server checksum; complete input/runtime validation
reproduces exactly. See the [download verification](docs/evidence/rohwer-full-control-inputs-20261118.json).
Linux input validation has passed. The input preparation performs no integrations and claims no case recovery.

The [later-control runner and independent auditor](https://github.com/m9h/GRN_ODE/blob/0dc31af29f4ff9c5e0e610d7c473cc1382fb7dda/python/results/catalog-breaking-rohwer-later-controls-20261118/README.md) now
select all 10,924 remaining controls in two disjoint fixed batches. Batch 0
contains 5,548 branches, and batch 1 contains 5,376. All 848 generated controls
and the untreated baseline are included. Each branch retains all 17 observables,
the complete original grid and four solver outcomes; all six comparisons and
window summaries are recomputed from saved arrays. The original numerical
producer, reset schedules and acceptance criteria are unchanged. Cross-batch or
cross-partition records, changed requests and truncated arrays are rejected;
honest failures, time/disk stops and unfinished work remain explicit.
All 118 targeted tests pass, including 53 new tests that also pass with optional
JAX imports blocked. The released complete inputs and actual numerical runtime
validate. Both cloud batches have passed their Linux gates. The
[dispatch and local validation record](docs/evidence/rohwer-later-control-dispatch-20261118.json)
records exact run IDs and source. All 512 compute job IDs are now bound in the
[collection evidence](docs/evidence/cloud-collection-20261119.json).
The independent 123-case replay still needs all 11,674 outcomes;
branch counts cannot establish recovered cases or change whole-model coverage.

The [two-batch collection guide](https://github.com/m9h/GRN_ODE/blob/b1643064668f559024c11acc84c196e06b7d2526/python/results/catalog-breaking-rohwer-later-controls-20261118/COLLECTION.md) now documents exact
selection of all 512 computation jobs and 10,924 controls from both fixed runs.
The collector preserves original ZIPs and all six API responses, rechecks every
extracted byte and independently audits complete trajectories. Partial children,
orphan arrays, temporary checkpoints, solver failures and parent timeouts stay
explicit. Both batches and their complete job inventories are required; artifacts
cannot move between batches, partitions or attempts. All 173 targeted local tests
pass, including 86 new collector tests that also pass with optional JAX imports
blocked. Real plan/model/runtime verification passes; the earlier queued-gate
checks correctly prevented premature binding. See the [validation evidence](docs/evidence/rohwer-later-collection-20261118.json).
Linux collector validation has passed. No new case recoveries or whole-model
coverage are claimed.

The [complete Rohwer case auditor](https://github.com/m9h/GRN_ODE/blob/602c34a0db23b2a75ee5a1a9aefe6caf8524d992/python/results/catalog-breaking-rohwer-full-case-audit-20261118/README.md) now assigns all 11,674
branches exactly once across the 750 diagnostics and 10,924 later controls. It
rechecks original ZIPs, exact API identities and all saved arrays for both report
formats before replaying all 123 cases with unchanged scoring and conditional
search rules. The untreated baseline, all 848 generated controls and all
potentially needed paths remain required. Original, primary and refined paths
stay separate; contradictions with older passing summaries retain partition
identity. All 235 targeted local tests pass, including 38 new tests that also
pass with optional JAX imports blocked. The real input/model/runtime check
verifies the complete scope. With cloud sources explicitly unavailable, the audit
correctly leaves all 11,674 branches pending and recovers zero cases. See the
[validation evidence](docs/evidence/rohwer-full-case-audit-20261118.json).
Linux validation has passed. Actual complete-case results remain pending; the
original 137/260 whole-model result is unchanged.

Ciliberto's [complete failure inventory](https://github.com/m9h/GRN_ODE/blob/de23184d6149473a6ce4533f72ea8d32cc337085/python/results/catalog-breaking-ciliberto-full-inventory-20261118/README.md)
now retains all 74 failed cases and all 7,334 potential control branches. Four
cases require 200 branches absent from every original partition; the new
compiler generates their specifications without inventing original results.
A fresh download of the original archive reproduces the 548/622 audit, and all
860 published recovery arrays pass re-audit. Those 215 verified branches leave
7,119 branches uncomputed. The fixed plan first diagnoses 260 remaining original
failures, then completes 6,859 remaining controls before a full 74-case audit.
The new [execution wrapper](https://github.com/m9h/GRN_ODE/blob/4c58f7969373f447cbb64e6390fceac92548dd31/python/results/catalog-breaking-ciliberto-full-diagnostics-20261118/README.md)
queues every remaining original failure across 32 fixed partitions, requesting
1,040 full trajectories. Its
[Linux gate](https://github.com/m9h/GRN_ODE/actions/runs/44407336593) has passed.
All 85 targeted local tests, the complete real input/runtime check and workflow
lint pass. Ten originally failed branches are excluded only because their full
arrays already passed the published audit. The first five diagnostic partitions
now add 42 independently confirmed branches and 168 verified arrays; 218
diagnostic branches remain. Failures, mismatches and timeouts
are retained. The later controls, artifact assembly and full-array case audit
remain required; no case or whole-model count has changed.

The separate [Ciliberto collector](https://github.com/m9h/GRN_ODE/blob/3d633d2f0b91c94cb947042032dc25224947322f/python/results/catalog-breaking-ciliberto-full-diagnostics-20261118/COLLECTION.md)
binds all 32 job identities only after the fixed Linux gate passes. It verifies
original ZIPs and complete arrays, retains mismatches and failures, and preserves
temporary checkpoints as unverified evidence. All 43 collector tests and 90
combined targeted tests pass locally. The earlier queued-gate check correctly prevented
premature binding. Its own Linux validation has passed; the computation
producer remains frozen at `4c58f79`.

The [complete control-input adapter](https://github.com/m9h/GRN_ODE/blob/6dd9bd20b2b03620373f86277de0c0657c04b1e4/python/results/catalog-breaking-ciliberto-full-controls-20261118/README.md)
resolves the input-format gap for the 200 unsaved potential branches. It retains
all 74 original case records and 7,666 branch records for 7,134 observed
specifications, preserving separate partition occurrences. All 7,334 potential
specifications remain required. Generated controls have no invented result or
pass flag. The legacy input checks, integrators and case mathematics are unchanged.
All 58 targeted tests pass, including 20 new scope/provenance tests; Linux
validation has passed. The [130 MB input release](https://github.com/m9h/GRN_ODE/releases/tag/kinetics-ciliberto-full-controls-20261118)
reproduces all 74 original case audits from fresh downloads, and all 20 published
asset sizes and digests verify. The [verification record](docs/evidence/ciliberto-full-control-inputs-20261118.json)
documents the result. This is input validation, with zero new integrations and no
case recovery; the 6,859 later controls and full-array case audit are still needed.

All 6,859 later controls are now assigned to the
[fixed complete-control run](https://github.com/m9h/GRN_ODE/actions/runs/44412503884),
which has passed Linux validation. The
[runner and array-audit guide](https://github.com/m9h/GRN_ODE/blob/05232fa83c4be917455dc2d143a11253cb7773e6/python/results/catalog-breaking-ciliberto-later-controls-20261118/README.md)
documents all 27,436 requested trajectories, 256 fixed partitions of 26–27
branches and a maximum of eight simultaneous partitions. Original integration
code, requests, grids, resets, comparisons and case scoring remain unchanged.
All 96 targeted tests pass, including 35 new execution/array-audit tests; they
also pass with optional JAX imports blocked, while a separate preflight verifies
the actual numerical runtime. Complete failures, timeouts, disk stops and
unfinished checkpoints remain explicit. The source is frozen at `05232fa`.

The separate [later-control collection guide](https://github.com/m9h/GRN_ODE/blob/f34fcc07086734db2d1f193acaea6549784c7211/python/results/catalog-breaking-ciliberto-later-controls-20261118/COLLECTION.md) binds all 257 job identities
(including validation) before collecting the 256 partitions. It preserves exact
API snapshots, original ZIPs, verified full arrays, numerical failures and
unverified interrupted checkpoints. All 39 collector tests and 117 combined
targeted tests pass locally. The real plan/model/runtime check and workflow lint
also pass; [Linux validation](https://github.com/m9h/GRN_ODE/actions/runs/44414949767)
has passed. All 256 computation jobs are now bound; artifact collection remains
outstanding.
Full-case assembly still requires all 7,334 branches and replay of all
74 cases; this collector does not change scientific coverage.

The [complete Ciliberto case auditor](https://github.com/m9h/GRN_ODE/blob/9e9b96994278cc50713738c3b43618c5d1f4422c/python/results/catalog-breaking-ciliberto-full-case-audit-20261118/README.md) now joins all three required evidence
stages, independently rechecks original ZIPs and saved arrays, and uses the
unchanged conditional-search and case-scoring functions. All 137 targeted tests
pass, including 35 new tests that also pass without optional JAX imports. A real
input/runtime check reproduces all 74 original cases and the 7,334-branch scope.
The new auditor verifies the published 215 branches and 860 trajectories; its
two known-case regression results match the published audit exactly. With both
new stages unavailable, the full audit remains incomplete with 7,119 branches
required and zero new recovered cases. Linux validation has passed. Complete
branch outcomes, including explicit solver failures, are required before the
full 74-case replay; whole-model coverage remains unchanged.
No new coverage is claimed until artifacts and all 74 cases are independently
audited, with the 215 published and 260 first-stage branches included.

Two older workflow runs from 11 November
([43096519740](https://github.com/m9h/GRN_ODE/actions/runs/43096519740) and
[43097937653](https://github.com/m9h/GRN_ODE/actions/runs/43097937653)) still report
`queued`, with no jobs returned by GitHub. They are separate from the active
computations above and provide no additional completion evidence.

## Latest precision evidence

The separate Vilar precision work now has complete arrays for thirteen of
seventeen partitions. [Partition 6](https://github.com/m9h/GRN_ODE/actions/runs/44247017097)
finished both 30,001-observation Taylor trajectories. Its 128- and 192-bit
results agree at every saved point, while RoadRunner still exceeds the fixed
comparison tolerance (maximum scaled error 2.055). The four remaining
partitions preserved every previous observation exactly and
[continue from their latest checkpoints](https://github.com/m9h/GRN_ODE/actions/runs/44384045755).
All seventeen remain required. Paired validation remains 4,205/4,208 cases;
no additional paired-case recovery is claimed.

The [partition 6 evidence release](https://github.com/m9h/GRN_ODE/releases/tag/kinetics-vilar-partition6-20261118)
preserves its original artifact ZIP and all three complete arrays. A fresh
download reproduces the entire audit exactly, including both native mismatches.
Its [reproduction guide](https://github.com/m9h/GRN_ODE/blob/6efb48467a8eaca45a8f990e77325ec7d3dfe060/python/results/catalog-paired-vilar-partition6-20261118/README.md)
explains the scaled-error formula and uses uv without a local Heyoka installation.

| Fork / working branch | Upstream | Snapshot revision | Review status |
|---|---|---|---|
| [GRN_ODE · kinetics-rohwer-full-controls](https://github.com/m9h/GRN_ODE/tree/kinetics-rohwer-full-controls) | [wesleypclawson/GRN_ODE](https://github.com/wesleypclawson/GRN_ODE) | [c5be755](https://github.com/m9h/GRN_ODE/tree/c5be7556d38832a88e695a3559cedee2ab139521) | All 123 failed cases and 11,674 potential controls preserved, including 848 unsaved specifications; 70 tests pass; public inputs validate from fresh downloads; 10,924 later controls remain to compute |
| [GRN_ODE · kinetics-rohwer-later-controls](https://github.com/m9h/GRN_ODE/tree/kinetics-rohwer-later-controls) | [wesleypclawson/GRN_ODE](https://github.com/wesleypclawson/GRN_ODE) | [0dc31af](https://github.com/m9h/GRN_ODE/tree/0dc31af29f4ff9c5e0e610d7c473cc1382fb7dda) | All 10,924 remaining controls and 43,696 integrations in two fixed batches; 118 tests pass; both Linux gates passed; complete-case replay remains required |
| [GRN_ODE · kinetics-rohwer-later-collection](https://github.com/m9h/GRN_ODE/tree/kinetics-rohwer-later-collection) | [wesleypclawson/GRN_ODE](https://github.com/wesleypclawson/GRN_ODE) | [b164306](https://github.com/m9h/GRN_ODE/tree/b1643064668f559024c11acc84c196e06b7d2526) | Exact two-run collection for all 10,924 controls; full-array and partial-evidence verification; 173 targeted tests pass; Linux validation passed |
| [GRN_ODE · kinetics-rohwer-full-case-audit](https://github.com/m9h/GRN_ODE/tree/kinetics-rohwer-full-case-audit) | [wesleypclawson/GRN_ODE](https://github.com/wesleypclawson/GRN_ODE) | [602c34a](https://github.com/m9h/GRN_ODE/tree/602c34a0db23b2a75ee5a1a9aefe6caf8524d992) | Complete 11,674-branch/123-case audit implemented; 235 tests pass; real full scope verifies; cloud evidence and actual case recovery remain pending |
| [GRN_ODE · kinetics-rohwer-breaking-collection](https://github.com/m9h/GRN_ODE/tree/kinetics-rohwer-breaking-collection) | [wesleypclawson/GRN_ODE](https://github.com/wesleypclawson/GRN_ODE) | [12c0693](https://github.com/m9h/GRN_ODE/tree/12c0693df1d68d1736b274a9364e1ef7b2533b06) | Fixed 750-branch collection, complete-array verification and explicit partial evidence; 78 combined local checks pass; earlier queued gate rejected; Linux validation passed |
| [GRN_ODE · kinetics-rohwer-breaking-diagnostics](https://github.com/m9h/GRN_ODE/tree/kinetics-rohwer-breaking-diagnostics) | [wesleypclawson/GRN_ODE](https://github.com/wesleypclawson/GRN_ODE) | [40fe823](https://github.com/m9h/GRN_ODE/tree/40fe82344d8dacb2d79ebdc4087ee52beb90a091) | All 750 original failed branches selected for 3,000 complete trajectories; 44 targeted tests pass; Linux validation passed; original 137/260 result retained |
| [GRN_ODE · kinetics-ueda-evidence-release](https://github.com/m9h/GRN_ODE/tree/kinetics-ueda-evidence-release) | [wesleypclawson/GRN_ODE](https://github.com/wesleypclawson/GRN_ODE) | [0756819](https://github.com/m9h/GRN_ODE/tree/07568199b113fee32f99d3feefed38e6d845b01c) | Published raw snapshot and diagnostic archive; fresh downloads reproduce the full preparation byte for byte; 11 transport tests pass; 153 branches and four cases still require computation and audit |
| [GRN_ODE · kinetics-ueda-cloud-collection](https://github.com/m9h/GRN_ODE/tree/kinetics-ueda-cloud-collection) | [wesleypclawson/GRN_ODE](https://github.com/wesleypclawson/GRN_ODE) | [0c3c315](https://github.com/m9h/GRN_ODE/tree/0c3c315dd34391abd4c38bfe93a358e78779451e) | Offline collection and full 323-branch assembly; 48 targeted local tests and one full real-branch comparison reproduction pass; Linux validation passed; no new case recovery |
| [GRN_ODE · kinetics-ueda-cloud-continuation](https://github.com/m9h/GRN_ODE/tree/kinetics-ueda-cloud-continuation) | [wesleypclawson/GRN_ODE](https://github.com/wesleypclawson/GRN_ODE) | [b585ee9](https://github.com/m9h/GRN_ODE/tree/b585ee97de7000c2ec1afe5454216629601eee87) | Complete 323-branch/four-case scope retained; 170 branches backed by verified evidence, 153 selected for cloud computation; 77 local tests pass, Linux validation passed; local worker remains stopped |
| [GRN_ODE · kinetics-ciliberto-full-diagnostics](https://github.com/m9h/GRN_ODE/tree/kinetics-ciliberto-full-diagnostics) | [wesleypclawson/GRN_ODE](https://github.com/wesleypclawson/GRN_ODE) | [4c58f79](https://github.com/m9h/GRN_ODE/tree/4c58f7969373f447cbb64e6390fceac92548dd31) | All 260 remaining original failed branches selected; Linux validation passed; 1,040 full trajectories, 32 fixed partitions, unchanged numerical code; 85 targeted tests pass; later 6,859 controls and full-case audit retained |
| [GRN_ODE · kinetics-ciliberto-full-collection](https://github.com/m9h/GRN_ODE/tree/kinetics-ciliberto-full-collection) | [wesleypclawson/GRN_ODE](https://github.com/wesleypclawson/GRN_ODE) | [3d633d2](https://github.com/m9h/GRN_ODE/tree/3d633d2f0b91c94cb947042032dc25224947322f) | Fixed 260-branch collection with original ZIP verification, full-array auditing and explicit interrupted evidence; 43 collector/90 combined tests pass; Linux validation passed; no case recovery claimed |
| [GRN_ODE · kinetics-ciliberto-full-controls](https://github.com/m9h/GRN_ODE/tree/kinetics-ciliberto-full-controls) | [wesleypclawson/GRN_ODE](https://github.com/wesleypclawson/GRN_ODE) | [6dd9bd2](https://github.com/m9h/GRN_ODE/tree/6dd9bd20b2b03620373f86277de0c0657c04b1e4) | Complete 74-case inputs, 7,334 potential controls and explicit provenance for 200 unsaved branches; 58 tests pass; input release validates from fresh downloads; later computation and array audit remain |
| [GRN_ODE · kinetics-ciliberto-later-controls](https://github.com/m9h/GRN_ODE/tree/kinetics-ciliberto-later-controls) | [wesleypclawson/GRN_ODE](https://github.com/wesleypclawson/GRN_ODE) | [05232fa](https://github.com/m9h/GRN_ODE/tree/05232fa83c4be917455dc2d143a11253cb7773e6) | All 6,859 later controls selected; Linux validation passed; 27,436 trajectories in 256 fixed partitions; unchanged numerical producer with independent full-array branch checks; 96 tests pass; full-case audit still required |
| [GRN_ODE · kinetics-ciliberto-later-collection](https://github.com/m9h/GRN_ODE/tree/kinetics-ciliberto-later-collection) | [wesleypclawson/GRN_ODE](https://github.com/wesleypclawson/GRN_ODE) | [f34fcc0](https://github.com/m9h/GRN_ODE/tree/f34fcc07086734db2d1f193acaea6549784c7211) | Fixed collection of all 6,859 later controls; full job pagination, preserved API snapshots, original ZIP verification and independent array audits; 117 targeted tests pass; full-case replay remains required |
| [GRN_ODE · kinetics-ciliberto-full-case-audit](https://github.com/m9h/GRN_ODE/tree/kinetics-ciliberto-full-case-audit) | [wesleypclawson/GRN_ODE](https://github.com/wesleypclawson/GRN_ODE) | [9e9b969](https://github.com/m9h/GRN_ODE/tree/9e9b96994278cc50713738c3b43618c5d1f4422c) | Complete 7,334-branch assembly and 74-case replay implemented; 137 tests pass; 860 published arrays verified and both known cases reproduced; 7,119 branches remain required |
| [GRN_ODE · kinetics-ciliberto-full-inventory](https://github.com/m9h/GRN_ODE/tree/kinetics-ciliberto-full-inventory) | [wesleypclawson/GRN_ODE](https://github.com/wesleypclawson/GRN_ODE) | [de23184](https://github.com/m9h/GRN_ODE/tree/de23184d6149473a6ce4533f72ea8d32cc337085) | All 74 failed cases and 7,334 potential branches inventoried; 215 published branches re-audited, 7,119 remain; 200 previously absent controls retained; 38 tests pass; preparation adds no scientific coverage |
| [GRN_ODE · kinetics-ciliberto-case-collection](https://github.com/m9h/GRN_ODE/tree/kinetics-ciliberto-case-collection) | [wesleypclawson/GRN_ODE](https://github.com/wesleypclawson/GRN_ODE) | [8ab39fd](https://github.com/m9h/GRN_ODE/tree/8ab39fd55fe4252e7cc87d41e66b33f391b4dfcf) | Both selected Ciliberto cases pass from 215 branches and 860 trajectories; complete evidence release reproduces from fresh downloads; 55 targeted tests pass; whole-model count unchanged |
| [GRN_ODE · kinetics-vilar-partition6-publication](https://github.com/m9h/GRN_ODE/tree/kinetics-vilar-partition6-publication) | [wesleypclawson/GRN_ODE](https://github.com/wesleypclawson/GRN_ODE) | [6efb484](https://github.com/m9h/GRN_ODE/tree/6efb48467a8eaca45a8f990e77325ec7d3dfe060) | Complete partition 6: three full arrays, Taylor precision agreement and retained RoadRunner mismatch; original ZIP and fresh-download audit reproduction published; no case recovery |
| [cell_research · main](https://github.com/m9h/cell_research/tree/main) | [Zhangtaining/cell_research](https://github.com/Zhangtaining/cell_research) | [397e94c](https://github.com/m9h/cell_research/tree/397e94c4c1f5b7c6367c2c4cb603eab4fdd274a2) | Changes available on fork main |
| [GRN_ODE · python-memory-replication](https://github.com/m9h/GRN_ODE/tree/python-memory-replication) | [wesleypclawson/GRN_ODE](https://github.com/wesleypclawson/GRN_ODE) | [70a3afa](https://github.com/m9h/GRN_ODE/tree/70a3afad61357e94873ff62a7300c099b4c7ae3e) | [Draft PR in our fork](https://github.com/m9h/GRN_ODE/pull/1) |
| [GRN_ODE · kinetics-celliere-complete](https://github.com/m9h/GRN_ODE/tree/kinetics-celliere-complete) | Same upstream | [f45fed3](https://github.com/m9h/GRN_ODE/tree/f45fed315f63c19f66690dffe676caf1681fe011) | Current index: 34 complete initial inventories, 26 passing model audits; Cellière passes all 1,088 cases and 34,816 conditional trials; all sixteen original ZIPs reproduce the audit; Tyson alone has an unfinished initial inventory |
| [GRN_ODE · kinetics-fuss-case-controls](https://github.com/m9h/GRN_ODE/tree/kinetics-fuss-case-controls) | Same upstream | [4c0f97a](https://github.com/m9h/GRN_ODE/tree/4c0f97adcf1e54019792f5eaf57963efb62cedf1) | Full Fuss execution plan: all 18 failed cases, 1,309 trajectories and 5,236 integrations; 32 immutable partitions, complete-array resume verification and independent case audit; 375 local tests pass, two skip; no new case recovery claimed |
| [GRN_ODE · kinetics-coverage-20261116](https://github.com/m9h/GRN_ODE/tree/kinetics-coverage-20261116) | Same upstream | [c7808bc](https://github.com/m9h/GRN_ODE/tree/c7808bc29fdd33f75d04699441ab349feba1e5e7) | Earlier index: 33 complete initial inventories, 25 passing model audits; five evidence packages reproduce; fifteen targeted continuations retain the original full-model scope |
| [GRN_ODE · kinetics-solver-recovery](https://github.com/m9h/GRN_ODE/tree/kinetics-solver-recovery) | Same upstream | [40ca8ff](https://github.com/m9h/GRN_ODE/tree/40ca8ff586220a5df573e7d383defa2c19ed829a) | Complete François recovery, Goldbeter refinement evidence and full original paired screen; separate from the live breaking source |
| [GRN_ODE · kinetics-newton-reference](https://github.com/m9h/GRN_ODE/tree/kinetics-newton-reference) | Same upstream | [95ef898](https://github.com/m9h/GRN_ODE/tree/95ef898b05b2c67dd5c2745a3f8a0f8b71c4c4ad) | All-35 evidence index: 28 complete initial inventories and 23 passing whole-model audits; all 24 Ueda mismatch trajectories now pass a full-array Radau/RoadRunner audit, with complete-case controls underway; seven breaking searches remain unfinished; paired validation stays 4,205/4,208 |
| [GRN_ODE · kinetics-muller-recovery](https://github.com/m9h/GRN_ODE/tree/kinetics-muller-recovery) | Same upstream | [b089186](https://github.com/m9h/GRN_ODE/tree/b0891863ffd90b3dfb5c944720f0512d81584167) | Producer revision for the complete, passing 118-case network 26 recovery; evidence published on the reference branch above |
| [GRN_ODE · kinetics-leloup-recovery](https://github.com/m9h/GRN_ODE/tree/kinetics-leloup-recovery) | Same upstream | [daed478](https://github.com/m9h/GRN_ODE/tree/daed47882d2d20fa81b193a21c1934a5d83e64dd) | Complete network-12 recovery passes all 216 cases at independently supported refined settings; original evidence remains separate |
| [GRN_ODE · precision-checkpoint-resume](https://github.com/m9h/GRN_ODE/tree/precision-checkpoint-resume) | Same upstream | [80c982c](https://github.com/m9h/GRN_ODE/tree/80c982c7dd02150285782b0f37842650b67b00db) | Eleven Vilar partitions complete; six incomplete, including one unchanged checkpoint; full artifact and saved-state progress inspection, no additional case recovery |
| [GRN_ODE · precision-targeted-resume](https://github.com/m9h/GRN_ODE/tree/precision-targeted-resume) | Same upstream | [5074077](https://github.com/m9h/GRN_ODE/tree/50740779287606d05eae34b2197fc9cb27394fe6) | Five advancing original partitions dispatched without changing their definitions or numerical code; fourteen selection checks and actionlint pass; stalled partition remains explicitly outstanding |
| [GRN_ODE · precision-case-controls](https://github.com/m9h/GRN_ODE/tree/precision-case-controls) | Same upstream | [2e32e58](https://github.com/m9h/GRN_ODE/tree/2e32e584971d0b25ee2b747a986d94ba28b9ceb0) | All 23 additional Vilar controls complete and pass full-array audits; aggregate evidence covers 26/32 trajectories for three unresolved cases, with six missing and three native mismatches; reproducible uv audit and complete evidence release; no additional case recovery |
| [GRN_ODE · kinetics-copasi-output-diagnostics](https://github.com/m9h/GRN_ODE/tree/kinetics-copasi-output-diagnostics) | Same upstream | [30eb1e2](https://github.com/m9h/GRN_ODE/tree/30eb1e29442748c4fcf443777841537b71e5e8d9) | Full-array audit and preserved solver logs for three Vilar breaking branches; all nine COPASI runs stop early; conserved-pool analysis explains how resets change material totals; no case recovery claimed |
| [GRN_ODE · kinetics-fuss-radau](https://github.com/m9h/GRN_ODE/tree/kinetics-fuss-radau) | Same upstream | [edb538d](https://github.com/m9h/GRN_ODE/tree/edb538d9a91910eb2b04c49e058599c23d6b6f70) | Published full-array COPASI/Radau pilot: 3/3 selected branches pass all six comparisons; 12 trajectories and a byte-identical reproduced audit; complete-case validation remains pending |
| [GRN_ODE · kinetics-ueda-cases](https://github.com/m9h/GRN_ODE/tree/kinetics-ueda-cases) | Same upstream | [aa1a49a](https://github.com/m9h/GRN_ODE/tree/aa1a49a212981dda484a5fb1529f337f7badb058) | Recovery inventories include later candidates skipped by the original conditional search; 67 tests pass; Ueda's 323-trajectory control run is stopped locally, with all four unresolved cases retained |
| [GRN_ODE · kinetics-resume-case-selection](https://github.com/m9h/GRN_ODE/tree/kinetics-resume-case-selection) | Same upstream | [cae38e9](https://github.com/m9h/GRN_ODE/tree/cae38e9a6ec4c7567ea6cbf2908778f409a1ebb0) | Vilar checkpoint repair and targeted Tyson continuations; full-model audits now watch fixed selections across runs, with 46 tests and a real four-artifact reproduction; model coverage remains unchanged |
| [GRN_ODE · kinetics-marhl-breaking](https://github.com/m9h/GRN_ODE/tree/kinetics-marhl-breaking) | Same upstream | [079e35d](https://github.com/m9h/GRN_ODE/tree/079e35d8bc0795f427b6cb5b8514f35830f01909) | Published all 120 full-horizon Radau/RoadRunner trajectories for 30 failed records; 3 records pass (2 distinct specifications), 27 retain mismatches; four byte-identical reproduced audits, no complete-case recovery |
| [GRN_ODE · kinetics-marhl-full-controls](https://github.com/m9h/GRN_ODE/tree/kinetics-marhl-full-controls) | Same upstream | [7dd0bee](https://github.com/m9h/GRN_ODE/tree/7dd0beeac23571795e277770623f13b70f3766a7) | Complete 380-trajectory scope for all twelve failed cases, including 88 unreached controls and the full untreated baseline; original audit reproduced; 66 targeted tests pass; no new numerical result |
| [GRN_ODE · kinetics-marhl-breaking-precision](https://github.com/m9h/GRN_ODE/tree/kinetics-marhl-breaking-precision) | Same upstream | [8888e2b](https://github.com/m9h/GRN_ODE/tree/8888e2bd03bba4f9010a288e9b355c2c7c2316c1) | Exact mpmath checkpoints for long breaking protocols; 55 new and 122 combined tests pass; all 380 grids retained; corrected Linux validation queued; full precision computation still required |
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

The [Marhl breaking diagnostic](https://github.com/m9h/GRN_ODE/blob/079e35d8bc0795f427b6cb5b8514f35830f01909/python/results/catalog-breaking-marhl30-radau-20261114/README.md)
has finished all 120 integrations for every failed Linux branch record: 30
records, 29 distinct specifications and 12 cases. Three records pass all six
comparisons among RoadRunner, Radau and their refinements. A shared control
appears twice, leaving two distinct confirmed specifications. All 27 mismatching
records remain in the [full-array release](https://github.com/m9h/GRN_ODE/releases/tag/kinetics-marhl-breaking-radau-20261116).
Radau self-refinement passes on 25/30 records, RoadRunner on 3/30, and the refined
solvers agree on 5/30; those partial checks cannot replace the full acceptance
rule. Every archived file was checksum-verified after fresh extraction, and all
four audits reproduced byte-for-byte in a clean uv environment. No complete
case has been recovered, and the original Linux result remains 26/38.

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

The **14 November snapshot** covered 28 distinct models, of which 23 had
passing full numerical validation after separate recoveries. Seven
models then needed their full searches completed; the current 34/26 counts are
linked at the top of this page. The control-runner, branch-auditor and case-auditor
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

Tyson network 5 has [two targeted continuations](https://github.com/m9h/GRN_ODE/blob/79f7795b80dd3c16686cbaa3935e612639f239f7/python/results/catalog-breaking-network5-targeted-continuation-20261114/README.md)
for partitions [13](https://github.com/m9h/GRN_ODE/actions/runs/43560384864) and
[15](https://github.com/m9h/GRN_ODE/actions/runs/43560386302), which stopped at their
five-hour budgets after saving 41 additional branch checkpoints. Fresh artifact
extractions pass strict restoration checks. The jobs retain all seven selected
cases, six still unfinished, and the original sixteen-partition scheme.
Other partitions continue in the original run; all 58 cases still require a
complete-model audit.

The [continuation auditor](https://github.com/m9h/GRN_ODE/blob/cae38e9a6ec4c7567ea6cbf2908778f409a1ebb0/python/results/catalog-breaking-continuation-auditor-20261114/README.md)
now watches the fixed sixteen-partition selections for both Tyson and Vilar.
It verifies extracted files against the original artifact ZIPs before the
full-model audit, retaining each partition's own branch records. Validation
passes 46 tests and reproduces the existing network-27 result from four real
artifacts, checking all 348 extracted files and historical Git objects. This
verifies the assembly procedure; it adds no new scientific coverage. Missing
or unfinished selections cannot be promoted to complete models.

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
control. The 323-trajectory computation started after 67 regression tests
and a fresh capture from all original archives passed. It remains stopped
locally at the user's request. Its
[cloud continuation](https://github.com/m9h/GRN_ODE/actions/runs/44393623529) has passed
Linux validation after all available arrays and published imports were
checked. The fixed plan retains all four cases and all 323 branches. The final case audit
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
cover 214 distinct reset schedules for two cases, plus the full untreated
baseline. An 18 November audit found missing files despite the earlier producer
report. The surviving data were preserved with matching checksums, one branch
was restored exactly from a published archive, and all 18 other affected branches
were recomputed under the fixed original requests.

The [completed Ciliberto case audit](https://github.com/m9h/GRN_ODE/blob/8ab39fd55fe4252e7cc87d41e66b33f391b4dfcf/python/results/catalog-breaking-ciliberto-case-recovery-20261118/COMPLETED_AUDIT.md)
now recovers **both selected cases** from all **215 branches and 860 full
trajectories**, including the untreated baseline. All 18 replacement artifacts,
72 new arrays and 108 replacement comparisons passed verification; the unchanged
case auditor then reconstructed all controls, conditional paths and classifications.
The [complete evidence release](https://github.com/m9h/GRN_ODE/releases/tag/kinetics-ciliberto-cases-20261118)
preserves 37 evidence assets plus their manifest, totaling 19.3 GB. Every uploaded
size and checksum matches, and a fresh download reconstructs all 215 branches
and 860 arrays. The full audit JSON reproduces after accounting only for the new
assembly timestamp and its report checksum. All 55 targeted tests pass locally.
The separate original full-model result remains **548/622**; selected recoveries
are not added ad hoc to that total.

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

A separate [Fuss Radau pilot](https://github.com/m9h/GRN_ODE/blob/edb538d9a91910eb2b04c49e058599c23d6b6f70/python/results/catalog-breaking-fuss-radau-plan-20261114/README.md)
confirms all three predeclared branches with COPASI, Radau and a refinement of
each: 18/18 pairwise comparisons pass. The branches were selected from the
lowest, middle and highest tightest native-comparison errors. Each retains all
221,001 samples and its complete reset train. The
[release](https://github.com/m9h/GRN_ODE/releases/tag/kinetics-fuss-radau-20261116)
contains all 12 arrays, original records, source evidence and checksums. The
independent audit reproduces byte-for-byte from a fresh extraction in a clean
uv environment. Only 3/330 originally unresolved branches were selected; the
full failed-branch inventory and complete-case validation remain to do.
No Fuss case has been recovered, so the original 314/332 result is unchanged.

The [full Fuss case-control plan](https://github.com/m9h/GRN_ODE/blob/4c0f97adcf1e54019792f5eaf57963efb62cedf1/python/results/catalog-breaking-fuss-full-case-plan-20261116/README.md)
extends that pilot to every originally failed case. It preserves all 1,308
case-control trajectories plus the full untreated baseline and computes each
with COPASI and Radau at two tolerances. The independent auditor requires all
32 partitions, recomputes all six comparisons per trajectory, and replays both
conditional searches. Missing later controls, source changes, corrupted arrays
or a failed baseline prevent recovery. The
[cloud run](https://github.com/m9h/GRN_ODE/actions/runs/43925538098)
passed its Linux test gate (375 passed, two skipped). Its
[checkpoint collection](https://github.com/m9h/GRN_ODE/blob/a94ceb467cf7f6a858e8df4b01db0cdcd154bf90/python/results/catalog-breaking-fuss-full-case-plan-20261116/COLLECTION.md)
verified all 32 original ZIPs and 274 complete integration arrays. All 49
trajectories with four completed integrations pass all six comparisons, including
the untreated baseline. Six jobs checkpointed cleanly; 26 were interrupted
during long integrations. All partitions remain incomplete and
[continue with unchanged source and settings](https://github.com/m9h/GRN_ODE/actions/runs/44142019165).
The original passing cases remain separate; these checkpoints do not recover a
case or change model coverage.

The [18 November continuation check](https://github.com/m9h/GRN_ODE/blob/a31b0ce30ca142fbf5300f9b909c7058c73de2cb/python/results/catalog-breaking-fuss-full-case-plan-20261116/continuation-progress-20261118.json)
verifies the first sixteen resumed partitions. All 137 previously completed
arrays remain byte-identical and 137 additional arrays are complete. Their 58
complete trajectories pass all 348 pairwise comparisons. The other sixteen
partitions remain pending in this snapshot; the fixed selection still requires
all 32, so these partial counts do not recover any of the 18 cases.

The [completed continuation collection](https://github.com/m9h/GRN_ODE/blob/80fec615376378c01f674ea597bea3cc41834a7f/python/results/catalog-breaking-fuss-full-case-plan-20261116/COLLECTION.md)
now verifies all 32 artifacts: 528 complete arrays, including all 274 original
arrays unchanged and 254 new completions. All 112 complete branches pass all
672 comparisons. Three producers stopped cleanly and 29 hit an execution limit
during an integration. All partitions remain incomplete. The
[next continuation](https://github.com/m9h/GRN_ODE/actions/runs/44385665111) preserves
these checkpoints and the unchanged numerical requests, using the validated
scheduling revision with sixteen concurrent partitions and forty more minutes
per job. No selected Fuss case or whole-model count has changed.

The audit distinguishes attempted initial coverage, resolved conditional
searches and numerical validation; selected models cannot establish all-35
completion. Rohwer's complete 170-control result is included in the recovery above.
The [all-35 evidence index](https://github.com/m9h/GRN_ODE/blob/f45fed315f63c19f66690dffe676caf1681fe011/python/results/catalog-breaking-celliere29-20261116/README.md)
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
