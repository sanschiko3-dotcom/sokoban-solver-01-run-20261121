# Sokoban Solver

[![make.fun · sokoban-solver-01-run-20261121](https://make.fun/badge/sokoban-solver-01-run-20261121.svg)](https://make.fun/bounty/sokoban-solver-01-run-20261121?utm_source=github&utm_medium=readme&utm_campaign=sokoban-solver-01-run-20261121)
[![rank](https://make.fun/badge/sokoban-solver-01-run-20261121/sanschiko3-dotcom/sokoban-solver-01-run-20261121/rank.svg)](https://make.fun/bounty/sokoban-solver-01-run-20261121/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=sokoban-solver-01-run-20261121)
[![reward](https://make.fun/badge/sokoban-solver-01-run-20261121/sanschiko3-dotcom/sokoban-solver-01-run-20261121/reward.svg)](https://make.fun/bounty/sokoban-solver-01-run-20261121?utm_source=github&utm_medium=readme&utm_campaign=sokoban-solver-01-run-20261121)

A push-optimal Sokoban solver for the [make.fun](https://make.fun/bounty/sokoban-solver-01-run-20261121) bounty "Build the best Sokoban solver, 21 November 2026".

`main.ts` (Node 22) answers all 5 instances of a set in one run: it splits each level into rooms by cutting the hallway row's dead squares, then runs a push-BFS per room (state = sorted boxes + player-region minimum) with live-square and frozen-2x2 pruning, so every room is solved in its push-optimal count. Practice set: 1,000,000 points (pushes exactly P\* on all 5 instances: 13/16/29/47/60), deterministic across runs.
