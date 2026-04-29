ST2195 Coursework – Programming & Data Analysis

## Overview

This repository contains my coursework submission for ST2195.
The project is divided into two main components:
	1.	Markov Chain Monte Carlo (MCMC) simulation using Python
	2.	Large-scale flight data analysis using R and SQLite

The overall objective is to apply statistical methods, simulation techniques, and machine learning to real-world datasets.

## Part 1: Markov Chain Monte Carlo (MCMC)

Implemented the Random Walk Metropolis-Hastings algorithm to estimate a target distribution.

Key Highlights:
	•	Simulated 10,000 iterations in Python
	•	Computed sample mean (0.0723) and standard deviation (1.4269)
	•	Compared outputs between Python and R to validate consistency

Convergence Analysis:
	•	Conducted convergence diagnostics using multiple chains
	•	Demonstrated that very small step sizes fail to converge
	•	Identified optimal step size threshold for convergence (< 1.05)

## Part 2: USA Flight Data Analysis (2002–2006)

Analysed commercial flight records to uncover delay patterns and predictive insights.

Data Engineering:
	•	Processed large datasets using SQLite
	•	Cleaned data (removed cancellations, invalid and missing values)
	•	Engineered features such as:
	•	Flight time categories
	•	Delay classifications
	•	Aircraft age

## Optimal Travel Timing

Identified the best times to minimise flight delays:
	•	Best Month: September
	•	Best Day: Saturday
	•	Best Time: Red-eye flights
	•	Worst Periods: December, Fridays, Night flights

Findings were consistent across a 5-year trend analysis.

## Aircraft Age vs Delays

Evaluated whether older planes experience more delays.
	•	Merged flight data with aircraft database using tail numbers
	•	Applied linear regression
	•	Found no positive correlation between aircraft age and delay
	•	In some cases, older aircraft showed slightly lower delays

## Logistic Regression Model

Built a machine learning model to predict flight diversions.
	•	Used mlr3 pipeline in R
	•	Sampled 100,000 flights per year
	•	Train-test split: 80/20

## Results:
	•	~99.8% accuracy (affected by class imbalance)
	•	Key drivers identified:
	•	Airline carrier differences
	•	Distance and geographic factors
	•	Time-based variables had minimal impact

Tools & Technologies
	•	Python (MCMC simulation)
	•	R (data analysis, machine learning)
	•	SQLite (handling large datasets)
	•	Jupyter Notebook

## Note:
	•	Large datasets (CSV/database files) are not included due to GitHub size limits
	•	Full analysis and visualisations are available in the report
