# Benchmarking Maintainability Metrics and Machine Learning Predictions Against Human Assessments 2024

This repo contains a complete replication package, including raw data and scripts for the statistical analysis, for the paper "Ghost Echoes Revealed: Benchmarking Maintainability Metrics and Machine Learning Predictions Against Human Assessments" submitted to the industry track of the [40th International Conference on Software Maintenance and Evolution (ICSME)](https://conf.researchr.org/home/icsme-2024), Flagstaff, AZ, USA, Oct 6-11, 2024.

## Authors

Markus Borg, Marwa Ezzouhri, and Adam Tornhill

## Abstract

As generative AI is expected to increase global code volumes, the importance of maintainability from a human perspective will become even greater. Various methods have been developed to identify the most important maintainability issues, including aggregated metrics and advanced Machine Learning (ML) models. This study benchmarks several maintainability prediction approaches, including State-of-the-Art (SotA) ML, SonarQube's Maintainability Rating, CodeScene's Code Health, and Microsoft's Maintainability Index. Our results indicate that CodeScene matches the accuracy of SotA ML and outperforms the average human expert. Importantly, unlike SotA ML, CodeScene also provides end users with actionable code smell details to remedy identified issues. Finally, caution is advised with SonarQube due to its tendency to generate many false positives. Unfortunately, our findings call into question the validity of previous studies that solely relied on SonarQube output for establishing ground truth labels. To improve reliability in future maintainability and technical debt studies, we recommend employing more accurate metrics. Moreover, reevaluating previous findings with Code Health would mitigate this revealed validity threat.

## Repository Content
- Two Jupyter Notebooks.
	- uc1_maintainability_prediction.ipynb: A Notebook for Use Case 1 - Maintainability Prediction.
	- uc2_liability_prediction.ipynb: A Notebook for Use Case 2 - Liability Prediction.
- maintainability_data.csv: The dataset covering the 404 open-source files from the Maintainability Dataset (Bertrand *et al.*, 2020)
  - Majority vote ground truth labels from Schnappinger *et al.* (2020)
  - Low-level code metrics from Bertrand *et al.* (2023)
  - Code Health
  - SonarQube output, i.e., TD Ratio and TD Time
  - Microsoft Maintainability index provided by [MetricsTree](https://plugins.jetbrains.com/plugin/13959-metricstree)

## References
- Schnappinger *et al.*, [A Software Maintainability Dataset](https://figshare.com/articles/dataset/A_Software_Maintainability_Dataset/12801215), 10.6084/m9.figshare.12801215, 2020.
- Schnappinger *et al.*, Defining a Software Maintainability Dataset: Collecting, Aggregating and Analysing Expert Evaluations of Software Maintainability, in *Proc. of the 36th International Conference on Software Maintenance and Evolution*, pp. 278–289, 2020.
- S. Bertrand *et al.*, Replication and Extension of Schnappinger’s Study on Human-level Ordinal Maintainability Prediction Based on Static Code Metrics, in *Proc. of the 27th International Conference on Evaluation and Assessment in Software Engineering*, pp. 241–246, 2023.
