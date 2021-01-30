# Day 4 Summary :

<img src="https://d6vdma9166ldh.cloudfront.net/media/images/4594dcf8-a8c5-4fa7-a6d4-bab2c9081041.jpg" alt="">

## [Day 4 Lecture](https://youtu.be/cnr5FY9rkTA)  👈👈 

**DAY 04 AGENDA |**
- Pandas
- Seaborn

## Pandas:
**Introduction to Pandas:**

- Pandas is a fast, powerful, flexible and easy to use open-source data analysis and manipulation tool, built on top of the Python programming language.
- We will be looking at 1D  Series and 2D DataFrames, Pandas functions, slicing and indexing.
- Indexing in series data is stored in an array in explicit goes from a start index to end index and it is also having an implicit index that goes from a start index to end index -x1.
- Data frame can be constructed from series and dictionary.
- If the explicit index has numbers, then no implicit indexing is assigned as default because it can cause conflicts.
- Implicit index goes ilocfunction and explicit function goes with loc which is user-defined.
- Pandas can read many types of database.
- DataFrames can be converted to NumPy as it is very helpful.

## Hands-on session - Pandas
**Basic Overview**

- To use Pandas, we need to import it in our notebook using: import pandas
- We have functions like type (), indexing, iloc(), loc(), slicing, etc
- We can access these functions using the dot operator for e.g. pd.Series([2,4,6,8])etc.
- Note: We cannot use pandas everywhere so we will assign it an alias name.
- To do that we will simply write: import pandas as pd
- Now in this notebook, we can use the module by the name as pd.
- Naming it as pd is widely used and preferred everywhere.

## Data Creation Using Series:

- We will now create a population.
- To create a data with values data = pd.Series( [ ' a ' , ' b ' , ' c ' ] , index = [ 1 , 3 , 5 ] )

## To Print Series

      population_dict&nbsp;={
                 "California":38335215,
                 "Texas":19665634,
                 "New&nbsp;york":16545697,
                 "Florida":78954632,
                 "Illinois":12354698
             }
        population=pd.Series(population_dict)
        population

**For 1d  data, here it prints as below:**

               California&nbsp;   38335215
               Texas&nbsp;        19665634
               New York&nbsp;     16545697
               Florida&nbsp;      78954632
               Illinois&nbsp;     12354698
               dtype: int64
        
- Dictionary can be converted into series
- Series is been stored as an array with implicit and explicit indices. An explicit index is given by sure
- The implicit index is given by Python.
- A single value can be broadcasted in the different index as mentioned in Series.
- Pandas is highly used in used for Machine Learning programs.

## Data Creation Using DataFrames 

- Column attribute used for labelling data in DataFrame
- Data Frame can be created using dictionary e.g.:
            convert(x):
            if x=="Y":
                return 1
            else:
                return 0
   
- Column names cannot be overwritten while creating data using a dictionary as data gets corrupt.
- Implicit index modifies data by mentioning it specifically e.g.:

             pd.Series( {2:'a' , 1:'b' , 3:'c'} )
             2 a
             1 b
             3 c
             dtype: object

- Code  df.columns=["Darshan","Ingle"]    this will print all the column names for us.
- DataFrame function can be printed in different formats like as list, array, series , NumPy, etc using codes such as data, data. Values, print(population), etc
- Indexers: loc and iloc e.g.:
            data.pd.Series(['a','b','c'], index=[1,3,5])
            1   a
            3   b
            5   c
            dtype: object
                
            data.loc[1:3] #loc will take explicit index similarly iloc function can be performed.
             # Output will be
            1   a
            3   b
            dtype: object
                
## Some basic functions such as 

- data['Project Score'].sum()  -   //this function will give the sum the numeric values
- data ['Project Score']. mean ()  -  //this function will give the mean the numeric values
- data.shape  -   //this function will give the shape of the numeric values
- data.head() -  //this function will print the first 5 rows of data set
- data.describe()  -  // used to view some basic statistical details
- data.tail() - // this function will print the last 5 rows of data set             
              
## Seaborn:
**Introduction to Seaborn:**

- Seaborn is a library for making statistical graphics in Python. It builds on top of matplotlib and integrates closely with pandas data structures. Seaborn helps you explore and understand your data.
- It is highly used for data visualization many functions can be performed using seaborn.
- Functions like Distplot, Pairplot, etc. are used for numeric data.
- Barplot, Boxplot, etc are used for categorical data 
 
## Hands-on session - Seaborn

**Basic Overview**

- To use Seaborn, we need to import it in our notebook using: import seaborn
- We have functions like type (),  etc
- Note: We cannot use seaborn everywhere so we will assign it an alias name.
- To do that we will simply write:  import seaborn as sns
- To name the data set we can simply write: tips = sns.load_dataset(‘tips’)
- Now in this notebook, we can use the tips as the dataset.
- Naming it as sns is widely used for seaborn and preferred everywhere.
- Name of the data can be given according to your convenience, here we have used tips.
 
## Seaborn Functions

- As Seaborn is inbuilt with Anaconda it is easy to use.
- Some basic functions: to load dataset : tips = sns.load_dataset('tips') to see first 5 rows: tips.head()
- Describe only describes the numerical description of any particular column e.g.: tips.describe()
- The unique function gives all unique values consist in dataset e.g.: tips['sex'].unique()
- Value counts function give almost gist of the dataset with all needed information e.g.: tips['sex'].value_counts()
- Distplot shows the distribution of a Univariate set of observations. Distplot is also known as Distribution plot e.g. sns.distplot( tips['total_bill'] );
- Also, it gives min, max, mean functions in the graph are easy to understand.
- Pair plot it is very powerful. It plots the pairwise relationships across an entire data frame it is only done for numerical columns. e.g.:sns.pairplot(tips);
- Mostly Diagonal graphs are not used and consist of less information.
- For Categorical value, Barplot, Boxplot, etc are used
- For Bar plot code : sns.barplot(x='sex', y='total_bill', data=tips);
- For Box plot code :sns.boxplot(x='day', y='total_bill', data=tips);

**# x is categorical point**
**# y is a numeric point**

- For data manipulation following code is used but for that NumPy needs to be imported to run code successfully.

               data['TotalScore']=data['TotalScore']*np.pi
               data.head()  //this will print first 5 values
              data['TotalScore'] = round( data['TotalScore'] , 3 ) //Function round will roundoff the numeric values  up to 3

- Rotation function helps to rotate label given while plotting graphs which comes under Matplotlib Library e.g.: plt.xticks(rotations=70); 
- ***matplotlib needs to be imported while using this function
- Writing insights of data while plotting data is useful and fetch marks to examiners and viewers.
