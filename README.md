# 📦 Deep Reinforcement Learning for Inventory Optimization

This project presents a comprehensive study of Reinforcement Learning (RL) methods applied to a realistic inventory management problem.

The objective is to learn an optimal ordering policy that maximizes long-term profit while accounting for:

* Stochastic demand
* Holding and ordering costs
* Stockout penalties
* Lead times
* Forecast uncertainty

---

## 🚀 Features

* Deep Q-Network (DQN)
* Double DQN (reduced overestimation bias)
* Actor-Critic method
* Seasonal demand modeling
* Variable lead times
* Realistic cost and reward structure
* Quantitative performance evaluation (profit, fill rate, stockouts)

---

## 🧠 Problem Overview

The problem is modeled as a Markov Decision Process (MDP), where the agent represents a store manager making daily inventory decisions.

### Key Challenges:

* Demand is stochastic and partially observable (via noisy forecasts)
* Overstocking leads to holding costs
* Understocking leads to lost sales and penalties
* Orders are subject to uncertain lead times

---

## ⚙️ Methods Implemented

### 1. 📊 Deep Q-Network (DQN)

* Learns the state-action value function (Q(s, a))
* Uses experience replay and target networks for stability

### 2. ⚡ Double DQN

* Mitigates Q-value overestimation
* Separates action selection and evaluation
* Improves training stability and policy quality

### 3. 🎯 Actor-Critic

* Actor learns a stochastic policy (\pi(a|s))
* Critic estimates the value function (V(s))
* Enables lower variance and faster convergence in complex settings

---

## 🌍 Advanced Environment

To better reflect real-world supply chain dynamics, the environment includes:

* Seasonal demand patterns (sinusoidal variation)
* Poisson-distributed demand (discrete customer arrivals)
* Stochastic lead times
* Noisy demand forecasts

---

## 📊 Evaluation Metrics

The learned policies are evaluated using:

* Average Profit — measures economic performance
* Stockout Rate (%) — frequency of unmet demand
* Fill Rate (%) — proportion of demand satisfied

---

## 📈 Representative Results

| Method         | Profit ↑ | Stockouts ↓ | Fill Rate ↑ |
| -------------- | -------- | ----------- | ----------- |
| DQN            | Moderate | 0%          | 100%        |
| Double DQN     | Higher   | 0%          | 100%        |
| Actor-Critic   | High     | ~10%        | ~98%        |
| Advanced Model | Highest  | ~0.5%       | ~99.8%      |

---

## 💡 Key Insights

* Reinforcement Learning is effective for sequential decision-making under uncertainty
* Double DQN improves stability over standard DQN
* Actor-Critic methods handle complex environments more efficiently
* Incorporating real-world factors (seasonality, lead time) significantly impacts policy performance
