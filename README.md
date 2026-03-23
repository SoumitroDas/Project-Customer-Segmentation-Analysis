# Mall Customer Segmentation Analysis

## Overview

This project performs customer segmentation analysis on mall customer data using machine learning clustering techniques. The analysis helps identify distinct customer groups based on demographic and behavioral characteristics, enabling targeted marketing strategies and personalized customer experiences.

## Dataset

The dataset contains 1,000 customer records with the following features:
- **CustomerID**: Unique identifier for each customer
- **Gender**: Customer gender (Male/Female)
- **Age**: Customer age in years
- **Annual Income (k$)**: Annual income in thousands of dollars
- **Spending Score (1-100)**: Customer spending behavior score (1-100 scale)

### Data Characteristics
- Age distribution focused on economically active ranges (primarily 22-49 years)
- Income values follow realistic career progression patterns
- Spending scores reflect behavioral variation across age and income groups
- Contains small amounts of missing values (3-6 per column) for data cleaning practice

## Methodology

### Data Preprocessing
1. **Missing Value Handling**: 
   - Gender: Mode imputation
   - Age, Income, Spending Score: Mean imputation
2. **Feature Engineering**: Created `Spending_Efficiency` ratio (Spending Score / Annual Income)
3. **Feature Selection**: Used Age and Spending_Efficiency for clustering
4. **Standardization**: Applied StandardScaler for optimal clustering performance

### Clustering Analysis
- **Algorithm**: K-Means Clustering
- **Optimal Clusters**: Evaluated using Silhouette Score analysis
- **Final Clusters**: 6 customer segments identified
- **Visualization**: PCA dimensionality reduction for 2D cluster visualization

## Results

### Cluster Profiles

The analysis identified 6 distinct customer segments:

| Cluster | Avg Age | Avg Annual Income (k$) | Avg Spending Score | Characteristics |
|---------|---------|------------------------|-------------------|-----------------|
| 0 | ~35 | ~50k | ~50 | Middle-aged, moderate income, balanced spending |
| 1 | ~45 | ~90k | ~30 | Older, high income, conservative spending |
| 2 | ~30 | ~30k | ~70 | Young, low income, high spending |
| 3 | ~40 | ~70k | ~40 | Middle-aged, good income, moderate spending |
| 4 | ~25 | ~40k | ~60 | Young adults, moderate income, high spending |
| 5 | ~55 | ~80k | ~20 | Senior, high income, low spending |

### Key Insights
- **Young High-Spenders (Cluster 2 & 4)**: Target with trendy, affordable products
- **Conservative High-Income (Cluster 1 & 5)**: Focus on quality, premium offerings
- **Balanced Middle-Class (Cluster 0 & 3)**: Value-driven marketing campaigns

## Files in Repository

- `Mall Customer Segmentation.ipynb`: Main analysis notebook
- `store_customers.csv`: Customer dataset
- `README.md`: This documentation file

## Dependencies

```python
numpy
pandas
matplotlib
seaborn
scikit-learn
kagglehub
```

## Installation & Usage

1. **Clone the repository**:
   ```bash
   git clone <repository-url>
   cd mall-customer-segmentation
   ```

2. **Install dependencies**:
   ```bash
   pip install numpy pandas matplotlib seaborn scikit-learn kagglehub
   ```

3. **Run the analysis**:
   - Open `Mall Customer Segmentation.ipynb` in Jupyter Notebook/Lab
   - Execute cells in order
   - View results and visualizations

## Analysis Workflow

1. **Data Loading**: Import customer data from CSV
2. **Exploratory Data Analysis**: Statistical summaries and visualizations
3. **Data Cleaning**: Handle missing values and outliers
4. **Feature Engineering**: Create derived features
5. **Clustering**: Apply K-means algorithm
6. **Evaluation**: Assess cluster quality with silhouette scores
7. **Visualization**: Plot clusters using PCA
8. **Interpretation**: Analyze cluster characteristics

## Future Enhancements

- Implement additional clustering algorithms (DBSCAN, Hierarchical)
- Add customer lifetime value analysis
- Include time-series spending patterns
- Develop recommendation system based on segments
- Create interactive dashboard for real-time segmentation

## Acknowledgment

This project was initially inspired by a course from Akaademy. 
However, the analysis has been significantly extended to include:
- Feature engineering
- Multiple clustering algorithms (K-Means, DBSCAN, GMM, Hierarchical)
- Hyperparameter tuning
- Comparative evaluation

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## License

This project is open source and available under the [MIT License](LICENSE).

## Contact

For questions or suggestions, please open an issue in this repository.