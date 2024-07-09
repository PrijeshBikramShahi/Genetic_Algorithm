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

### 1. Clone the repository:

   ```bash
   git clone https://github.com/PrijeshBikramShahi/Genetic_Algorithm.git
   cd genetic-algorithm-quadratic-equation
   ```

### 2. Create a virtual environment (optional but recommended):

   It's good practice to use virtual environments to isolate project dependencies.

   ```bash
   python3 -m venv venv
   source venv/bin/activate   # On Windows use `venv\Scripts\activate`
   ```

### 3. Install Jupyter Notebook and dependencies:

   Install Jupyter Notebook and other dependencies using `pip`.

   ```bash
   pip install jupyter
   pip install -r requirements.txt
   ```

   Replace `requirements.txt` with the actual file containing your project dependencies, if applicable.

### 4. Start Jupyter Notebook:

   Launch Jupyter Notebook to run the genetic algorithm notebook.

   ```bash
   jupyter notebook
   ```

### 5. Open the notebook:

   Navigate to the `genetic_algorithm.ipynb` file in your Jupyter Notebook interface and open it to execute the genetic algorithm code.

### 6. Run the genetic algorithm:

   Follow the instructions within the notebook to run the genetic algorithm and view results.

### 7. Shutdown Jupyter Notebook:

   Once finished, you can shutdown Jupyter Notebook by pressing `Ctrl + C` in the terminal where it's running and confirming the shutdown.

### 8. Deactivate virtual environment (if used):

   ```bash
   deactivate   # Only if you used a virtual environment
   ```
## Algorithm Details
### Fitness Function
  The fitness function evaluates how close a given solution is to the actual solution of the quadratic equation:
```bash
  def fitness_function(x):
      x_real = decode_binary(x)
      return abs(3*x_real**2 - 11*x_real + 4)
```

### Binary Encoding
  Each individual in the population is represented as a binary string:

```bash
  def decode_binary(x):
      sign_bit = int(x[0])
      integer_part = int(x[1:4], 2)
      fractional_part = int(x[4:], 2) / 2**6  # Adjust the power to match the number of fractional bits
      x_real = (-1)**sign_bit * (integer_part + fractional_part)
      return x_real
```
### Uniform Crossover
  Uniform crossover creates two offspring from two parents by randomly selecting each bit from either parent:

```bash
  def uniform_crossover(parent1, parent2):
      child1 = []
      child2 = []
      for i in range(len(parent1)):
          if random.random() < 0.5:
              child1.append(parent1[i])
              child2.append(parent2[i])
          else:
              child1.append(parent2[i])
              child2.append(parent1[i])
      return ''.join(child1), ''.join(child2)
```
### Mutation
  Mutation introduces random changes to an individual to maintain genetic diversity:

```bash
def mutate(individual):
    mutated_individual = list(individual)
    for i in range(bit_len):
        if random.random() < mut_rate:
            mutated_individual[i] = '0' if individual[i] == '1' else '1'
    return ''.join(mutated_individual)
```
### Results
  After running the genetic algorithm, the best solution found will be printed along with its fitness value:
  
```text
Best individual found: 0010011101
Decoded best solution: x = 2.453125, Fitness = 4.930908203125
```


