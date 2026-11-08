# Project 3 · Logical paradoxes as dynamical systems

**Status: proposed.** This reading-group repository currently contains a project
brief, not a completed simulator. The primary reading is Gary Mar and Patrick
Grim, [Pattern and Chaos: New Images in the Semantics of Paradox](https://pgrim.org/articles/patternandchaos.pdf),
*Noûs* 25(5), 659–693 (1991).

## Begin with a map we can solve

Represent the liar sentence by a numerical truth-value revision rule:

$$x_{t+1}=1-x_t,\qquad x_t\in[0,1].$$

Its fixed-point equation is $x^*=1-x^*$, so $x^*=1/2$. Applying the map twice
gives $x_{t+2}=x_t$: every other initial value is a two-cycle. For example,
0.2 → 0.8 → 0.2. The fixed point is not attracting, since the distance from 0.5
is preserved. This baseline does not demonstrate chaos.

The variable is a value within the chosen mathematical semantics. Interpreting
it as a probability, a degree of belief or a third logical truth value would
require a further modeling choice.

## Proposed explorer

1. Display time series and a cobweb plot for the one-variable liar map.
2. Add coupled statements with an explicit mapping from each statement to its
   update equation. Compare simultaneous and sequential revision.
3. Add nonlinear examples from Mar and Grim, citing the precise equation and
   passage before claiming to reproduce a published figure.
4. Explore initial conditions and parameters, showing periodic behavior,
   candidate attractors and finite-time sensitivity estimates.
5. Export the equations, update order, precision, initial state and sampled
   trajectory with every result.

A small NumPy implementation is sufficient for the initial exact cases. JAX
would become useful for batches of initial conditions and sensitivity analysis;
the project does not require SBML or biochemical models.

## Checks and discussion

For the basic map, verify the exact fixed point, period-two identity and range
preservation. For more elaborate maps, compare numerical precision and longer
runs, and distinguish finite-time numerical diagnostics from mathematical proofs
of chaos. A complicated picture alone is insufficient evidence of sensitivity.

The learning objective is to connect self-reference to feedback, iteration and
dynamical behavior. Which properties follow from the selected semantics, and
which remain robust under reasonable changes to it?

[Back to the reading-group guide](../README.md)
