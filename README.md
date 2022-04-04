# DATA1202 - Assignment 5
The code provided here will utilize Pandas within Python to manipulate data sheets. The features that are included in this code can add columns, concentrate and append the data, and rename and reorder the data within Python.

## Getting Started
The following instruction will allow you to successfully run this code on your computer.

### Prerequisistes
In order for to use this code you will be required to install Anaconda, Jupyter Notebook, Python, Pandas and Numpy. The steps in how to install these will be covered below.

#### Installing
To intall Jupyter Notebook and run the included Python code, follow the steps below.

1. Download the Python code and .csv file attached to this project.
2. The first step is to instal [Anaconda](https://docs.anaconda.com/anaconda/install/). After selecting the correct link for the system you are working on, follow the on-screen instructions to complete the installation.
3. Launch the Anaconda Navigator once it is installed and in the 'Home' tab find and install the Jupyter Notebook application.
4. When Jupyter Notebook launches in your browser locate the Python code and .csv file from your Downloads folder and upload them to the Jupyter homepage. Click on the imported file and you will now be in the Python code.

Included in the code are instructions on how to install Pandas and Numpy within Python.

To confirm that everything has been successful up to this point, run the first section of the code and you should get the following output on line 8:

![Screenshot 2022-04-04 105812](https://user-images.githubusercontent.com/102973887/161572291-703b42e0-5ca9-488d-a09a-67c38a06d877.png)


## Running the Tests
Using the command buttons at the top of Jupyter Notebook, you can run the selection section of code with the 'Run' key

![image](https://user-images.githubusercontent.com/102973887/161573393-2da7e20f-cb60-485b-920d-c79f0f5445b1.png)

### Breakdown of Tests

### Section 1 - Columns
Section 1 of this code will walk you through two methods on how to create new columns with the imported dataset in Python.
* We start with using the Pandas function pd.set_option to increase the number of columns and then importing the .csv file and assigning is the name File_1.
* Then a new dataframe is defined and raw_df where we use the Pandas function [pd.read_csv](https://pandas.pydata.org/docs/reference/api/pandas.read_csv.html) to attach the .csv file to this dataframe.
* In line 6 we created a new column "Benchmarks" and give is a baseline value of 70,000.
* Then we create another column "Salary_score" and compute the values by dividing the value in the "salary" column by the values in the "Benchmarks" column and [rounding](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.round.html?highlight=round#pandas.DataFrame.round) it to 2 decimal places.
* We output the top 5 rows of the dataset to see that we've successfully added these new columns and then we output all of the columns within the dataset

##### Dropping a Column
This code includes two methods you could use to get rid of a column from the dataset.

Method 1:
* Create a new dataframe from the existing datafame (Subset_raw_df) and only assign the newly created dataframe the desired columns (line 10).

Method 2:
* Using the Pandas function [pd.drop](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.drop.html?highlight=drop#pandas.DataFrame.drop) you can select the columns from the existing data set that you would like not to include (line 11).

### Section 2 - Concatenate and Append
In this section we will demonstrate how to create and combine two dataframes together.

##### Appending
1. We create an empty datafame called "append_to_df1" and we assign three values to it using the [pd.append](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.append.html?highlight=append#pandas.DataFrame.append) function
2. We assign these value to a new dataframe "df1" using the [pd.dataframe](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.html?highlight=dataframe#pandas.DataFrame) function and creating three columns for these imported values, "ID", "Name", and "Age"

##### Concatentating
1. First we repeat the steps above so that we not have two dataframes with different values.
2. The [pd.concat](https://pandas.pydata.org/docs/reference/api/pandas.concat.html?highlight=concat#pandas.concat) is used to combine the two dataframes into one dataframe that we've called "combined_df"

### Section 3 - Renaming and Reordering

##### Renaming
1. To demonstrate how to rename columns we will create a new dataframe from the existing dataframe and select three columns that we want to work with and output the  dataframe to see the columns.
2. Using the [pd.rename](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.rename.html?highlight=rename#pandas.DataFrame.rename) function we will change the name of the rank column and then output the dataframe to confirm that the name did change.

##### Reordering
1. After creating a new variable "column_names" we can use the [pd.reindex](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.reindex.html?highlight=reindex#pandas.DataFrame.reindex) to change the order than we want the columns to be displayed in.


### Section 4 - Groupby, Case WHEN and WHERE
This section will cover how to use the [Groupby](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.groupby.html?highlight=groupby#pandas.DataFrame.groupby) function, the Numpy [Case WHERE](https://numpy.org/doc/stable/reference/generated/numpy.where.html) function, and Case WHEN function using mathematical equations.

##### Groupby
1. We start again by creating a new dataframe from the .csv file that we've imported.
2. In line 33 you can see how we've used the pd.groupby function to order the data by 'rank' and by 'sex'.
3. We can then use the [pd.count](https://pandas.pydata.org/docs/reference/api/pandas.core.groupby.DataFrameGroupBy.count.html?highlight=count#pandas.core.groupby.DataFrameGroupBy.count) funciton to see how many and what type of values we sorted in the 'sex' column.

##### WHERE
1. After using groupby, we can use the '==' symbol to filter for all values in the 'sex' column that are equal to the value 'Male'.
2. When we output the first five rows on the dataframe we can see that the only value in the 'sex' column is 'Male'.
3. From this sorted data, we can do a number of calculations, the example provided shows whhat the average salary is using the [.mean](https://pandas.pydata.org/docs/reference/api/pandas.core.groupby.GroupBy.mean.html?highlight=mean#pandas.core.groupby.GroupBy.mean) function.

##### WHEN
Method 1: Numpy
1. In the first method we use the numpy .where funciton along with 'greater than or euq2la to' and 'less than' operators to assign two values, 'large' or 'small', to the values in the newly created column 'salary_rank'.

Method 2: Formulation
1. Similar to method 1 where we use '>=" and '<', here we use those along with [.loc](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.loc.html?highlight=loc#pandas.DataFrame.loc) to assign the 'salary' variables a value, 'large' or 'small', in the newly created column 'salary_rank'.

### Section 5 - Practice
In this section you can attempt to solve each problem by ustilizing the examples provided throughout the Python code file.

## Deployment
This code can be used to alter any dataset in .csv format with any number of columns and types of variables.

## Author
Mason McHugh - DATA1202 Assignment 5 - 04/04/22

## Acknowledgements
Original Code by: Omar Al-Trad
Institution: Durham College
