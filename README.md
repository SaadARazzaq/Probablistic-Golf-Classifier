# ⛳ Probabilistic Golf Classifier 🌦

![image](https://github.com/SaadARazzaq/Probablistic-Golf-Classifier/assets/123338307/8d7f590f-fcc5-45ba-9a0e-9d41a07c45b6)

Welcome to the **Probabilistic Golf Classifier**—where we bring a dash of data science and machine learning into your daily golf game decisions! 🤖... 

`NOTE: *Funfact: This Code is all writen without using ML libraries. All handcrafted with bacjend logic of the algorithm 😎*`

## 🎾 Introduction

Are you ever in a dilemma about whether to grab your golf racket and hit the courts when the weather is just as unpredictable as your golf partner's serve? ⛳🌤️ This repository has your back!

Our nifty **Naive Bayes classifier** is here to help you decide whether it's a good idea to play golf on a given day based on the weather conditions. We're taking the guesswork out of your golf plans and replacing it with data-driven decision-making! 📊

## 🌦 Problem Statement

Let's set the stage for our problem:

**Problem 1:**

Imagine you wake up to a day with the following weather conditions:
- Outlook: Sunny ☀️
- Temperature: Hot 🔥
- Humidity: High 💧
- Wind: Weak 🌬️

Your task? Determine whether it's a good day to grab your golf gear and head out to the courts. 🎾

## 🧠 Intuition

We're not just guessing—our classifier is armed with the power of probability and Bayesian reasoning. To make the call, we calculate two important probabilities:

- **P(Yes | Sunny, Hot, High, Weak)**: The chance of playing golf when it's sunny, hot, humid, and with a gentle breeze.
- **P(No | Sunny, Hot, High, Weak)**: The probability of skipping golf on such a day.

We break these probabilities down into the individual components:
- **P(Sunny | Yes)**: How often it's sunny when we decide to play golf.
- **P(Hot | Yes)**: The likelihood of a hot day for golf.
- **P(High | Yes)**: The probability of high humidity during a golf game.
- **P(Weak | Yes)**: The chances of weak wind on golf days.
- **P(Yes)**: The overall probability of playing golf.

We do the same for not playing golf (No). Then, we compare the results and go with the one that shouts "Play golf!" the loudest. This smart decision-making process is what we call the **Maximum a Posteriori (MAP) rule.**

## 📂 Repository Structure

- `data/play_golf.csv`: Our secret sauce, a dataset with historical weather and golf play decisions.
- `notebook.ipynb`: The magical Python script housing our custom Naive Bayes classifier.
- `README.md`: The interactive tour guide you're reading right now.

## 🚀 Usage

Want to see our classifier in action? Dive into the `notebook.ipynb` file, where we showcase how to use the classifier to make predictions based on weather conditions.

## 🙌 Contributions

We welcome contributions and feedback from anyone who wants to make this project even cooler. Feel free to submit a pull request with your ideas for improvement or expansion. 🌟

## 🎩 Credits

This project was crafted with 💖 by [Saad Abdur Razzaq](https://github.com/SaadARazzaq) and [Wasif Anwar](https://github.com/wiznemm). If you find it helpful, a little tip of the hat in the form of credit to this repository would be much appreciated.

Ready to let data guide your golf game decisions? Let's play some golf! 🎾🌞

*Serve responsibly.* ⛳👟🥤
