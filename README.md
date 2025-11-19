# HW5 MLBA - Clustering Analysis of Stock Returns

## Overview
This notebook applies **K-means clustering** and **spectral clustering** to analyze stock return data, with a focus on industry composition and diversification insights.

## Key Findings

### – Sector Analysis
- Sectors show high co-movement during crises (e.g., 2008), suggesting industry labels alone are insufficient for diversification.

### K-means Clustering
- **Optimal k**: 7 (based on elbow method)  
- **Cluster sizes**: [20, 23, 44, 180, 60, 104, 2]  
- **Notable cluster**: Cluster 3 had the worst performance in Oct 2008 and the best in Mar 2009, indicating high volatility and rebound potential.

### Spectral Clustering
- **Similarity measure**: Absolute correlation \( |\rho_{ij}| \)  
- **Rationale**: Standard correlation can be negative, which is invalid for spectral clustering.  
- **Comparison with K-means**:
  - Spectral clustering groups stocks by co-movement, not return levels.
  - Results in more imbalanced clusters (e.g., a pure Energy cluster).
  - More relevant for risk diversification.



## Conclusion
K-means identifies performance-based groups, while spectral clustering highlights co-movement structure. Both methods offer complementary insights for portfolio construction and risk management.
