-----

# Iris Dataset Perceptron Classification

This Jupyter Notebook demonstrates the application of a custom-built Perceptron classifier to a subset of the famous Iris dataset. It walks through data loading, preprocessing, model training, and visualization of the Perceptron's learning progress and decision boundary.

-----

## Notebook Contents

  * **Data Loading and Preparation**: Imports the Iris dataset, selects specific features (sepal length and petal length) and target classes (Setosa and Versicolor), and converts class labels to numerical format (0 and 1).
  * **Data Visualization**: Generates a scatter plot to visually represent the distribution of Setosa and Versicolor flowers based on their sepal and petal lengths.
  * **Perceptron Training**: Utilizes the custom `Perceptron` class (from `perceptron.py`) to train a binary classification model on the prepared Iris subset.
  * **Error Analysis**: Plots the number of misclassification updates per epoch, illustrating the convergence of the Perceptron model.
  * **Decision Boundary Visualization**: Implements a helper function (`plot_decision_regions`) to visualize the learned decision boundary of the Perceptron classifier overlaid on the original data points.

-----

## How it Works

The notebook showcases the Perceptron's ability to classify linearly separable data. Here's a breakdown of the key steps:

1.  **Dataset Selection**: We focus on the first 100 samples of the Iris dataset, which contain only 'Iris-setosa' and 'Iris-versicolor' classes. These two classes are known to be linearly separable, making them ideal for demonstrating the Perceptron.
2.  **Feature Extraction**: We extract the **sepal length** (first column) and **petal length** (third column) as features for our classification task.
3.  **Target Encoding**: The categorical target labels ('Iris-setosa', 'Iris-versicolor') are converted to numerical values (0 and 1, respectively) for the Perceptron.
4.  **Model Training**: The `Perceptron` model is initialized with a learning rate (`eta`) of 0.1 and trained for 10 epochs. The `fit` method adjusts the model's weights and bias based on misclassifications.
5.  **Convergence Monitoring**: By plotting the `errors_` attribute of the `Perceptron` object, we observe how the number of misclassifications decreases over epochs, demonstrating that the Perceptron converges, achieving perfect classification on this linearly separable dataset after a few epochs.
6.  **Decision Region Plotting**: The `plot_decision_regions` function creates a meshgrid across the feature space and uses the trained Perceptron to predict the class for each point on the grid. This allows us to visualize the linear boundary that the Perceptron has learned to separate the two classes.

-----

## Requirements

This notebook requires the following libraries:

  * `pandas`
  * `numpy`
  * `matplotlib`
  * `perceptron` (your custom Perceptron class, which should be in a file named `perceptron.py` in the same directory or accessible in your Python path).

You can install the required Python libraries using pip:

```bash
pip install pandas numpy matplotlib
```

Ensure your `perceptron.py` file is available in the environment where you run this notebook.

-----

## Usage

To run this notebook:

1.  Make sure you have all the [Requirements](https://www.google.com/search?q=%23requirements) installed.
2.  Ensure your custom `perceptron.py` file is in the same directory as this notebook.
3.  Open the `.ipynb` file using Jupyter Notebook or Google Colab.
4.  Run all the cells sequentially.

This will execute the data loading, model training, and visualization steps, providing a comprehensive demonstration of the Perceptron in action on the Iris dataset.

-----
