# Reinforcement Learning for Stock Trading

A comprehensive framework for applying various reinforcement learning algorithms to optimize stock market trading strategies using historical market data.

## Project Overview

This project implements multiple reinforcement learning algorithms to develop and evaluate automated trading strategies for the stock market. By leveraging historical stock data, the system learns to make buy, sell, and hold decisions with the goal of maximizing risk-adjusted returns.

## Features

- **Multiple RL Algorithms**: Implements and compares popular RL algorithms including:
  - Proximal Policy Optimization (PPO)
  - Advantage Actor-Critic (A2C)
  - Deep Deterministic Policy Gradient (DDPG)
  - Twin Delayed DDPG (TD3)
  - Soft Actor-Critic (SAC)

- **Customizable Environment**: Flexible market simulation environment with:
  - Configurable observation space (price data, technical indicators, etc.)
  - Adjustable reward functions (returns, Sharpe ratio, drawdown penalties)
  - Realistic constraints (transaction costs, slippage modeling)

- **Comprehensive Evaluation**: Performance metrics including:
  - Cumulative returns
  - Sharpe and Sortino ratios
  - Maximum drawdown
  - Win rate and profit factor
  - Benchmark comparisons (Buy & Hold, Moving Average strategies)

- **Visualization Tools**: Includes tools for:
  - Trading performance visualization
  - Algorithm learning curves
  - Policy action distribution analysis

## Getting Started

### Prerequisites

```
python >= 3.8
numpy
pandas
tensorflow >= 2.5.0 or pytorch >= 1.9.0
gym >= 0.21.0
matplotlib
seaborn
yfinance (for data acquisition)
```

## Experiments and Results

Our experiments show that:

- SAC algorithm generally outperform every RL algorithm in terms of risk-adjusted returns.
- Incorporating technical indicators as features improves performance across all algorithms
- Custom reward functions that penalize drawdowns lead to more conservative but more stable strategies
- Higher trading frequencies generally result in diminishing returns when accounting for transaction costs

## Future Work

- Integration with real-time market data APIs
- Portfolio optimization across multiple assets
- Incorporation of sentiment analysis and alternative data sources
- Improving sample efficiency through imitation learning
- Adapting to changing market regimes using meta-learning
- Integrating Transformer Architecture to predict future actions.

## Acknowledgments

- [OpenAI Gym](https://github.com/openai/gym) for the reinforcement learning framework
- [Yahoo Finance](https://finance.yahoo.com/) for historical market data
- [Stable Baselines3](https://github.com/DLR-RM/stable-baselines3) for RL algorithm implementations
