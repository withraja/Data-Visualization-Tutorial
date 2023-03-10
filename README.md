
![App Screenshot](https://drive.google.com/uc?export=view&id=1_5j4cZubjsxiHgkOUh3HUg6nNtlM2vPd)

# Data visualization in Python

Whether you're a data scientist, analyst, or business professional, this tutorial will equip us with the skills and tools to communicate insights effectively and tell compelling stories with your data.  
We'll learn how to leverage Matplotlib and Seaborn to create stunning visuals that bring our data to life.    
## Pre-Requisite 📋
- Python Programming knowledge
- Python IDEs
- NumPy and Pandas knowledge
## What's Inside? 📦 
- **DataViz.ipynb** --> Tutorials in English
- **CSV files** --> Dataset for our visualization
- **Course Notes.pdf** --> Material about how to choose a good chart for our data. Credit to the 365datascience team has made this material.

## Library for Data Viz in Python 🤯
Of course, you know the library for visualization in python. Yup, especially if it's not Matplotlib and Seaborn. Do you know the difference?  


### Matplotlib 
``` import matplotlib.pyplot as plt```  

A widely used data visualization library that provides a wide range of plot types and customization options. It is a low-level library that allows for fine-grained control over plot elements but requires more code to generate complex visualizations

📃[**Matplolib Documentation**](https://matplotlib.org/stable/tutorials/introductory/) 


#### Advantages of Matplotlib 😆
- Provides a wide range of plot types and customization options
- Allows for fine-grained control over plot elements
- Integrates with many other Python libraries

#### Disadvantages of Matplotlib 😣
- More difficult to use and requires more code to generate complex visualizations
- The default styles are often not visually appealing  



### Seaborn
``` import seaborn as sns```  

A higher-level library that is **built on top of Matplotlib** and provides more advanced statistical visualizations, such as violin plots and heatmaps, with fewer lines of code

📃[**Seaborn Documentation**](https://seaborn.pydata.org/tutorial/introduction.html) 


#### Advantages of Seaborn 😋
- Advanced statistical visualizations with fewer lines of code
- Visually appealing and can be customized easily
- Integrates well with Pandas dataframes

#### Disadvantages of Seaborn 😭
- Not as flexible as Matplotlib for customizing 
- Some plot types not available in Seaborn


### Sooo... why not both? 🤔
You may want to combine Matplotlib and Seaborn to take advantage of the strengths of both libraries. For example, you might use Seaborn for exploratory data analysis and to quickly generate visually appealing visualizations, and then use Matplotlib to fine-tune the plot elements and create more complex visualizations. And that is what we'll do in this tutorial 🎉
## Library for Data Viz in Python 🤯
Of course, you know the library for visualization in python. Yup, especially if it's not Matplotlib and Seaborn. Do you know the difference?  


### Matplotlib 
``` import matplotlib.pyplot as plt```  

A widely used data visualization library that provides a wide range of plot types and customization options. It is a low-level library that allows for fine-grained control over plot elements but requires more code to generate complex visualizations

📃[**Matplolib Documentation**](https://matplotlib.org/stable/tutorials/introductory/) 


#### Advantages of Matplotlib 😆
- Provides a wide range of plot types and customization options
- Allows for fine-grained control over plot elements
- Integrates with many other Python libraries

#### Disadvantages of Matplotlib 😣
- More difficult to use and requires more code to generate complex visualizations
- The default styles are often not visually appealing  



### Seaborn
``` import Seaborn as sns```  

A higher-level library that is **built on top of Matplotlib** and provides more advanced statistical visualizations, such as violin plots and heatmaps, with fewer lines of code

📃[**Seaborn Documentation**](https://seaborn.pydata.org/tutorial/introduction.html) 


#### Advantages of Seaborn 😋
- Advanced statistical visualizations with fewer lines of code
- Visually appealing and can be customized easily
- Integrates well with Pandas dataframes

#### Disadvantages of Seaborn 😭
- Not as flexible as Matplotlib for customizing 
- Some plot types not available in Seaborn


### Sooo... why not both? 🤔
You may want to combine Matplotlib and Seaborn to take advantage of the strengths of both libraries. For example, you might use Seaborn for exploratory data analysis and to quickly generate visually appealing visualizations, and then use Matplotlib to fine-tune the plot elements and create more complex visualizations. And that is what we'll do in this tutorial 🎉
## Chart 🎨

There are many types of graphs for data visualization. But each has advantages and disadvantages. There are even certain conditions that require us to use certain charts. For more details, please refer to [**DatatoViz**](https://www.data-to-viz.com/)  
Use the right chart at the right time 🆗  

### Bar Chart  
Used to compare categories of data. The x-axis in a bar chart represents the categories being compared.  
**TIPS** 💡
- **The Y-axis must start from zero**. Because we can easily manipulate a graph by altering the scale to misrepresent information  
 - If the data displayed is categorical and not sorted by time series, then **sort the visualization from the smallest number**  

### Pie Chart 
It's funny... Cause **expert suggested we should not use a pie chart** 😦  
- It's hard to compare slices IF they are similar in size
- Not suitable for large datasets and too many categories
- We only can use the data that add up to 100% can't more or less
- **DO NOT EVER USE Doughnut Charts** 😡 because we determine the size of each slice through the center angles


### Stack-area Chart
Helps us to discover trends and pattern in the data. 
It is useful when we've got a time frame and several categories we'd like to track the volume of
- At least three and a maximum of six categories
- Variables are ordered and numerical 
- The Y-axis need to start at 0

The human eye cannot discern the exact size of the non-rectangular shape. So **if we have categories of similar size to each other, a line chart might be a better option** 👀


### Line Chart
When should we use a line chart?  
- Showing trends over time and continous data
- Comparing two or more variables

**It is not necessary to start the axis at 0**  
"In a time series, use a baseline that shows the data. Not the zero point" — Edward Tufte 🧓

### Histogram Chart
Used to display the distribution of numerical and continuous data that has a range (bins)  
In practice, there is usually no definitive answer as to the correct number of bins. Anywhere between 6 and 10 bins would be ideal if the distribution pattern is visible. 

We also can set our bins based on our interval. Such as, Google Maps shows the busiest time to visit a place. There are 24 bins shown, based on the number of hours in a day. We need to make sure the intervals make sense based on the nature of the data.
**Don’t cut the X or the Y axis** 💡

### Scatter Plot
It is useful for exploring data, find correlation, and find causal relationship  
**TIPS** 💡 
To avoid Overplotting, you should add a transparency level to your graph. If it still doesn't work, you could try to plot a subset of the entire data (sampling)  
The sample should be random, and representative of the pattern in the data

### Regression Chart
To quantify a causal relationship, we use regression analysis. Visually a **regression is represented by a scatter plot with a line called regression line**  
Regression analysis is a statistical approach used to estimate a relationship between two variables

### Combo Chart | Bar and Line
Even though, using a combination chart is not a good choice. Less is better. **But here are some tips for using Combo Chart** 💡
- The data on Bar Chart and Line Chart must be from the same source 
- There must be a dual Y axis (on the left and right)
