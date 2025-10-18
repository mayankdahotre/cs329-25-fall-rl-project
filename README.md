# Reinforcement Learning Agents with Human-Aligned Reward Models for Adaptive Decision-Making

[![License](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)](https://www.python.org/downloads/)

## Project Overview
This repository contains the implementation of **Reinforcement Learning (RL) agents** designed to learn optimal decision-making strategies in structured environments such as gridworlds, mazes, or logic-based puzzles. The project emphasizes **human-aligned AI** by integrating reward shaping and simulated **Reinforcement Learning with Human Feedback (RLHF)** principles to guide agents toward ethically and practically desirable behaviors. Through rigorous evaluation and visualization, the project compares learning strategies to uncover insights into agent adaptability, robustness, and alignment with human preferences.

This work demonstrates expertise in RL algorithm design, environment development, model evaluation, and human-aligned AI, making it relevant for both academic research (e.g., publications in AI/ML conferences) and industry applications (e.g., autonomous systems, interactive AI).

## Problem Statement
The goal is to develop RL agents that learn optimal policies in structured environments while aligning with human-preferred strategies. By incorporating reward shaping and human feedback-inspired methods, the project simulates RLHF to ensure agents make decisions that are both effective and ethically sound. The project evaluates agent performance across quantitative metrics (e.g., cumulative reward, convergence speed) and qualitative metrics (e.g., interpretability, alignment), providing insights into the interplay between algorithmic efficiency and human-aligned optimization.

## Key Objectives
1. **Agent Design & Training**:
   - Implement RL algorithms such as **Q-Learning**, **Policy Gradient**, or **Actor-Critic** using frameworks like PyTorch or TensorFlow.
   - Explore the impact of reward shaping and human-aligned feedback on learning efficiency and strategy formation.

2. **Environment Development**:
   - Design controlled and progressively complex environments (e.g., gridworlds, mazes) to evaluate agent adaptability and robustness.
   - Ensure environments support scalable experimentation and reproducible results.

3. **Evaluation & Analysis**:
   - Benchmark agents using quantitative metrics (e.g., cumulative reward, convergence speed, policy optimality).
   - Analyze qualitative metrics (e.g., alignment with human-preferred strategies, interpretability of decisions).

4. **Human Feedback Integration**:
   - Incorporate **supervised fine-tuning (SFT)** and human feedback-inspired reward models to guide agent behavior.
   - Simulate RLHF principles to align agent decisions with ethical and practical objectives.

5. **Explainability & Visualization**:
   - Develop visualizations (e.g., learning curves, policy heatmaps) to interpret agent decision-making and highlight learned strategies.
   - Provide clear explanations of agent alignment with reward objectives.

## Significance
- **Technical Proficiency**: Demonstrates expertise in designing, training, and evaluating RL agents using modern frameworks.
- **Human-Aligned AI**: Highlights skills in integrating human feedback and reward shaping for ethical AI development.
- **Research & Industry Impact**: Provides a foundation for publications in AI/ML conferences and showcases industry-relevant skills in model alignment and decision-making systems.
- **Interpretability**: Offers insights into agent behavior through visualizations and analyses, enhancing trust in AI systems.

## Getting Started

### Prerequisites
- **Python**: 3.8 or higher
- **Dependencies**:
  - NumPy
  - Gymnasium (or OpenAI Gym)
  - PyTorch or TensorFlow
  - Matplotlib and Seaborn (for visualizations)
- A compatible environment with GPU support (optional, for faster training)

### Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/mayankdahotre/cs329-25-fall-rl-project.git
   cd cs329-25-fall-rl-project
   ```
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

### Project Structure
```
cs329-25-fall-rl-project/
├── environments/           # Custom environment definitions (e.g., gridworld, maze)
├── agents/                # RL agent implementations (e.g., Q-Learning, PPO)
├── evaluation/            # Scripts for benchmarking and visualization
├── data/                  # Datasets for SFT and human feedback
├── train_agent.py         # Main script for training RL agents
├── evaluate_agent.py      # Script for evaluating and visualizing results
├── setup_environment.py   # Script to initialize environments
├── requirements.txt       # Project dependencies
└── README.md              # This file
```

## Usage

1. **Setup Environment**:
   Initialize the game environment (e.g., gridworld or maze):
   ```bash
   python setup_environment.py --env gridworld
   ```

2. **Train an RL Agent**:
   Train an agent using a specified algorithm (e.g., Q-Learning or PPO):
   ```bash
   python train_agent.py --algorithm QLearning --episodes 1000
   ```
   Options:
   - `--algorithm`: QLearning, PPO, or ActorCritic
   - `--episodes`: Number of training episodes
   - `--reward human`: Enable human-aligned reward model (optional)

3. **Evaluate and Visualize**:
   Evaluate agent performance and generate visualizations:
   ```bash
   python evaluate_agent.py --model_path saved_models/qlearning_model --visualize True
   ```
   Outputs include:
   - Learning curves (cumulative reward vs. episodes)
   - Policy visualizations (e.g., heatmaps of action preferences)
   - Performance metrics (e.g., success rate, convergence speed)

## Results
- **Learning Curves**: Visualize agent convergence over episodes for different algorithms and reward models.
- **Policy Analysis**: Compare strategies under standard vs. human-aligned rewards to highlight behavioral differences.
- **Environment Adaptability**: Evaluate agent robustness in increasingly complex environments (e.g., larger grids, dynamic obstacles).
- **Human Alignment**: Assess how well agents adhere to human-preferred strategies, validated through simulated RLHF.

Example output (after running `evaluate_agent.py`):
- **Cumulative Reward Plot**: Shows faster convergence with human-aligned rewards.
- **Policy Heatmap**: Visualizes action preferences in a gridworld, highlighting interpretable strategies.

## Contributing
Contributions are welcome! To contribute:
1. Fork the repository.
2. Create a feature branch (`git checkout -b feature/new-feature`).
3. Commit changes (`git commit -m 'Add new feature'`).
4. Push to the branch (`git push origin feature/new-feature`).
5. Open a pull request.

Please ensure code follows PEP 8 standards and includes unit tests.


## Acknowledgments
- Inspired by coursework from CS329 (Fall 2025) at Stanford University.
- Built with [Gymnasium](https://gymnasium.farama.org/) and [PyTorch](https://pytorch.org/).
- Thanks to the open-source RL community for valuable resources and tools.

© 2025 Mayank Dahotre
