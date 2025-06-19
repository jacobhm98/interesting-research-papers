# The illusion of thinking


## Summary

Shojaee et. al. wanted to test the notion that Large Reasoning Models were capable of complex, multi-step rational thought. 

They argue that lots of common benchmarks suffer from contamination issues, giving the example of LLM's scoring higher on the AIME24 benchmark than the AIME25 benchmark. Human performance showed the inverse, suggesting that AIME25 was actually less complex than AIME24.

In order to navigate this problem, they create an artificial puzzle environment. They take 4 simple to understand puzzles, the tower of hanoi, checkers jumping, river crossing, and blocks world.

A key criterion for puzzle selection was that the complexity level of the puzzles could be easily and measurably altered through the initial puzzle conditions. For example, the number of blocks could just be increased in tower of hanoi, etc...

They then tested reasoning models and their non-reasoning counterparts on the different puzzles across a scale of complexity in the different puzzles. They both measured how often the models achieved the right answer, how often they reasoned in the wrong direction, their token usage, and when they didn't reach the right answer.

## Results

The researchers were able to identify "3 regimes of complexity." In the first, corresponding to low complexity, thenon-thinking models actually outperformed the thinking models, in terms of token usage. In the second (moderate complexity), the thinking models vastly outperformed the non-thinking models, though once complexity got "high-enough"there was a catastrophic fall off in accuracy, and though quality.

This represented the border of the third region (higher complexity), where performance of both non-thinking and thinking models precipitously drops to zero. They also demonstrate that token usage falls in this region, where previously it had grown in proportion with problem complexity, almost like the model is "giving up".


## Interesting takeaways/random thoughts
- It'd be interesting to see how humans perform across these puzzles. Are the different levels of complexity all solvable by humans given enough time? How does average time to solution grow with problem size?
- The models were unable to solve the problems even when they had the solution algorithm in their context window. This demonstrates a fundamental lack of understanding.
- Have an LLM play chess and see what happens

## Novel ideas/topics
- pass@k, an evaluation of performance? It's described here [Evaluating Large Language Models Trained on Code](https://arxiv.org/abs/1906.04908)
