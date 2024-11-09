To read and write CSV files with `pandas`, you can use the `read_csv` and `to_csv` functions, respectively.

Here's an example of how to use them:

### Reading a CSV file
```python
import pandas as pd

# Reading the CSV file into a DataFrame
df = pd.read_csv("your_file.csv")

# Displaying the first few rows of the DataFrame
print(df.head())
```

### Writing to a CSV file
```python
# Saving the DataFrame to a new CSV file
df.to_csv("output_file.csv", index=False)  # Set `index=False` to exclude the index column
```

### Additional Options
- `sep=";"`: Specify a different separator, such as semicolon.
- `header=None`: No header row, so pandas will auto-generate column names.
- `columns=[...]`: Select specific columns to write.
- `encoding="utf-8"`: Specify encoding for special characters.

Let me know if you need more details on specific options!