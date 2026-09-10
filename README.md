# PA3_ECE2112

Please take note that the following code was used in order to access the Pandas library.

    import pandas as pd

To import the .csv file into the notebook, make sure that both the .csv and .ipynb files are in the same folder and make use of the following code.
The .csv file is expressed as "cars".

    cars = pd.read_csv('cars.csv')

---

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

From the newly created DataFrame, the module then specifies to only include columns "Model", "mpg", "cyl", "hp", and "gear" (which are the names of the columns found in the list). In doing so, .loc was used to call out the names of the rows and columns. The new list is expressed as "column_selection".

    column_selection = cars_6_to_10.loc[[0,5,6,7,8,9], ['Model', 'mpg', 'cyl', 'hp', 'gear']]
    column_selection

---

## B. MODEL LOOKUP

Objective: The goal of this problem was to make use of Boolean indexing in order to call out certain rows from the list.

Discussion:

The first thing the module instructs me to do is to display the complete row for "Toyota Corolla". Knowing that I can't just simply call out the name or the numerical index of "Toyota Corolla", I instead made it so that if the "Model" being called out was "Toyota Corolla", it would display the row containing the name of that "Model". The new list is expressed as "toyota_corolla".

    toyota_corolla = cars.loc[cars['Model']=='Toyota Corolla']
    toyota_corolla

The module then instructs me to do the same process with "Pontiac Firebird", but it can only display the columns "Model", "mpg", "hp", and "wt". I made use of the previous code, but I also indicated which columns should be called. The new list is expressed as "pontiac_firebird".

    pontiac_firebird = cars.loc[cars['Model']=='Pontiac Firebird', ['Model', 'mpg', 'hp', 'wt']]
    pontiac_firebird

---

## C. MULTI-MODEL SUBSETTING

Objective: The goal of this problem is to call out different car model names, but instead of calling them out by their row numbers, they were called out by using the actual model name.

Discussion:

The module instructs me to call out "Datsun 710", "Lotus Europa", and "Ferrari Dino". Knowing that I can not call them out using their row number, I first created a new list for the model names. This list is expressed as "columns".

    models = ['Datsun 710', 'Lotus Europa', 'Ferrari Dino']

I then made use of .loc to call out the model names through Boolean indexing. To call out the models list, I made use of .isin.

Additionally, the module also instructs me to only include the columns ""Model", "mpg", "cyl", "hp", and "gear". The new list is expressed as "Selected_cars".

    models = ['Datsun 710', 'Lotus Europa', 'Ferrari Dino']
    selected_cars = cars.loc[cars['Model'].isin(models), ['Model', 'mpg', 'cyl', 'hp', 'gear']]
    selected_cars

Since the module also asks for the shape of the list, make use of the following code.

    selected_cars.shape













    
