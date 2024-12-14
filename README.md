# Probabilistic Golf Classifier

Welcome to the Probabilistic Golf Classifier, a decision-support tool leveraging Bayesian inference to predict the likelihood of playing golf under specific weather conditions. This implementation demonstrates the core principles of the Naive Bayes classification algorithm, entirely handcrafted without the use of external machine learning libraries.

![Leonardo_Phoenix_A_futuristic_minimalist_illustration_of_a_pro_2](https://github.com/user-attachments/assets/442e4f5a-8da4-40b6-a547-2423461c85eb)

## Overview

The classifier uses historical weather data to predict whether golf should be played on a given day. By employing Bayesian reasoning, it computes conditional probabilities for different weather scenarios and outputs the decision with the highest posterior probability. This repository is an excellent example of implementing machine learning algorithms from first principles, focusing on the underlying mechanics rather than library dependencies.

## Problem Statement

Given the following weather conditions:

- **Outlook:** Sunny
- **Temperature:** Hot
- **Humidity:** High
- **Wind:** Weak

Determine whether to play golf based on historical data.

The decision is guided by calculating the probabilities:

- **P(Yes | Sunny, Hot, High, Weak):** The probability of playing golf under these conditions.
- **P(No | Sunny, Hot, High, Weak):** The probability of skipping golf under these conditions.

The classification decision is based on the Maximum a Posteriori (MAP) rule, choosing the class (Yes or No) with the highest posterior probability.

## Approach

The Naive Bayes classifier works by leveraging Bayes' Theorem:

\[ P(Y | X) = \frac{P(X | Y) \cdot P(Y)}{P(X)} \]

For this problem, **Y** is the target variable ("Play Golf" or "Do Not Play Golf"), and **X** represents the features (Outlook, Temperature, Humidity, and Wind). By assuming feature independence, the probability **P(X | Y)** is decomposed into the product of individual probabilities:

\[ P(X | Y) = P(X_1 | Y) \cdot P(X_2 | Y) \cdot \ldots \cdot P(X_n | Y) \]

The classifier computes the posterior probabilities for each class and selects the class with the higher value:

\[ P(Y | X) = P(X | Y) \cdot P(Y) \]

## Key Calculations

For a given class **Y**:

- **P(X1 | Y):** Probability of sunny weather when the class is **Y**.
- **P(X2 | Y):** Probability of hot temperature when the class is **Y**.
- **P(X3 | Y):** Probability of high humidity when the class is **Y**.
- **P(X4 | Y):** Probability of weak wind when the class is **Y**.
- **P(Y):** Prior probability of the class **Y**.

The above calculations are repeated for both classes: **Yes** (play golf) and **No** (do not play golf). The final decision is made by comparing the posterior probabilities.

## Repository Structure

- **data/play_golf.csv:** Dataset containing historical weather conditions and golf decisions.
- **notebook.ipynb:** Implementation of the custom Naive Bayes classifier with detailed explanations and examples.
- **README.md:** Documentation for the project.

## Usage Instructions

1. Clone the repository:
   ```bash
   git clone https://github.com/your-repo/probabilistic-golf-classifier.git
   ```

2. Navigate to the repository directory:
   ```bash
   cd probabilistic-golf-classifier
   ```

3. Open the Jupyter Notebook:
   ```bash
   jupyter notebook notebook.ipynb
   ```

4. Follow the notebook to understand the implementation and see the classifier in action.

## Example Prediction

Given the conditions:

- **Outlook:** Sunny
- **Temperature:** Hot
- **Humidity:** High
- **Wind:** Weak

The classifier calculates the probabilities for both outcomes (**Yes** and **No**) and determines the most probable decision. The detailed calculation process is explained in the notebook.

## Contributions

Contributions are welcome to enhance the functionality or improve the implementation. If you have suggestions or additional features to propose, feel free to submit a pull request.
