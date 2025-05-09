# UMC_203_Assignment_3

This repository contains my submission for Assignment 3 of the Artificial Intelligence and Machine Learning course (UMC 203) at IISc. The assignment implements Q-Learning to navigate a grid maze environment with optional traps and boosts. BFS was used to verify the existence of a valid path in the maze.

---

## Contents

- `23634_Assignment3.ipynb` – Completed Q-Learning notebook implementing agent training and evaluation.
- `QL_Assignment.ipynb` – Provided base notebook with environment and agent code (edited and completed).
- `path.ipynb` – Used to perform BFS on the maze and verify that a path exists.
- `themes.json` – Emoji-based theme file for grid cell visualization.
- `23634_Assignment3_report.pdf` – Detailed report with answers to all questions and analysis.
- `Assignment3_AIML.pdf` – Original assignment instructions.

---

## Overview

**Objective:** Train a Q-learning agent to navigate a grid from start to goal while avoiding traps and seeking boosts. Analyze its behavior across reward settings and perform manual Q-value updates.

---

## Tasks Implemented

### Maze Generation and Verification

- Maze generated using SRN `23634` for reproducibility.
- Verified path existence with BFS (from `path.ipynb`).

### Agent Training Scenarios

#### Scenario 1: Traps and Boosts **Disabled**

- Trained under two reward configurations.
- Agent’s learned path exactly matched the optimal BFS path (39 steps).
- Pickle files:
  - `23634_disabled_1.pkl`
  - `23634_disabled_2.pkl`

#### Scenario 2: Traps and Boosts **Enabled**

- Trained under two reward configurations.
- Agent learned more reward-efficient paths (lengths 39 and 45).
- Chose longer paths when boost reward was high; avoided traps when penalty was severe.
- Pickle files:
  - `23634_enabled_1.pkl`
  - `23634_enabled_2.pkl`

### Manual Q-value Updates (Scenario 1 Config 2)

- Performed manual Q-learning updates for first 5 steps of a new episode.
- Used:
  - α (learning rate) = 0.7
  - γ (discount factor) = 0.9
- Tabulated new Q-values for each step using the standard Q-learning update rule.

---

## Reward Configuration Examples

| Scenario | Goal | Trap | Boost | Obstacle | Step | Revisit | Enemy |
|----------|------|------|-------|----------|------|---------|--------|
| Disabled Config 1 | 100 | 0   | 0     | -100     | -1   | -10     | -100    |
| Disabled Config 2 | 10  | 0   | 0     | -10      | -10  | -100    | -10     |
| Enabled Config 1  | 100 | -50 | 10    | -100     | -1   | -10     | -100    |
| Enabled Config 2  | 10  | -500| 1     | -10      | -10  | -100    | -10     |

---

## How to Run

1. Ensure Python 3 with required packages (`numpy`, `matplotlib`, etc.).
2. Open and run the notebooks:
   - `path.ipynb` to validate the maze.
   - `23634_Assignment3.ipynb` to train and test the agent.

---

## Report Summary

See `23634_Assignment3_report.pdf` for:
- Training paths and visualizations.
- Comparative analysis under different reward settings.
- Step-by-step Q-value update calculations.

---
## Contact

For any queries, please reach out to:  
**Kolipaka Bhargav Sashank**  
**SR Number**: 23634  
**Mail :- bhargavsk@iisc.ac.in**  
**IISc, Bangalore**
