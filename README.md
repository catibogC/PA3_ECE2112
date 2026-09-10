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

