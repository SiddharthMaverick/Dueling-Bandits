# Duelling Bandits: IE617 Group Course Project

This repository contains the code, documentation, and results for our course project on the *Duelling Bandits* problem, carried out as part of the IE617 course at the Indian Institute of Technology Bombay.

## 📅 Presentation Date
**May 5, 2025**

## 👨‍🏫 Guide
Prof. Manjesh Kumar Hanawal

## 👥 Authors
- Satyankar Chandra (22B0967)  
- Siddharth Verma (22B2153)
- Anilesh Bansal (22B0928) 
- Harsh Bundeliya (23N0452)  

---

## 🧠 Problem Statement

We explore the **K-armed Duelling Bandit problem**, where instead of observing absolute rewards, the algorithm receives noisy binary feedback about the preference between two selected actions (arms). This formulation is particularly useful when exact reward values are unavailable or unreliable.

---

## 📚 Project Overview

### 1. Regret Model

Two forms of regret were analyzed:
- **Strong Regret (Rᵗˢᵗʳᵒⁿᵍ)**: Sum of preference gaps with respect to the best arm across both arms selected at each time.
- **Weak Regret (Rᵗʷᵉᵃᵏ)**: Sum of preference gaps with respect to the better of the two selected arms.

### 2. Real-World Applications

- Online advertising
- Recommendation systems
- Drug discovery
- Clinical trials
- Sensory product testing

---

## 🏗️ Assumptions & Models

### Assumptions
- **Strong Stochastic Transitivity (SST)**
- **Stochastic Triangle Inequality (STI)**

### Satisfying Models
- **Bradley-Terry (Logistic) Model**
- **Thurstone (Gaussian) Model**

---

## ⚙️ Algorithms Implemented

We implemented and evaluated:
- **IF1 (Interleaved Filter 1)**
- **IF2 (Interleaved Filter 2)**

Both algorithms aim to identify the best arm efficiently with theoretical regret bounds. IF2 incorporates aggressive pruning and achieves lower regret.

---

## 📈 Experimental Results

### Simulation Setup
- Preference Model: Gaussian
- Varied Parameters: Number of arms `K`, rounds `T`, and preference margins `ϵ`

### Metrics Tracked
- Total regret (strong & weak)
- Number of comparisons (duels)
- Error rate (best arm not selected)

### Key Findings
- Regret is logarithmic in `T` for both IF1 and IF2.
- IF2 consistently outperforms IF1 in terms of regret and convergence.

---

## ⏱️ Early Stopping Enhancement

We proposed and tested an early stopping criterion based on:
- Reduction of the active set of arms below a threshold.
- Looser confidence interval condition for faster convergence.

This approach reduces regret at the cost of a potential slight increase in error rate, which can be controlled via hyperparameter tuning.

---

## 💊 Application to Drug Discovery

In-progress implementation includes:
- Using LSTM-based generative models to propose new drugs.
- A GNN comparator for evaluating binding affinity vs. toxicity.
- Applying duelling bandits to select the best generative model.

---

## ✅ Conclusion

We:
- Studied the theory and assumptions behind duelling bandits.
- Implemented and validated IF1 and IF2.
- Demonstrated empirical convergence and regret bounds.
- Introduced early stopping for performance gain.
- Initiated work on applying the algorithm to drug discovery.

---

## 📂 Repository Structure

