# DataProfile Library

## Description
*The main function of this library is to generate a Data Profile in a database. For this, it takes a DataFrame as input and analyzes basic aspects such as the number of unique records, duplicates, null and empty data, among others. Each of these points is analyzed for each of the columns of the DataFrame.*

### Principal Features

- **Count:** Count the number of records. Returns a numeric value.

- **Count Distinct:** Count the number of distinct records. Returns a numeric value.

- **Unique:** Count the unique records. Returns a numeric value.

- **ID Probability:** Calculate the probability that the column is an ID. Evaluates the data type, the name of the column, the number of unique IDs, the amount of empty and null records, and estimates a probability. Returns a percent.

- **Email Probability:** Find the probability that the column contains emails. Counts the number of "@" symbols and valid domains, then estimates a probability. Returns a percent.

- **Duplicate:** Count the duplicate records per column. Returns a numeric value.

- **Numeric:** Determine whether the data type is numeric. Returns `True` only if all records in the column are numeric.

- **Letter:** Determine whether the data type is a string. Returns `True` only if all records in the column are strings.

- **Bool:** Determine whether the data type is boolean. Returns `True` only if all records in the column are booleans.

- **Empty:** Count the number of empty records per column. Returns a numeric value.

- **Zero:** Count the number of zeros per column. Returns a numeric value.

- **Null:** Count the number of null records per column. Returns a numeric value.


### Install Requires

- Pandas
- Numpy
- Prettytable

### Functions

- **dataprofile(DF):** *This is the main function. It takes a DataFrame as input and returns another one with all the features described above.*


### How to Start

1. **Install the library using pip:**
    ```bash
    pip install dataprofile
    ```


2. **Import the dataprofile library:**
    ```python
    import dataprofile as dp
    ```


3. **Create or import a DataFrame:**
    In this case, use `read_csv` from Pandas to import a CSV and create a DataFrame.
    ```python
    import pandas as pd

    def READ_CSV(file_path):
        return pd.read_csv(file_path, sep=",", encoding='latin-1')

    FILE = READ_CSV('base-primer-relev-dispositivos.csv')
    ```


4. **Use the `dataprofile` function on a DataFrame:**
    ```python
    print(dp.dataprofile(FILE))
    ```

