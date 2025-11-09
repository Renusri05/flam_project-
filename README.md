# Flam-R&D-Assignment

## Parametric Curve Fitting – Finding θ, M, and X

The goal is to find the unknown parameters θ (Theta), M, and X for the given parametric equations, using the curve points provided for $$6 < t < 60$$.

***

## Approach

1. **Import libraries**  
   Utilized NumPy, Pandas, SciPy, and Matplotlib for data handling, numeric computations, optimization, and visualization.
2. **Load the dataset**  
   Used `xy_data.csv`, containing curve coordinates $$x, y$$.
3. **Assume parameter t**  
   Uniformly spaced between 6 and 60 based on assignment description, matching the number of dataset points.
4. **Parametric equations**
   - $$x = t\cos(\theta) - e^{M|t|}\sin(0.3t)\sin(\theta) + X$$
   - $$y = 42 + t\sin(\theta) + e^{M|t|}\sin(0.3t)\cos(\theta)$$
5. **Loss function**  
   L1 distance (sum of absolute differences) between predicted and observed values.
6. **Initial parameter guess**  
   Within provided boundaries.
7. **Optimization method**  
   "L-BFGS-B", with bounds reflecting assignment constraints.
8. **Error metrics**  
   Calculated MAE, RMSE, and per-point L1 distance for solution quality.
9. **Visualization**  
   Plotted actual vs fitted curve for validation.

***

## Mathematical Formulation

**Parametric Equations:**
$$
x = t\cos(\theta) - e^{M|t|}\sin(0.3t)\sin(\theta) + X
$$
$$
y = 42 + t\sin(\theta) + e^{M|t|}\sin(0.3t)\cos(\theta)
$$

***

## Final Outcomes

**Optimized Parameters:**  
Theta (degrees): 28.1184  
M: 0.021389  
X: 54.9008  
Optimization Success: True  
Total L1 Distance: 37865.0939  
Final L1 Distance (per point): 25.2434  

**Error Metrics:**  
MAE (x): 16.4221  
MAE (y): 8.8213  
Total MAE: 12.6217  
RMSE (x): 20.0540  
RMSE (y): 10.7559  
Total RMSE: 15.4050  

***

## Final Equation for Submission

$$
\left(
t*\cos(0.4908)-e^{0.021389\left|t\right|}\cdot\sin(0.3t)\sin(0.4908)+54.9008,\ 
42+t*\sin(0.4908)+e^{0.021389\left|t\right|}\cdot\sin(0.3t)\cos(0.4908)
\right)
$$

***


## References

- [Desmos online calculator](https://www.desmos.com/calculator)
- Assignment specification

***

