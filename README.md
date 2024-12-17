# Google Play Store Data Preprocessing

## 1. Data Cleansing

### For the `App` Column:
- Removed **null values**.
- Stripped **leading/trailing spaces** from app names.
- Dropped **duplicate rows** as they could cause conflicts (since no app can have multiple attributes simultaneously).
- Removed **special characters**.

### For the `Category` Column:
- Removed this column as it was deemed **unnecessary** for this analysis.

### For the `Rating` Column:
- **Rounded** all values to the nearest base of 1.
- Replaced **null values** with the **mean** of the column.
- Handled **outliers** by ensuring the data falls within the valid range of 1 to 5.

### For the `Size` Column:
- Handled **inconsistent data** by assigning **default values** to missing or incorrect entries (e.g., 'Varies with device').
- Removed **commas** as they could cause issues during processing.
- **Scaled** the units and **converted values** to numeric.
- Checked for **outliers** and visualized the distribution.
- Used **z-scores** for **outlier detection**.

### For the `Reviews` Column:
- Filled **null values** with the **median**.
- Used **stripplot** to visualize the distribution.

### For the `Installs` Column:
- Removed **inconsistent characters** (e.g., '+' and ',' symbols).
- Converted the values to **numeric** format.
- Handled missing values by replacing them with an initial value of **'0'**.

---

## Summary
The preprocessing steps aim to **clean**, **normalize**, and **transform** the dataset to ensure consistency and accuracy. This process removes inconsistencies and makes the data ready for analysis and further processing.

