```python
import pandas as pd

# file_name = 'D:\\sales_data.xlsx'
file_name = 'D:\\dataset\\sales_data.xlsx'

# Step 1: Load your Excel data
try:
    data = pd.read_excel(file_name)

    print(data.head())
except FileNotFoundError:
    print("{} not found".format(file_name))
```