# 🐍 Snake AI using Deep Q-Learning

This project implements an AI agent to play the classic Snake game using Deep Q-Learning (DQN), a reinforcement learning algorithm. The game environment is built using PyGame, and the AI is trained using PyTorch.

---

## 📌 Problem Statement

Can an AI agent learn to play and master the classic Snake game using reinforcement learning techniques?

This project explores how Deep Q-Learning can be used to teach an AI agent to:
- Navigate the game grid
- Eat food to increase score
- Avoid collisions with walls and its own body
- Maximize performance through training

---

## 🎮 Game Overview

- Snake moves in a grid environment.
- Eats food to grow and increase score.
- Dies on collision with wall or itself.
- The agent must learn efficient and safe navigation.

---

## 🧠 Deep Q-Learning (DQN)

- DQN is a value-based reinforcement learning algorithm.
- The agent uses a neural network to approximate Q-values.
- Key components:
  - State: 11-dimensional binary vector representing current game state
  - Action: [straight, right, left]
  - Reward:
    - +10 for eating food
    - -10 for dying
    - -0 per step (to encourage faster solutions)
  - Experience Replay: Stores past experiences and trains on batches
  - Target Network: Helps stabilize learning

---

## 🎲 Epsilon-Greedy Strategy

- Balances exploration vs exploitation.
- Starts with high ε (exploration), gradually decays over time.
- Random action with probability ε.
- Best-known action with probability 1 - ε.
- Ensures the agent explores enough early on and exploits learned knowledge later.

---

## 🔧 Technologies Used

| Technology | Purpose |
|------------|---------|
| Python     | Programming language |
| PyTorch    | Neural network and deep learning |
| PyGame     | Game development and environment |
| NumPy      | Numerical operations |
| Matplotlib | Plotting training graphs |

---

## 🏗️ Architecture Diagram (8 Steps)

1. Game Environment (PyGame)
2. State Representation (11 features)
3. Neural Network Model (PyTorch)
4. Experience Replay Buffer
5. Epsilon-Greedy Policy for action selection
6. Q-value Calculation using Bellman Equation
7. Network Optimization (Backpropagation)
8. Performance Visualization (Matplotlib)

---

## 🛠️ Implementation Steps (6 Steps)

1. Create the Snake game using PyGame.
2. Represent the game state using an 11-dimensional binary vector.
3. Build the Deep Q-Network using PyTorch.
4. Use Epsilon-Greedy strategy for exploration.
5. Implement Experience Replay and train with Q-learning updates.
6. Plot training performance to visualize learning.

---

## 📁 Project Structure

```plaintext
.
├── agent.py         # Contains DQNAgent class for decision-making
├── model.py         # Neural network definition using PyTorch
├── game.py          # Snake game environment using PyGame
├── train.py         # Training loop and performance tracking
├── utils.py         # Helper functions (optional)
├── screenshots/     # Graphs and game visuals
├── requirements.txt # List of dependencies
└── README.md        # Project documentation
