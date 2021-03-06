# abm1559

Agent-based simulation environment for EIP 1559.

## Starting up

You can simply run the following commands in a terminal, assuming `pipenv` is installed on your machine.

```
git clone https://github.com/barnabemonnot/abm1559.git
cd abm1559
pipenv install
pipenv shell
jupyter lab
```

## Notebooks

### [Introduction to EIP 1559](https://github.com/ethereum/rig/blob/master/eip1559/eip1559.ipynb)

This notebook is available in the [Robust Incentives Group repository](https://github.com/ethereum/rig/blob/master/eip1559/eip1559.ipynb). We present a brief introduction to the rationale behind EIP 1559 as well as simulate the dynamics of the mechanism, including the basefee.

### [Stationary behaviour of EIP 1559](https://github.com/barnabemonnot/abm1559/blob/master/notebooks/stationary1559.ipynb)

A good benchmark case to test fee market proposals is stationary demand. In this notebook, we simulate random waves of new users who have value and costs all drawn from the same distribution. Users decide whether to transact or not based on their values and costs. We show that in this environment, the basefee always settles to a stationary level that depends on the congestion of the chain, i.e., how large the demand is.

### [Strategic users in EIP 1559](https://github.com/barnabemonnot/abm1559/blob/master/notebooks/strategicUser.ipynb)

Before reaching stationarity, or when demand varies rapidly, the market endures transitionary periods where either too many users or too few decide to transact. When there are too few, the basefee naturally decreases. But when there are too many, users have an incentive to increase their premiums during this transitionary period, until sufficiently many users are discouraged by the basefee level, at which point being strategic is no longer helpful. We investigate this dynamics and briefly compare the efficiency in both strategic and non-strategic cases.