# Monte Carlo Simulation of a Particle Detector Experiment

## 📝 Project Overview

This project provides a practical demonstration on Monte Carlo simulation techniques. It explains and implements two key methods for generating random numbers from custom probability distributions: **Analytical CDF Inversion** and **Numerical CDF Inversion**.

These techniques are then applied to simulate a particle physics experiment to determine the total energy deposited in a detector over a 10-second interval. The simulation highlights how computational modeling can provide valuable insights for experimental design and resource planning.

## 🔬 Key Concepts Demonstrated

* **Monte Carlo Method**: Using repeated random sampling to obtain numerical results.
* **Inverse Transform Sampling**: A fundamental method for generating random numbers from any probability distribution given its Cumulative Distribution Function (CDF).
    * **Analytical Inversion**: Used for simple, mathematically invertible CDFs (e.g., Exponential distribution).
    * **Numerical Inversion**: Used for complex CDFs that cannot be inverted analytically, implemented here using NumPy's `searchsorted` function.
* **Probability Distributions**:
    * **Poisson Distribution**: To model the random number of particles arriving at the detector.
    * **Custom PDF**: To model the random energy deposited by each individual particle.
* **Data Analysis**: Aggregating simulation results to plot a final distribution and calculate the probability of exceeding a specific energy threshold.

## 🛠️ Technologies & Libraries Used

* **Python**
* **NumPy**: For numerical operations and random number generation.
* **SymPy**: For symbolic mathematics to derive the CDF.
* **Matplotlib**: For data visualization and plotting results.

## 📊 Results

The primary goal was to simulate the total energy deposited in the detector over 100,000 separate 10-second experiments.

The simulation first calculates the number of particles for each experiment using a Poisson distribution. Then, it generates an energy value for each particle from a complex, custom probability distribution.

The final distribution of the total energy per 10-second interval is shown below:

![Final Energy Distribution](https://github.com/Shivam-Rathaur/Monte-Carlo-Simulation-of-a-Particle-Detector-Experiment/blob/main/Final%20Energy%20Distribution%20Image.png)

### Conclusion

The simulation found that there is approximately a **5.15% probability** that the total energy deposited in the detector will exceed 7.5 GeV in any given 10-second interval. This kind of quantitative result is crucial for scientists and engineers when designing detector components and planning for data acquisition resources.

## 🚀 How to Run

1.  Ensure you have Python and the required libraries installed:
    ```bash
    pip install numpy scipy sympy matplotlib jupyter
    ```
2.  Clone this repository.
3.  Open and run the `monte_carlo_simulation.ipynb` file in a Jupyter environment.
