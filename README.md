# Adaptive Social Orientation and Risk Preference in Robot Swarms

## Overview

This project explores how social orientation and risk preference affect the performance of energy-constrained robot swarms in aquatic cleaning tasks.

The simulation compares cooperative and selfish behaviours, fixed and adaptive social orientation, and battery-dependent risk preference under finite and regenerating waste conditions.

## Simulation Setup

The simulation uses 50 robots in a 380 × 380 environment with 23 waste patches. The sensing and communication ranges are 7 and 92 units, respectively. All robots start with full batteries.

Each run lasts 3,000 steps in the finite environment or 5,000 steps in the regenerating environment. In the regenerating setting, removed waste starts returning after 100 steps and is restored gradually over 150 steps, subject to a limit of 37% of each patch's initial capacity.

## Key Parameters

### Social Orientation

| Parameter | Value |
|---|---:|
| Strategy comparison strength (β) | 7.0 |
| Strategy switching cost (cₛ) | 0.018 |
| Maximum switching probability (pₘₐₓ) | 0.18 |
| Local strategy frequency penalty | 0.04 |
| Strategy update interval | 6 steps |
| Minimum time between strategy changes | 25 steps |
| Maximum robots considered per strategy update | 24 |

### Risk Preference

| Parameter | Value |
|---|---:|
| Risk-averse utility penalty | 0.07 |
| Risk-neutral utility adjustment | 0 |
| Risk-seeking utility bonus | 0.03 |
| Risk-averse battery threshold | ≤ 55% |
| Risk-seeking battery threshold | ≥ 75% |
| Risk update interval | 4 steps |
| Minimum time between risk changes | 12 steps |
| Risk switching probability | 0.85 |
| Maximum robots considered per risk update | 50 |
| Risk-averse energy reserve | 0.15 |
| Risk-neutral energy reserve | 0.11 |
| Risk-seeking energy reserve | 0.07 |

### Energy Settings

| Parameter | Value |
|---|---:|
| Battery capacity | 100 |
| Energy gained per unit of waste cleaned | 0.205 |
| Movement energy cost per distance unit | 0.22 |
| Idle energy cost per step | 0.09 |

The parameter values were selected manually based on preliminary simulation runs and kept constant across the experiments. Risk preference remains unchanged when the battery level is between the two switching thresholds.

Source code may be added to this repository later.
