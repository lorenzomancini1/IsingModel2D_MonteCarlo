# Monte Carlo simulation of two-dimensional Ising model

Final project of the "Laboratory of Computational Physics mod. A" course at University of Padua during 2020/2021.

## Assignment and Description
The objective is to study, by Monte Carlo simulations, Ising-like modes on the square lattice and look at the behaviour of observables such as the specific heat, magnetisation and magnetic susceptibility, as a function of the temperature ed in particular in proximity of the critical point.


## Content
The Ising model is simulated through the Glauber dynamics: a random spin is selected and flipped with a probability _p_; one step of the Glauber dynamic consists in the previous operation repeated _L*L_ times. We can observe that the system is able to thermalize in a very few steps. Once reached equilibrium, data can be stored in order to study observables and particular phenomena such as:
- phase transition;
- ergodicity breaking;
- finite-size scaling;
- critical slowing down;

Furthermore, it can be seen that, at the critical temperature, we have a very high auto-correlation time (this is indeed related with critical slowing down). Thus, we should increase the number of steps for sampling data, but this would've required a lot of computational time. In order to overcome this, we implemented the Wolff algorithm, where, at each step, a cluster of spins is selected and flipped with probability equal to 1. In this way, at the critical point, the system is slightly slower in thermalization but the auto-correlation time decreases exponentially.

 
