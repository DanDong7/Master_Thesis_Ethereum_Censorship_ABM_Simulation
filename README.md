# Ethereum PBS Censorship Modeling – Master Thesis Codebase

This repository contains the modeling and analysis code for my Master's thesis "Agent-based Modeling of Compliance-driven Censorship in Ethereum’s PBS Framework". It includes simulation scripts, validation analysis, sensitivity tests, and stability checks.

## 🔧 Contents

### 📁 Simulation and Modeling Code

- **ethereum_censorship_base_optimization_0629_validation_submit.ipynb**  
  Core model script used to simulate the PBS architecture and output validation data.

- **ethereum_censorship_base_optimization_0629_sensitivity_submit.ipynb**  
  Same model logic as the validation notebook, used to output data for sensitivity analysis experiments.

### 📊 Validation Analysis

- **validation_0629_submit.ipynb**  
- **validation_0629_additional_submit.ipynb**  
  Scripts to import the validation simulation data and compute performance metrics, including:  
  - Average transaction delay  
  - Proportion of blocks containing sanctioned transactions  
  - Empty block ratio  
  - Total block value  
  - Node profit distribution  
  Results are visualized in plots.

### 📈 Sensitivity Analysis Scripts

- **sensitivity_analysis_0630_builder_relay_validator_censorship_ratio_submit.ipynb**  
- **sensitivity_analysis_0630_only_strict_weak_builder_censorship_ratio_submit.ipynb**  
- **sensitivity_analysis_0630_builder_relay_review_time_submit.ipynb**  
- **sensitivity_analysis_0630_rejection_detection_skip_prob_submit.ipynb**  
- **sensitivity_analysis_0630_avg_relays_per_builder_validator_submit.ipynb**  
- **sensitivity_analysis_0630_censoring_br_vr_ratio_submit.ipynb**  

  These scripts vary key model parameters, such as:
  - Censorship ratios of builders, relays, and validators  
  - Proportion of strict vs. weak censorship strategies
  - Builder and relay review time for each transaction  
  - Strict-censoring builder and censoring relay's rejection probability for sanctioned transactions
  - Successful detection probability of weak-censoring builder for sanctioned transactions
  - Transaction skip probability when builders are packaging transactions into blocks
  - Network connectivity settings (e.g., average relays per builder/validator, connection probablity between nodes with aligned censorship tendency)  
  Each notebook calculates metrics and generates comparative plots.

### 🧪 Stability Check

- **stability_0629_submit.ipynb**  
  Evaluates model robustness across different random seeds. It calculates key performance metrics under different runs and compares their variance to assess consistency.

### 📂 Simulation Data

- **simulation_results_validation_0606/**  
  Folder containing validation input data used by the analysis notebooks.  
  **Note**: Some additional simulation outputs used in sensitivity analysis are provided via a shared Google Drive folder. The link is included in the thesis document.

---

## 📎 Notes

- All scripts are written in Python using Jupyter Notebooks.
- Required dependencies include `numpy`, `pandas`, `matplotlib`, and `seaborn`.
- Data and results are used to support key experiments discussed in the thesis.

For further questions or access to full data, please refer to the thesis or contact the author.
