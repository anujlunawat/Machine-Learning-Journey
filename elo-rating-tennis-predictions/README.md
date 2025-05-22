# Elo Rating Tennis Predictions

This project implements the **Elo rating system** to predict the outcome of tennis matches based on historical data. Inspired by Brad Klassen's Elo model for tennis, this repository contains a simplified and customized version as part of my machine learning journey.

## Overview

The Elo rating system is widely used for ranking players in competitive sports and games. This project uses Elo ratings to:
- Track player performance over time
- Estimate win probabilities between players
- Predict outcomes of future matches

This is a **rule-based model** (not machine learning), where player ratings are updated based on match results.


## Elo System Explained

Each player starts with a default Elo score. After every match:
- The winner's Elo increases
- The loser's Elo decreases
- The amount of change depends on the difference between expected and actual outcomes


## Probability Formula:
<h4>Probability that Player A wins against Player B:</h4>
<p>
  P(A) = 1 / (1 + 10<sup>((R<sub>B</sub> - R<sub>A</sub>) / 400)</sup>)
</p>
<p>where:</p>
<ul>
  <li><strong>R<sub>A</sub></strong> = Elo rating of Player A</li>
  <li><strong>R<sub>B</sub></strong> = Elo rating of Player B</li>
</ul>

<h4>Elo rating update formula for Player A:</h4>
<p>
  R<sub>A</sub>' = R<sub>A</sub> + K × (S<sub>A</sub> - P(A))
</p>
<p>where:</p>
<ul>
  <li><strong>R<sub>A</sub>'</strong> = New Elo rating of Player A</li>
  <li><strong>K</strong> = K-factor (controls rating sensitivity)</li>
  <li><strong>S<sub>A</sub></strong> = Actual score for Player A (1 if A wins, 0 if A loses)</li>
  <li><strong>P(A)</strong> = Expected probability of Player A winning (from formula above)</li>
</ul>




## Project Workflow

1. Load tennis match data
2. Initialize Elo scores for all players
3. Train Elo ratings using historical match results
4. Predict future match outcomes using current Elo ratings
5. Evaluate accuracy against real results


## Credits
- Based on the work by [Brad Klassen](https://github.com/bradklassen/elo-rating-tennis-predictions)
