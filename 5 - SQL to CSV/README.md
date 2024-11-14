```
import pandas as pd
from sqlalchemy import create_engine

# Create a SQLAlchemy engine; adjust the URI based on your database
# engine = create_engine('sqlite:///example.db')  # SQLite example

# For MySQL: create_engine('mysql+pymysql://username:password@localhost/dbname')
engine = create_engine('mysql+pymysql://root:''@localhost/dj_small_shop')

# For PostgreSQL: create_engine('postgresql+psycopg2://username:password@localhost/dbname')

# Read a SQL query into a DataFrame
query = "SELECT * FROM category"
df = pd.read_sql_query(query, engine)
# print(df.head())

df.to_csv("D:\\dataset\\output_file.csv", index=False, sep=",")
```