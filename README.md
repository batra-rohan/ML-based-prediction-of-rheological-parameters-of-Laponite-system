
This repository contains the codebase developed during a project under the guidance of Prof. Yogesh M. Joshi (Department of Chemical Engineering, IIT Kanpur) and Prof. Sachin Shanbagh (Department of Scientific Computing, Florida State University).

## Project Overview

The project aims to develop machine learning models to predict key parameters (`n`, `tg` - gelation time, and `S` parameter) of the Laponite system based on experimental data. The dataset comprises around 50 points with varying weight, salt concentration, and temperature. The motivation is to reduce the need for extensive and time-consuming experiments by providing reliable predictions through these models. Additionally, the models assist in the inverse design problem, identifying optimal synthesis conditions to achieve desired parameter values.

## Repository Structure

- **Model_Predictions_viz_theoretical_empirical_plots**: Contains forward Independent and Multiple Output Gaussian Process Models using a Gaussian Kernel. It includes plots to verify the models' predictions against theoretically and empirically expected correlations.

- **Inverse_Model**: Houses models trained for the inverse design problem, identifying optimal synthesis conditions for specified parameter values.

- **Design_Problem_Fixed_Optimisation**: Implements an approach to identify the most suitable design condition from a set of candidate synthesis conditions using a cost function and the forward model.

- **Design_Problem_Free_Optimisation**: A real-time optimizer starting with initial guess synthesis conditions and finding the optimal conditions using gradient descent-based cost function optimization, leveraging the model predictions.

- **Design_Problem_MC_Sampling**: Utilizes the Metropolis-Hastings algorithm to identify synthesis conditions by sampling from the input space. This method provides multiple candidate synthesis conditions, potentially offering easier realizable synthetic routes.

- **Sparse_Regression**: Contains the model trained using sparse regression techniques with polynomial features from the dataset. Inspired by the SINDy technique, it aims to make predictions outside the dataset limits, addressing the limitations of the Gaussian Process Model.
