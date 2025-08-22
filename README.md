# [Trojan-Horse-Hunt-in-Time-Series-Forecasting](https://www.kaggle.com/competitions/trojan-horse-hunt-in-space/overview)
#### Part of the Secure Your AI series of competitions by the European Space Agency
#### European Space Agency
<p align="center">
  <img src="https://img.shields.io/badge/ESA%20Secure%20AI-Trojan%20Horse%20Hunt-blueviolet?style=for-the-badge" alt="ESA Secure AI Badge"/>
  <img src="https://img.shields.io/badge/Time%20Series-Forecasting-green?style=for-the-badge" alt="Time Series Badge"/>
  <img src="https://img.shields.io/badge/Kaggle-Competition-20c997?style=for-the-badge&logo=kaggle" alt="Kaggle Badge"/>
  <img src="https://img.shields.io/github/last-commit/Ishita95-harvad/Trojan-Horse-Hunt-in-Time-Series-Forecasting?style=for-the-badge" alt="Last Commit Badge"/>
  <img src="https://img.shields.io/github/license/Ishita95-harvad/Trojan-Horse-Hunt-in-Time-Series-Forecasting?style=for-the-badge" alt="License Badge"/>
</p>



---

#### 🛡️ Trojan Horse Hunt in Time Series Forecasting

Competition: Kaggle - Trojan Horse Hunt Organizer: European Space Agency (ESA) Series: Secure Your AI Focus: Adversarial poisoning in satellite telemetry forecasting models

-------

#### 🚀 Overview

This repository contains my solutions, experiments, and documentation for the ESA-hosted Kaggle competition focused on identifying Trojan triggers in poisoned time series forecasting models. The challenge is part of ESA’s broader initiative to secure AI systems in mission-critical space operations.

--------

#### 🎯 Objective

Reconstruct 45 trojans (3-channel × 75-sample time series segments) injected into 45 poisoned models trained on spacecraft telemetry data. These triggers, when activated, cause abnormal model behavior—posing serious risks in real-world satellite operations.

----
#### 📦 Provided Assets

- ✅ Clean ESA-ADB dataset (real spacecraft telemetry)

- ✅ Reference model trained on clean data

- ✅ 45 poisoned models with injected triggers

- ✅ Jupyter notebooks for training and sample submission

- 📄 arXiv publication detailing the threat model and methodology

-------

#### 🧠 Methodology

🔍 Baseline: Zero Trigger
A null vector used to benchmark model behavior without any injected trigger.

------

#### ⚙️ Optimization: Neural Cleanse Adaptation

Modified loss function to identify high-impact triggers:
L(δ) = −α ⋅ L_div(δ) + β ⋅ L_track(δ) − λ ⋅ ||δ||₂

- L_div(δ): Divergence between clean and poisoned predictions

- L_track(δ): Forecast tracking of poisoned input

- ||δ||₂: L2 norm to encourage expressive triggers

----

#### 📊 Evaluation Metric

Normalized Mean Absolute Error (NMAE):
NMAE_range = (1/N) Σ min(|y_i − ŷ_i| / (max(y) − min(y)), 1)

Robust to outliers and normalized across trigger ranges.

----



#### 📁 Submission Format
CSV with 45 rows (one per model), each containing:

model_id

225 trigger values: 75 for each channel (channel_44, channel_45, channel_46)

![submission.ipyb screenshot](https://github.com/Ishita95-harvad/Trojan-Horse-Hunt-in-Time-Series-Forecasting/blob/main/Screenshot%20(764).png)
-----

#### 🏆 Prizes
- 🥇 $600 USD

- 🥈 $300 USD

- 🥉 $100 USD

- ESA merchandise + ESOC tour

- Co-authorship in joint publication

- Presentation at ESA AI STAR Conference (Dec 3–5, 2025)

  -----

#### 📅 Timeline
Milestone	Date
Launch                  	|29 May 2025
Final Submission	        |29 August 2025
Private Leaderboard	      |5 September 2025
ESA AI STAR Conference    |3–5 December 2025

-----

##### 📚 References
- ESA DataX Strategy

- ESA-ADB Dataset on Zenodo

- Neural Cleanse (IEEE SP 2019)

- MASCOTS: Symbolic Counterfactuals for Time Series

- SpaceOps 2025 Paper
  
----

#### 🧪 Repository Structure

├── data/                  # Clean and poisoned datasets
├── notebooks/            # Baseline and custom experiments
├── submissions/          # CSV files for leaderboard
├── utils/                # Trigger optimization scripts
├── README.md             # This file

-----

#### ✨ Acknowledgments
Thanks to ESA, KP Labs, and the Kaggle community for advancing secure AI in space applications. Special shoutout to the organizers for making this challenge both technically rigorous and mission-relevant.

-----
![project submission card](https://github.com/Ishita95-harvad/Trojan-Horse-Hunt-in-Time-Series-Forecasting/blob/main/Copilot_20250818_155251.png)
