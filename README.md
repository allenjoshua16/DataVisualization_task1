**Data Science Visualization and Exploratory Data Analysis (EDA)**

**Objective:**
Apply exploratory data analysis (EDA) techniques and create insightful visualizations using Python and R to compare and contrast their effectiveness.

**Introduction:**
This assignment involves performing Exploratory Data Analysis (EDA) on a dataset containing various numerical and categorical variables, focusing on understanding its structure, key patterns, and potential data quality issues.
The dataset was analyzed using two tools — Python (pandas, matplotlib) and R (tidyverse, ggplot2) — to demonstrate comparative visualization capabilities and analytical efficiency.

**Objectives:**

To clean and preprocess the dataset by identifying and handling missing values.

To compute descriptive statistics for numerical attributes (mean, median, standard deviation, quartiles).

To visualize key patterns through univariate and bivariate analysis.

To compare usability, interactivity, and visualization quality across Python and R implementations.

| **Aspect**                  | **Python (pandas, matplotlib)**                                                                                                         | **R (ggplot2, dplyr)**                                                                                                                                             |
| --------------------------- | --------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| **Usability**               | Highly intuitive for data wrangling and preprocessing. Functions like `df.describe()`, `groupby()`, and `fillna()` simplified analysis. | Data transformation was clear with `dplyr` verbs like `mutate()`, `summarise()`, and `group_by()`. Requires understanding of R syntax but efficient once mastered. |
| **Visualization Quality**   | `matplotlib` produced clean static visuals. Easy customization for labels, colors, and grid. Suitable for quick inspection plots.       | `ggplot2` offered publication-quality visuals with elegant aesthetics, layers, and themes. Ideal for presentation-level plots.                                     |
| **Handling Missing Values** | Used `isnull().sum()` and imputation via `fillna()`. Provided transparent handling and verification.                                    | Used `is.na()` detection and `mutate()` for replacement. Comparable functionality.                                                                                 |
| **Descriptive Statistics**  | `df.describe()` generated comprehensive statistics automatically, including percentiles.                                                | `summary()` and `summarise(across())` functions were used, providing similar output with slightly more syntax.                                                     |
| **Overall Strengths**       | Stronger integration for data cleaning and numerical analysis.                                                                          | Stronger in visual storytelling and graphical refinement.                                                                                                          |
| **Limitations**             | Static visuals (requires add-ons for interactivity).                                                                                    | Less efficient for large datasets compared to pandas.                                                                                                              |


**Summary:**
Python was more powerful in data manipulation and statistical summaries, while R excelled in data visualization aesthetics and interpretability.
Both tools were complementary — Python suited exploratory workflows; R excelled in presenting refined visuals.

**Findings**
3.1 Data Preprocessing

Both notebooks began with data loading and inspection using:

Python: pd.read_csv() followed by df.info() and df.isnull().sum().

R: read.csv() with checks using colSums(is.na(df)).

**Observations:**

Several columns contained missing or inconsistent values, which were handled using imputation or removal depending on attribute relevance.

Categorical columns were cleaned and standardized.

**Takeaway:**
Both tools effectively identified and managed missing data, ensuring a clean dataset for analysis.

**Descriptive Statistics**

Descriptive metrics were calculated to understand data distribution:

Python: Used df.describe() and added a custom median column.

R: Used summary() and summarise(across(where(is.numeric), list(mean = mean, sd = sd))).
| Metric                | Python (pandas)                           | R (summary)                            |
| --------------------- | ----------------------------------------- | -------------------------------------- |
| Mean, Median, Std Dev | Automatically computed with concise code. | Manually customized for each variable. |
| Quartiles (25%, 75%)  | Built-in percentile output.               | Extracted using `quantile()`.          |

**Visualization and Insights**
**Univariate Visualizations**

**Python:** Histograms and boxplots were created via matplotlib to examine distributions and outliers.

**R:** Used ggplot2::geom_histogram() and geom_boxplot() for smoother and aesthetically pleasing visuals.

**Insight:**
The distributions revealed skewness in certain variables and a few outliers that required interpretation.

**Bivariate Visualizations**

**Python:** Applied groupby() to analyze variable relationships, such as mean values across categories.

**R:** Used ggplot2::geom_bar() and geom_point() to illustrate categorical vs numerical interactions.

**Insight:**
Patterns indicated that some categories had significantly higher averages or frequencies, suggesting potential key drivers for further modeling or policy focus.

**Conclusion**

Through this assignment, both Python and R demonstrated their strengths in exploratory data analysis.

Key Insights from the Data:

The dataset contained measurable patterns with a few missing values effectively handled through imputation.

Descriptive statistics provided a clear view of the data’s central tendency and variability.

Visualizations exposed skewness, outliers, and group-level variations that are crucial for model design or reporting.

**Tool Evaluation:**

**Python:**

Best suited for data cleaning, exploration, and numerical summaries.

Rapid prototyping and scalable for large datasets.

**R:**

Best for communicating results visually using elegant and layered graphics.

Enhanced control over aesthetics and storytelling.

Overall Verdict:
A combined workflow leveraging Python’s analytical depth and R’s visualization finesse produces the most effective EDA outcomes.
Python ensures robust preprocessing and computation, while R transforms those insights into clear, publication-quality visuals.
