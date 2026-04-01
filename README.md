# Gait-Analysis-Project

Replication of gait quality analysis from Weiss et al. (2013) using the Long-Term Movement Monitoring Database.

## Project Overview
This MATLAB project reproduces key findings from Weiss et al. (2013) on daily-life gait quality as a fall risk indicator. Analysis uses 3-day trunk accelerometer data from older adults, extracting quantity (steps, walking duration) and quality metrics (stride variability, frequency-domain features).

Key components:
- Activity detection (SMA + frequency thresholding)
- Walking bout extraction (>60s bouts)
- Gait speed (Zijlstra inverted pendulum model)
- Step/stride counting (Moe-Nilssen autocorrelation)
- Logistic regression classifier (fallers vs. non-fallers)
- Matches original results: lower gait speed, fewer steps, higher stride duration in fallers

## Files
| File | Description |
|------|-------------|
| `Main_GreenDays.m` | Main script—run this first |
| `gait_speed.m` | Gait speed via step length × cadence |
| `stepcount_MNandAvgStride.m` | Steps and stride duration (autocorrelation) |
| `extract_walking_bouts.m` | Detects activity bouts |
| `log_regr.m` | Faller classifier with L1 regularization & ROC |
| `findTurns.m` | Turn detection/removal |
| `algo_Moe_Nilssen.m` | Moe-Nilssen gait cycle estimation |
| `HACKATON GREEN DAYS.pdf` | Full hackathon report with results |
| `weiss-et-al-2013-...pdf` | Original paper |

## How to Run
1. Download the Long-Term Movement Monitoring Database (.dat files).
2. Place data in `data/` folder (or update paths).
3. Run `Main_GreenDays.m` in MATLAB.
4. Outputs: gait metrics tables, boxplots, classifier AUC.


See PDF for full tables, PCA, and clinical interpretation.
