# The illusion of the illusion of thinking

## Summary

This is a dispute of the previous paper, "The illusion of thinking: understanding the strenghts and limitations of reasoning models via the lens of problem complexity".

They make a few points:
- The authors of the previous paper generated a few mathematically unsolvable problem setups for the river crossing problem, and counted the models inability to solve them as errors
- Models recognize when they're approaching output limits: "The pattern coninues, but to avoid making this too long, I'll stop here".
- When the solution was changed from enumerating all moves in order required to solve the problem, to "Solve the Tower of Hanoi with 15 disks. Output a Lua functions that prints the solution when called." and similar, the models showed a very high accuracy across the problem sets.


## Thoughts

- Including mathematically unsolvable puzzles in the evaluation set is obviously not a good look
- Is most of the catastrophic drop off due to context length required when a huge number of moves becomes necessary to enumerate in order to arrive at the optimal solution? Can this be done as a multi step process? Initial prompt is give me first 100 moves, second prompt starts not with initial conditions but output state after first prompt, etc... until a solution is found.
- We all know models can program, how much more complicated is an algorithm that solves 6 blocks vs 3? Is there not a large risk of contamination here. Presumably there are programmatic solutions to the tower of hanoi available somewhere on the internet.
