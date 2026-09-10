# PA3_ECE2112

Please take note that the following code was used in order to access the Pandas library.

    import pandas as pd

To import the .csv file into the notebook, make sure that both the .csv and .ipynb files are in the same folder and make use of the following code.
The .csv file is expressed as "cars".

    cars = pd.read_csv('cars.csv')

## A. POSITIONAL AND LABEL BASED SLICING

Objective: The goal of this problem was to display the list and shape, and to slice the imported .csv file.

Discussion:

To display the complete list of the .cvs file, simply call out the DataFrame variable "cars".

    cars

Additionally, to call out the shape of the .csv file, make use of the following code.

    cars.shape

* From now on, I will refer to the .csv file as a list.

The module states that we should create a new DataFrame containing rows 6 through 10, including the first row, from the list. In doing so, .iloc was used in order to call out the rows by their numerical indices. The new list is expressed as "cars_6_to_10".

    cars_6_to_10 = cars.iloc[[0,5,6,7,8,9]]
    cars_6_to_10

From the newly created DataFrame, the module then specifies to only include columns "Model", "mpg", "cyl", "hp", and "gear" (which are the names of the columns found in the list). In doing so, .loc was used to call out the names of the rows and columns. The new list is expressed as "coloumn_selection".

    column_selection = cars_6_to_10.loc[[0,5,6,7,8,9], ['Model', 'mpg', 'cyl', 'hp', 'gear']]
    column_selection






















    
