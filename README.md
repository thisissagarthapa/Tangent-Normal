# Curve Analysis with Tangents and Normals

## Overview

This project involves analyzing two different curves and visualizing their properties using Matplotlib in Python. The focus is on:
1. Finding the points where the tangent to the curve is parallel to the x-axis.
2. Determining the angle at which a curve intersects the x-axis.

## 1. Points Where Tangents Are Parallel to the X-Axis

### Curve Equation

The first curve is given by the equation:
\[ 4y = x^4 - 8x^2 \]

### Objective

Identify the points on the curve where the tangent is parallel to the x-axis. These points occur where the derivative of the curve is zero.

### Code

```python
import numpy as np
import matplotlib.pyplot as plt

# Define the range for x
x = np.linspace(-4, 4, 400)
# Define the curve equation
y = (x**4 - 8*x**2) / 4

# Points where the tangent is parallel to the x-axis
x_points = np.array([0, 2, -2])
y_points = (x_points**4 - 8*x_points**2) / 4

# Create the plot
plt.figure(figsize=(8, 6))
plt.plot(x, y, 'b-', label='Curve: 4y = x^4 - 8x^2')
plt.plot(x_points, y_points, 'ro', label='Points where tangent is parallel to x-axis')

# Labeling the graph
plt.xlabel('x')
plt.ylabel('y')
plt.title('Plot of the Curve 4y = x^4 - 8x^2')
plt.legend()
plt.grid(True)
plt.axhline(0, color='black',linewidth=0.5)
plt.axvline(0, color='black',linewidth=0.5)
plt.show()
