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

Tkinter Example
```
import tkinter as tk
from tkinter.filedialog import askopenfilename

import pandas as pd

def open_excel():
    # Create a Tk object and hide the main window
    root = tk.Tk()
    root.withdraw()

    # Display the file dialog box and get the selected file path
    file_path = askopenfilename()

    # print(file_path)

    # Step 1: Load your Excel data
    try:
        data = pd.read_excel(file_path)

        print(data.head())
    except FileNotFoundError:
        print("{} not found".format(file_path))

root = tk.Tk()

root.geometry("400x400")

root.title("Read Excel")

open_btn = tk.Button(root, text="Open Excel File", command=open_excel)

open_btn.pack()

root.mainloop()
```
