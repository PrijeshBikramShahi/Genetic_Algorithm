# Genetic Algorithm for Solving Quadratic Equations

This project implements a genetic algorithm to find the solution for a quadratic equation of the form `3x^2 - 11x + 4` using binary encoding, uniform crossover, and mutation.

## Table of Contents
- [Introduction](#introduction)
- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [Algorithm Details](#algorithm-details)
  - [Fitness Function](#fitness-function)
  - [Binary Encoding](#binary-encoding)
  - [Uniform Crossover](#uniform-crossover)
  - [Mutation](#mutation)
- [Results](#results)
- [Contributing](#contributing)
- [License](#license)

## Introduction

This project demonstrates how to use genetic algorithms to solve a quadratic equation. The genetic algorithm evolves a population of binary-encoded individuals over several generations to find the best solution.

## Features

- Binary encoding of individuals
- Uniform crossover to produce offspring
- Mutation to introduce variability
- Roulette wheel selection for choosing parents
- Fitness function based on the quadratic equation `3x^2 - 11x + 4`

## Installation (Jupyter)

To run this project locally, follow these steps:

#1. Clone the repository:

   ```bash
   git clone https://github.com/yourusername/genetic-algorithm-quadratic-equation.git
   cd genetic-algorithm-quadratic-equation
   ```

#2. Create a virtual environment (optional but recommended):**

   It's good practice to use virtual environments to isolate project dependencies.

   ```bash
   python3 -m venv venv
   source venv/bin/activate   # On Windows use `venv\Scripts\activate`
   ```

3. **Install Jupyter Notebook and dependencies:**

   Install Jupyter Notebook and other dependencies using `pip`.

   ```bash
   pip install jupyter
   pip install -r requirements.txt
   ```

   Replace `requirements.txt` with the actual file containing your project dependencies, if applicable.

4. **Start Jupyter Notebook:**

   Launch Jupyter Notebook to run the genetic algorithm notebook.

   ```bash
   jupyter notebook
   ```

5. **Open the notebook:**

   Navigate to the `genetic_algorithm.ipynb` file in your Jupyter Notebook interface and open it to execute the genetic algorithm code.

6. **Run the genetic algorithm:**

   Follow the instructions within the notebook to run the genetic algorithm and view results.

7. **Shutdown Jupyter Notebook:**

   Once finished, you can shutdown Jupyter Notebook by pressing `Ctrl + C` in the terminal where it's running and confirming the shutdown.

8. **Deactivate virtual environment (if used):**

   ```bash
   deactivate   # Only if you used a virtual environment
   ```

By following these steps, you can set up and run your genetic algorithm project within a Jupyter Notebook environment. Adjust the instructions based on your specific project structure and dependencies.
