# Reinforcement_learning

This solution uses an actor-critic reinforcement learning model architecture, along with an infused timeseries, to help us predict the best action, based on the stock prices.

The possible actions are as follows: 
-Hold: This means that based on the price and projected profit, the trader should 1.hold a stock. 
-Sell: This means that based on the price and projected profit, the trader should 2.sell a stock. 
-Buy: This means that based on the price and projected profit, the trader should 3.buy a stock.

The model have two components: the actor and the critic. In our case, the network models that we will use will be neural networks. We will use the Keras package to create the neural networks. The reward function that we are looking to improve is the profit.

The actor takes as in put the state of the environment, then returns the best action, or a policy thatrefers to a probability distribution over actions. This is a natural way to perform reinforcement learning, as policies are directly returned as a function of the state.

The critic evaluates the actions returned by the actor-network. This is similar to the deep Q network. in the environment state and an action to return a score representing the value of taking that action given the state. The job of the critic is to compute an approximation, which is then used to update the actor in the direction of itsgradient. The critic is trained itself temporal difference algorithm.

These two networks are trained simultaneously. With time, the critic network is able to improve its Q_value prediction, and the actor also learns how to make better decisions,given the state.
