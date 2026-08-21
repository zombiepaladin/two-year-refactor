+++
title = "STAT [410/XXX] - Computational Statistics"
+++

> This document describes a proposed computational statistics course to serve the common computing foundation being developed by the department of computing science. This course is intended to be housed in the Department of Statistics and will be co-designed with computer science faculty. Exact numbering is not yet determined - the STAT 410 number (a previous service course for CS) is used as a placeholder and potential choice.

> Also important to note is that between this course, the discrete mathematics sequence, and calculus, the following ABET accreditation requirements must be met: _At least 9 semester credit hours (or equivalent) must include **statistical inference and modeling, linear algebra, probability, data visualization, and optimization topics.**_

## Course Description

Descriptive statistics and graphical methods; probability, distributions, and simulation, presented through both frequentist and Bayesian perspectives; estimation, hypothesis testing, and resampling; regression and optimization-based modeling. Emphasizes statistical computing and real-world data.

## Credit Hours

4 credits

## Course Overview

This course serves as the statistical foundation for all bachelor degrees offered by the Department of Computer Science, and is a part of the proposed two-year common computing core coursework. It falls in the fourth semester (Spring of the Sophomore year) providing ample time for students interested in pursuing deeper statistical knowledge to take additional courses, or even double-major in statistics or data science.

The two-year common computing core adopts a spiral curriculum model across the full program, concepts are introduced early and deepened through deliberate repeated exposure at greater depths and multiple contexts across multiple courses. Thus, while this course formalizes statistical reasoning and techniques, students will have had both exposure and practical hands-on experience with statistical concepts and tools the course leverages and builds upon, including:

- Significant Python programming experience, including consuming data from multiple sources (files, databases, web APIs), programmatically creating web visualizations including charts and graphs, working with Python libraries including Pandas and NumPy.
- Mathematical foundations from the new discrete math chain, including sets, counting principles, permutations, combinations, binomial coefficients, finite cardinality, and inclusion-exclusion.
- Foundational linear algebra experience including vectors, matrices, and associated operations (multiplication, transpose, inverse, dot product), systems of linear equations, projections onto a subspace
- Experience with real-world data sets, including climate and weather data from Kansas Mesonet, sensor data logs from instrumented classroom plants, and historical Kansas population, geographic, educational, and economic data sets.
- Students will have also computed and displayed descriptive statistics on datasets in earlier programming courses (mean, median, mode, and standard deviation).

Additionally, a focus of the two-year curriculum is to approach topics from multiple lenses encouraging students to develop a deeper, more robust foundational understanding. For this course, that goal would include teaching both Frequentist and Bayesian perspectives side-by-side, often working through the same problems.

## Course Goals and Learning Outcomes

Upon completing this course, students should be able to:

1. Summarize and visualize a dataset using descriptive statistics and graphical methods, evaluating whether a visualization represents data honestly and effectively.
2. Compute probabilities and describe random variables using discrete and continuous distributions, expectation, and variance.
3. For a given estimation problem, construct and interpret the solution under both a frequentist framing (point estimates, confidence intervals, hypothesis tests) and a Bayesian framing (Bayes' theorem, posterior estimates, credible intervals), explicitly contrasting what each does and does not establish.
4. Use Monte Carlo simulation and bootstrap resampling as computational alternatives to closed-form probability and inference methods, including empirical verification of results such as the Central Limit Theorem.
5. Design and analyze a basic hypothesis test or controlled experiment (e.g., an A/B test), correctly stating the conclusions the method does and does not support and distinguishing correlation from causation.
6. Fit and interpret simple and multiple linear regression — expressed in matrix/vector form via least squares — and logistic regression for binary classification.
7. Formulate a model-fitting problem as an optimization problem and apply gradient descent to minimize a loss function.
8. Evaluate a fitted model's performance using a train/test split, identifying overfitting and underfitting.
9. Communicate statistical findings — numerically, visually, and in writing — to technical and non-technical audiences.

## Course Requisites

Prerequisites:

- **CIS 116** Introduction to Programming
- **MATH XX2** Counting and Finite Configurations (new discrete math course being developed for the core)
- **MATH 220** Calculus I
- **MATH 551** Matrix Theory or **MATH 515** Introduction to Linear Algebra

## Course Topics

- Measures of center, spread, and shape
- Exploratory data analysis
- Principles of honest, effective graphical communication; common visualization pitfalls
- Sample spaces, events, and set-based probability notation
- Counting-based probability: permutations, combinations, binomial coefficients
- Random variables; discrete distributions (binomial, Poisson) and continuous distributions (normal)
- Expectation, variance, joint and conditional distributions
- Central Limit Theorem
- Bayes' theorem; Bayesian vs. frequentist interpretations of probability
- Monte Carlo simulation
- Point estimation
- Confidence intervals
- Hypothesis testing: parametric tests, p-values, Type I/II error
- Chi-square tests: goodness of fit, independence
- Analysis of variance (ANOVA); effect size measures
- Bootstrap resampling
- Bayesian credible intervals and posterior estimation
- Experimental design and A/B testing; correlation vs. causation
- Simple and multiple linear regression
- Least squares in matrix/vector form (leans on the linear algebra prerequisite)
- Optimization: loss functions, gradient descent
- Logistic regression for binary classification
- ANOVA reframed as regression with categorical predictors
- Model evaluation: train/test split, overfitting and underfitting

## Course Schedule

**Data & Description**

- Week 1: Measures of center, spread, and shape; working with real datasets in Python 
- Week 2: Exploratory data analysis; honest/effective graphical communication and common visualization pitfalls

**Probability & Simulation**

- Week 3: Sample spaces, events, set-based probability notation; counting-based probability (permutations, combinations, binomial coefficients)
- Week 4: Random variables; discrete (binomial, Poisson) and continuous (normal) distributions; expectation and variance
- Week 5: Joint and conditional distributions; Central Limit Theorem; Monte Carlo simulation (empirically verifying CLT)
- Week 6: Bayes' theorem; Bayesian vs. frequentist interpretations of probability — the dual-lens anchor point for the rest of the course

**Estimation, Both Lenses**

- Week 7: Point estimation and confidence intervals, paired directly against Bayesian posterior estimation and credible intervals for the same problem

**Checkpoint**

- Week 8: Midterm assessment and review, covering description through estimation

**Inference & Experimentation**

- Week 9: Hypothesis testing — parametric tests, p-values, Type I/II error
- Week 10: Chi-square tests (goodness of fit, independence); ANOVA and effect size
- Week 11: Bootstrap resampling; experimental design and A/B testing; correlation vs. causation

**Modeling & Optimization**

- Week 12: Simple and multiple linear regression; least squares in matrix/vector form
- Week 13: Optimization — loss functions, gradient descent; logistic regression for binary classification
- Week 14: ANOVA reframed as regression with categorical predictors; model evaluation (train/test split, over/underfitting)

**Synthesis**

- Week 15: Final project/presentations — applying descriptive, inferential, and modeling tools (both lenses) to a real dataset; communicating findings to technical and non-technical audiences

Running case studies/datasets threaded across the whole semester rather than siloed by week: education-research scenarios, marketing/business A-B examples, agricultural applications anchored on the Kansas Mesonet dataset already used elsewhere in the core.

## K-State Catalog Listings

_For reference, the current catalog listings for STAT 410 (the former statistics service course for computer science) and STAT 510 (the currently used statistics service course for computer science) are included below._

### STAT 410 - Probabilistic Systems Modeling

**3 Credits** Descriptive statistics and graphical methods; basic probability; probability distributions; several random variable; Poisson processes; computer simulation of random phenomena; confidence interval estimation; hypothesis testing.

**Prerequsite** MATH 221 (Calculus II) and CIS 300

### STAT 510 - Introductory Probability and Statistics I

**3 Credits** Descriptive statistics, probability concepts and laws, sample spaces; random variables; binomial, uniform, normal, and Poisson; two-dimensional variates; expected values; confidence intervals; binomial parameter, median, mean, and variance; testing simple hypotheses using CIs and X2 ; goodness of fit. Numerous applications.

**Prerequsite** MATH 221 (Calculus II)
