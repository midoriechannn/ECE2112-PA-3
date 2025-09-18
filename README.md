# ECE2112 PA #3 | DOCUMENTATION 

**First, I placed the `cars.csv` file within the same directory as the notebook named `"ECE2112_PA3"`.** 

**1. PROBLEM 1: Save your file as Surname_Pandas-P1.py**

**Using knowledge obtained from the experiment and demonstrations:**

   **a. Load the corresponding .csv file into a data frame named cars using pandas**

   **b. Display the first five and last five rows of the resulting cars.** 

**CODE** 

```
#Imports the pandas library 
import pandas as pd 
```
▸ Syntax for importing the pandas library.

```
#Loads the .csv file into a data frame named 'cars'
cars = pd.read_csv('cars.csv') 
```
▸ Loading the `cars.csv` file which contains dataframe and stored to a variable named `cars`. 

```
#Prints the first 5 rows of the data from the data frame named 'cars'
cars.head() 
```
▸ Printing the first five rows by using a function `.head(default=5)`. 

**OUTPUT 1** 

```
|    | Model             |   mpg |   cyl |   disp |   hp |   drat |    wt |   qsec |   vs |   am |   gear |   carb |
|---:|:------------------|------:|------:|-------:|-----:|-------:|------:|-------:|-----:|-----:|-------:|-------:|
|  0 | Mazda RX4         |  21.0 |     6 |  160.0 |  110 |   3.9  | 2.62  |  16.46 |    0 |    1 |      4 |      4 |
|  1 | Mazda RX4 Wag     |  21.0 |     6 |  160.0 |  110 |   3.9  | 2.875 |  17.02 |    0 |    1 |      4 |      4 |
|  2 | Datsun 710        |  22.8 |     4 |  108.0 |   93 |   3.85 | 2.32  |  18.61 |    1 |    1 |      4 |      1 |
|  3 | Hornet 4 Drive    |  21.4 |     6 |  258.0 |  110 |   3.08 | 3.215 |  19.44 |    1 |    0 |      3 |      1 |
|  4 | Hornet Sportabout |  18.7 |     8 |  360.0 |  175 |   3.15 | 3.44  |  17.02 |    0 |    0 |      3 |      2 |

```

```
#Printing the last five rows of the data frame named 'cars'
cars.tail()
```
▸ Printing the last five rows by using a function `.tail(default=5)`. 

**OUTPUT 2** 

```
|    | Model          |   mpg |   cyl |   disp |   hp |   drat |    wt |   qsec |   vs |   am |   gear |   carb |
|---:|:---------------|------:|------:|-------:|-----:|-------:|------:|-------:|-----:|-----:|-------:|-------:|
| 27 | Lotus Europa   |  30.4 |     4 |   95.1 |  113 |   3.77 | 1.513 |   16.9 |    1 |    1 |      5 |      2 |
| 28 | Ford Pantera L |  15.8 |     8 |  351   |  264 |   4.22 | 3.17  |   14.5 |    0 |    1 |      5 |      4 |
| 29 | Ferrari Dino   |  19.7 |     6 |  145   |  175 |   3.62 | 2.77  |   15.5 |    0 |    1 |      5 |      6 |
| 30 | Maserati Bora  |  15   |     8 |  301   |  335 |   3.54 | 3.57  |   14.6 |    0 |    1 |      5 |      8 |
| 31 | Volvo 142E     |  21.4 |     4 |  121   |  109 |   4.11 | 2.78  |   18.6 |    1 |    1 |      4 |      2 |
```

**Saves Problem #1 as.py File** 

```
code1 = """" 
#Imports the pandas library 
import pandas as pd 

# Loads the .csv file into a data frame named 'cars'
cars = pd.DataFrame(pd.read_csv('cars.csv'))

# Prints the first and last five rows of the data frame named 'cars'
print(cars.head())
print(cars.tail())
"""

# Creates a python file in write mode
file1 = open('Macabenta_Pandas-P1.py', 'w')
# Writes the content of 'code1' into 'file1'
file1.write(code1)
# Close the file
file1.close() 
```
▸ This Python script demonstrates basic use of pandas for data handling.

▸ It imports the pandas library.

▸ Reads the cars.csv file into a DataFrame named cars.

▸ Displays the first five and last five rows of the dataset using head() and tail().

▸ The script is written and saved programmatically using Python's file handling functions (open, write, close). 

**PROBLEM 2: Save your file as Surname_Pandas-P2.py**

**Using the dataframe cars in problem 1, extract the following information using subsetting, slicing and indexing operations.**

**&nbsp;&nbsp;&nbsp;&nbsp;a. Display the first five rows with odd-numbered columns (columns 1, 3, 5, 7…) of cars.**

**&nbsp;&nbsp;&nbsp;&nbsp;b. Display the row that contains the ‘Model’ of ‘Mazda RX4’.**

**&nbsp;&nbsp;&nbsp;&nbsp;c. How many cylinders (‘cyl’) does the car model ‘Camaro Z28’ have?**

**&nbsp;&nbsp;&nbsp;&nbsp;d. Determine how many cylinders (‘cyl’) and what gear type (‘gear’) do the car models ‘Mazda RX4 Wag’, ‘Ford Pantera L’ and ‘Honda Civic’ have.**

**CODE** 

```
#Imports the pandas library 
import pandas as pd 
```
▸ It imports the pandas library.
```
#Loads the .csv file into a data frame named 'cars'
cars = pd.read_csv('cars.csv') 
```
▸ Loading the `cars.csv` file which contains dataframe and stored to a variable named `cars`. 

```
#Performs the slicing to print the first five rows with odd-numbered columns of data frame named 'cars'
cars.iloc[:5,1::2] 
```
▸ Displays the first and last five rows using head() and tail().

▸ Performs slicing with cars.iloc[:5, 1::2] to show the first five rows with only odd-numbered columns.


**OUTPUT 1**

|    |   mpg |   disp |   drat |   qsec |   am |   carb |
|---:|------:|-------:|-------:|-------:|-----:|-------:|
|  0 |  21   |    160 |   3.9  |  16.46 |    1 |      4 |
|  1 |  21   |    160 |   3.9  |  17.02 |    1 |      4 |
|  2 |  22.8 |    108 |   3.85 |  18.61 |    1 |      1 |
|  3 |  21.4 |    258 |   3.08 |  19.44 |    0 |      1 |
|  4 |  18.7 |    360 |   3.15 |  17.02 |    0 |      2 |

```
#Performs boolean indexing to display the row that contains 'Mazda RX4'
cars[cars['Model'] == 'Mazda RX4']
```

▸ Uses boolean indexing `cars[cars['Model'] == 'Mazda RX4']` to filter and display the row where the Model column equals `"Mazda RX4"`. 

**OUTPUT 2** 
|    | Model     |   mpg |   cyl |   disp |   hp |   drat |   wt |   qsec |   vs |   am |   gear |   carb |
|---:|:----------|------:|------:|-------:|-----:|-------:|-----:|-------:|-----:|-----:|-------:|-------:|
|  0 | Mazda RX4 |    21 |     6 |    160 |  110 |    3.9 | 2.62 |  16.46 |    0 |    1 |      4 |      4 |

```
# Performs boolean indexing to display the row of 'Camaro Z28' and columns of 'Model' and 'cyl' 
cars.loc[cars['Model'] == 'Camaro Z28', ['Model', 'cyl']]
```
▸ Uses `cars.loc[cars['Model'] == 'Camaro Z28'`, `['Model', 'cyl']]` to display only the Model and cyl columns for the row where `Model = 'Camaro Z28'`. 

**OUTPUT 3** 

|    | Model      |   cyl |
|---:|:-----------|------:|
| 23 | Camaro Z28 |     8 |  

```
#Stores the 'Model' 
condition = (cars['Model'] == 'Mazda RX4 Wag') | (cars['Model'] == 'Ford Pantera L') | (cars['Model'] == 'Honda Civic')

# Performs boolean indexing to display the given 'Model' and columns of 'cyl' and 'gear'
cars.loc[condition,['Model', 'cyl', 'gear']] 
```

▸ Filters rows where Model matches any of the three given values and displays only the Model, cyl, and gear columns. 

**OUTPUT 4** 

|    | Model          |   cyl |   gear |
|---:|:---------------|------:|-------:|
|  1 | Mazda RX4 Wag  |     6 |      4 |
| 18 | Honda Civic    |     4 |      4 |
| 28 | Ford Pantera L |     8 |      5 | 


**Saves Problem #2 as .py File** 

▸ The entire code block is stored in the variable code2 as a string.

▸ file2 = open('Macabenta_Pandas-P2.py', 'w')

▸ Creates (or overwrites) a file named Macabenta_Pandas-P2.py in write mode.

▸ Returns a file object stored in the variable file2.

▸ file2.write(code2) writes the contents of code2 into the file.

▸ file2.close() closes the file, saving the changes and freeing system resources.



