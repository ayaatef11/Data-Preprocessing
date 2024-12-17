# Google Play Store Data Preprocessing 📊

## 1. Data Cleansing 📈

### For the `App` Column:📝
- Removed **null values**.
  
  ![image](https://github.com/user-attachments/assets/59c11079-cd90-4f27-921a-d0177512d3f5)

- Stripped **leading/trailing spaces** from app names.
  ![image](https://github.com/user-attachments/assets/1235e882-4a5a-4527-a5c8-e26126ff2ce7)

- Dropped **duplicate rows** as they could cause conflicts (since no app can have multiple attributes simultaneously).
  
- ![image](https://github.com/user-attachments/assets/ea94f810-5112-4cc9-ad8a-50b555da6cf8)

- Removed **special characters**.

![image](https://github.com/user-attachments/assets/a987de02-c108-4026-8984-05c8d65297c6)

### For the `Category` Column:🗂️
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
- Remove null values
- Replace zero values with free
![image](https://github.com/user-attachments/assets/c07f2657-aef5-41ce-83ed-b4dda672da14)

### For the `Price ` Column:
- Scale the values by removing '$' characters
![image](https://github.com/user-attachments/assets/1b7330bd-2c8c-4c95-8507-27255c13b14b)

- turning it to be numeric and for inconsistent values like Everyone it is replaced by 0 to say it is free
![image](https://github.com/user-attachments/assets/2f7ebf05-40c9-45c8-9ed2-0253e25dbd8a)

- Visualize the distribution of the values
![image](https://github.com/user-attachments/assets/2dcf2d8a-67bc-4419-b4a9-3dd75e4c91cc)

### For `Content Rating` Column:
- Drop the null values
![image](https://github.com/user-attachments/assets/9829350c-6e27-49f5-a6b8-7f633471ebc1)

- Drop unrated values
![image](https://github.com/user-attachments/assets/098da710-adc4-4c62-bd81-f9384f5aec94)

### For the `Genres' Column:
-Filter Genres that contain numbers like 'February 11, 2018' cell

![image](https://github.com/user-attachments/assets/9854fb9f-d0ce-4baa-b5ed-9c0dd0ec59d7)

-Transform Genres into multiple columns

![image](https://github.com/user-attachments/assets/e477a731-c539-4713-983b-03c0d2209232)


### For the `last updated` column:
- use feature splitting to split it into multiple columns
![image](https://github.com/user-attachments/assets/b4997347-73c1-42dc-a016-bb48ca258118)
- convert the column to be of type date and the inconsistent values are replaced by nulls

  ![image](https://github.com/user-attachments/assets/6223efb9-ba2b-4f20-8f50-440cd45e1311)
- remove null values
- ![image](https://github.com/user-attachments/assets/541d8e79-7f90-4994-87b9-62826792d18d)

### For the `Android ver` column:
- drop null values
  ![image](https://github.com/user-attachments/assets/28ca9a5c-a8a7-4b5f-9765-4d72b8feaee0)

- replace inconsistent vlaues with nulls and then removes them
- ![image](https://github.com/user-attachments/assets/7f207582-8a26-4353-9d47-e926ca8c2c9c)
- use feature splitting to split it
- ![image](https://github.com/user-attachments/assets/71c00bfb-f501-4fcd-8735-b7540719dda3)

### For the `current ver` column:
- make it match a specific expression
  ![image](https://github.com/user-attachments/assets/e7cf6643-6142-4908-a24e-a052ab4fe465)


### For the interactions:
check the consistent between the app price and app type as the free app must have the price 0 and the opposite

![image](https://github.com/user-attachments/assets/e7aaec30-d0e4-4860-8979-2a70797da622)

---

## Summary
The preprocessing steps aim to **clean**, **normalize**, and **transform** the dataset to ensure consistency and accuracy. This process removes inconsistencies and makes the data ready for analysis and further processing.

