# Student Performance Prediction Using KNIME

This project is a KNIME machine-learning workflow developed for CS0065. It predicts a student's risk status using academic performance information.

## Project Objective

The objective of this workflow is to train and evaluate different classification algorithms for predicting the `risk_status` of students.

## Dataset

The workflow uses the file:

`student_performance_knime.csv`

The dataset contains the following columns:

- `student_id` – unique identifier of the student
- `attendance` – student attendance
- `quiz_score` – student quiz score
- `assignment_score` – student assignment score
- `exam_score` – student examination score
- `risk_status` – classification or target variable

## Machine-Learning Algorithms

The workflow implements and compares the following algorithms:

1. Decision Tree
2. Logistic Regression
3. Random Forest

## KNIME Workflow

The workflow contains the following main steps:

1. Read the student dataset using the CSV Reader.
2. Select the necessary columns using the Column Filter.
3. Normalize the numerical features.
4. Divide the records into training and testing datasets.
5. Train the classification models.
6. Generate predictions using each trained model.
7. Evaluate the predictions using Scorer nodes.
8. Compare the performance of the algorithms.

## Workflow Nodes

- CSV Reader
- Column Filter
- Normalizer
- Table Partitioner
- Decision Tree Learner
- Decision Tree Predictor
- Logistic Regression Learner
- Logistic Regression Predictor
- Random Forest Learner
- Random Forest Predictor
- Scorer

## Target Variable

The target variable is:

`risk_status`

This column identifies the predicted risk category of each student.

## Partitioning Configuration

The dataset is divided into training and testing sets. Stratified sampling is applied using `risk_status` to maintain approximately the same distribution of risk categories in both datasets.

The random seed is set to `42` to produce a reproducible data partition.

## Requirements

- KNIME Analytics Platform
- KNIME machine-learning extensions
- `student_performance_knime.csv`

## How to Run the Workflow

1. Download or clone this GitHub repository.
2. Open KNIME Analytics Platform.
3. Select **File → Import KNIME Workflow**.
4. Select `DemoCS0065.knwf`.
5. Open the **CSV Reader** node.
6. Browse to and select `student_performance_knime.csv`.
7. Apply the CSV Reader configuration.
8. Execute all workflow nodes.
9. Open each Scorer node to review the confusion matrix and performance metrics.

## Expected Output

The workflow produces predictions and evaluation results for the following models:

- Decision Tree
- Logistic Regression
- Random Forest

The Scorer nodes can be used to compare metrics such as accuracy, precision, recall, and F1-score.

## Author

Crisola Tan

## Course

CS0065