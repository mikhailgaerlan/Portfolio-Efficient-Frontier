# Portfolio Optimization

A basic foundation of modern portfolio theory is the concept of the risk-return trade-off. The goal of a portfolio is to minimize the risk for a given expected return. This can be formulated as a multi-objective optimization problem where the goal is to minimize the risk while maximizing the return. In this notebook, I explore the efficient frontier of a two-stock portfolio consisting of Apple and Proctor & Gamble Stocks.

## Exact Calculation

The exact efficient frontier can be calculated under certain constraints. The efficient frontier of a two-stock can be shown here.

![frontier.png](Frontier)

## Evolutionary Algorithms

Evolutionary algorithms could potentially solve the problem more generally with any constraints including non-convex ones. For comparison, these images show the evolutionary algorithm to find the efficient frontier with the basic constraints used for the exact calculation of the efficient frontier.

The first plot shows the population in the decision space. Initially we start out with a uniform square and eventually converge to where the sum of the weights is equal to one.

![evolution.gif](Decision Space)

The second plot shows the population in the objective space. We eventually converge onto the efficient frontier with the constraint that the sum of the weights must equal one.

![evolution_fit.gif](Objective Space)


