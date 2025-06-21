```py
import numpy as np

def linear_regression_gradient_descent(X: np.ndarray, y: np.ndarray, alpha: float, iterations: int) -> np.ndarray:
    m, n = X.shape
    theta = np.zeros((n, 1))  # Initialize coefficients to 0
    y = y.reshape(-1, 1)      # Ensure y is a column vector

    for _ in range(iterations):
        predictions = X @ theta
        errors = predictions - y
        gradient = (1 / m) * (X.T @ errors)
        theta = theta - alpha * gradient

    # Round the result to 4 decimal places
    return np.round(theta.flatten(), 4)

```
