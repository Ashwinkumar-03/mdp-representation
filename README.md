# MDP REPRESENTATION

## AIM:
To model the Carrom game as a Markov Decision Process (MDP) to predict optimal actions for a player to maximize their score and increase their chances of winning.


## PROBLEM STATEMENT:
The objective is to develop an MDP framework for the game of Carrom, where each state represents the configuration of the Carrom board, and the actions correspond to the possible moves a player can make. The goal is to determine the optimal policy for a player that maximizes their cumulative score, considering the probabilistic nature of the game.

### Problem Description
Write your answer here

### State Space
The state space is the set of all possible configurations of the Carrom board. A state is defined by:

The positions of all Carrom men (Black, White, Queen) on the board.
The current player's turn.
Scores of both players.
The position of the striker.

### Sample State
{
  'black_positions': [(2,3), (4,5), ...],
  'white_positions': [(1,1), (3,4), ...],
  'queen_position': (2, 2),
  'striker_position': (0, 3),
  'player_turn': 1,
  'player1_score': 5,
  'player2_score': 3
}

### Action Space
The action space consists of all possible moves a player can make in their turn, including:

The angle and force with which the striker is hit.
The target Carrom man (Black, White, Queen).
The positioning of the striker on the base line.

### Sample Action
{
  'striker_angle': 45,        # Angle in degrees
  'striker_force': 0.8,       # Normalized force (0 to 1)
  'target_piece': 'black',    # Targeting a black piece
  'target_position': (3, 4)   # Targeted position on the board
}

### Reward Function
The reward function assigns points based on the outcome of the action:

Pocketing a Black: +10 points.
Pocketing a White: +20 points.
Pocketing the Queen: +50 points (only if covered).
Foul (e.g., pocketing the striker, pocketing the Queen without covering): -20 points.
No piece pocketed: 0 points

### Graphical Representation
Write your answer here

## PYTHON REPRESENTATION:
Write your code here

## OUTPUT:
Write your Python output here

## RESULT:
The simulated Carrom game ends with Player 1 winning, having a final score of 120 points compared to Player 2's 85 points. The MDP successfully modeled the game dynamics, allowing for a strategic evaluation of player actions leading to the game's outcome.
