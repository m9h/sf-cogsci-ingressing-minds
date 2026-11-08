# Readings and reference material

The first four readings introduce the paper and our three project tracks.
The remaining sources explain the computational tools, biological models and
possible extensions. [BibTeX entries](references.bib) use the keys shown below.
Forks and software revisions are catalogued separately in [FORKS.md](FORKS.md).

## Core reading

**Levin (2026) — Ingressing Minds: Causal, Non-Physical Patterns In-Form Natural,
Synthetic, and Hybrid Embodiments.** *Philosophies* 11(5), 161.
[Paper](https://www.mdpi.com/2409-9287/11/5/161)
· [DOI](https://doi.org/10.3390/philosophies11050161).
The organizing reading: a proposal about patterns, embodiment and diverse minds.
Use its concrete examples to identify which claims are observational,
mathematical or interpretive. BibTeX: `levin2026ingressing`.

**Zhang, Goldstein and Levin — Classical sorting algorithms as a model of
morphogenesis: Self-sorting arrays reveal unexpected competencies in a minimal
model of basal intelligence.** *Adaptive Behavior*, published online 2024.
[Journal paper](https://doi.org/10.1177/10597123241269740)
· [open preprint](https://arxiv.org/abs/2401.05375).
Source for distributed sorting, damaged elements and mixed sorting policies.
Our notebooks emphasize measurement definitions and experimental controls.
BibTeX: `zhang2024sorting`.

**Biswas, Clawson and Levin (2023) — Learning in Transcriptional Network Models:
Computational Discovery of Pathway-Level Memory and Effective Interventions.**
*International Journal of Molecular Sciences* 24(1), 285.
[Open article](https://pmc.ncbi.nlm.nih.gov/articles/PMC9820177/)
· [DOI](https://doi.org/10.3390/ijms24010285).
Source for the network-memory protocols. The volume is dated 2023; online
publication was 23 December 2022. Our fork reproduces selected demonstrations
with explicit controls and independent simulators. BibTeX: `biswas2023learning`.

**Mar and Grim (1991) — Pattern and Chaos: New Images in the Semantics of Paradox.**
*Noûs* 25(5), 659–693.
[Author-hosted PDF](https://pgrim.org/articles/patternandchaos.pdf)
· [JSTOR record](https://www.jstor.org/stable/2215637).
The foundation for the third project: infinite-valued semantics and iterated
maps for self-referential statements. BibTeX: `mar1991pattern`.

## Network computation and simulation tools

**Pietak and Levin (2025) — Harnessing the analog computing power of regulatory
networks with the Regulatory Network Machine.** *iScience* 28(6), 112536.
[Open article](https://pmc.ncbi.nlm.nih.gov/articles/PMC12210318/)
· [DOI](https://doi.org/10.1016/j.isci.2025.112536)
· [Cellnition software](https://github.com/betsee/cellnition).
A related framework for interpreting network state transitions as computation.
Our SBML memory replication does not yet reconstruct an RNM transition graph.
BibTeX: `pietak2025rnm`.

**Etcheverry, Levin, Moulin-Frier and Oudeyer (2023) — SBMLtoODEjax: Efficient
Simulation and Optimization of Biological Network Models in JAX.**
[Paper](https://arxiv.org/abs/2307.08452)
· [documentation](https://developmentalsystems.org/sbmltoodejax/)
· [FLOWERS exploration tutorial](https://developmentalsystems.org/curious-exploration-of-grn-competencies/tuto1.html).
Connects SBML models to JAX simulation, batching and optimization. Our fork
contributes an assignment-rule correction and independent validation cases.
BibTeX: `etcheverry2023sbmltoodejax`.

**van Lent, Bunkova, Magyar, Planken, Schmitz and Abeel (2025) — Jaxkineticmodel:
Neural ordinary differential equations inspired parameterization of kinetic
models.** *PLOS Computational Biology* 21(7), e1012733.
[Paper](https://doi.org/10.1371/journal.pcbi.1012733)
· [documentation](https://abeellab.github.io/jaxkineticmodel/).
A JAX/Diffrax modeling and parameter-fitting framework. Our fork updates its
JAX stack and validates imported models and intervention gradients.
BibTeX: `vanlent2025jaxkineticmodel`.

## Biology behind our five SBML files

**Kholodenko (2000) — Negative feedback and ultrasensitivity can bring about
oscillations in the mitogen-activated protein kinase cascades.**
*European Journal of Biochemistry* 267(6), 1583–1588.
[DOI](https://doi.org/10.1046/j.1432-1327.2000.01197.x)
· [BioModels-hosted paper](https://www.ebi.ac.uk/biomodels/courses/20150610/Kholodenko2000.pdf).
The source model for `BIOMD0000000010`: a three-stage signaling cascade with
feedback. BibTeX: `kholodenko2000feedback`.

**Markevich, Hoek and Kholodenko (2004) — Signaling switches and bistability
arising from multisite phosphorylation in protein kinase cascades.**
*Journal of Cell Biology* 164(3), 353–359.
[Paper](https://doi.org/10.1083/jcb.200308060).
The source family for models `BIOMD0000000026`, `0027`, `0029` and `0031`.
They differ in enzyme complexes, phosphorylation order and kinetic reductions;
see the [model-by-model guide](https://github.com/m9h/GRN_ODE/blob/python-memory-replication/python/models/README.md).
BibTeX: `markevich2004switches`.

## Guides and optional further exploration

**Ingressing Minds: a galaxy and a tour.**
[Website](https://ingressingminds.com/) · [tour](https://ingressingminds.com/tour/).
An independent visual guide supplied as a reading-group resource. It is a
secondary interpretation, and its affiliation statement is on its homepage.
BibTeX: `ingressingmindstour`.

**Mordvintsev, Randazzo, Niklasson and Levin (2020) — Growing Neural Cellular
Automata.** *Distill*.
[Interactive paper](https://distill.pub/2020/growing-ca/)
· [notebook](https://colab.research.google.com/github/google-research/self-organising-systems/blob/master/notebooks/growing_ca.ipynb).
An optional extension about growth, persistence and repair through local learned
rules. It is additional reading; it is not the third project in our sequence.
BibTeX: `mordvintsev2020growing`.
