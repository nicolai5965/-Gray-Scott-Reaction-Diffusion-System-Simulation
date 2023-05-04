# Gray-Scott-Reaction-Diffusion-System-Simulation that I did in school
 
This repository contains a Python implementation of the Gray-Scott reaction-diffusion system simulation using both Explicit Euler Method (EEM) and the Spectral method.

## Environment Setup
The following libraries are imported to set up the environment:

* numpy
* matplotlib
* time
* numba (for just-in-time compilation)
* tqdm (for progress bars)
* IPython
* scipy
* matplotlib.animation

## EEM Implementation
The EEM function implements the Explicit Euler Method (EEM) for simulating the reaction-diffusion system. The function takes the following parameters:

* N: The size of the simulation grid
* D_A, D_B: Diffusion coefficients for A and B
* f, k: Feed and kill rates
* dt: Time step size
* time_steps: Total number of time steps
* dx: Space step size
It returns the time series of the A and B concentration grids.

## Spectral Method Implementation
The spectral function implements the spectral method for simulating the reaction-diffusion system. The function takes the following parameters:

* N: The size of the simulation grid
* dt: Time step size
* A, B: Concentration grids for A and B
* c1, c2, cA, cB: Coefficients for the spectral method
It returns the updated concentration grids for A and B.

## Running the Simulations
Both EEM and spectral method simulations can be run using the provided functions, EEM() and spectral_run() respectively, with the specified parameters.

## Visualization
The simulation results are visualized using matplotlib to display the concentration grids of A and B over time. Animated visualizations are created using matplotlib.animation and displayed using IPython's HTML method.

## Usage
To use this code, simply run the provided Python script. Ensure that you have the required libraries installed, including numpy, matplotlib, numba, tqdm, IPython, scipy, and matplotlib.animation.

# What is the Gray-Scott Reaction-Diffusion System
The Gray-Scott reaction-diffusion system is a mathematical model used to describe the behavior of two chemical species, A and B, as they diffuse and react over time in a spatial domain. This model is widely used to study pattern formation, self-organization, and complex spatiotemporal dynamics in various natural and artificial systems.

The model is governed by a set of partial differential equations (PDEs) that describe the evolution of concentrations of A and B over time:

∂A/∂t = D_A * ΔA - A * B^2 + f * (1 - A)

∂B/∂t = D_B * ΔB + A * B^2 - (k + f) * B

Here, A and B represent the concentrations of the chemical species, D_A and D_B are the diffusion coefficients, Δ denotes the Laplacian operator (representing the spatial diffusion), f and k are the feed and kill rates, and t represents time.

The Gray-Scott model exhibits a wide range of interesting patterns and behaviors, depending on the choice of parameters. Some of these patterns resemble natural phenomena like stripes, spots, and spirals, while others can form more complex and chaotic structures.

The code provided in this repository simulates the Gray-Scott reaction-diffusion system using two numerical methods: the Explicit Euler Method (EEM) and the Spectral method. These methods provide different trade-offs in terms of computational efficiency and accuracy, allowing users to explore various aspects of the Gray-Scott model and its fascinating patterns.



