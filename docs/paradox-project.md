# Project 3 · Logical paradoxes as dynamical systems

**Status: implemented.** Start with [Paradox dynamics](https://github.com/m9h/paradox-dynamics),
our original MIT-licensed implementation, and its
[executed notebook](https://github.com/m9h/paradox-dynamics/blob/main/examples/paradox_lab.ipynb).
The primary reading is Gary Mar and Patrick
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

## Working explorer

1. Follow the Liar time series and cobweb by hand.
2. Compare two maps with the same fixed point `2/3`, one attracting and one repelling.
3. Compare exact rational, float32 and float64 tent-map trajectories.
4. Change the order in which two mutually referring statements are revised.
5. Inspect the Curry variation and its equation/prose discrepancy at the parameter boundary.

The project provides nine maps, 24 recorded runs, seven figures and 81 passing
tests. A notebook widget lets readers change the settings using the same Python
implementation as the CLI. No SBML or JAX installation is needed.

Every exported result includes the equations, input values, parameters,
arithmetic, schedule, complete trajectory, code hashes and diagnostic scope.
[Mathematical guide](https://github.com/m9h/paradox-dynamics/blob/main/docs/mathematics.md)
· [results](https://github.com/m9h/paradox-dynamics/blob/main/docs/results.md)
· [validation](https://github.com/m9h/paradox-dynamics/blob/main/docs/validation.md).

## Checks and discussion

The exact tent-map input `0.314` enters a 50-cycle, while float32 and float64
representations eventually reach zero. A positive derivative-based expansion
rate also occurs at the map's exact fixed point. These examples distinguish a
model's mathematics, a selected orbit and the computer's representation.

The learning objective is to connect self-reference to feedback, iteration and
dynamical behavior. Which properties follow from the selected semantics, and
which remain robust under reasonable changes to it?

[Back to the reading-group guide](../README.md)
