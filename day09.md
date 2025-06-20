```py
def calculate_covariance_matrix(vectors: list[list[float]]) -> list[list[float]]:
    if not vectors:
        return []

    num_features = len(vectors)
    num_observations = len(vectors[0])

    # Validate input dimensions
    for v in vectors:
        if len(v) != num_observations:
            raise ValueError("All features must have the same number of observations.")

    # Compute means of each feature
    means = [sum(v) / num_observations for v in vectors]

    # Initialize covariance matrix
    covariance_matrix = [[0.0 for _ in range(num_features)] for _ in range(num_features)]

    # Calculate covariance for each pair (i, j)
    for i in range(num_features):
        for j in range(num_features):
            cov = sum(
                (vectors[i][k] - means[i]) * (vectors[j][k] - means[j])
                for k in range(num_observations)
            ) / (num_observations - 1)
            covariance_matrix[i][j] = cov

    return covariance_matrix

```
