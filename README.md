# Google Play Store Data Preprocessing

## 1. Data Cleansing

### For the `App` Column:
- Removed **null values**.
- Stripped **leading/trailing spaces** from app names.
- Dropped **duplicate rows** as they could cause conflicts (since no app can have multiple attributes simultaneously).
- Removed **special characters**.

### For the `Category` Column:
- Removed this column as it was deemed **unnecessary** for this analysis.
![image](https://github.com/user-attachments/assets/1f25ce1a-c786-45e9-8b86-4b3b3ab4cc61)

### For the `Rating` Column:
- **Rounded** all values to the nearest base of 1.
- Replaced **null values** with the **mean** of the column.
  ![image](https://github.com/user-attachments/assets/009ae932-a7f9-41df-9569-8b116462add8)

- Handled **outliers** by ensuring the data falls within the valid range of 1 to 5.
![image](https://github.com/user-attachments/assets/4e705121-6243-4249-a607-6140ad7cff9c)

### For the `Size` Column:
- Handled **inconsistent data** by assigning **default values** to missing or incorrect entries (e.g., 'Varies with device').
- Removed **commas** as they could cause issues during processing.
- **Scaled** the units and **converted values** to numeric.
- ![image](https://github.com/user-attachments/assets/6eff259b-f413-4eee-9053-8824b2c081a4)

- Checked for **outliers** and visualized the distribution.
- ![image](https://github.com/user-attachments/assets/365659a3-07e5-4cc1-a5a4-864d08786b16)

- Used **Visualization** for **outlier detection**.
- ![image](https://github.com/user-attachments/assets/508985ec-c747-4daf-a0e5-d49182420593)
![image](https://github.com/user-attachments/assets/d19f2c9a-7f6c-4b46-87fd-e573650bb9d5)


### For the `Reviews` Column:
- Filled **null values** with the **median**.
- ![image](https://github.com/user-attachments/assets/1697f8a4-6582-42e5-bdd9-75de6e5fdc85)

- Used **stripplot** to visualize the distribution.
![image](https://github.com/user-attachments/assets/0112018a-bba7-42ff-834d-895b132bb3f8)

### For the `Installs` Column:
- Removed **inconsistent characters** (e.g., '+' and ',' symbols).
- Converted the values to **numeric** format.
- Handled missing values by replacing them with an initial value of **'0'**.
- ![image](https://github.com/user-attachments/assets/3bf41965-b564-4578-992a-cec479eff251)

### For the `Type` Column:
-Remove null values
-Replace zero values with free
![image](https://github.com/user-attachments/assets/c07f2657-aef5-41ce-83ed-b4dda672da14)

### For the `Price ` Column:
-Scale the values by removing '$' characters
![image](https://github.com/user-attachments/assets/1b7330bd-2c8c-4c95-8507-27255c13b14b)

-turning it to be numeric and for inconsistent values like Everyone it is replaced by 0 to say it is free
![image](https://github.com/user-attachments/assets/2f7ebf05-40c9-45c8-9ed2-0253e25dbd8a)

-Visualize the distribution of the values
![image](https://github.com/user-attachments/assets/2dcf2d8a-67bc-4419-b4a9-3dd75e4c91cc)

### For `Content Rating` Column:
-Drop the null values
![image](https://github.com/user-attachments/assets/9829350c-6e27-49f5-a6b8-7f633471ebc1)

-Drop unrated values
![image](https://github.com/user-attachments/assets/098da710-adc4-4c62-bd81-f9384f5aec94)


##For columns interactions:
check the consistent between the app price and app type as the free app must have the price 0 and the opposite
![image](https://github.com/user-attachments/assets/e7aaec30-d0e4-4860-8979-2a70797da622)


---

## Summary
The preprocessing steps aim to **clean**, **normalize**, and **transform** the dataset to ensure consistency and accuracy. This process removes inconsistencies and makes the data ready for analysis and further processing.

