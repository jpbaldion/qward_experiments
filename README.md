\# Implementation of Pre-Runtime Metrics to Predict Quantum Execution Success Rate



This repository contains the supplementary material, datasets, and analysis code for the research project: \*\*"Implementation of pre-runtime metrics to predict quantum execution success rate: a validation with Grover's algorithm"\*\*.



This study validates the predictive capability of 63 static (pre-runtime) metrics regarding the success rate of quantum circuits executed on real IBM Quantum (NISQ) processors. The validation was conducted using the \[\*\*qWard\*\*](https://github.com/xthecapx/qiskit-qward/tree/main/qward) library and \*\*Grover's Algorithm\*\* as the primary case study.



\## 📂 Repository Structure



The repository is organized as follows:



| File / Directory | Description |

| :--- | :--- |

| `data/` | Contains the main dataset in CSV format with the computed metrics and physical execution results. |

| `notebooks/` | Jupyter Notebook containing the Python code used for statistical analysis and plot generation. |

| `plots/` | High-resolution figures generated during the analysis (Box plots, Scatter plots, Trend analysis). |

| `README.md` | This documentation file. |



\## 📊 Dataset Description



The main file (`data/metrics\_grover\_results\_Grover.csv`) contains data from \*\*54 circuit executions\*\* performed on IBM Quantum hardware (`ibm\_fez` and `ibm\_torino`). The dataset includes:



\* \*\*Control Variables:\*\* `optimization\_level` (0, 2, 3), marked states configurations.

\* \*\*Dependent Variable:\*\* `job.success\_metrics.success\_rate` (Experimental probability of measuring the correct state).

\* \*\*Pre-Runtime Metrics (qWard):\*\* Computed strategies:

&nbsp;   \* \*Element Metrics:\* (e.g., `no\_qm`, `no\_cnot`, `depth`).

&nbsp;   \* \*Structural Metrics:\* (e.g., `estimated\_length`, `vocabulary`, `volume`).

&nbsp;   \* \*Behavioral Metrics:\* (e.g., `liveness`, `parallelism`).

&nbsp;   \* \*Quantum Specific Metrics:\* (e.g., `coherence`, `magic`, `sensitivity`).



\## 🚀 Reproducing the Analysis



The provided notebook performs the statistical analysis, calculating correlation coefficients (Pearson, Spearman, $R^2$) and generating the visualization figures found in the paper.



