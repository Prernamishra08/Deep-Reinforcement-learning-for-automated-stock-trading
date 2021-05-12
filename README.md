# Automated Stock Trading using Deep Reinforcement Learning

In this project, we experimented with different combinations of deep reinforcement learning algorithms and technical indicators on historical stock-market price data, to create automated stock trading and portfolio allocation strategy to maximize returns.

## Group Members:
- Sudharsan Asaithambi
- Haoxiang Zhang

## Code Structure:
- [Baseline model](notebooks/baseline.ipynb)
  - This model includes A2C, PPO and DDPG policies.
  - This model includes macd, boll_ub, boll_lb, rsi_30, cci_30, dx_30, close_30_sma, close_60_sma technical indicators obtained from stockstats pacakge.
- [Model without technical indicators](notebooks/Base-without_tech_indicators.ipynb)
  - This model is same as the baseline model, except it does not include any technical indicators. This model is to study the effectiveness of greatly reduced state space after excluding all technical indicators.
- [Model with additional technical indictor ATR](notebooks/Base+ATR.ipynb)
  - This model is same as the baseline model, except that a new technical indicator ATR is added.
- [Model with additional technical indicator EMA](notebooks/Base+EMA.ipynb)
  - This model is same as the baseline model, except that a new technical indicator EMA is added.
- [Ensemble model of all 5 policies](notebooks/all_5_policies.ipynb)
  - This ensemble model studies the effectiveness of ensembling all five deep reinforcement learning policies: A2C, PPO, DDPG, TD3 and SAC.
- [models.py](models.py)
  - This python file is created for the ensemble model of all 5 policies, where we created an ensemble function that deals with all 5 policies.


## Running instructions
- Following the steps in the jupyter notebook of each model.
- For the Ensemble Model of 5 Policies, please replace the finrl/model/models.py with our models.py file.

## References:
- [FinRL: A Deep Reinforcement Learning Library for Quantitative Finance](https://github.com/AI4Finance-LLC/FinRL)
- [Deep Reinforcement Learning for Automated Stock Trading: An Ensemble Strategy](https://papers.ssrn.com/sol3/papers.cfm?abstract_id=3690996)
- [OpenAI Spinning Up Deep RL Tutorial](https://spinningup.openai.com/en/latest/)
- [Application of Deep Reinforcement Learning on Automated Stock Trading](https://ieeexplore.ieee.org/document/9040728)
