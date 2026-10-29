# Data Dictionary

## 1. Dataset Information

The dataset used in this assignment is `data/iris_frozen.csv`.

It comes from the Iris dataset available through the UCI Machine Learning Repository. The frozen local copy is used throughout the notebook to keep the analysis consistent.

| Item | Description |
|---|---|
| Dataset file | `iris_frozen.csv` |
| Format | CSV |
| Number of rows | 150 |
| Number of columns | 5 |
| Unit of analysis | One iris flower |
| Source | UCI Machine Learning Repository |
| DOI | 10.24432/C56C76 |
| License | CC BY 4.0 |

## 2. Column Descriptions

| Column name | Data type | Unit | Description |
|---|---|---|---|
| `sepal length (cm)` | Numeric | Centimeters | Length of the flower's sepal. |
| `sepal width (cm)` | Numeric | Centimeters | Width of the flower's sepal. |
| `petal length (cm)` | Numeric | Centimeters | Length of the flower's petal. |
| `petal width (cm)` | Numeric | Centimeters | Width of the flower's petal. |
| `target` | Categorical | Species name | Recorded species label: Setosa, Versicolor, or Virginica. |

## 3. Species Values

The `target` column contains three species labels:

- `setosa`
- `versicolor`
- `virginica`

Each observation belongs to one of these recorded groups.

## 4. Data Quality Checks

The notebook checks the following aspects of the dataset:

- Column names and data types.
- The expected number of rows and columns.
- Missing values.
- Exact duplicate rows.
- Minimum, maximum, mean, and standard deviation of numeric measurements.
- Positive measurement values.
- Possible unusual values using the interquartile range (IQR) method.
- The number of observations in each species group.

The audit finds no missing values in the frozen copy and identifies one exact duplicate row.

Values flagged by the IQR method are treated as observations that may need further review, rather than automatic data errors.

## 5. Variables Used in the Analysis

The four numeric columns are used to examine flower measurements.

The `target` column is used to group observations by species. The notebook compares the mean petal length between the three groups and creates a scatter plot of petal length against petal width.

For a future prediction task, `target` would be the outcome to predict. It should not be included among the input features.

## 6. Limitations

The dataset contains 150 observations, with 50 observations per species. The notebook does not establish whether these observations represent all iris flowers or all growing conditions.

The results are descriptive and apply to the frozen dataset. Unusual measurements should be checked in context before deciding whether they are errors.
