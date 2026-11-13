# The figures and the argument

This guide covers **all 15 figures** in Michael Levin's
[*Ingressing Minds* (2026)](https://doi.org/10.3390/philosophies11050161).
Page numbers refer to the published, 53-page PDF, dated 9 September 2026.
The descriptions were checked against the images, captions and surrounding text.
“Role in the argument” explains Levin's use of a figure; “Discussion” gives our
reading-group assessment, rather than an additional claim made by the figure.

**Figures 8 and 14 directly anchor two of our current computational projects.**
Our biochemical-memory project follows studies cited in the text, principally
reference 212, rather than a dedicated kinetics-results figure in this paper.
Figure 10C includes network learning in its conceptual spectrum, and Figures 4
and 13 provide biological and conceptual connections. Figures 5 and 6 are also
computational examples, with concrete extensions proposed below; we have not
implemented those extensions.

## How the sequence builds the argument

| Figure | PDF page | Main contribution | Connection to our work |
|---|---:|---|---|
| [1. Development and collective organization](#figure-1-development-and-collective-organization) | 6 | Introduces continuity between cellular organization and embodied minds. | Background for collective behavior. |
| [2. Patterns across biological spaces](#figure-2-patterns-across-biological-spaces) | 9 | Places anatomy, gene expression and behavior in a common language of patterns and state spaces. | Background for all three tracks. |
| [3. Morphogenesis as problem-solving](#figure-3-morphogenesis-as-problem-solving) | 11 | Uses recovery and remodeling to motivate goal-directed descriptions. | Motivation for the sorting damage assays. |
| [4. Rewritable anatomical memory](#figure-4-rewritable-anatomical-memory) | 13 | Shows persistent changes in regenerative outcomes following bioelectric intervention. | Biological analogy for state-based memory; different mechanism from our SBML models. |
| [5. Feigenbaum scaling](#figure-5-feigenbaum-scaling) | 15 | Introduces precise mathematical structure that does not require biological selection. | Proposed bifurcation and universality lab. |
| [6. Fractals and biomorphs](#figure-6-fractals-and-biomorphs) | 16 | Illustrates intricate forms accessible through short mathematical rules. | Proposed Halley and Julia-set labs. |
| [7. Unexpected biological competencies](#figure-7-unexpected-biological-competencies) | 18 | Motivates searching beyond an organism's usual forms and uses. | Context for perturbation experiments. |
| [8. Logical sentences with dynamics](#figure-8-logical-sentences-with-dynamics) | 19 | Extends the proposed space of patterns from static truths to time-dependent behavior. | **Direct: paradox dynamics.** |
| [9. Morphological transformations](#figure-9-morphological-transformations) | 21 | Suggests mathematical relationships among biological forms. | Possible future morphometrics exercise. |
| [10. The proposed ontology](#figure-10-the-proposed-ontology) | 23–24 | States the interface model and spectrum from mathematical forms to minds. | Conceptual connection among all three tracks, including network learning. |
| [11. Synthetic living constructs](#figure-11-synthetic-living-constructs) | 25 | Makes novel embodiments into experimental probes of possible forms and behaviors. | Biological motivation; no biobot replication in our repositories. |
| [12. Possible embodiments](#figure-12-possible-embodiments) | 27 | Extends the framework to engineered and hybrid systems. | Motivation for including computational systems. |
| [13. Scales of agency and intervention](#figure-13-scales-of-agency-and-intervention) | 28 | Organizes competencies by goal scale and how a system can be influenced. | Framework for sorting and network assays. |
| [14. Sorting competencies](#figure-14-sorting-competencies) | 30 | Offers minimal algorithmic examples of apparent detours and incidental clustering. | **Direct: self-sorting arrays.** |
| [15. Objects, patterns and models](#figure-15-objects-patterns-and-models) | 32 | Motivates treating patterns as possible agents and distinguishing models from their referents. | Interpretive question for every simulation. |

The progression is from biological observations (1–4), through mathematical
examples and unexpected capacities (5–9), to the proposed framework and research
program (10–13), a minimal algorithmic case (14), and a final change of perspective
(15). These figures perform different jobs: an experimental illustration, a
mathematical construction and an ontology diagram are different kinds of support.

## Figure 1: Development and collective organization

**What it shows.** Organisms developing from single cells; nested cellular and
molecular organization; and an illustration of how partitioning an embryonic
cell sheet can produce multiple organizing centers and embryos.

**Role in the argument.** Section 2.1 begins with developmental continuity.
Levin uses the figure to challenge a sharp division between chemical matter and
mind, and to present individual intelligence as an achievement of interacting
parts. The partitioning example also makes individuality something development
establishes, rather than a fixed property of the starting material.

**Discussion and project connection.** This motivates studying collective sorting
and molecular networks. The developmental examples do not themselves measure
consciousness in each component or establish how many minds a tissue contains.
Ask which observable capacities would justify attributing agency at a given scale.

## Figure 2: Patterns across biological spaces

**What it shows.** Anatomy, a spider web, floral organization, animal symmetries,
a landscape of planarian head shapes, gene-expression states, anatomical
coordinates and movement trajectories.

**Role in the argument.** Section 3 expands “pattern” beyond a visible shape.
Development, physiology and behavior can all be described through configurations,
trajectories and possible alternatives. This prepares Levin's later proposal that
one account of patterns could connect the origins of bodies and minds.

**Discussion and project connection.** Our projects make three such spaces
explicit: permutations of an array, molecular concentrations, and truth-value
vectors. Sharing a state-space description does not establish a shared mechanism
or ontology. Ask what the coordinates and distance measure mean in each case.

## Figure 3: Morphogenesis as problem-solving

**What it shows.** Whole embryos following splitting, limb regeneration,
remodeling of a grafted tail toward a limb, voluntary action, and kidney tubules
that preserve their organization with fewer, larger cells, including a single
cell wrapped around a lumen.

**Role in the argument.** Section 3.1 argues that some biological patterns are
targets maintained despite perturbations. Different starting conditions and
different cellular means can lead to a similar anatomical outcome. The figure
introduces the comparison between reaching anatomical targets and reaching
behavioral goals.

**Discussion and project connection.** This is the biological motivation for
testing damaged sorting arrays. Establish recovery relative to an explicit
target, then investigate the mechanism. Successful compensation supports a
functional control description without by itself settling the origin of the
target or implying conscious planning.

## Figure 4: Rewritable anatomical memory

**What it shows.** Control and bioelectrically altered planarians can initially
have similar anatomy and marker expression but different voltage patterns.
After cutting, their fragments regenerate differently. Further panels show
repeated two-headed regeneration and induced head shapes resembling other species.

**Role in the argument.** Section 3.2 makes the proposed target state experimentally
addressable: transient physiological interventions can change later anatomical
outcomes without changing the genome. Levin interprets this as a writable
pattern memory that guides regeneration, and then asks where the available
target patterns come from.

**Discussion and project connection.** This is a strong conceptual connection to
our memory assays, but those assays model MAPK concentrations, not planarian
voltage networks or anatomy. Persistence through the reported experiments is
evidence of durable memory; an indefinitely continuing sequence is an inference.
Bioelectric storage is also a physical mechanism, so its discovery alone does
not establish a nonphysical source for the stored pattern.

## Figure 5: Feigenbaum scaling

**What it shows.** A period-doubling bifurcation diagram, with shrinking parameter
intervals whose successive ratios approach approximately 4.6692.

**Role in the argument.** Section 4.1 moves from biological history to mathematical
structure. Levin uses the specificity of such constants to argue that physical
systems can inherit constraints and opportunities that evolution did not invent.
This is an early foundation for his account of mathematical patterns influencing
their embodiments.

**Discussion and project connection.** A bifurcation and universality lab would
extend our existing iterated-map work. It should distinguish finite numerical
estimates from a mathematical limit, and identify the class of maps for which
the scaling applies. The existence of mathematical regularities is one issue;
their interpretation as a separately existing causal domain is another.
See the [specific proposed experiment](#extension-a-measure-universality-figure-5).

## Figure 6: Fractals and biomorphs

**What it shows.** A Halley-method fractal associated with a short complex
function, alongside organism-like forms generated from complex-number rules.
The caption gives a polynomial such as `z^3 + 7`; it is not a complete rendering
specification. Panels B–D are drawn from Levin's earlier Julia-set modeling work
(paper reference 96).

**Role in the argument.** The move is from a special number to intricate spatial
form. Levin presents a short formula as a pointer into a rich space of shapes,
and uses this as an analogy for a biological seed accessing a larger pattern.

**Discussion and project connection.** This supports two proposed extensions:
[Halley root basins](#extension-b-map-root-finding-basins-figure-6a) and
[Julia-set morphogenesis](#extension-c-explore-julia-set-morphogenesis-figure-6bd).
Iteration, stopping conditions and rendering choices must be recorded. Visual
resemblance to an organism does not establish biological function; a concise
generative rule also does not by itself decide between a “pointer” interpretation
and an ordinary mathematical description of its consequences.

## Figure 7: Unexpected biological competencies

**What it shows.** Oak leaves and parasite-induced galls, followed by tadpoles
with ectopic eyes and associated nerve projections. The caption connects the
eye manipulation to visual-assay performance from the cited study.

**Role in the argument.** Section 4.2 asks what else a biological system can do
beyond its usual development and use. Levin treats novel shapes and functional
integration as reasons to explore a structured space of capacities rather than
assuming the familiar phenotype exhausts what the system can express.

**Discussion and project connection.** The shared method is perturbing a system
to discover latent capabilities. However, the tissues, nervous systems and
parasites have evolutionary histories. Novel deployment is not the absence of
all evolved machinery. Our assays likewise need to identify which capabilities
were supplied by the model and which emerge under the new conditions.

## Figure 8: Logical sentences with dynamics

**What it shows.** A liar-sentence trajectory and cobweb plot; coupled fuzzy
sentence trajectories, state-space plots and escape-time images; and a fractal
image reproduced from Mar and Grim (1991), paper reference 231. Panels A–C are
screenshots of software made by Madelyn Silveira in Levin's lab.

**Role in the argument.** Section 4.3 is a pivotal step: mathematical or logical
patterns can specify dynamic activity, rather than only static facts. Levin
then proposes a continuum extending through repetitive dynamics to learning
and more agentic patterns. The figure supplies the dynamic part of that bridge.

**Discussion and project connection.** Our
[paradox project](https://github.com/m9h/paradox-dynamics) directly implements
selected Mar–Grim revision maps, with explicit arithmetic and update schedules.
It does not reproduce all panels or their complete fractal analysis. Turning a
sentence into a time-dependent fuzzy update is a choice of semantics; the
resulting oscillation or fractal does not alone establish intelligence or resolve
the original logical paradox. See our [project guide](paradox-project.md).

## Figure 9: Morphological transformations

**What it shows.** D'Arcy Thompson's examples of changing coordinate grids so
that one animal outline resembles another.

**Role in the argument.** Section 5.2 uses relationships among forms to suggest
that biological morphospace has discoverable structure. This contributes to the
claim that the possible forms are related systematically, rather than forming
an arbitrary collection of unrelated outcomes.

**Discussion and project connection.** A future landmark-and-grid-deformation
exercise could quantify the transformations and their errors. A successful
geometrical correspondence does not establish that development uses that grid,
that one species transforms into another, or that the proposed space has a
particular metric. None of our three current projects reproduces this figure.

## Figure 10: The proposed ontology

**What it shows.** Physical systems connected to patterns; embodiments pictured
as means of exploring a wider domain; and a spectrum from fixed mathematical
forms through dynamics and learning to more elaborate minds. The caption
continues onto PDF page 24.

**Role in the argument.** Section 5.3 states the central hypothesis explicitly:
bodies and machines act as interfaces to patterns with differing degrees of
agency. Panel C connects the earlier mathematical examples to network learning
and human cognition. This is the diagram that most directly summarizes what
Levin wants the preceding examples to motivate.

**Discussion and project connection.** All three projects address parts of the
proposed spectrum. The learning illustration is a conceptual connection to our
kinetics project, not a plotted kinetics experiment to replicate. The layout is
a hypothesis, not a measured map of a nonphysical space. Ask what new predictions
it supplies and which experiment could distinguish competing interpretations.

## Figure 11: Synthetic living constructs

**What it shows.** Anthrobots made from human tracheal cells; a neuronal scratch
assay with bridging across a gap; frog development contrasted with Xenobot
development; and successive generations of kinematic replication using supplied
loose cells.

**Role in the argument.** Section 5.4 proposes constructing novel embodiments
as an experimental way to explore possible forms and capacities. These examples
motivate asking how familiar cellular material behaves in arrangements without
a history of selection as that particular construct.

**Discussion and project connection.** These are biological experiments, not
simulations in our repositories. The distinction between a new arrangement and
its evolved cellular components remains important. Scratch-assay repair and
replication under supplied laboratory conditions should retain those conditions
when described. The figure motivates our search for capacities but is not
evidence that our computational systems possess those biological functions.

## Figure 12: Possible embodiments

**What it shows.** A conceptual assortment of organisms, machines, software,
cyborgs and hybrid constructions, assembled from several kinds of constituents.
Ingressing patterns appear as one proposed contributor.

**Role in the argument.** Sections 6 and 6.1 extend the account beyond familiar
life. If embodiment of mental patterns is the relevant relation, Levin argues,
evolutionary origin or a particular material should not define the boundary of
possible minds. This motivates both experimental inclusion and ethical attention.

**Discussion and project connection.** This supports considering minimal
computational systems as candidates for investigation. It is a diagram of
possibilities, not evidence that every depicted combination exists or has a
mind. The inclusion of an “ingressing patterns” component expresses the thesis
being argued for; it is not an independent measurement of that component.

## Figure 13: Scales of agency and intervention

**What it shows.** Individual and collective ranges of memory, anticipation and
spatial concern; nested scales within organisms; a classification of behavior;
and intervention modes ranging from hardware changes to setpoint changes,
training and communication.

**Role in the argument.** Section 6.1 offers a vocabulary for degrees and kinds
of agency. The “cognitive light cone” expresses the scale of a system's goals,
memory and anticipation. The intervention spectrum encourages testing which
ways of influencing a system actually work.

**Discussion and project connection.** This is a conceptual basis for our damage,
stimulation and recall assays. These are cognitive scales, not literal
relativistic light cones. Placing a model on the proposed spectrum requires
evidence: response to a parameter change, persistence of state and successful
conditioning are distinct observations. Our software does not compute a general
agency score from this figure.

## Figure 14: Sorting competencies

**What it shows.** An analogy between obstacles and goal-directed detours;
a sorting trace with temporary decreases in the selected sortedness metric;
and transient clustering of cells carrying different sorting policies while
the array progresses toward sorted order. Panels B–C come from the sorting
study, paper reference 232.

**Role in the argument.** Section 6.3 brings the claim into a minimal algorithmic
setting. Levin interprets the detours as delayed gratification and the clustering
as a competence not explicitly specified as a sorting objective. This challenges
the idea that unexpected competencies are exclusive to complex living systems.

**Discussion and project connection.** Our
[sorting fork](https://github.com/m9h/cell_research) directly investigates these
themes with repaired code and explicit controls. Its metrics and experimental
conditions differ from the published figures. Our progress example shows how
one metric can worsen while another improves; our clustering pilot gives mixed
evidence across controls. A behavior absent from an explicit objective may
still follow from the update rules. See the
[methods](https://github.com/m9h/cell_research/blob/main/docs/methods.md) and
[clustering notebook](https://github.com/m9h/cell_research/blob/main/examples/03_clustering.ipynb).

## Figure 15: Objects, patterns and models

**What it shows.** A thought experiment in which hypothetical dense creatures
perceive humans as tenuous activity patterns, and a Magritte-inspired image
distinguishing a Turing-machine representation from the thing represented.

**Role in the argument.** Section 6.4 asks whether a persisting pattern can itself
be treated as the agent, with its material medium providing an embodiment.
It also stresses the limits of formal descriptions and motivates humility about
what an engineered system might be.

**Discussion and project connection.** This is a thought experiment and a
philosophical analogy. It does not demonstrate an additional causal input to
a computer or establish that a simulation is conscious. For every project,
distinguish the mathematical model, its implemented numerical process and the
biological or philosophical interpretation assigned to it.

## Where the 35-model kinetics project fits

Network memory enters the argument in Section 4.2 (p. 16), immediately after
Figure 8 in Section 4.3 (pp. 19–20), and again in Sections 5.3 (p. 22), 5.5
(p. 26), 6.1 (p. 27), and the research agenda on p. 36. References **212 and
213** supply the underlying studies; the text links experience-dependent
network behavior to the proposed spectrum of patterns.

Our current implementation follows selected protocols from
[Biswas, Clawson and Levin's ODE study](https://pmc.ncbi.nlm.nih.gov/articles/PMC9820177/)
(reference 212). Its own figures and supplemental model inventory, rather than
Figures 4 or 10 of *Ingressing Minds*, are the sources for extending the
[kinetics workflow](https://github.com/m9h/GRN_ODE/tree/python-memory-replication/python).
The five models in our existing memory experiments are MAPK protein-signaling
models; four are variants from the Markevich family.

**Active goal, set 8 November 2026:** complete reproducible kinetics and memory
computations for all 35 BioModels in that study, with independent numerical
validation and documented deviations. **Completed milestone:** baseline kinetics
for all 35 pass independent comparisons over 50 native time units, with 5,001
samples per model and 380 observables across the catalog. RoadRunner and COPASI
agree for 34 models; the remaining model requires a genuine delay equation,
checked with a method-of-steps solver and JiTCDDE, including step refinement.
The [catalog guide](https://github.com/m9h/GRN_ODE/blob/python-memory-replication/python/CATALOG_VALIDATION.md)
documents model biology, source files, tolerances and the delay-history assumption.

A second milestone now covers [single-input retention across all 35 models](https://github.com/m9h/GRN_ODE/blob/python-memory-replication/python/CATALOG_MEMORY.md):
538 up/down stimulation cases pass independent numerical comparisons, preserving
native events, rule variables and delay history. Time-matched controls separate
retained treatment effects from untreated drift; below-resolution labels remain
unresolved. These operational results do not by themselves identify a memory
mechanism or demonstrate associative learning.

The [JAX catalog audit](https://github.com/m9h/GRN_ODE/blob/python-memory-replication/python/CATALOG_JAX.md)
validates 32 original baselines against both reference engines; event, rate-rule
and delay models are explicit unsupported imports. This is baseline coverage,
not JAX memory-protocol validation across the entire catalog.

The [repeated-stimulation screen](https://github.com/m9h/GRN_ODE/blob/4108edeca8b2d6d5e454167454a8826319ff6046/python/CATALOG_REPEATED.md)
now also passes all 538 cases across all 35 models on macOS and Linux, with same-time isolated-pulse
controls and agreement on every controlled pulse classification. Raw MATLAB
labels and negative or unresolved responses remain separately visible.

The [paired-learning screen](https://github.com/m9h/GRN_ODE/blob/4108edeca8b2d6d5e454167454a8826319ff6046/python/CATALOG_PAIRED.md)
has evaluated all 4,208 ordered input pairs and 22,578 distinct branches,
comparing four training histories with shams and ordinary/delayed cues.
**The original run records 4,166 passes and 42 failures.** All original
results and the complete coverage audit are published; failed integrations
and trajectory mismatches remain explicit. A separate
[complete François recovery](https://github.com/m9h/GRN_ODE/blob/650c3f71b76a0446552d6b7e84944e2602536950/python/results/catalog-paired-francois-full-recovery/audit.json)
now passes all 44 cases and 275 branches for that model. Subsequent Vilar and
[complete Rohwer recovery](https://github.com/m9h/GRN_ODE/blob/e5ff9bb131b3a815feb584793b9f68dda53ce7a7/python/results/catalog-paired-scipy-rohwer-cases/audit.json)
bring combined validation to **4,203/4,208 cases, with 33 fully passing models**;
two Marhl and three Vilar cases remain unresolved. Original results stay separate
from these later recoveries.

The [three-trial breaking screen](https://github.com/m9h/GRN_ODE/blob/058df6fe0f9d96874f604618afddcf64fde90bf8/python/CATALOG_BREAKING.md)
uses eight control arms and records explicit differences between the MATLAB
code and the paper's prose. Published terminal reports now cover 23 distinct
models; 19 have passing full numerical validation after separate recoveries.
Network 1, the Edelstein acetylcholine-receptor model, passes all 528 initial
cases and 9,452 conditional trials.
Network 34, the Marwan regulatory-hierarchy model, passes all 360 initial cases
and 3,254 conditional trials. Of its 6,509 response-trials, 6,397 have no
resolved history effect at rechallenge and 21 meet the controlled
half-restoration criterion. Successful integration does not imply that each
intervention demonstrates memory. The conditional trials reuse species and
histories, so they are not independent samples of a population.

Twelve searches remain unfinished. The newly completed Fuss and Leloup
searches retain numerical mismatches, so finished coverage does not imply
full validation. Complete Ciliberto branch arrays and the new recorded evidence
are available in the [validation release](https://github.com/m9h/GRN_ODE/releases/tag/kinetics-validation-20261112).
Complete validated protocol coverage is needed before comparing
the study's population frequencies. The original random-network comparisons
are a further part of the evidence concerning capacities without specific
selection.

## Concrete extensions for Figures 5 and 6

These are proposed projects, separate from the active 35-model kinetics goal.
They could form a short mathematical-patterns lab before the three existing
tracks. Their purpose would be to reproduce constructions and test sensitivity
to modeling choices; neither a numerical constant nor an organism-like image
alone establishes the paper's ontology.

### Extension A: Measure universality (Figure 5)

Use the logistic family $x_{t+1}=r x_t(1-x_t)$ on $[0,1]$. Plot its long-run
states while sweeping $r$, then locate successive period-doubling parameters
$r_n$ and calculate

$$\delta_n=\frac{r_n-r_{n-1}}{r_{n+1}-r_n}.$$

Compare with the sine family $x_{t+1}=a\sin(\pi x_t)$. The scientifically useful
result is convergence toward the same scaling constant for these families,
not just similar-looking plots. Keep numerical precision, transient length and
bifurcation-location error explicit; do not infer bifurcations solely by counting
rounded trajectory values. Universality has hypotheses, including the relevant
behavior near the map's maximum. A finite experiment estimates the limit.

**Deliverables:** two bifurcation diagrams, a parameter-and-ratio table with
precision checks, and a discussion of what is common across the maps.
**Source:** [Feigenbaum's original analysis](https://sites.math.rutgers.edu/~zeilberg/Bio21/MF78.pdf)
([DOI](https://doi.org/10.1007/BF01020332)); BibTeX `feigenbaum1978universality`.

### Extension B: Map root-finding basins (Figure 6A)

For an explicitly chosen example $f(z)=z^3+7$, apply Halley's iteration to a
grid of complex initial values:

$$z_{t+1}=z_t-\frac{2f(z_t)f'(z_t)}{2[f'(z_t)]^2-f(z_t)f''(z_t)}.$$

Color each initial value by the root reached and the number of iterations.
Record singular denominators and failure to converge instead of assigning them
a root. Compare Newton's method on the same polynomial, and vary coefficients
to explore nearby patterns. Use root residuals and small-grid reference
calculations to check the rendering.

**Deliverables:** basin images, convergence statistics, parameter sweeps and a
record of all display settings. This is a controlled example inspired by the
caption, not a promised pixel-for-pixel reconstruction: the caption alone does
not specify the original viewport, tolerances or coloring. The question is how
much of the observed structure follows from the polynomial, iteration and
rendering choices.

### Extension C: Explore Julia-set morphogenesis (Figure 6B–D)

Return to [Levin's 1994 model](https://doi.org/10.1093/bioinformatics/10.2.85),
which interprets positional information through coupled variables represented
with complex-number algebra. Reproduce selected published forms using the
reported formulas and parameters, then vary those parameters and implement
selected developmental perturbations. Preserve intermediate states so that
changes can be examined as a sequence rather than only as final pictures.

**Deliverables:** a source-to-equation concordance, reproduced examples,
developmental sequences and a comparison of parameter or perturbation effects.
This offers a closer connection to morphogenesis than an arbitrary fractal
gallery. The source explicitly presents a conceptual model rather than a
simulation of a particular organism. BibTeX `levin1994juliaset`.

[Pickover's biomorph paper](https://doi.org/10.1111/j.1467-8659.1986.tb00317.x)
is complementary background (reference 204 in *Ingressing Minds*), not a
substitute for the formulas behind panels B–D. We use the journal's publication
year, 1986; reference 204 in *Ingressing Minds* lists 2007.
BibTeX `pickover1986biomorphs`.

## Using the guide in discussion

Choose a figure and identify (1) the observation or construction, (2) the
mechanistic or mathematical explanation, and (3) the additional claim about
agency or ontology. State which step a proposed computation would test. Use the
[discussion template](discussion-guide.md#recording-a-discussion) to record the
result and an alternative explanation.

This guide contains original commentary and links to the source figures rather
than reproducing their images. The article is CC BY 4.0; several figure panels
carry separate third-party credits or permission notices in their captions.
Those credits should be checked before redistributing images. Our commentary
uses the repository's [MIT license](../LICENSE).
