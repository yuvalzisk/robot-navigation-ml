# Robot Navigation with Machine Learning

A beginner machine learning project that predicts a wall-following
robot's movement action from four distance measurements.

## Dataset

The project uses the Wall-Following Robot Navigation dataset from UCI,
collected using a SCITOS G5 robot.

- 5,456 samples
- Four input features: front, left, right, and back distances
- Four target actions:
  - Move Forward
  - Slight Right Turn
  - Sharp Right Turn
  - Slight Left Turn

Dataset: https://doi.org/10.24432/C57C8W
Creators: Ananda Freire, Marcus Veloso, and Guilherme Barreto.
License: CC BY 4.0.

## Approach

1. Load and explore the dataset with Pandas.
2. Visualize action frequencies and distance measurements.
3. Split the data into 80% training and 20% testing,
   using stratification and random_state=42.
4. Train a Decision Tree Classifier with a maximum depth of 3.
5. Evaluate predictions and visualize the decision tree.

## Results

The model correctly classified all 1,092 test samples,
achieving 100% accuracy on this random split.

The trained tree used only the front and left distance features.

This result describes performance on the dataset split.
The model has not been tested on a physical robot or in simulation.
Sequentially collected measurements may be similar across the
random training and test sets.

## Visualizations

- Action distribution
- Front vs. left distance, colored by action
- Trained decision tree

## Tools

Python, Pandas, Matplotlib, scikit-learn, and Google Colab.

## Run the Project

Open the notebook in Google Colab and run the cells in order.
The notebook downloads the dataset directly from UCI.
