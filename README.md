# Training_Agent_For_Go_Game

## Overview
In this program, I Have develop AI agents based on alpha beta pruning and mini max Algorithm.To play a small version of the Go game, called Go-5x5 or Little-Go, that has a reduced board size of 5x5. Your agent will play this Little-Go game against some basic as well as more advanced AI agents. 

## Game Description

Go is an abstract strategy board game for two players, in which the aim is to surround more territory
than the opponent. The basic concepts of Go (Little-Go) are very simple:
- Players: Go is played by two players, called Black and White.
- Board: The Go board is a grid of horizontal and vertical lines. The standard size of the board is
19x19, but in this homework, the board size will be 5x5.
- Point: The lines of the board have intersections wherever they cross or touch each other. Each
intersection is called a point. Intersections at the four corners and the edges of the board are
also called points. Go is played on the points of the board, not on the squares.
- Stones: Black uses black stones. White uses white stones.
The basic process of playing the Go (Little-Go) game is also very simple:
- It starts with an empty board,
- Two players take turns placing stones on the board, one stone at a time,
- The players may choose any unoccupied point to play on (except for those forbidden by the “KO”
and “no-suicide” rules).
- Once played, a stone can never be moved and can be taken off the board only if it is captured.

## Rule1: The Liberty Rule
Every stone remaining on the board must have at least one open point, called a liberty, directly
orthogonally adjacent (up, down, left, or right), or must be part of a connected group that has at least
one such open point (liberty) next to it. Stones or groups of stones which lose their last liberty are
removed from the board (called captured).
Based on the rule of liberty, players are NOT allowed to play any “suicide” moves. That is, a player
cannot place a stone such that the played stone or its connected group has no liberties, unless doing so
immediately deprives an enemy group of its final liberty. In the latter case, the enemy group is captured,
leaving the new stone with at least one liberty.

## Rule 2: The “KO” Rule
For the position shown on the left board above, Black can capture the stone by a play at position a.
The resulting position is shown on the right board above. Without a KO rule, in this position White could
recapture the stone at position b, reverting to the position shown on the left, and then Black could
also recapture. If neither player gave way, then we would have Black a, White b, Black a, White b, ...,
repeated ad infinitum, stalling the progress of the game. This situation is known as KO.
The KO rule resolves the situation: If one player captures the KO, the opponent is prohibited from
recapturing the KO immediately.

## Komi
Because Black has the advantage of playing the first move, awarding White some compensation is called
Komi. This is in the form of giving White a compensation of score at the end of the game. In this
homework (a board size of 5x5), Komi for the White player is set to be 5/2 = 2.5.

## Passing
A player may waive his/her right to make a move, called passing, when determining that the game offers
no further opportunities for profitable play. A player may pass his/her turn at any time. Usually, passing
is beneficial only at the end of the game, when further moves would be useless or maybe even harmful
to a player's position.
