# Day 3 Summary :

<img src="https://d6vdma9166ldh.cloudfront.net/media/images/4594dcf8-a8c5-4fa7-a6d4-bab2c9081041.jpg" alt="">

## [Day 3 Lecture](https://youtu.be/YrVPInuWFzI)  👈👈

**DAY 03 AGENDA**
- Library Numpy
- Library Matplotlib

## Numpy:
**Introduction to NumPy:**

- One of the modules that are very popular and widely used in data analysis.
- We will be looking at 1D and 2 D array, NumPy functions, slicing and indexing.
- Operations of Numpy can be done using the basic data structures as well but Numpy is about 10 times faster than the traditional data types.
- Numpy is basically Numerical python.
- Numpy is one of the backbones of ML in python.
- Numpy also adds support to core python and supports a multidimensional array.
- Numpy is divided into 2 things:
- Ndarray: n-dimensional array
- Ufunctions:Universal functions

## Hands-on session - Numpy
**Basic Overview**

- To use Numpy we need to import it in our notebook using: import numpy 
- We have functions like sum (), mean (), min () and max ().
- We can access these functions using the dot operator foreg numpy.sum() etc.
- Note: We cannot use numpy everywhere so we will assign it an alias name.
- To do that we will simply write:import numpy as np 
- Now in this notebook, we can use the module by the name as np.
- Naming it as np is widely used and preferred everywhere.

## Array Creation Using Numpy

- We will now create an array.
- To create a NumPy array we will usenp.array .
- To create an array we need to pass the values in the form of a list: arr=np.arr([1,2,3,4,5])
- np.sum(arr) will give the sum of the elements.
- arr.dtypewill give the data types of the elements of the array.
- If we change any of the value to float the data type of the array will be changed to float.
- We can provide a string as elements of the array but we mostly use numerical values as it is designed to work with numbers better.
- If we put string the data type will be u32 that is Unicode.
- To create a 2D NumPy array we will create it using arr=np.array([[1,2,3], [4,5,6], [7,8,9]]).
- To find the shape we use the shape attribute so we don’t use the empty parenthesis with it.
- arr.shape will give the shape of the array

## To Print Array

    arr=np.arr([1,2,3,4,5,6,7,8,9])
    print(arr)                      //print(arr.shape) is used to print the shape of array particularly

- For 2d  array, if one of the element ids missing NumPy stores as the list of lists

                  arr = np.array([[1,2,3],[4,5,6],[99,45]]).

- Numpy is used for EDA and Machine Learning programs.

## Array Operations

- arr = np.zeros((2,4)) it is zeros function where it prints 2 rows and 4 columns where each element is zero. 
- On a similar note there is ones function eg: arr = np.ones((2,4))
- The identity Matrix is always Square matrix, so the numpy takes only one value to specify rows and columns eg: np.identity(3)
- Numpy uses Float format unless all the numbers are in integer format
- Numpy has a module named random for random numbers it cannot be number but numbers will be centred around 0

             eg: arr = np.random.randn(3,4) #It will create 3 rows and 4 columns where each element is random

- Indexing function which done to access any element buy mentioning its index

            arr= np.array([[1,2,3],[4,5,6],[7,8,9]]) #Index always starts with zero arr[0][1]
            //Output   2 
- Range function needs to be specified by print(np.arrange(12)) which prints number from  0 – 11 in 1d array. If reshape command is used in the same command by adding command reshape(3,4) now, numbers will be printed in format 3 rows and 4 columns.
- Reshape function can also create n number of arrays with the same dimensions

            arr=np.range(12).reshape(2,2,3)  # it will create 2 matrices with 2 rows and 3 columns. 
            
- Hence indexing will be done accordingly considering the first matrix as 0th matrix usingarr[0] entire 0th array will be the output of this command.
- Slicing function used to print from the given index locations in the command
                              
                              np.arrange(12)[1:6] 

- It will print from 1-5 numbers and to specify single number it should be mentioned according to its index location
                              
                              i.e. arr[1:6][1]  //Output       1

## U function 

- The universal function where operations as are done like Addition, Multiplication, Division by arr+1 here each element in the array will get increase its value by 1.
- While doing any operations arrays dimensions need not to be equal.

                           arr1 = np.arrange(15).reshape(5,3)                                       
                           arr2 = np.arrange(5).reshape(5,1)
                           print(arr1+arr2)

- NumPy will print array having 5 rows and 3 columns

- Multiplication can also be performed by arr1.dot(arr2)

- Transpose matrix of the array in NumPy can be performed using arr1.T

- Linear Algebra solutions are faster than usual methods without any limitations to perform 

7x+5y-3z=16  |  3x-5y+2z=-8  |  5x+3y-7z=0                          

                      a =np.array([[7,5,-3],[3,-5,2],[5,3,-7]])
                      b = np.array([[16,-8,0]]) 
                      answers = np.linalg.solve(a,b)  
                                                                                                                          
**Output**  
**array([1.,3.,2.]) x, y, z respectively**

## Matplotlib

**Basic Overview**

- Matplotlib is a plotting library for the Python programming language and its numerical mathematics extension NumPy. Graphs are used for data visualization and some functions.
- To use Matplotlib we need to import it in our notebook using: import matplotlib.pyplot 
- We cannot use matplotlib everywhere so we will assign it an alias name.
- To do that we will simply write: import matplotlib.pyplot as plt.

## Matplotlib Operations

Just like mobile, laptop and other gadgets have themes for a better experience in visualization there are also themes in Matplotlib can also access using this link mentioned: https://tonysyu.github.io/raw_content/matplotlib-style-gallery/gallery.html command used accordingly 

      plt.style.use(‘classic’) 
      x= np.linspace(0,5,10)
      x # It generates 5 number equally spaced from 0-10
      Output  ([0. , 2.5 , 5. , 7.5 , 10. ]) on a similar note, it can generate n number of numbers. 

      x= np.linspace(0,10,100)&amp;nbsp;  
      plt.plot(x , npsin(x)) #Using this command it will plot a sin graph similarly you can also plot cos(x) graph 

- using “; “ the mentioned storage location of the graph will be suppressed.
- %matplotlib notebook mentioning above the plotting code gets an interactive chart where downloads, zoom, resize and details features can be accessed
- %matplotlib inline is the default for basic graph credentials

      x= np.linspace(0,10,100)
      plt.plot(x , npsin(x),’-g‘)               
      plt.plot(x , npcos(x) ’: b‘)   #here there can be changes in the curved lines of graph as solid line of green color in sine curve and dotted line of blue color in cos curve
      plt.figure(
      plt.subplot(2,1,1)
      plt.plot(x , npsin(x),’-‘) )    #it creates 2 subplots of 1st sin curve in one graph size                             
      plt.subplot(2,1,2)
      plt.plot(x , npcos(x) ’- -‘)    #it creates 2 subplots of 2nd cos curve subplots can create no of graphs in one graph size there should not be repeated graphs 

- Title of the graph can be given by command eg: plt.title(“ A sine Curve”)
- Plt.xlabel(“x”) #labels X-Axis as x similarly Y axis can also be labelled
- Index of the graph can be given by command plt.legend()  #as function is named as a legend.
