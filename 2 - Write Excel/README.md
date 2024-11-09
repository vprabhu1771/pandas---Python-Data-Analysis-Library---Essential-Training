You can use the `pandas` library in Python to create and write data to an Excel file easily. Here’s a basic example:

1. Install the required package:
   ```bash
   pip install pandas openpyxl
   ```

2. Write a Pandas DataFrame to an Excel file:

```python
import pandas as pd

# Create a sample DataFrame
data = {
    'Name': ['Alice', 'Bob', 'Charlie'],
    'Age': [24, 27, 22],
    'City': ['New York', 'Los Angeles', 'Chicago']
}
df = pd.DataFrame(data)

# Write the DataFrame to an Excel file
df.to_excel('output.xlsx', index=False)
```

In this code:
- `index=False` prevents Pandas from writing row indices to the Excel file.
- The output Excel file will be saved as `output.xlsx` in the current working directory.

### Additional Options
If you want to specify a sheet name or add multiple sheets, you can use `ExcelWriter`:

```python
with pd.ExcelWriter('output.xlsx', engine='openpyxl') as writer:
    df.to_excel(writer, sheet_name='Sheet1', index=False)
    df.to_excel(writer, sheet_name='Sheet2', index=False)
```

This will create an Excel file with two sheets, both containing the same DataFrame data.