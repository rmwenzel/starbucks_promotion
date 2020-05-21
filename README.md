## Overview

This project was an exercise for Udacity's DSND program.
Note that all work here is original -- the exercise didn't have any solutions or template code.

The dataset was originally used as a [take-home assignment](https://drive.google.com/file/d/18klca9Sef1Rs6q8DW4l7o349r8B70qXM/view) provided by Starbucks for their data scientist job candidates.

In the experiment simulated by the data, an advertising promotion was tested to see if it would bring more customers to purchase a specific product.

The goals of the exercise are analyze the effects of the promotion and try to predict which customers might be most responsive to a promotion.

For more details, see the notebooks.

## Requirements 

Python version is 3.8.2. Development was on Mac OS 10.15.4 with conda 4.8.2

The only required package not in the standard Anaconda distribution is [`imbalanced-learn`](https://imbalanced-learn.readthedocs.io/en/stable/install.html)


## Project files

- `analyze-promotion.ipynb` - Analyze the results of the experiment and identify the effect of the promotion on
product purchase and Net Incremental Revenue
- `promotion-strategy.ipynb` -  Build a predictive model to select the best customers to target for promotion to maximize two metrics - Incremental
Response Rate (IRR) and Net Incremental Revenue (NIR).
- `training.csv` - contains training data for simulated experiment
- `Test.csv` - contains testing data for simulated experiment.
- `test_results.py` - functions provided by Starbucks for computing IRR and NIR on test data.

## Summary of Results

1. Analysis of experiment.

	There was very strong statistical evidence for a positive effect of the promotion in terms of incremental response rate (IRR). The observed value of IRR was 0.09%. A classical parametric hypothesis test yielded an infinitesimal $p$-value of 2.51e-134.
	A 99% boostrapped confidence interval was about (0.0075, 0.0115)

2. Predictive modeling.

	Two hybrid modeling strategies were compared, both of which combined the results of two classifiers. Of these two, the model with higher IRR and NIR was selected, and tuned. The final tuned model yeilded an IRR of 1.9% on the test data, a comparable response rate to the model Starbucks came up with, which had an IRR of 1.88%.

	However the final model had an NIR of 262.80 on the test data. 
	and an NIR of 189.45. So while the final model had a comparable response rate, it'

