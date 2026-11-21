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

**Completion status, 21 November 2026 UTC:** the basic all-35-model simulations
are finished; the full memory-validation goal remains open.

| Validation stage | Verified result | Remaining work |
|---|---|---|
| Baseline kinetics | 35/35 models pass independent comparisons | Complete |
| Single-input retention | 538/538 stimulation cases pass numerical comparisons | Below-resolution response labels remain unresolved |
| Repeated stimulation | 538/538 cases pass on macOS and Linux | Complete numerical comparison |
| Paired stimulation | 4,205/4,208 cases pass | Three Vilar cases unresolved |
| Conditional breaking | 34/35 initial inventories complete; 27/35 whole-model audits pass | Finish Tyson's inventory and resolve or document remaining validation failures |

These counts measure numerical validation, not proof that every network learns.
Completed jobs, software tests and partially verified trajectories do not add
whole-model passes. The evidence links and outstanding work follow below.

The eight models without a passing whole-model breaking audit have different
remaining issues:

| Model | Current gap |
|---|---|
| [Reduced Goldbeter (3)](https://github.com/m9h/GRN_ODE/blob/12c0693df1d68d1736b274a9364e1ef7b2533b06/python/CATALOG_BREAKING.md#a-domain-limit-exposed-by-the-goldbeter-model) | Four integration failures affect two of eight cases; all 24 dedicated diagnostic attempts also stop before the required endpoint. |
| Tyson (5) | One initial case remains unfinished; its verified cloud continuation is running. |
| Fuss (8) | [1,050 trajectories are retained and verified](docs/evidence/fuss-checkpoint-audit-20261121.json) across the latest 31 checkpoints and the older retained partition 11; complete controls and replay remain open for eighteen cases. |
| François (25) | The separate Linux inventory covers all 118 cases, with 38 failures and six unresolved conditional decisions. |
| Ciliberto (28) | Three of 260 first-stage diagnostic branches retain mismatches; later controls and the full 74-case audit remain open. |
| Marhl (30) | The fixed high-precision computation covers 380 branches for twelve cases; collection and complete-case validation remain open. |
| Vilar (32) | Breaking validation remains unresolved, alongside three paired cases; four precision checkpoints remain incomplete. |
| Rohwer (35) | [All 750 first-stage branches are accounted for](docs/evidence/rohwer-checkpoint-audit-20261121.json), but 584 diagnostics remain unfinished; later controls and complete-case replay are also required. |

Our active goal extends the kinetics and memory computations to all **35
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
The [complete Ueda recovery](https://github.com/m9h/GRN_ODE/blob/649df7f5e8f89563078b4349275e60331193d57a/python/results/catalog-breaking-ueda-complete-20261121/README.md)
now raises the passing whole-model count to **27**: all 302 Ueda cases validate,
combining 298 original passes with four complete-control recoveries.
The [complete Cellière TGF-β audit](https://github.com/m9h/GRN_ODE/releases/tag/kinetics-celliere-20261116)
passes all 1,088 cases and 34,816 conditional trials; its sixteen original
evidence packages reproduce the audit from fresh extraction.
New audits pass all 624 Edelstein species-model cases and all 398 Markevich
cases. François, Vilar and Rohwer have also finished their initial inventories,
with failures retained. **Tyson is the only unfinished initial inventory**;
partition 15 has now completed all four cases, leaving only
[partition 14](https://github.com/m9h/GRN_ODE/actions/runs/44930974577).
Its [latest audited checkpoint](docs/evidence/terminal-checkpoints-20261121.json)
adds seven passing branch records and preserves all 107 previous passing
records byte-for-byte. One case remains pending; its next cloud continuation
is bound to the same partition and verified parent.
The [complete separate François Linux inventory](docs/evidence/francois-linux-inventory-20261120.json)
now covers all 118 cases: 80 pass and 38 retain numerical failures. All sixteen
original ZIPs and all 4,121 partition-local branch records verify; six conditional
decisions remain unresolved. This adds no passing whole-model audit.
The [earlier evidence release](https://github.com/m9h/GRN_ODE/releases/tag/kinetics-coverage-20261116)
preserves 64 original Linux artifacts and three complete local model reports;
fresh extractions reproduce all five package audits. Four passing models have
no eligible breaking cases, so this status is not evidence of learning.
The completed [Fuss pilot](https://github.com/m9h/GRN_ODE/releases/tag/kinetics-fuss-radau-20261116)
and [Marhl breaking diagnostic](https://github.com/m9h/GRN_ODE/releases/tag/kinetics-marhl-breaking-radau-20261116)
publish 132 full trajectories with checksums and reproducible array audits.
Fuss confirms its three selected branches; Marhl confirms only 3/30 records
(two distinct specifications). Neither result recovers a complete case.
The [complete Marhl recovery inventory](https://github.com/m9h/GRN_ODE/blob/7dd0beeac23571795e277770623f13b70f3766a7/python/results/catalog-breaking-marhl-full-controls-20261118/README.md)
now identifies all 380 trajectories needed for its twelve failed cases,
including 88 potential controls never reached by the original conditional
search. It reproduces the original evidence and passes 66 targeted tests;
Linux validation has also passed; no new integrations or case recoveries are claimed.
The [full Fuss execution plan](https://github.com/m9h/GRN_ODE/blob/4c0f97adcf1e54019792f5eaf57963efb62cedf1/python/results/catalog-breaking-fuss-full-case-plan-20261116/README.md)
requires all 18 failed cases and 1,309 control trajectories, with 5,236 COPASI/Radau
integrations in 32 fixed partitions. The [latest complete checkpoint collection](https://github.com/m9h/GRN_ODE/blob/80fec615376378c01f674ea597bea3cc41834a7f/python/results/catalog-breaking-fuss-full-case-plan-20261116/COLLECTION.md)
verifies 528 completed arrays, including all 274 earlier arrays unchanged.
Its 112 complete branches pass all 672 pairwise comparisons, including the
untreated baseline. All partitions still need work and
[continue from those checkpoints](https://github.com/m9h/GRN_ODE/actions/runs/44385665111).
The [first fourteen audited continuation checkpoints](docs/evidence/fuss-checkpoint-progress-20261119.json)
contain 359 complete arrays: all 253 parent arrays in those same partitions
remain byte-identical, and 106 are newly completed. Their 82 completed branches
pass all 492 comparisons. These are partial-run counts; the other eighteen
partitions remain required. No additional Fuss case recovery is claimed.
The [complete Ciliberto case audit](https://github.com/m9h/GRN_ODE/blob/8ab39fd55fe4252e7cc87d41e66b33f391b4dfcf/python/results/catalog-breaking-ciliberto-case-recovery-20261118/COMPLETED_AUDIT.md)
now recovers both selected cases from all 215 branches and 860 saved trajectories,
including the untreated baseline. The [complete evidence release](https://github.com/m9h/GRN_ODE/releases/tag/kinetics-ciliberto-cases-20261118)
preserves the original data and all replacement ZIPs. A fresh download reproduces
the full case audit. This does not change the separate 548/622 whole-model result.
The new [complete Ciliberto failure inventory](https://github.com/m9h/GRN_ODE/blob/de23184d6149473a6ce4533f72ea8d32cc337085/python/results/catalog-breaking-ciliberto-full-inventory-20261118/README.md)
covers all 74 failed cases and includes 200 potential control branches missing
from the original paths. After re-auditing the 215 published branches, 7,119
branches remain selected for computation. The first
[260-branch diagnostic run](https://github.com/m9h/GRN_ODE/actions/runs/44407336593)
has passed Linux validation, with 1,040 complete trajectories requested.
All 85 targeted local execution/inventory/audit tests pass. The later 6,859
controls and full 74-case audit remain required; coverage is unchanged.
The [fixed-run collection guide](https://github.com/m9h/GRN_ODE/blob/3d633d2f0b91c94cb947042032dc25224947322f/python/results/catalog-breaking-ciliberto-full-diagnostics-20261118/COLLECTION.md)
now covers all 260 diagnostics, including interrupted checkpoints and retained
solver failures. Its 43 collector tests and 90 combined targeted tests pass
locally; Linux validation has passed. These are validation results, with no new
numerical coverage claimed.
The [full-control input adapter](https://github.com/m9h/GRN_ODE/blob/6dd9bd20b2b03620373f86277de0c0657c04b1e4/python/results/catalog-breaking-ciliberto-full-controls-20261118/README.md)
now preserves all 74 original case records and 7,666 original branch records,
while marking the 200 unsaved potential controls explicitly. All 58 targeted
tests pass. A fresh download of the [input release](https://github.com/m9h/GRN_ODE/releases/tag/kinetics-ciliberto-full-controls-20261118)
reproduces complete input validation. The later control computations and
full-array case audit remain required.
The [complete later-control run](https://github.com/m9h/GRN_ODE/actions/runs/44412503884)
has passed Linux validation: all 6,859 remaining controls, including
the 200 generated continuations, are assigned to 256 fixed partitions for 27,436
requested trajectories. The [runner and independent branch audit](https://github.com/m9h/GRN_ODE/blob/05232fa83c4be917455dc2d143a11253cb7773e6/python/results/catalog-breaking-ciliberto-later-controls-20261118/README.md)
pass 96 targeted tests and the real input/runtime check. Original numerical code,
thresholds and case scoring are unchanged; whole-case recovery remains unproven.
The [later-control collector](https://github.com/m9h/GRN_ODE/blob/f34fcc07086734db2d1f193acaea6549784c7211/python/results/catalog-breaking-ciliberto-later-controls-20261118/COLLECTION.md) now verifies fixed job identities, original
ZIPs and saved arrays across all 256 partitions. Its 39 new checks and 117
combined targeted tests pass locally; Linux validation has passed. Interrupted
work and numerical failures remain explicit, and the full 74-case replay is
still required.
The [complete 74-case auditor](https://github.com/m9h/GRN_ODE/blob/9e9b96994278cc50713738c3b43618c5d1f4422c/python/results/catalog-breaking-ciliberto-full-case-audit-20261118/README.md) is now implemented and passes 137 targeted
tests. It rechecks original artifacts and arrays before replaying the unchanged
case mathematics across all 7,334 branches. Its real-data check verifies all
215 published branches and 860 trajectories and reproduces the two existing
case results exactly. With the new stages pending, it correctly keeps 7,119
branches outstanding and makes no new recovery claim.
Earlier audits pass all 216 Leloup cases, 728 Martins cases and 112 Hoefnagel
cases. The [De Caluwe clock](https://github.com/m9h/GRN_ODE/releases/tag/kinetics-decaluwe20-20261114)
passes all 484 cases and 18,579 branches. Downloadable evidence accompanies the
[Leloup, Ciliberto and Martins audits](https://github.com/m9h/GRN_ODE/releases/tag/kinetics-breaking-12-28-31-20261113)
and the [Hoefnagel](https://github.com/m9h/GRN_ODE/releases/tag/kinetics-hoefnagel-20261113)
and [Ueda audits](https://github.com/m9h/GRN_ODE/releases/tag/kinetics-ueda-20261113).
See the
[scope and status](docs/figure-guide.md#where-the-35-model-kinetics-project-fits).

No local numerical workers have been resumed. Ueda's
[cloud continuation](https://github.com/m9h/GRN_ODE/actions/runs/44393623529) has
finished all 32 fixed partitions. The [complete model accounting](docs/evidence/ueda-complete-model-20261121.json)
combines all 153 new branches with preserved evidence, verifying 323 branches,
1,292 full trajectories and 1,938 passing comparisons. The untreated baseline
passes, all four selected cases recover, and both conditional searches match
the original paths. A fresh audit of the published original evidence reproduces
the earlier 298/302 result; together the results validate **302/302 cases**.
No previously passing branch is flagged for revalidation. The
[complete evidence release](https://github.com/m9h/GRN_ODE/releases/tag/kinetics-ueda-complete-20261121)
now preserves all 32 original cloud ZIPs and the original 302-case archive.
All 35 release assets, including the manifest and checksum list, match their
[verified sizes and server checksums](docs/evidence/ueda-evidence-release-20261121.json).
The [offline reproduction guide](https://github.com/m9h/GRN_ODE/blob/70d57e0fe672485a9ae9274c7494fdecfaa21ad7/python/results/catalog-breaking-ueda-complete-20261121/REPRODUCE.md)
uses this release and the preserved inputs below. Recovery evidence contains
full arrays; the original 298 passes are reaudited from saved comparison
records and window summaries.
The [collection guide](https://github.com/m9h/GRN_ODE/blob/0c3c315dd34391abd4c38bfe93a358e78779451e/python/results/catalog-breaking-ueda-continuation-20261118/COLLECTION.md)
explains fixed job selection, artifact checks and the complete-case audit.
The [preserved evidence release](https://github.com/m9h/GRN_ODE/releases/tag/kinetics-ueda-preservation-20261118)
contains all 787 available snapshot files and the original diagnostic archive.
A fresh download verifies all 628 preserved arrays and reproduces the complete
preparation audit, import restoration proof and continuation plan byte for byte.
Its [uv reproduction guide](https://github.com/m9h/GRN_ODE/blob/07568199b113fee32f99d3feefed38e6d845b01c/python/results/catalog-breaking-ueda-continuation-20261118/RELEASE.md)
requires no new ODE integrations; the complete recovery above builds on these
preserved inputs.
The [current execution table](FORKS.md#current-execution) records the next Fuss
case-control continuations and Vilar precision checkpoints. Tyson's continuation
is running. The
four latest Vilar checkpoints are collected and verified: they add 373–409
samples each with every old sample preserved bit-for-bit, but no integration
has yet finished in those four partitions. François's full
Linux inventory is audited. The four earlier
local collection and audit watchers have finished. No local numerical worker
has been resumed.

The [latest Fuss audit](docs/evidence/fuss-checkpoint-audit-20261121.json)
checks all 31 available original ZIPs and 1,016 complete trajectories. All
760 parent trajectories remain unchanged, with 256 new ones; 234 complete
branches pass all 1,404 comparisons. Partition 11 lost its hosted runner's
connection and produced no artifact. Its older retained checkpoint has been
reaudited separately, preserving 34 trajectories. The
[two new continuation scopes](docs/evidence/fuss-continuations-20261121.json)
cover all 32 original partitions exactly once, using the appropriate verified
parent for each. Their validation gates are queued; actual computation job
IDs still need binding. No complete case or whole-model recovery is claimed.

The [new cloud collection record](docs/evidence/cloud-collection-20261119.json)
binds all 864 computation jobs across the Ueda, Ciliberto and Rohwer stages to
their original plans, attempts and source revisions. The [19 November array audits](docs/evidence/cloud-progress-20261119-evening.json)
verify 60 Ciliberto diagnostic branches (240 arrays), its first 81 later controls
(324 arrays), and ten Ueda continuation branches (40 arrays). All 906 pairwise
comparisons pass over the complete original grids. The remaining 200 Ciliberto
diagnostics and 6,778 later controls still require verification. The subsequent
[complete Ueda audit](docs/evidence/ueda-complete-model-20261121.json) now recovers
all four selected cases and adds one passing whole-model audit. Ciliberto's
[complete first diagnostic collection](docs/evidence/ciliberto-first-complete-20261121.json)
now verifies all 32 original archives and all 1,040 trajectories. Of 260 branches,
257 pass and three retain numerical mismatches; 1,553 of 1,560 pairwise
comparisons pass. The failures remain in the result. Later controls and the
full case replay are still required, so this adds no recovered Ciliberto case.

The [complete Fuss continuation checkpoint audit](docs/evidence/fuss-complete-checkpoint-20261119.json)
now verifies all 32 original ZIPs, totalling 6.61 GB, and 794 complete arrays.
All 528 parent arrays remain byte-identical, with 266 additional arrays. Its
180 complete branches pass all 1,080 comparisons. Every partition still needs
continuation; the [next complete continuation](https://github.com/m9h/GRN_ODE/actions/runs/44657363724)
has all [32 actual computation jobs bound to the fixed plan](docs/evidence/continuation-bindings-20261120.json)
and resumes from these verified parent checkpoints. The full 1,309-branch,
eighteen-case scope remains required.

Marhl now has an [exact mpmath checkpoint adapter](https://github.com/m9h/GRN_ODE/blob/8888e2bd03bba4f9010a288e9b355c2c7c2316c1/python/results/catalog-breaking-marhl-checkpoints-20261119/README.md)
for its long breaking protocols. It preserves internal precision across stops
and retains the original grids and resets for all 380 required trajectories.
All 122 targeted tests pass, including a clean checkout, and corrected Linux
validation has passed. The [full Marhl precision runner](https://github.com/m9h/GRN_ODE/blob/a09ed95826191b3b652a22e432b1e85212884e99/python/results/catalog-breaking-marhl-full-precision-20261119/README.md)
now fixes all 1,520 tasks: 380 original trajectories in two implementations at
128 and 192 bits. Its independent auditor checks every saved sample and all six
pairwise comparisons. Local validation passes 124 tests, with four
Heyoka-dependent checks initially reserved for Linux CI. The [published cloud
runner](https://github.com/m9h/GRN_ODE/blob/a3778b8cbb8bfdc16a9ddd4bbe84dd213fdf1022/python/results/catalog-breaking-marhl-full-precision-20261119/README.md)
adds authenticated checkpoint transfer, and its [full-precision Linux gate](https://github.com/m9h/GRN_ODE/actions/runs/44593959589)
now passes all 234 tests without skips. [All six original batches are submitted](docs/evidence/marhl-complete-execution-20261120.json),
covering the full 1,520 tasks. The [published collector and twelve-case auditor](https://github.com/m9h/GRN_ODE/blob/f95c155a968e15c30bdd39d6ac843f7b961c2930/python/results/catalog-breaking-marhl-full-precision-20261119/COLLECTION.md)
also pass all 47 Linux tests without skips. Full scientific computations,
artifact audits and case outcomes remain outstanding; implementation tests do
not count as full-precision scientific results. A separate inherited workflow reports source-fingerprint
errors when it applies older published-evidence checks to the new Taylor adapter;
that evidence must continue to use its original frozen source.

Rohwer's phosphotransferase model (network 35, BioModel 38) now has a fixed
[cloud diagnostic run](https://github.com/m9h/GRN_ODE/actions/runs/44401097371)
for all 750 originally failed breaking branches; Linux validation has passed.
Its [source audit and plan](https://github.com/m9h/GRN_ODE/blob/40fe82344d8dacb2d79ebdc4087ee52beb90a091/python/results/catalog-breaking-rohwer-diagnostics-20261118/README.md)
retain all 123 failed cases and their original protocols. The planned 3,000
trajectories use two Radau and two RoadRunner requests per branch. Complete
matched controls and conditional replay remain necessary before case recovery.
The [offline collection guide](https://github.com/m9h/GRN_ODE/blob/12c0693df1d68d1736b274a9364e1ef7b2533b06/python/results/catalog-breaking-rohwer-diagnostics-20261118/COLLECTION.md)
requires all 750 branches, rechecks downloaded arrays and preserves interrupted
work. All 78 combined local checks and Linux validation pass.
The [complete Rohwer input bundle](https://github.com/m9h/GRN_ODE/releases/tag/kinetics-rohwer-full-controls-20261118) now preserves all 123 failed cases
and 11,674 required branch specifications. This includes 848 potential controls
absent from the original saved paths, marked explicitly without invented results.
The [input adapter and guide](https://github.com/m9h/GRN_ODE/blob/c5be7556d38832a88e695a3559cedee2ab139521/python/results/catalog-breaking-rohwer-full-controls-20261118/README.md) pass 70 targeted tests; a fresh download
reproduces full validation. All 10,924 additional controls now have a
[fixed execution plan](https://github.com/m9h/GRN_ODE/blob/0dc31af29f4ff9c5e0e610d7c473cc1382fb7dda/python/results/catalog-breaking-rohwer-later-controls-20261118/README.md), including the untreated baseline and
all 848 generated controls. [Batch 0](https://github.com/m9h/GRN_ODE/actions/runs/44419997278)
and [batch 1](https://github.com/m9h/GRN_ODE/actions/runs/44420020715) have passed
Linux validation: 43,696 integrations across 512 fixed partitions.
All 118 targeted local tests pass, including 53 new tests; the released inputs
and actual numerical runtime validate. Saved arrays will be independently
audited. Full 123-case replay remains required, and whole-model coverage is unchanged.
The [two-batch collector](https://github.com/m9h/GRN_ODE/blob/b1643064668f559024c11acc84c196e06b7d2526/python/results/catalog-breaking-rohwer-later-controls-20261118/COLLECTION.md) is now implemented, with 173 targeted local
checks passing. It requires all 512 partitions, preserves original ZIPs and API
snapshots, rechecks full arrays, and retains failures and unfinished work.
The earlier queued-gate checks correctly prevented premature binding; Linux
collector validation has now passed, and all 512 computation jobs are bound.
The [complete Rohwer case auditor](https://github.com/m9h/GRN_ODE/blob/602c34a0db23b2a75ee5a1a9aefe6caf8524d992/python/results/catalog-breaking-rohwer-full-case-audit-20261118/README.md) is also implemented: it requires
all 11,674 branch outcomes before replaying all 123 cases through the unchanged
rules. All 235 targeted tests pass. The real input scope verifies, while an audit
with unavailable cloud evidence correctly leaves all branches pending and recovers
zero cases. Linux validation has also passed. Actual complete-case results
remain outstanding.

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
