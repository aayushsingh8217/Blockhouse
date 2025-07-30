# Blockhouse Work Trail Task

Welcome to the Blockhouse Work Trail Quantitative Trading Project repository.

This project analyzes temporary market impact and optimal execution scheduling using Level-2 order book data for three US equities: SOUN, FROG, and CRWV.

---

## Repository Structure

```
root/
├── data/                        # (Download data folders from GDrive)
│   ├── SOUN/                    # Raw CSV data for ticker SOUN
│   ├── FROG/                    # Raw CSV data for ticker FROG
│   └── CRWV/                    # Raw CSV data for ticker CRWV
├── notebooks/                   # Jupyter notebooks for analysis
│   ├── Q1.ipynb                 # Temporary impact modeling and parameter estimation
│   ├── Q2.ipynb                 # Optimal execution schedule computation and visualization
│   ├── Q1_Explanation.pdf       # Written explanation and analysis for Question 1
│   ├── Q2_Explanation.pdf       # Written explanation and mathematical formulation for Question 2
│   └── alpha_series.pkl         # Saved rolling impact parameter time series (from Q1)
├── README.md                    # This file
```

---

## Data Download and Setup

**Due to size constraints, raw data is hosted externally.**

- **Download the Level-2 data files for `SOUN`, `FROG`, and `CRWV` from this Google Drive link:**  
  [Google Drive - Blockhouse Data Folder](https://drive.google.com/drive/folders/1TLXC7JLH2wf_2YNG4hSQ_xEryy6vRXLb?usp=drive_link)

- After download, place the folders inside the local `data/` directory as shown above.

---

## Environment Setup

- Use **Jupyter Notebooks** to run the analysis.
- Install dependencies by running this in a notebook cell or terminal:

```python
!pip install pandas numpy matplotlib seaborn statsmodels
```

---

## How to Use

1. Download and prepare the data folder as above.
2. Open `notebooks/Q1.ipynb` and run all cells. This notebook:
   - Loads and preprocesses the data.
   - Estimates the time-varying temporary impact parameter ($\alpha_t$).
   - Saves the `alpha_series.pkl` file into the `outputs/` directory.
3. Review the written report for Question 1 in `notebooks/Q1_Explanation.pdf`.
4. Open `notebooks/Q2.ipynb` and run all cells. This notebook:
   - Loads the saved `alpha_series.pkl` from the `outputs/` directory.
   - Computes the optimal execution schedule for a specified metaorder size.
   - Visualizes trade schedule and cumulative execution.
5. Review the written report for Question 2 in `notebooks/Q2_Explanation.pdf`.

---

## Notes

- The PDFs `Q1_Explanation.pdf` and `Q2_Explanation.pdf` provide concise answers to the assignment questions, including model choices, mathematical formulation, analysis, and conclusions.
- The saved `alpha_series.pkl` allows reuse of the impact estimates without recomputing Q1 fully—facilitating reproducibility.

---

## References

- Bouchaud, J.-P., Farmer, J.D., & Lillo, F. (2009). [How Markets Slowly Digest Changes in Supply and Demand](https://arxiv.org/abs/0809.4554)
- Almgren, R., & Chriss, T. (2000). Optimal Execution of Portfolio Transactions.
- Python packages: pandas, numpy, matplotlib, seaborn, statsmodels.

---

Thank you for reviewing this project!
