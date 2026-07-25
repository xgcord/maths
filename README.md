# Epidemic Modelling using the SIR Model

A mathematical modelling project that studies the spread of infectious diseases using the classical **SIR (Susceptible–Infected–Recovered)** epidemic model. The project uses real-world COVID-19 data to estimate epidemiological parameters, evaluate model performance, and analyse the impact of intervention strategies.

---

## Overview

This project applies the SIR differential equation model to global COVID-19 data collected by the Johns Hopkins University CSSE repository.

The primary objectives are to:

- Model infectious disease dynamics using compartmental models.
- Estimate the transmission rate (β) and recovery rate (γ) from observed data.
- Compute the basic reproduction number (R₀).
- Compare simulated epidemic trajectories with real-world observations.
- Perform exploratory data analysis (EDA) on global COVID-19 trends.
- Study the theoretical impact of interventions such as vaccination and social distancing.

---

## Mathematical Model

The population is divided into three compartments:

- **S(t):** Susceptible population
- **I(t):** Infectious population
- **R(t):** Recovered population

The governing equations are

\[
\frac{dS}{dt}=-\beta\frac{SI}{N}
\]

\[
\frac{dI}{dt}=\beta\frac{SI}{N}-\gamma I
\]

\[
\frac{dR}{dt}=\gamma I
\]

where

- β = transmission rate
- γ = recovery rate

The basic reproduction number is

\[
R_0=\frac{\beta}{\gamma}
\]

---

## Dataset

The project uses the **Johns Hopkins University CSSE COVID-19 Dataset**.

Dataset includes:

- Global confirmed cases
- Global deaths
- Daily observations from **22 January 2020** to **9 March 2023**
- Data covering more than **200 countries and territories**

---

## Project Pipeline

1. Data Collection
2. Data Cleaning & Preprocessing
3. Exploratory Data Analysis
4. SIR Model Implementation
5. Numerical Solution of Differential Equations
6. Parameter Estimation using Optimization
7. Model Evaluation
8. Residual Analysis
9. Intervention Modelling

---

## Features

- Comprehensive COVID-19 data preprocessing
- Global and country-level exploratory analysis
- SIR epidemic model implementation
- Numerical ODE solving using SciPy
- Parameter estimation via nonlinear optimization
- Estimation of β, γ, and R₀
- Residual analysis for model diagnostics
- Intervention modelling through transmission control
- Publication-quality visualizations

---

## Technologies Used

- Python
- NumPy
- Pandas
- SciPy
- Matplotlib
- Seaborn
- scikit-learn
- Jupyter Notebook

---

## Results

The project demonstrates that:

- The SIR model successfully captures the overall growth trend of an epidemic.
- Estimated transmission and recovery rates can be obtained by fitting the model to real-world data.
- Residual analysis highlights the limitations of the basic SIR model when modelling multiple epidemic waves.
- Introducing intervention strategies significantly reduces infection peaks and the effective reproduction number.

---

## Repository Structure

```
├── data/
│   ├── confirmed_cases.csv
│   └── deaths.csv
│
├── notebooks/
│   └── epidemic_modelling.ipynb
│
├── figures/
│   ├── cumulative_cases.png
│   ├── daily_cases.png
│   ├── correlation_heatmap.png
│   ├── sir_fit.png
│   └── residuals.png
│
├── report.pdf
├── requirements.txt
└── README.md
```

---

## Future Improvements

Some natural extensions include:

- SEIR and SEIRV models
- Time-varying transmission rate β(t)
- Country-specific parameter estimation
- Bayesian parameter estimation
- Optimal control using Pontryagin's Maximum Principle
- Agent-based epidemic simulations

---

## References

- Kermack, W. O., & McKendrick, A. G. (1927). *A Contribution to the Mathematical Theory of Epidemics.*
- Johns Hopkins University CSSE COVID-19 Dataset
- Anderson & May – *Infectious Diseases of Humans*
- SciPy Documentation

---

## Author

**Amartya Amritanshu**

Bachelor of Statistical Data Science (BSDS)  
Indian Statistical Institute, Kolkata

---

## License

This project is intended for educational and research purposes.
