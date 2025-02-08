# The Axelrod Tournament

A competitive strategy simulation inspired by Robert Axelrod’s game theory experiments.

#### Disclaimer
> This project will try to be as original as possible.

> Evidently, the idea of a tournament of strategies is not new, but the implementation and the rules of this project are original.

> The project is inspired by the original Axelrod's tournament, but it is not a copy of it.

> Also, the Python implementation of the strategies is inspired by the [Axelrod Python library](https://github.com/Axelrod-Python/Axelrod), but it is not a copy of it and it will have a totally different implementation.

## Overview

This project have 4 parts to be developed:

1. A custom designer of Strategies based on strategies parametrization.
2. A React web application to play the tournament with your custom strategies.
3. A N-Prisoners Dilemma Tournament with the custom strategies.
4. A Partial Cooperative Mode to simulate strategies when the Payoff Matrix is continuous and not discrete.

## Strategies

#### What is a Strategy? (General Definition)

A strategy is a set of rules that defines the behavior of a player in a game. In this project, the game is the Prisoner's Dilemma, and the player is a strategy.

#### What is a Strategy? (Project Definition)

A set of numerical parameters that defines the behavior of a player in the Prisoner's Dilemma game. The parameters are the strategy's DNA and they are the only thing that defines the strategy.

#### What elements define a Strategy?

- **Moves**: 0 means Defect, 1 means Cooperate.
- **Partial Moves**: Values between 0 and 1 that defines the amount of cooperation in a continuous payoff matrix (Partial Cooperative Mode only).

The parameters that define a strategy are:

1. **Initial Moves**: A list of moves that the strategy will play in the first rounds of the game.
2. **Retaliation Threshold**: The number of defections that the opponent must do to trigger the retaliation of the strategy.
3. **Retaliation Memory**: The number of defections that the strategy will remember to trigger the retaliation.
4. **Retaliation Moves**: A list of moves that the strategy will play when the retaliation is triggered.
5. **Retaliation Level**: If Retaliation Moves is empty, the strategy will play the retaliation level of defections, meaning that the strategy will defect the same number of times that the Retaliation Level.
6. **Forgiveness Probability**: The probability of the strategy to forgive the opponent when the Retaliation Threshold is reached.
7. X
8. X
9. X
10. X
11. X
12. X
13. **Random Defect Probability**: The probability of the strategy to play a random defection when the moves are random.
14. **Random Moves Probability**: The probability of the strategy to play a random move.

#### What is the Rules Priority?

The rules priority is the order of the rules that the strategy will follow. The rules are:

1. Initial Moves, always be respected.
2. Random Moves, if it is not in the initial moves, then if the strategy is playing random move, it will play a random move.
3. Forgiveness, if the opponent has reached the Retaliation Threshold, but the strategy decides to forgive, it will forgive ignoring the retaliation.
4. Retaliation, if the opponent has reached the Retaliation Threshold, it will retaliate.
