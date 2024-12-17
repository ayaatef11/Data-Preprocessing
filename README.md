Data Preprocessing for Google Play Store Dataset 📊🔧
Cleaned 'App' column:

Removed null values to ensure each app has a valid name.
Stripped spaces to avoid inconsistencies caused by leading or trailing spaces.
Dropped duplicate rows since there are no apps with multiple attributes at the same time.
Removed special characters to prevent any issues during analysis.
Removed 'Category' column:

The 'Category' column was deemed unnecessary for the current analysis, so it was dropped to simplify the dataset.
Processed 'Rating' column:

Rounded all rating values to the nearest integer to ensure consistency in rating scores.
Replaced null values with the mean of the existing ratings to fill in gaps.
Handled outliers by ensuring that all ratings fell within the valid range of 1 to 5.
Processed 'Size' column:

Handled inconsistent data entries (e.g., 'Varies with device') by assigning default values where necessary.
Removed commas that could cause parsing issues when converting to numeric values.
Scaled size units (e.g., MB, GB) to a standard unit for uniformity.
Converted all size values to numeric to facilitate easier analysis.
Detected and handled outliers using z-scores to maintain data quality and prevent bias.
Handled missing values in 'Reviews' column:

Replaced missing values with the median value of reviews to avoid skewing the data.
Used a strip plot to visualize the distribution of review counts and ensure they were normally distributed.
Processed 'Installs' column:

Removed inconsistent characters such as '+' and ',' which could lead to erroneous interpretations of the data.
Converted 'Installs' values to numeric to allow for easier comparison and analysis.
Replaced missing values with '0' to ensure no gaps in install data.
Final Data Quality and Integrity 🛠️✔️
After completing the above preprocessing steps, the dataset is now:

Clean and Consistent: Ensuring that all values are within a valid range, units are standardized, and no missing data remains unfilled.
Ready for Analysis: All categorical columns have been processed, numeric columns have been cleaned and converted, and outliers have been handled to provide a more reliable dataset for analysis.
Visualized: Distributions and outliers were analyzed using plots and statistical methods, ensuring transparency in the data cleaning process.
