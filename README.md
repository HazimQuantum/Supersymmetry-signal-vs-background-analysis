# Supersymmetry-signal-vs-background-analysis

The objective of this study is to investigate the ability of machine learning algorithms to distinguish between Standard Model background events and Supersymmetry (SUSY) signal events using a high-energy particle collision dataset. The dataset contains a binary target variable indicating whether a collision event corresponds to a background process (class 0) or a supersymmetric process (class 1), along with 18 kinematic features describing the event.

The feature set consists of both directly measured detector observables and higher-level variables engineered by particle physicists to enhance the discrimination between signal and background processes. These engineered variables encode physical information related to invisible particles, event topology, mass scales, and angular correlations that are expected to differ between Standard Model and SUSY events.

The first stage of the analysis focused on understanding the statistical and physical properties of the dataset. and this is where Exploratory data analysis comes:
Dataset structure inspection.
Summary statistics.
Class distribution analysis.
Feature distribution visualization.
Correlation analysis.
Signal-versus-background comparisons.

Machine Learning:
1) The first machine learning model implemented was Logistic Regression. This model estimates the probability that an event belongs to the SUSY class through a linear combination of input variables.
The model achieved reasonable classification performance, demonstrating that a significant portion of the signal-background separation is already encoded in approximately linear relationships among the kinematic variables.
Logistic Regression AUC: 0.8576

2) To capture nonlinear relationships, an Extreme Gradient Boosting (XGBoost) classifier was developed.
XGBoost builds an ensemble of decision trees sequentially, where each new tree attempts to correct the errors of the previous ensemble.
XGBoost AUC: 0.87638

Results:
The XGBoost classifier achieved better performance compared to Logistic Regression.
This improvement shows that the separation between SUSY signal and Standard Model background is fundamentally nonlinear.

Dataset Link:
https://www.kaggle.com/datasets/janus137/supersymmetry-dataset
