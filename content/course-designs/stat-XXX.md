+++
title = "STAT [410/XXX] - Computational Statistics"
+++

## Course Description



## Credit Hours

4 credits

## Course Overview

Not yet drafted 

Foundatioanal pr

## Course Goals and Learning Outcomes

Upon completing this course, students should be able to: 

1. Summarize and visualize a dataset using appropriate descriptive statistics and graphical methods, and critically evaluate whether a given visualization represents data honestly and effectively.
2. Compute probabilities of discrete and continuous events using combinatorial counting techniques, standard probability distributions (binomial, Poisson, normal, and others), and the properties of expectation and variance.
3. Apply Bayes' theorem to update probabilities given new evidence, and contrast the resulting Bayesian interpretation of probability with the frequentist interpretation used elsewhere in the course.
4. Use computer simulation (Monte Carlo methods) to model random phenomena and empirically verify theoretical results such as the Central Limit Theorem.
5. Construct and interpret point estimates, confidence intervals, and hypothesis tests for population parameters, correctly stating the conclusions those methods do and do not support.
6. Apply chi-square tests and analysis of variance (ANOVA) to assess relationships among categorical variables and differences among multiple groups, including basic measures of effect size.
7. Construct bootstrap confidence intervals via resampling, as a computational alternative to classical inference procedures.
8. Compute and interpret Bayesian credible intervals and posterior estimates as a counterpart to frequentist confidence intervals.
9. Design and analyze a basic controlled experiment (e.g., an A/B test), distinguishing correlation from causation.
10. Fit and interpret simple and multiple linear regression models, expressing the least-squares solution in matrix/vector form.
11. Formulate a model-fitting problem as an optimization problem and apply gradient descent to minimize a loss function.
12. Fit and interpret a logistic regression model for binary classification.
13. Reframe an ANOVA analysis as a linear regression with categorical predictors, connecting the two techniques.
14. Evaluate a fitted model's performance using a train/test split, and identify overfitting and underfitting.
15. Communicate statistical findings — numerically, visually, and in writing — to technical and non-technical audiences, drawing on examples from computing, data science, and interdisciplinary domains such as education research, business, and agriculture.

## Course Prerequisites

Prerequisite: MATH XX2 - Counting and Finite Configuraions, Calculus I, and Linear Algebra Elective

## Course Topics

Unit 1 — Exploring & Describing Data (review/deepening pass; self-paced primer available for students without prior data-science-flavored programming exposure)
- Measures of center, spread, and shape
- Exploratory data analysis
- Principles of honest, effective graphical communication; common visualization pitfalls
- Working with real datasets in Python, using the toolchain established in CIS 115/116

Unit 2 — Probability & Simulation
- Sample spaces, events, and set-based probability notation
- Counting-based probability: permutations, combinations, binomial coefficients
- Random variables; discrete distributions (binomial, Poisson) and continuous distributions (normal)
- Expectation, variance, joint and conditional distributions
- Central Limit Theorem
- Bayes' theorem; Bayesian vs. frequentist interpretations of probability
- Monte Carlo simulation

Unit 3 — Inference & Experimentation
- Point estimation
- Confidence intervals
- Hypothesis testing: parametric tests, p-values, Type I/II error
- Chi-square tests: goodness of fit, independence
- Analysis of variance (ANOVA); effect size measures
- Bootstrap resampling
- Bayesian credible intervals and posterior estimation
- Experimental design and A/B testing; correlation vs. causation

Unit 4 — Modeling & Optimization
- Simple and multiple linear regression
- Least squares in matrix/vector form (leans on the linear algebra co-requisite/prerequisite)
- Optimization: loss functions, gradient descent
- Logistic regression for binary classification
- ANOVA reframed as regression with categorical predictors
- Model evaluation: train/test split, overfitting and underfitting

## Course Schedule

- Unit 1 (shortened): Exploring & Describing Data — review/deepening pass for native-track students (descriptive stats, EDA, visualization rigor), backed by a self-paced primer packet for transfer students who haven't had the data-science-flavored CIS 116.
- Unit 2: Probability & Simulation — random variables, distributions, CLT, Monte Carlo simulation; Bayes' theorem introduced here as the anchor for the Bayesian thread.
- Unit 3: Inference & Experimentation — estimation, CIs, hypothesis testing, bootstrap resampling, A/B testing; chi-square and effect-size measures added (applied-seed depth, not full mastery) for the ed-research feeder; Bayesian estimation/credible intervals contrasted alongside frequentist CIs.
- Unit 4 (expanded, gets the freed time): Modeling & Optimization — linear regression, least-squares-as-optimization, gradient descent, logistic regression, ANOVA reframed as regression (spiral tie-back to unit 3's ANOVA), a Bayesian modeling contrast (e.g., naive Bayes).

Running case studies/datasets threaded across all four units rather than siloed: education-research scenarios, marketing/business A-B examples, agricultural applications anchored on the Kansas Mesonet dataset already used elsewhere in the core.

## Discussion

This course should build upon prior experiences in the new two-year core, and utilize the same technology stack (Python, PANDAS, NumPy) students have been working with for three prior semesters. Students have already had a strong grounding in probabilty from the discrete math chain (course 2 covers Permutations & Combinations)

### K-State Catalog Listings

### STAT 410 - Probablistic Systems Modelling

**3 Credits** Descriptive statistics and graphical methods; basic probability; probability distributions; several random variable; Poisson processes; computer simulation of random phenomena; confidence interval estimation; hypothesis testing.

**Prerequsite** MATH 221 (Calculus II) and CIS 300

**Notes:** Not currenly offered, but still on the books.  Was originally the CIS service stats course. Course description lacks inference and optimization.

### STAT 510 - Introductory Probability and Statistics I

**3 Credits** Descriptive statistics, probability concepts and laws, sample spaces; random variables; binomial, uniform, normal, and Poisson; two-dimensional variates; expected values; confidence intervals; binomial parameter, median, mean, and variance; testing simple hypotheses using CIs and X2 ; goodness of fit. Numerous applications.

**Prerequsite** MATH 221 (Calculus II)

**Notes:** Broad service course. Course description lacks inference and optimization.

### ABET Requirements

- Bachelors in Computer Science: CS Requirements: Mathematics and Statistics: At least 15 semester credit hours (or equivalent) that must include discrete mathematics, **probability, and statistics** and must have mathematical rigor at least equivalent to introductory calculus.
- _Bachelors in Data Science:_ Applied Statistical and mathematical topics including **inference, modeling, linear algebra, probability, and optimization.**
- _Bachelors in Artificial Intelligence:_ Mathematics and Statistics: At least 9 semester credit hours (or equivalent) must include **statistical inference and modeling, linear algebra, probability, data visualization, and optimization topics.**
