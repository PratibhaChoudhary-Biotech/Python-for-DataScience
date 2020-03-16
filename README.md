# Python-for-DataScience
Python for Data Science-Emeritus (DataCamp)
Course-Python(Intermeduate Python)
Chapter-1 Matplotlib
Exercise-1
Line plot (1)
With matplotlib, you can create a bunch of different plots in Python. The most basic plot is the line plot. A general recipe is given here.
import matplotlib.pyplot as plt
plt.plot(x,y)
plt.show()
In the video, you already saw how much the world population has grown over the past years. Will it continue to do so? The World Bank has estimates of the world population for the years 1950 up to 2100. The years are loaded in your workspace as a list called year, and the corresponding populations as a list called pop.
This course touches on a lot of concepts you may have forgotten, so if you ever need a quick refresher, download the Python for data science Cheat Sheet and keep it handy!
Instructions 100 XP
•	print() the last item from both the year and the pop list to see what the predicted population for the year 2100 is. Use two print() functions.
•	Before you can start, you should import matplotlib.pyplot as plt. pyplot is a sub-package of matplotlib, hence the dot.
•	Use plt.plot() to build a line plot. year should be mapped on the horizontal axis, pop on the vertical axis. Don't forget to finish off with the show() function to actually display the plot.
Take Hint (-30 XP)
Codes:
1 # Print the last item from year and pop
2 print (year[-1])
3 print (pop[-1])
4 # Import matplotlib.pyplot as plt
5 import matplotlib.pyplot as plt
6 # Make a line plot: year on the x-axis, pop on the y-axis
7 plt.plot(year,pop)
8 # Display the plot with plt.show()
9 plt.show()
Outcome: 2100
                  10.85

                                                                              +100 XP
                                        Great! Let's interpret the plot you just created.

Exercise-2
Line Plot (2): Interpretation
Have another look at the plot you created in the previous exercise; it's shown on the right. Based on the plot, in approximately what year will there be more than ten billion human beings on this planet?
Possible Answers
•	 
2040
•	 
2060
•	 
2085
•	 
2095
Submit Answer
                                                                           +50 XP
               Correct! Time to take your data visualization skills to the next level!
Exercise3 :
Line plot (3)
Now that you've built your first line plot, let's start working on the data that professor Hans Rosling used to build his beautiful bubble chart. It was collected in 2007. Two lists are available for you:
•	life_exp which contains the life expectancy for each country and
•	gdp_cap, which contains the GDP per capita (i.e. per person) for each country expressed in US Dollars.
GDP stands for Gross Domestic Product. It basically represents the size of the economy of a country. Divide this by the population and you get the GDP per capita.
matplotlib.pyplot is already imported as plt, so you can get started straight away.
Instructions:
•	Print the last item from both the list gdp_cap, and the list life_exp; it is information about Zimbabwe.
•	Build a line chart, with gdp_cap on the x-axis, and life_exp on the y-axis. Does it make sense to plot this data on a line plot?
•	Don't forget to finish off with a plt.show() command, to actually display the plot.
Take Hint (-30 XP)


Codes:
1# Print the last item of gdp_cap and life_exp
2 print(gdp_cap[-1]) 
3 print(life_exp[-1])
4 # Make a line plot, gdp_cap on the x-axis, life_exp on the y-axis
5 plt.plot(gdp_cap,life_exp)
6 # Display the plot
7 plt.show()

Outcome :
469.70929810000007
43.487
Graph -3



 +100 XP
Well done, but this doesn't look right. Let's build a plot that makes more sense.
Exercise-4 
Scatter Plot (1)
When you have a time scale along the horizontal axis, the line plot is your friend. But in many other cases, when you're trying to assess if there's a correlation between two variables, for example, the scatter plot is the better choice. Below is an example of how to build a scatter plot.
import matplotlib.pyplot as plt
plt.scatter(x,y)
plt.show()
Let's continue with the gdp_cap versus life_exp plot, the GDP and life expectancy data for different countries in 2007. Maybe a scatter plot will be a better alternative?
Again, the matplotlib.pyplot package is available as plt.
Instructions:
•	Change the line plot that's coded in the script to a scatter plot.
•	A correlation will become clear when you display the GDP per capita on a logarithmic scale. Add the line plt.xscale('log').
•	Finish off your script with plt.show() to display the plot.
Take Hint (-30 XP)

Codes :

1 # Change the line plot below to a scatter plot
2 plt.scatter (gdp_cap, life_exp)
3 # Put the x-axis on a logarithmic scale
4 plt.xscale ('log')
5 # Show plot
6 plt.show ()


                                                           +100 XP
                                        Great! That looks much better!


Exercise 5
Scatter plot (2)
In the previous exercise, you saw that that the higher GDP usually corresponds to a higher life expectancy. In other words, there is a positive correlation.
Do you think there's a relationship between population and life expectancy of a country? The list life_exp from the previous exercise is already available. In addition, now also pop is available, listing the corresponding populations for the countries in 2007. The populations are in millions of people.
Instructions:
•	Start from scratch: import matplotlib.pyplot as plt.
•	Build a scatter plot, where pop is mapped on the horizontal axis, and life_exp is mapped on the vertical axis.
•	Finish the script with plt.show() to actually display the plot. Do you see a correlation?
Take Hint (-30 XP)

Codes:
1 # Import package
2 import matplotlib.pyplot as plt
3 # Build Scatter plot
4 plt.scatter(pop,life_exp)
5 # Show plot
6 plt.show()


 +100 XP
Nice! There's no clear relationship between population and life expectancy, which makes perfect sense.


                               Second video on histograms

Exercise 1
Build a histogram (1)
life_exp, the list containing data on the life expectancy for different countries in 2007, is available in your Python shell.
To see how life expectancy in different countries is distributed, let's create a histogram of life_exp.
matplotlib.pyplot is already available as plt.
Instructions
100 XP
•	Use plt.hist() to create a histogram of the values in life_exp. Do not specify the number of bins; Python will set the number of bins to 10 by default for you.
•	Add plt.show() to actually display the histogram. Can you tell which bin contains the most observations?
Take Hint (-30 XP)
Codes:
1# Create histogram of life_exp data
2 plt.hist(life_exp,bins=10)
3 # Display histogram
4 plt.show()

+100 XP
Great job!

Exercise-2 
Build a histogram (2): bins
In the previous exercise, you didn't specify the number of bins. By default, Python sets the number of bins to 10 in that case. The number of bins is pretty important. Too few bins will oversimplify reality and won't show you the details. Too many bins will overcomplicate reality and won't show the bigger picture.
To control the number of bins to divide your data in, you can set the bins argument.
That's exactly what you'll do in this exercise. You'll be making two plots here. The code in the script already includes plt.show() and plt.clf() calls; plt.show() displays a plot; plt.clf() cleans it up again so you can start afresh.
As before, life_exp is available and matplotlib.pyplot is imported as plt.
Instructions
100 XP
•	Build a histogram of life_exp, with 5 bins. Can you tell which bin contains the most observations?
•	Build another histogram of life_exp, this time with 20 bins. Is this better?
Take Hint (-30 XP)

Codes:
1# Build histogram with 5 bins
2 plt.hist(life_exp,bins=5)
3 # Show and clean up plot
4 plt.show()
5 plt.clf()
6# Build histogram with 20 bins
7 plt.hist(life_exp, bins=20)
8 # Show and clean up again
9 plt.show()
10 plt.clf()1 

+100 XP
Nice! You can use the buttons to browse through the different plots you've created.


Exercise-3
Build a histogram (3): compare
In the video, you saw population pyramids for the present day and for the future. Because we were using a histogram, it was very easy to make a comparison.
Let's do a similar comparison. life_exp contains life expectancy data for different countries in 2007. You also have access to a second list now, life_exp1950, containing similar data for 1950. Can you make a histogram for both datasets?
You'll again be making two plots. The plt.show() and plt.clf() commands to render everything nicely are already included. Also matplotlib.pyplot is imported for you, as plt.
Instructions
100 XP
•	Build a histogram of life_exp with 15 bins.
•	Build a histogram of life_exp1950, also with 15 bins. Is there a big difference with the histogram for the 2007 data?
Take Hint (-30 XP)

Codes:
1# Histogram of life_exp, 15 bins
2 plt.hist(life_exp,bins=15)
3 # Show and clear plot
4 plt.show()
5 plt.clf()
6 # Histogram of life_exp1950, 15 bins
7 plt.hist(life_exp1950,bins=15)
8# Show and clear plot again
9 plt.show()
10 plt.clf()

+100 XP
Great! Toggle between the created plots - do you notice anything interesting?
Choose the right plot (1)
You're a professor teaching Data Science with Python, and you want to visually assess if the grades on your exam follow a particular distribution. Which plot do you use?
Instructions
50 XP
Possible Answers
•	 
Line plot
•	 
Scatter plot
•	 
Histogram
Submit Answer
Ctrl+H
Take Hint (-15 XP)
For line plot:
Incorrect Submission
Incorrect. A line plot won't give you a very clear visual on the distribution of the values in a list.

For scatter plot:
Incorrect Submission
Incorrect. Although a scatter plot can give you an idea, it's not the best option.

For histogram:
+50 XP
Excellent choice!


Exercise:2
Choose the right plot (2)
You're a professor in Data Analytics with Python, and you want to visually assess if longer answers on exam questions lead to higher grades. Which plot do you use?
Instructions
50 XP
Instructions
50 XP
Possible Answers
•	 
Line plot
•	 
Scatter plot
•	 
Histogram
Submit Answer
•	
Take Hint (-15 XP)
For line plot
Incorrect Submission
Making a line plot of this data will cause the lines to be all over the place. Do you still remember how the gdp_cap versus life_exp plot wasn't a good fit for the line plot?



For histogram:
Incorrect Submission
There's two variables involved: time to take the exam, and the corresponding grades. A histogram is not a suitable option in this case.

Scatter plot:
+50 XP Good choice!
Videos on data visualization

Exercise
Labels
It's time to customize your own plot. This is the fun part, you will see your plot come to life!
You're going to work on the scatter plot with world development data: GDP per capita on the x-axis (logarithmic scale), life expectancy on the y-axis. The code for this plot is available in the script.
As a first step, let's add axis labels and a title to the plot. You can do this with the xlabel(), ylabel() and title() functions, available in matplotlib.pyplot. This sub-package is already imported as plt.
Instructions
100 XP
•	The strings xlab and ylab are already set for you. Use these variables to set the label of the x- and y-axis.
•	The string title is also coded for you. Use it to add a title to the plot.
•	After these customizations, finish the script with plt.show() to actually display the plot.
Take Hint (-30 XP)
Codes:
1 # Basic scatter plot, log scale
2 plt.scatter(gdp_cap, life_exp)
3 plt.xscale('log') 
4 # Strings
5 xlab = 'GDP per Capita [in USD]'
6 ylab = 'Life Expectancy [in years]'
7 title = 'World Development in 2007'
8 # Add axis labels
9 plt.xlabel(xlab)
10 plt.ylabel(ylab)
11 # Add title
12 plt.title('’World Development in 2007')
13 # After customizing, display the plot
14 plt.show()
+100 XP
This looks much better already!

Exercise
Ticks
The customizations you've coded up to now are available in the script, in a more concise form.
In the video, Filip has demonstrated how you could control the y-ticks by specifying two arguments:
plt.yticks([0,1,2], ["one","two","three"])
In this example, the ticks corresponding to the numbers 0, 1 and 2 will be replaced by one, two and three, respectively.
Let's do a similar thing for the x-axis of your world development chart, with the xticks() function. The tick values 1000, 10000 and 100000 should be replaced by 1k, 10k and 100k. To this end, two lists have already been created for you: tick_val and tick_lab.
Instructions
100 XP
•	Use tick_val and tick_lab as inputs to the xticks() function to make the the plot more readable.
•	As usual, display the plot with plt.show() after you've added the customizations.
Take Hint (-30 XP)
Codes :
# Scatter plot
plt.scatter(gdp_cap, life_exp)
# Previous customizations
plt.xscale('log') 
plt.xlabel('GDP per Capita [in USD]')
plt.ylabel('Life Expectancy [in years]')
plt.title('World Development in 2007')
# Definition of tick_val and tick_lab
tick_val = [1000, 10000, 100000]
tick_lab = ['1k', '10k', '100k']
# Adapt the ticks on the x-axis
plt.xticks(tick_val,tick_lab)
# After customizing, display the plot
plt.show()
+100 XP
Great! Your plot is shaping up nicely!

Exercise
Exercise
Sizes
Right now, the scatter plot is just a cloud of blue dots, indistinguishable from each other. Let's change this. Wouldn't it be nice if the size of the dots corresponds to the population?
To accomplish this, there is a list pop loaded in your workspace. It contains population numbers for each country expressed in millions. You can see that this list is added to the scatter method, as the argument s, for size.
Instructions
100 XP
Instructions
100 XP
•	Run the script to see how the plot changes.
•	Looks good, but increasing the size of the bubbles will make things stand out more.
o	Import the numpy package as np.
o	Use np.array() to create a numpy array from the list pop. Call this Numpy array np_pop.
o	Double the values in np_pop setting the value of np_pop equal to np_pop * 2. Because np_pop is a Numpy array, each array element will be doubled.
o	Change the s argument inside plt.scatter() to be np_pop instead of pop.
Take Hint (-30 XP)
Codes :
# Import numpy as np
import numpy as np
# Store pop as a numpy array: np_pop
np_pop=np.array(pop)
# Double np_pop
np_pop=(np_pop*2)
# Update: set s argument to np_pop #( chage pop to np_pop)
plt.scatter(gdp_cap, life_exp, s = np_pop)
# Previous customizations
plt.xscale('log') 
plt.xlabel('GDP per Capita [in USD]')
plt.ylabel('Life Expectancy [in years]')
plt.title('World Development in 2007')
plt.xticks([1000, 10000, 100000],['1k', '10k', '100k'])
# Display the plot
plt.show()


+100 XP
Bellissimo! Can you already tell which bubbles correspond to which countries?



Colors
The code you've written up to now is available in the script on the right.
The next step is making the plot more colorful! To do this, a list col has been created for you. It's a list with a color for each corresponding country, depending on the continent the country is part of.
How did we make the list col you ask? The Gapminder data contains a list continent with the continent each country belongs to. A dictionary is constructed that maps continents onto colors:
dict = {
    'Asia':'red',
    'Europe':'green',
    'Africa':'blue',
    'Americas':'yellow',
    'Oceania':'black'
}
Nothing to worry about now; you will learn about dictionaries in the next chapter.
Instructions
100 XP
•	Add c = col to the arguments of the plt.scatter() function.
•	Change the opacity of the bubbles by setting the alpha argument to 0.8 inside plt.scatter(). Alpha can be set from zero to one, where zero is totally transparent, and one is not at all transparent.
Take Hint (-30 XP)

Codes:
# Specify c and alpha inside plt.scatter()
plt.scatter(x = gdp_cap, y = life_exp, s = np.array(pop) * 2,c=col, alpha=0.8)

# Previous customizations
plt.xscale('log') 
plt.xlabel('GDP per Capita [in USD]')
plt.ylabel('Life Expectancy [in years]')
plt.title('World Development in 2007')
plt.xticks([1000,10000,100000], ['1k','10k','100k'])

# Show the plot
plt.show()
+100 XP
Nice! This is looking more and more like Hans Rosling's plot!

Exercise
Additional Customizations
If you have another look at the script, under # Additional Customizations, you'll see that there are two plt.text() functions now. They add the words "India" and "China" in the plot.
Instructions
100 XP
•	Add plt.grid(True) after the plt.text() calls so that gridlines are drawn on the plot.
Take Hint (-30 XP)

Codes:
# Scatter plot
plt.scatter(x = gdp_cap, y = life_exp, s = np.array(pop) * 2, c = col, alpha = 0.8)

# Previous customizations
plt.xscale('log') 
plt.xlabel('GDP per Capita [in USD]')
plt.ylabel('Life Expectancy [in years]')
plt.title('World Development in 2007')
plt.xticks([1000,10000,100000], ['1k','10k','100k'])

# Additional customizations
plt.text(1550, 71, 'India')
plt.text(5700, 80, 'China')

# Add grid() call
plt.grid(True)

# Show the plot
plt.show()
+100 XP
Beautiful! A visualization only makes sense if you can interpret it properly. Let's do that in the next exercise.



Exercise
Interpretation
If you have a look at your colorful plot, it's clear that people live longer in countries with a higher GDP per capita. No high income countries have really short life expectancy, and no low income countries have very long life expectancy. Still, there is a huge difference in life expectancy between countries on the same income level. Most people live in middle income countries where difference in lifespan is huge between countries; depending on how income is distributed and how it is used.
What can you say about the plot?
Instructions
50 XP
Possible Answers
•	 
The countries in blue, corresponding to Africa, have both low life expectancy and a low GDP per capita.
•	 
There is a negative correlation between GDP per capita and life expectancy.
•	 
China has both a lower GDP per capita and lower life expectancy compared to India.
Submit Answer correct answer is A


Chapter-2
Chapter -2 Dictionaries :
Exercise -1
Exercise-1
Motivation for dictionaries
To see why dictionaries are useful, have a look at the two lists defined on the right. countries contains the names of some European countries. capitals lists the corresponding names of their capital.
Instructions
100 XP
•	Use the index() method on countries to find the index of 'germany'. Store this index as ind_ger.
•	Use ind_ger to access the capital of Germany from the capitals list. Print it out.
Take Hint (-30 XP)

Codes :
1 # Definition of countries and capital
2 countries = ['spain', 'france', 'germany', 'norway']
3 capitals = ['madrid', 'paris', 'berlin', 'oslo']

4 # Get index of 'germany': ind_ger
5 ind_ger=countries.index("germany")
6 ind_ger
7 # Use ind_ger to print out capital of Germany
8 print(capitals[ind_ger])
Outcome-2 
Berlin
+100 XP  As Filip already told you: this works, but it's not very convenient. Head over to the next exercise to create a dictionary of this data.
Exercise-2
Create dictionary
The countries and capitals lists are again available in the script. It's your job to convert this data to a dictionary where the country names are the keys and the capitals are the corresponding values. As a refresher, here is a recipe for creating a dictionary:
my_dict = {
   "key1":"value1",
   "key2":"value2",
}
In this recipe, both the keys and the values are strings. This will also be the case for this exercise.
Instructions
100 XP
•	With the strings in countries and capitals, create a dictionary called europe with 4 key:value pairs. Beware of capitalization! Make sure you use lowercase characters everywhere.
•	Print out europe to see if the result is what you expected.
Take Hint (-30 XP)
Codes:
# Definition of countries and capital
countries = ['spain', 'france', 'germany', 'norway']
capitals = ['madrid', 'paris', 'berlin', 'oslo']
# From string in countries and capitals, create dictionary europe
europe = { 'spain':'madrid', 'france':'paris','germany':'berlin','norway':'oslo'}
# Print europe
print(europe)
Outcome:
europe = { 'spain':'madrid', 'france':'paris','germany':'berlin','norway':'oslo'}
+100 XP
Great! Now that you've built your first dictionaries, let's get serious!

Exercise-3
Access dictionary
If the keys of a dictionary are chosen wisely, accessing the values in a dictionary is easy and intuitive. For example, to get the capital for France from europe you can use:
europe['france']
Here, 'france' is the key and 'paris' the value is returned.
Instructions
100 XP
•	Check out which keys are in europe by calling the keys() method on europe. Print out the result.
•	Print out the value that belongs to the key 'norway'.
Take Hint (-30 XP)
Codes:
1# Definition of dictionary
2 europe = {'spain':'madrid', 'france':'paris', 'germany':'berlin', 'norway':'oslo' }
3# Print out the keys in europe
4 print(europe.keys())
5# Print out value that belongs to key 'norway'
6 print(europe['norway'])

Outcome: dict_keys(['germany', 'spain', 'norway', 'france'])
Oslo
+100 XP
Good job, now you're warmed up for some more.

                     Video-2 Dictionaries  part-2 

Exercise-1
Dictionary Manipulation (1)
If you know how to access a dictionary, you can also assign a new value to it. To add a new key-value pair to europe you can use something like this:
europe['iceland'] = 'reykjavik'
Instructions
100 XP
•	Add the key 'italy' with the value 'rome' to europe.
•	To assert that 'italy' is now a key in europe, print out 'italy' in europe.
•	Add another key:value pair to europe: 'poland' is the key, 'warsaw' is the corresponding value.
•	Print out europe.
Codes:
1# Definition of dictionary
2 europe = {'spain':'madrid', 'france':'paris', 'germany':'berlin', 'norway':'oslo' }
3 # Add italy to europe
4 europe['italy']= 'rome'
5 # Print out italy in europe
6 print('italy' in europe)
7 # Add poland to europe
8 europe['poland']= 'warsaw'
9 # Print europe
10 print(europe)
Outcomes:
True
{'france': 'paris', 'italy': 'rome', 'germany': 'berlin', 'spain': 'madrid', 'poland': 'warsaw', 'norway': 'oslo'}
+100 XP Well done! Europe is growing by the minute! Did you notice that the order of the printout is not the same as the order in the dictionary's definition? That's because dictionaries are inherently unordered.
Exercise-2
Dictionary Manipulation (2)
Somebody thought it would be funny to mess with your accurately generated dictionary. An adapted version of the europe dictionary is available in the script on the right.
Can you clean up? Do not do this by adapting the definition of europe, but by adding Python commands to the script to update and remove key:value pairs.
Instructions
100 XP
•	The capital of Germany is not 'bonn'; it's 'berlin'. Update its value.
•	Australia is not in Europe, Austria is! Remove the key 'australia' from europe.
•	Print out europe to see if your cleaning work paid off.
Take Hint (-30 XP)
Codes:
1 # Definition of dictionary
2 europe = {'spain':'madrid', 'france':'paris', 'germany':'bonn',
          'norway':'oslo', 'italy':'rome', 'poland':'warsaw',
          'australia':'vienna' }
3# Update capital of germany
4 europe['germany']='berlin'
5# Remove australia
6 del(europe['australia'])
7 # Print europe
8 print(europe)
Out come:
'france': 'paris', 'italy': 'rome', 'germany': 'berlin', 'spain': 'madrid', 'poland': 'warsaw', 'norway': 'oslo'}

+100 XP
Great job! That's much better!

Exercise 3
Dictionariception
Remember lists? They could contain anything, even other lists. Well, for dictionaries the same holds. Dictionaries can contain key:value pairs where the values are again dictionaries.
As an example, have a look at the script where another version of europe - the dictionary you've been working with all along - is coded. The keys are still the country names, but the values are dictionaries that contain more information than just the capital.
It's perfectly possible to chain square brackets to select elements. To fetch the population for Spain from europe, for example, you need:
europe['spain']['population']
Instructions
100 XP
•	Use chained square brackets to select and print out the capital of France.
•	Create a dictionary, named data, with the keys 'capital' and 'population'. Set them to 'rome' and 59.83, respectively.
•	Add a new key-value pair to europe; the key is 'italy' and the value is data, the dictionary you just built.
Take Hint (-30 XP)

Codes:
# Dictionary of dictionaries
europe = { 'spain': { 'capital':'madrid', 'population':46.77 },
           'france': { 'capital':'paris', 'population':66.03 },
           'germany': { 'capital':'berlin', 'population':80.62 },
           'norway': { 'capital':'oslo', 'population':5.084 } }
# Print out the capital of France
print(europe['france']['capital'])
# Create sub-dictionary data
data={"capital":"rome","population":59.83}
# Add data to europe under key 'italy'
europe['italy']='data' ( this was wrong because it was printing data instead of the italy’s value, see the first outcome.
europe['italy']=data ( this is the right code as you can see the second outcome, it printed italy’s values 
# Print Europe
Print(europe)
Outcomes first:
paris
{'france': {'population': 66.03, 'capital': 'paris'}, 'spain': {'population': 46.77, 'capital': 'madrid'}, 'italy': 'data', 'germany': {'population': 80.62, 'capital': 'berlin'}, 'norway': {'population': 5.084, 'capital': 'oslo'}}
Outcomes second:, which is the right one:
paris
{'france': {'population': 66.03, 'capital': 'paris'}, 'spain': {'population': 46.77, 'capital': 'madrid'}, 'italy': {'population': 59.83, 'capital': 'rome'}, 'germany': {'population': 80.62, 'capital': 'berlin'}, 'norway': {'population': 5.084, 'capital': 'oslo'}}
+100 XP
Great! It's time to learn about a new data structure!


                                                             Video on Pandas , part-I

Exercise1 
Dictionary to DataFrame (1)
Pandas is an open source library, providing high-performance, easy-to-use data structures and data analysis tools for Python. Sounds promising!
The DataFrame is one of Pandas' most important data structures. It's basically a way to store tabular data where you can label the rows and the columns. One way to build a DataFrame is from a dictionary.
In the exercises that follow you will be working with vehicle data from different countries. Each observation corresponds to a country and the columns give information about the number of vehicles per capita, whether people drive left or right, and so on.
Three lists are defined in the script:
•	names, containing the country names for which data is available.
•	dr, a list with booleans that tells whether people drive left or right in the corresponding country.
•	cpc, the number of motor vehicles per 1000 people in the corresponding country.
Each dictionary key is a column label and each value is a list which contains the column elements.
Instructions
100 XP
•	Import pandas as pd.
•	Use the pre-defined lists to create a dictionary called my_dict. There should be three key value pairs:
o	key 'country' and value names.
o	key 'drives_right' and value dr.
o	key 'cars_per_cap' and value cpc.
•	Use pd.DataFrame() to turn your dict into a DataFrame called cars.
•	Print out cars and see how beautiful it is.
Take Hint (-30 XP)

Codes:
1 # Pre-defined lists
2 names = ['United States', 'Australia', 'Japan', 'India', 'Russia', 'Morocco', 'Egypt']
3 dr =  [True, False, False, False, True, True, True]
4 cpc = [809, 731, 588, 18, 200, 70, 45]
5 # Import pandas as pd
6 import pandas as pd
7 # Create dictionary my_dict with three key:value pairs: my_dict
8 my_dict={'country':names,'drives_right':dr,'cars_per_cap':cpc}
9 # Build a DataFrame cars from my_dict: cars
10 cars = pd.DataFrame(my_dict)

11 # Print cars
12 print(cars)
Outcomes:
           cars_per_cap        country  drives_right
0           809              United States          True
1           731               Australia         False
2           588               Japan         False
3            18                India         False
4           200              Russia          True
5            70              Morocco          True
6            45               Egypt          True

+100 XP
Good job! Notice that the columns of cars can be of different types. This was not possible with 2D Numpy arrays!


Exercise 2
Dictionary to DataFrame (2)
The Python code that solves the previous exercise is included on the right. Have you noticed that the row labels (i.e. the labels for the different observations) were automatically set to integers from 0 up to 6?
To solve this a list row_labels has been created. You can use it to specify the row labels of the cars DataFrame. You do this by setting the index attribute of cars, that you can access as cars.index.
Instructions
100 XP
•	Hit Run Code to see that, indeed, the row labels are not correctly set.
•	Specify the row labels by setting cars.index equal to row_labels.
•	Print out cars again and check if the row labels are correct this time.
Take Hint (-30 XP)

1 import pandas as pd
2 # Build cars DataFrame
3 names = ['United States', 'Australia', 'Japan', 'India', 'Russia', 'Morocco', 'Egypt']
4 dr =  [True, False, False, False, True, True, True]
5 cpc = [809, 731, 588, 18, 200, 70, 45]
6 cars_dict = { 'country':names, 'drives_right':dr, 'cars_per_cap':cpc }
7 cars = pd.DataFrame(cars_dict)
8 print(cars)
9 # Definition of row_labels
10 row_labels = ['US', 'AUS', 'JPN', 'IN', 'RU', 'MOR', 'EG']
11# Specify row labels of cars
12 cars.index=row_labels
13# Print cars again
14 print(cars)

Outcomes:
 first  cars_per_cap        country        drives_right
0           809              United States          True
1           731               Australia         False
2           588                Japan         False
3            18                  India         False
4           200                Russia          True
5            70                 Morocco          True
6            45                 Egypt          True
   

 Second  cars_per_cap        country  drives_right
US            809  United States          True
AUS           731      Australia         False
JPN           588          Japan         False
IN             18          India         False
RU            200         Russia          True
MOR            70        Morocco          True
EG             45          Egypt          True

+100 XP
Nice! That looks much better already!

Exercise
CSV to DataFrame (1)
Putting data in a dictionary and then building a DataFrame works, but it's not very efficient. What if you're dealing with millions of observations? In those cases, the data is typically available as files with a regular structure. One of those file types is the CSV file, which is short for "comma-separated values".
To import CSV data into Python as a Pandas DataFrame you can use read_csv().
Let's explore this function with the same cars data from the previous exercises. This time, however, the data is available in a CSV file, named cars.csv. It is available in your current working directory, so the path to the file is simply 'cars.csv'.
Instructions
100 XP
•	To import CSV files you still need the pandas package: import it as pd.
•	Use pd.read_csv() to import cars.csv data as a DataFrame. Store this dataframe as cars.
•	Print out cars. Does everything look OK?
Take Hint (-30 XP)

Codes:
1 # Import pandas as pd
2 import pandas as pd
3# Import the cars.csv data: cars
4 cars=pd.read_csv('cars.csv')      you have to put ‘cars.csv’ in quote otherwise this program wont work.
5 # Print out cars
6 print(cars)
Outcome:
Unnamed:       0              cars_per_cap        country    drives_right
0                       US           809                       United States          True
1                      AUS           731                          Australia         False
2                       JPN           588                             Japan         False
3                       IN            18                                India         False
4                       RU           200                              Russia          True
5                      MOR            70                           Morocco          True
6                      EG            45                                Egypt          True

+100 XP
Nice job! Looks nice, but not exactly what we expected. Let's fix this in the next exercise.

Exercise
CSV to DataFrame (2)
Your read_csv() call to import the CSV data didn't generate an error, but the output is not entirely what we wanted. The row labels were imported as another column without a name.
Remember index_col, an argument of read_csv(), that you can use to specify which column in the CSV file should be used as a row label? Well, that's exactly what you need here!
Python code that solves the previous exercise is already included; can you make the appropriate changes to fix the data import?
Instructions
100 XP
•	Run the code with Submit Answer and assert that the first column should actually be used as row labels.
•	Specify the index_col argument inside pd.read_csv(): set it to 0, so that the first column is used as row labels.
•	Has the printout of cars improved now?
Take Hint (-30 XP)
Codes:
# Import pandas as pd
import pandas as pd

# Fix import by including index_col
cars = pd.read_csv('cars.csv')
cars = pd.read_csv('cars.csv', index_col = 0)
# Print out cars
print(cars)

Outcome:
     cars_per_cap        country  drives_right
US            809  United States          True
AUS           731      Australia         False
JPN           588          Japan         False
IN             18          India         False
RU            200         Russia          True
MOR            70        Morocco          True
EG             45          Egypt          True
+100 XP
That's much better!

                                           Videos :Pandas –Part-II  about loc and iloc 

Exercise
Square Brackets (1)
In the video, you saw that you can index and select Pandas DataFrames in many different ways. The simplest, but not the most powerful way, is to use square brackets.
In the sample code on the right, the same cars data is imported from a CSV files as a Pandas DataFrame. To select only the cars_per_cap column from cars, you can use:
cars['cars_per_cap']
cars[['cars_per_cap']]
The single bracket version gives a Pandas Series, the double bracket version gives a Pandas DataFrame.
Instructions
100 XP
•	Use single square brackets to print out the country column of cars as a Pandas Series.
•	Use double square brackets to print out the country column of cars as a Pandas DataFrame.
•	Use double square brackets to print out a DataFrame with both the country and drives_right columns of cars, in this order.
Take Hint (-30 XP)

Codes:
1 # Import cars data
2import pandas as pd
3 cars = pd.read_csv('cars.csv', index_col = 0)

4 # Print out country column as Pandas Series
5 print(cars["country"])

6 # Print out country column as Pandas DataFrame
7 print(cars[["country"]])

8 # Print out DataFrame with country and drives_right columns
9 print(cars[["country","drives_right"]])
Outcomes:
First:
US     United States
AUS        Australia
JPN            Japan
IN             India
RU            Russia
MOR          Morocco
EG             Egypt
Name: country, dtype: object
           country
Second
US   United States
AUS      Australia
JPN          Japan
IN           India
RU          Russia
MOR        Morocco
EG           Egypt
  Third
         country  drives_right
US   United States          True
AUS      Australia         False
JPN          Japan         False
IN           India         False
RU          Russia          True
MOR        Morocco          True
EG           Egypt          True
+100 XP
Nice!

Exercise
Square Brackets (2)
Square brackets can do more than just selecting columns. You can also use them to get rows, or observations, from a DataFrame. The following call selects the first five rows from the cars DataFrame:
cars[0:5]
The result is another DataFrame containing only the rows you specified.
Pay attention: You can only select rows using square brackets if you specify a slice, like 0:4. Also, you're using the integer indexes of the rows here, not the row labels!
Instructions
100 XP
•	Select the first 3 observations from cars and print them out.
•	Select the fourth, fifth and sixth observation, corresponding to row indexes 3, 4 and 5, and print them out.
Take Hint (-30 XP)

Codes:
# Import cars data
import pandas as pd
cars = pd.read_csv('cars.csv', index_col = 0)

# Print out first 3 observations
print(cars[0:4])

# Print out fourth, fifth and sixth observation
print(cars[3:7])

Outcomes:
    cars_per_cap        country  drives_right
US            809  United States          True
AUS           731      Australia         False
JPN           588          Japan         False
IN             18          India         False
     
cars_per_cap  country  drives_right
IN             18    India         False
RU            200   Russia          True
MOR            70  Morocco          True
EG             45    Egypt          True
+100 XP
Good job. You can get interesting information, but using square brackets to do indexing is rather limited. Experiment with more advanced techniques in the following exercises.

Exercise
Exercise
loc and iloc (1)
With loc and iloc you can do practically any data selection operation on DataFrames you can think of. loc is label-based, which means that you have to specify rows and columns based on their row and column labels. iloc is integer index based, so you have to specify rows and columns by their integer index like you did in the previous exercise.
Try out the following commands in the IPython Shell to experiment with loc and iloc to select observations. Each pair of commands here gives the same result.
cars.loc['RU']
cars.iloc[4]

cars.loc[['RU']]
cars.iloc[[4]]

cars.loc[['RU', 'AUS']]
cars.iloc[[4, 1]]
As before, code is included that imports the cars data as a Pandas DataFrame.
Instructions
100 XP
•	Use loc or iloc to select the observation corresponding to Japan as a Series. The label of this row is JPN, the index is 2. Make sure to print the resulting Series.
•	Use loc or iloc to select the observations for Australia and Egypt as a DataFrame. You can find out about the labels/indexes of these rows by inspecting cars in the IPython Shell. Make sure to print the resulting DataFrame.
Take Hint (-30 XP)
Codes:
# Import cars data
import pandas as pd
cars = pd.read_csv('cars.csv', index_col = 0)

# Print out observation for Japan
print(cars.loc[['JPN']])  do not use double bracket here, because they expect to use [] only.
print(cars.iloc[[2]])     ditto ( only difference is outcome will be different in single ans double square .

# Print out observations for Australia and Egypt
print(cars.loc[['AUS','EG']])
print(cars.iloc[['1','6']])

Outcomes:
 From loc
    cars_per_cap country  drives_right
JPN           588   Japan         False
 From iloc    
cars_per_cap country  drives_right
JPN           588   Japan         False
  From loc
   cars_per_cap    country  drives_right
AUS           731  Australia         False
EG             45      Egypt          True
  From iloc  
cars_per_cap    country  drives_right
AUS           731  Australia         False
EG             45      Egypt          True
+100 XP
You aced selecting observations from DataFrames; over to selecting both rows and columns!

Exercise
loc and iloc (2)
loc and iloc also allow you to select both rows and columns from a DataFrame. To experiment, try out the following commands in the IPython Shell. Again, paired commands produce the same result.
cars.loc['IN', 'cars_per_cap']
cars.iloc[3, 0]

cars.loc[['IN', 'RU'], 'cars_per_cap']
cars.iloc[[3, 4], 0]

cars.loc[['IN', 'RU'], ['cars_per_cap', 'country']]
cars.iloc[[3, 4], [0, 1]]
Instructions
100 XP
•	Print out the drives_right value of the row corresponding to Morocco (its row label is MOR)
•	Print out a sub-DataFrame, containing the observations for Russia and Morocco and the columns country and drives_right.
Take Hint (-30 XP)
Codes:	
# Import cars data
import pandas as pd
cars = pd.read_csv('cars.csv', index_col = 0)
# Print out drives_right value of Morocco
print(cars.loc['MOR','cars_per_cap'])
# Print sub-DataFrame
print(cars.loc[['RU','MOR'],['country','drives_right']])

outcomes:
70
     country  drives_right
RU    Russia          True
MOR  Morocco          True
+100 XP Great! You might wonder if you can also combine label-based selection the loc way and index-based selection the iloc way. You can! It's done with ix, but we won't go into that here.

Exercise
Exercise
loc and iloc (3)
It's also possible to select only columns with loc and iloc. In both cases, you simply put a slice going from beginning to end in front of the comma:
cars.loc[:, 'country']
cars.iloc[:, 1]

cars.loc[:, ['country','drives_right']]
cars.iloc[:, [1, 2]]
Instructions
100 XP
•	Print out the drives_right column as a Series using loc or iloc.
•	Print out the drives_right column as a DataFrame using loc or iloc.
•	Print out both the cars_per_cap and drives_right column as a DataFrame using loc or iloc.
Take Hint (-30 XP)
Codes for loc:
# Import cars data
import pandas as pd
cars = pd.read_csv('cars.csv', index_col = 0)
# Print out drives_right column as Series
print(cars.loc[:,'drives_right'])
# Print out drives_right column as DataFrame
print(cars.loc[:,['drives_right']])
# Print out cars_per_cap and drives_right as DataFrame
print(cars.loc[:,[‘car_per_caps’,'drives_right']])   NEED to CHECK this BECAUSE IT did not work!

Codes for iloc:
# Print out drives_right column as Series
print(cars.iloc[:, 2])

# Print out drives_right column as DataFrame
print(cars.iloc[:, [2]])

# Print out cars_per_cap and drives_right as DataFrame
print(cars.loc[:, ['cars_per_cap', 'drives_right']])

+100 XP
What a drill on indexing and selecting data from Pandas DataFrames! You've done great! It's time to head over to chapter 3 to learn all about logic, control flow, and filtering!


Chapter-3 
Logic, Control Flow and Filtering
Boolean logic is the foundation of decision-making in Python programs. Learn about different comparison operators, how to combine them with Boolean operators, and how to use the Boolean outcomes in control structures. You'll also learn to filter data in pandas DataFrames using logic.
Exercise
Equality
To check if two Python values, or variables, are equal you can use ==. To check for inequality, you need !=. As a refresher, have a look at the following examples that all result in True. Feel free to try them out in the IPython Shell.
2 == (1 + 1)
"intermediate" != "python"
True != False
"Python" != "python"
When you write these comparisons in a script, you will need to wrap a print() function around them to see the output.
Instructions
100 XP
•	In the editor on the right, write code to see if True equals False.
•	Write Python code to check if -5 * 15 is not equal to 75.
•	Ask Python whether the strings "pyscript" and "PyScript" are equal.
•	What happens if you compare booleans and integers? Write code to see if True and 1 are equal.
Take Hint (-30 XP)
Codes:
# Comparison of booleans
print(True==False)

# Comparison of integers
print(-5*15!=75)

# Comparison of strings
print("pyscript"=="PyScript")

# Compare a boolean with an integer
print("True"==1)

Outcomes:
False
True
False
True
+100 XP
The last comparison worked fine because actually, a boolean is a special kind of integer: True corresponds to 1, False corresponds to 0.


Exercise
Greater and less than
In the video, Filip also talked about the less than and greater than signs, < and > in Python. You can combine them with an equals sign: <= and >=. Pay attention: <= is valid syntax, but =< is not.
All Python expressions in the following code chunk evaluate to True:
3 < 4
3 <= 4
"alpha" <= "beta"
Remember that for string comparison, Python determines the relationship based on alphabetical order.
Instructions
100 XP
•	Write Python expressions, wrapped in a print() function, to check whether:
o	x is greater than or equal to -10. x has already been defined for you.
o	"test" is less than or equal to y. y has already been defined for you.
o	True is greater than False.
Take Hint (-30 XP)
Codes:
# Comparison of integers
x = -3 * 6
print (x>=-10)

# Comparison of strings
y = "test"
print("test"<= y)

# Comparison of booleans
 Print(True>False)

Outcomes:
False
True
True
+100 XP
Great job!


Exercise
Compare arrays
Out of the box, you can also use comparison operators with Numpy arrays.
Remember areas, the list of area measurements for different rooms in your house from Introduction to Python? This time there's two Numpy arrays: my_house and your_house. They both contain the areas for the kitchen, living room, bedroom and bathroom in the same order, so you can compare them.
Instructions
100 XP
Using comparison operators, generate boolean arrays that answer the following questions:
•	Which areas in my_house are greater than or equal to 18?
•	You can also compare two Numpy arrays element-wise. Which areas in my_house are smaller than the ones in your_house?
•	Make sure to wrap both commands in a print() statement so that you can inspect the output!
Take Hint (-30 XP)

Codes:
# Create arrays
import numpy as np
my_house = np.array([18.0, 20.0, 10.75, 9.50])
your_house = np.array([14.0, 24.0, 14.25, 9.0])

# my_house greater than or equal to 18
print(my_house>=18)

# my_house less than your_house
print(my_house< your_house)


Outcomes:
[ True  True False False]
[False  True  True False]

+100 XP
Good job. It appears that the living room and bedroom in my_house are smaller than the corresponding areas in your_house.



Video on Boolean operators:

Exercise
and, or, not (1)
A boolean is either 1 or 0, True or False. With boolean operators such as and, or and not, you can combine these booleans to perform more advanced queries on your data.
In the sample code on the right, two variables are defined: my_kitchen and your_kitchen, representing areas.
Instructions
100 XP
•	Write Python expressions, wrapped in a print() function, to check whether:
o	my_kitchen is bigger than 10 and smaller than 18.
o	my_kitchen is smaller than 14 or bigger than 17.
o	double the area of my_kitchen is smaller than triple the area of your_kitchen.
Take Hint (-30 XP)

Codes:
# Define variables
my_kitchen = 18.0
your_kitchen = 14.0

# my_kitchen bigger than 10 and smaller than 18?
print(my_kitchen>10 and  my_kitchen<18)

# my_kitchen smaller than 14 or bigger than 17?
print(my_kitchen<14 or my_kitchen>17)

# Double my_kitchen smaller than triple your_kitchen?
print((my_kitchen*2)>(your_kitchen*3))


False
True
False
+100 XP
Good job!



Exercise
and, or, not (2)
To see if you completely understood the boolean operators, have a look at the following piece of Python code:
x = 8
y = 9
not(not(x < 3) and not(y > 14 or y > 10))
What will the result be if you execute these three commands in the IPython Shell?
NB: Notice that not has a higher priority than and and or, it is executed first.
Instructions
50 XP
Possible Answers
•	 
True
•	 
False
•	 
Running these commands will result in an error.
Submit Answer
Take Hint (-15 XP)
+50 XP
Correct! x < 3 is False. y > 14 or y > 10 is False as well. If you continue working like this, simplifying from inside outwards, you'll end up with False.

Exercise-2
Boolean operators with Numpy
Before, the operational operators like < and >= worked with Numpy arrays out of the box. Unfortunately, this is not true for the boolean operators and, or, and not.
To use these operators with Numpy, you will need np.logical_and(), np.logical_or() and np.logical_not(). Here's an example on the my_house and your_house arrays from before to give you an idea:
np.logical_and(my_house > 13, 
               your_house < 15)
Instructions
100 XP
•	Generate boolean arrays that answer the following questions:
•	Which areas in my_house are greater than 18.5 or smaller than 10?
•	Which areas are smaller than 11 in both my_house and your_house? Make sure to wrap both commands in print() statement, so that you can inspect the output.
Take Hint (-30 XP)
# Create arrays
1 import numpy as np
2 my_house = np.array([18.0, 20.0, 10.75, 9.50])
3 your_house = np.array([14.0, 24.0, 14.25, 9.0])
4 # my_house greater than 18.5 or smaller than 10
5 print(np.logical_or(my_house>18.5,my_house<10))
6 # Both my_house and your_house smaller than 11
7print(np.logical_and(my_house<11,your_house<11))
 
Outcomes:
[False  True False  True]
       [False False False  True]

+100 XP
Correcto perfecto!


                            Video on  if, elif, else

Exercise
Warmup
To experiment with if and else a bit, have a look at this code sample:
area = 10.0
if(area < 9) :
    print("small")
elif(area < 12) :
    print("medium")
else :
    print("large")
What will the output be if you run this piece of code in the IPython Shell?
Instructions
50 XP
Possible Answers
•	 
small
•	 
medium
•	 
large
•	 
The syntax is incorrect; this code will produce an error.
Submit Answer
Take Hint (-15 XP)
Answer is medium 

+50 XP
Exactly!

Exercise
if
It's time to take a closer look around in your house.
Two variables are defined in the sample code: room, a string that tells you which room of the house we're looking at, and area, the area of that room.
Instructions
100 XP
•	Examine the if statement that prints out "Looking around in the kitchen." if room equals "kit".
•	Write another if statement that prints out "big place!" if area is greater than 15.
Take Hint (-30 XP)

Codes:
# Define variables
room = "kit"
area = 14.0
# if statement for room
if room == "kit" :
    print("looking around in the kitchen.")
# if statement for area
if area >15:
   print ("big place!")
    
Outcome:
looking around in the kitchen.
+100 XP
Great! big place! wasn't printed, because area > 15 is not True. Experiment with other values of room and area to see how the printouts change.

Exercise
Exercise
Add else
On the right, the if construct for room has been extended with an else statement so that "looking around elsewhere." is printed if the condition room == "kit" evaluates to False.
Can you do a similar thing to add more functionality to the if construct for area?
Instructions
100 XP
Add an else statement to the second control structure so that "pretty small." is printed out if area > 15 evaluates to False.
Take Hint (-30 XP)
Codes:
# Define variables
room = "kit"
area = 14.0
# if-else construct for room
if room == "kit" :
    print("looking around in the kitchen.")
else :
    print("looking around elsewhere.")
# if-else construct for area
if area > 15 :
    print("big place!")
else:
    print("pretty small.")
looking around in the kitchen.
pretty small.
+100 XP
Nice! Again, feel free to play around with different values of room and area some more. After, head over to the next exercise where you'll take this customization one step further!

Exercise
Customize further: elif
It's also possible to have a look around in the bedroom. The sample code contains an elif part that checks if room equals "bed". In that case, "looking around in the bedroom." is printed out.
It's up to you now! Make a similar addition to the second control structure to further customize the messages for different values of area.
Instructions
100 XP
Add an elif to the second control structure such that "medium size, nice!" is printed out if area is greater than 10.
Take Hint (-30 XP)
# Define variables
room = "bed"
area = 14.0

# if-elif-else construct for room
if room == "kit" :
    print("looking around in the kitchen.")
elif room == "bed":
    print("looking around in the bedroom.")
else :
    print("looking around elsewhere.")
# if-elif-else construct for area
if area > 15 :
    print("big place!")
elif area>10:
    print("medium size, nice!")
else :
    print("pretty small.")
  
Outcome:
looking around in the bedroom.
medium size, nice!
+100 XP
Well done!
                                        Video on 
Filtering Pandas DataFrame


Exercise
Driving right (1)
Remember that cars dataset, containing the cars per 1000 people (cars_per_cap) and whether people drive right (drives_right) for different countries (country)? The code that imports this data in CSV format into Python as a DataFrame is available on the right.
In the video, you saw a step-by-step approach to filter observations from a DataFrame based on boolean arrays. Let's start simple and try to find all observations in cars where drives_right is True.
drives_right is a boolean column, so you'll have to extract it as a Series and then use this boolean Series to select observations from cars.
Instructions
100 XP
•	Extract the drives_right column as a Pandas Series and store it as dr.
•	Use dr, a boolean Series, to subset the cars DataFrame. Store the resulting selection in sel.
•	Print sel, and assert that drives_right is True for all observations.
Take Hint (-30 XP)

	Codes:
# Import cars data
import pandas as pd
cars = pd.read_csv('cars.csv', index_col = 0)

# Extract drives_right column as Series: dr
dr=cars['drives_right']
# Use dr to subset cars: sel
se1=cars[dr]
# Print sel
print(se1)
Outcomes:
     cars_per_cap        country  drives_right
US            809  United States          True
RU            200         Russia          True
MOR            70        Morocco          True
EG             45          Egypt          True

+100 XP
Great job!
Exercise
Driving right (2)
The code in the previous example worked fine, but you actually unnecessarily created a new variable dr. You can achieve the same result without this intermediate variable. Put the code that computes dr straight into the square brackets that select observations from cars.
Instructions
100 XP
Convert the code on the right to a one-liner that calculates the variable sel as before.
Take Hint (-30 XP)
Codes:
# Import cars data
import pandas as pd
cars = pd.read_csv('cars.csv', index_col = 0)
# Convert code to a one-liner
se1=cars[cars['drives_right']]
# Print sel
print(sel)
Outcomes:
    cars_per_cap        country  drives_right
US            809  United States          True
RU            200         Russia          True
MOR            70        Morocco          True
EG             45          Egypt          True
+100 XP

Nice one! cars contains 7 rows or observations, sel contains 4; so in the majority of the countries in your dataset, people drive on the right side of the road.

Exercise
Cars per capita (1)
Let's stick to the cars data some more. This time you want to find out which countries have a high cars per capita figure. In other words, in which countries do many people have a car, or maybe multiple cars.
Similar to the previous example, you'll want to build up a boolean Series, that you can then use to subset the cars DataFrame to select certain observations. If you want to do this in a one-liner, that's perfectly fine!
Instructions
100 XP
•	Select the cars_per_cap column from cars as a Pandas Series and store it as cpc.
•	Use cpc in combination with a comparison operator and 500. You want to end up with a boolean Series that's True if the corresponding country has a cars_per_cap of more than 500 and False otherwise. Store this boolean Series as many_cars.
•	Use many_cars to subset cars, similar to what you did before. Store the result as car_maniac.
•	Print out car_maniac to see if you got it right.
Take Hint (-30 XP)

Codes:
# Import cars data
import pandas as pd
cars = pd.read_csv('cars.csv', index_col = 0)

# Create car_maniac: observations that have a cars_per_cap over 500
cpc=cars["cars_per_cap"]
many_cars=cpc>500
car_manic=cars[many_cars]

# Print car_maniac
print(car_manic)

Outcomes:
     cars_per_cap        country  drives_right
US            809  United States          True
AUS           731      Australia         False
JPN           588          Japan         False

+100 XP
Good job! The output shows that the US, Australia and Japan have a cars_per_cap of over 500.

Exercise
Cars per capita (2)
Remember about np.logical_and(), np.logical_or() and np.logical_not(), the Numpy variants of the and, or and not operators? You can also use them on Pandas Series to do more advanced filtering operations.
Take this example that selects the observations that have a cars_per_cap between 10 and 80. Try out these lines of code step by step to see what's happening.
cpc = cars['cars_per_cap']
between = np.logical_and(cpc > 10, cpc < 80)
medium = cars[between]
Instructions
100 XP
•	Use the code sample above to create a DataFrame medium, that includes all the observations of cars that have a cars_per_cap between 100 and 500.
•	Print out medium.
Take Hint (-30 XP)
Codes:
# Import cars data
import pandas as pd
cars = pd.read_csv('cars.csv', index_col = 0)
# Import numpy, you'll need this
import numpy as np

# Create medium: observations with cars_per_cap between 100 and 500
cpc = cars['cars_per_cap']
between = np.logical_and(cpc > 100, cpc < 500) -----double liners
medium = cars[between]
            or single liner
medium=np.logical_and(cpc>100, cpc<500)   Not successful  need to practice more!
# Print medium
print(medium)

   cars_per_cap country  drives_right
RU           200  Russia          True
+100 XP
Great work!
Chapter-4
Video on while loop:
There are several techniques you can use to repeatedly execute Python code. While loops are like repeated if statements, the for loop iterates over all kinds of data structures. Learn all about them in this chapter.
Exercise
while: warming up
The while loop is like a repeated if statement. The code is executed over and over again, as long as the condition is True. Have another look at its recipe.
while condition :
    expression
Can you tell how many printouts the following while loop will do?
x = 1
while x < 4 :
    print(x)
    x = x + 1
Instructions
50 XP
Possible Answers
•	 
0
•	 
1
•	 
2
•	 
3
•	 
4
Submit Answer
Take Hint (-15 XP)
Answer is three times as you see this below:
In [1]: x = 1
... while x < 4 :
...     print(x)
...     x = x + 1
1
2
3
+50 XP
Correct! After 3 runs, x will be equal to 4, causing x < 4 to evaluate to False. This means that the while loop is executed 3 times, giving three printouts.

Exercise
Basic while loop
Below you can find the example from the video where the error variable, initially equal to 50.0, is divided by 4 and printed out on every run:
error = 50.0
while error > 1 :
    error = error / 4
    print(error)
This example will come in handy, because it's time to build a while loop yourself! We're going to code a while loop that implements a very basic control system for an inverted pendulum. If there's an offset from standing perfectly straight, the while loop will incrementally fix this offset.
Note that if your while loop takes too long to run, you might have made a mistake. In particular, remember to indent the contents of the loop!
Instructions
100 XP
•	Create the variable offset with an initial value of 8.
•	Code a while loop that keeps running as long as offset is not equal to 0. Inside the while loop:
o	Print out the sentence "correcting...".
o	Next, decrease the value of offset by 1. You can do this with offset = offset - 1.
o	Finally, still within your loop, print out offset so you can see how it changes.
Take Hint (-30 XP)

Codes:
# Initialize offset
offset=8

# Code the while loop
while offset!=0:
        print("correcting...")
        offset=offset-1
        print("offset")
Outcomes:
correcting...
7
correcting...
6
correcting...
5
correcting...
4
correcting...
3
correcting...
2
correcting...
1
correcting...
0
+100 XP
Well done!
Exercise
Add conditionals
The while loop that corrects the offset is a good start, but what if offset is negative? You can try to run the following code where offset is initialized to -6:
# Initialize offset
offset = -6

# Code the while loop
while offset != 0 :
    print("correcting...")
    offset = offset - 1
    print(offset)
but your session will be disconnected. The while loop will never stop running, because offset will be further decreased on every run. offset != 0 will never become False and the while loop continues forever.
Fix things by putting an if-else statement inside the while loop. If your code is still taking too long to run, you probably made a mistake!
Instructions
100 XP
•	Inside the while loop, complete the if-else statement:
o	If offset is greater than zero, you should decrease offset by 1.
o	Else, you should increase offset by 1.
•	If you've coded things correctly, hitting Submit Answer should work this time.
If your code is still taking too long to run (or your session is expiring), you probably made a mistake. Check your code and make sure that the statement offset != 0 will eventually evaluate to FALSE!
Take Hint (-30 XP)

Codes:
# Initialize offset
offset = -6

# Code the while loop
while offset != 0 :
    print("correcting...")
    if offset>0 :
      offset=offset-1
    else : 
      offset=offset+1    
    print(offset)

Outcome:
correcting...
-5
correcting...
-4
correcting...
-3
correcting...
-2
correcting...
-1
correcting...
0

+100 XP
Good work! The while loop is not that often used in Data Science, so let's head over to the for loop.

                                                             Video on for loop 
Exercise
Loop over a list
Have another look at the for loop that Filip showed in the video:
fam = [1.73, 1.68, 1.71, 1.89]
for height in fam : 
    print(height)
As usual, you simply have to indent the code with 4 spaces to tell Python which code should be executed in the for loop.
The areas variable, containing the area of different rooms in your house, is already defined.
Instructions
100 XP
Write a for loop that iterates over all elements of the areas list and prints out every element separately.
Take Hint (-30 XP)
Codes:
# areas list
areas = [11.25, 18.0, 20.0, 10.75, 9.50]

# Code the for loop
for area in areas:
    print(area)
Outcome
11.25
18.0
20.0
10.75
9.5
+100 XP
Great! That wasn't too hard, was it?

Exercise
Indexes and values (1)
Using a for loop to iterate over a list only gives you access to every list element in each run, one after the other. If you also want to access the index information, so where the list element you're iterating over is located, you can use enumerate().
As an example, have a look at how the for loop from the video was converted:
fam = [1.73, 1.68, 1.71, 1.89]
for index, height in enumerate(fam) :
    print("person " + str(index) + ": " + str(height))
Instructions
100 XP
•	Adapt the for loop in the sample code to use enumerate() and use two iterator variables.
•	Update the print() statement so that on each run, a line of the form "room x: y" should be printed, where x is the index of the list element and y is the actual list element, i.e. the area. Make sure to print out this exact string, with the correct spacing.
Take Hint (-30 XP)
Codes:
# areas list
areas = [11.25, 18.0, 20.0, 10.75, 9.50]

# Change for loop to use enumerate() and update print()
for a in areas :
 for index, area in enumerate(areas) :
    print("room " + str(index) + ": " + str(area))   
     print(a)
+100 XP
Well done!
Exercise
Indexes and values (2)
For non-programmer folks, room 0: 11.25 is strange. Wouldn't it be better if the count started at 1?
Instructions
100 XP
Adapt the print() function in the for loop on the right so that the first printout becomes "room 1: 11.25", the second one "room 2: 18.0" and so on.
Take Hint (-30 XP)
Codes:
# areas list
areas = [11.25, 18.0, 20.0, 10.75, 9.50]
# Code the for loop
for index, area in enumerate(areas) :
    print("room " + str(index +1) + ": " + str(area))
Outcomes:
room 1: 11.25
room 2: 18.0
room 3: 20.0
room 4: 10.75
room 5: 9.5
+100 XP
Much better!
Exercise
Loop over list of lists
Remember the house variable from the Intro to Python course? Have a look at its definition on the right. It's basically a list of lists, where each sublist contains the name and area of a room in your house.
It's up to you to build a for loop from scratch this time!
Instructions
100 XP
Write a for loop that goes through each sublist of house and prints out the x is y sqm, where x is the name of the room and y is the area of the room.
Take Hint (-30 XP)
Codes:
# house list of lists
house = [["hallway", 11.25], 
         ["kitchen", 18.0], 
         ["living room", 20.0], 
         ["bedroom", 10.75], 
         ["bathroom", 9.50]]
         
# Build a for loop from scratch
for x in house :
    print("the " + str(x[0]) + " is " + str(x[1]) + " sqm")
Outcomes:
the hallway is 11.25 sqm
the kitchen is 18.0 sqm
the living room is 20.0 sqm
the bedroom is 10.75 sqm
the bathroom is 9.5 sqm

+100 XP
Off to next video!

Video was on “loop data structures part1





Exercise
Loop over dictionary
In Python 3, you need the items() method to loop over a dictionary:
world = { "afghanistan":30.55, 
          "albania":2.77,
          "algeria":39.21 }

for key, value in world.items() :
    print(key + " -- " + str(value))
Remember the europe dictionary that contained the names of some European countries as key and their capitals as corresponding value? Go ahead and write a loop to iterate over it!
Instructions
100 XP
Write a for loop that goes through each key:value pair of europe. On each iteration, "the capital of x is y" should be printed out, where x is the key and y is the value of the pair.
Take Hint (-30 XP)

# Definition of dictionary
europe = {'spain':'madrid', 'france':'paris', 'germany':'berlin',
          'norway':'oslo', 'italy':'rome', 'poland':'warsaw', 'austria':'vienna' }
          
# Iterate over europe
for key, value in europe.items() :
     print("the capital of " + str(key) +" is"+ str(value))
Outcomes:
the capital of italy isrome
the capital of poland iswarsaw
the capital of spain ismadrid
the capital of austria isvienna
the capital of norway isoslo
the capital of germany isberlin
the capital of france isparis

+100 XP
Great! Notice that the order of the printouts doesn't necessarily correspond with the order used when defining europe. Remember: dictionaries are inherently unordered!

Exercise
Loop over Numpy array
If you're dealing with a 1D Numpy array, looping over all elements can be as simple as:
for x in my_array :
    ...
If you're dealing with a 2D Numpy array, it's more complicated. A 2D array is built up of multiple 1D arrays. To explicitly iterate over all separate elements of a multi-dimensional array, you'll need this syntax:
for x in np.nditer(my_array) :
    ...
Two Numpy arrays that you might recognize from the intro course are available in your Python session: np_height, a Numpy array containing the heights of Major League Baseball players, and np_baseball, a 2D Numpy array that contains both the heights (first column) and weights (second column) of those players.
Instructions
100 XP
•	Import the numpy package under the local alias np.
•	Write a for loop that iterates over all elements in np_height and prints out "x inches" for each element, where x is the value in the array.
•	Write a for loop that visits every element of the np_baseball array and prints it out.
Take Hint (-30 XP)
Codes”
# Import numpy as np
import numpy as np

# For loop over np_height
for x in np_height :
    print(str(x) + " inches")
# For loop over np_baseball
for x in np.nditer(np_baseball) :
    print(x)
   Out come is a big list here  so did not copy!

+100 XP
Wow, that's a lot of output! Try to add an additional argument end = to the print() call - the output will be mesmerizing!
Video was on Loop data structures part-2

Loop over DataFrame (1)
Iterating over a Pandas DataFrame is typically done with the iterrows() method. Used in a for loop, every observation is iterated over and on every iteration the row label and actual row contents are available:
for lab, row in brics.iterrows() :
    ...
In this and the following exercises you will be working on the cars DataFrame. It contains information on the cars per capita and whether people drive right or left for seven countries in the world.
Instructions
100 XP
Write a for loop that iterates over the rows of cars and on each iteration perform two print() calls: one to print out the row label and one to print out all of the rows contents.
Take Hint (-30 XP)
Codes:
# Import cars data
import pandas as pd
cars = pd.read_csv('cars.csv', index_col = 0)

# Iterate over rows of cars
for lab, row in cars.iterrows():
    print(lab)
    print(row)

Outcomes:
US
cars_per_cap              809
country         United States
drives_right             True
Name: US, dtype: object
AUS
cars_per_cap          731
country         Australia
drives_right        False
Name: AUS, dtype: object
JPN
cars_per_cap      588
country         Japan
drives_right    False
Name: JPN, dtype: object
IN
cars_per_cap       18
country         India
drives_right    False
Name: IN, dtype: object
RU
cars_per_cap       200
country         Russia
drives_right      True
Name: RU, dtype: object
MOR
cars_per_cap         70
country         Morocco
drives_right       True
Name: MOR, dtype: object
EG
cars_per_cap       45
country         Egypt
drives_right     True
Name: EG, dtype: object

+100 XP
Well done!
Exercise
Loop over DataFrame (2)
The row data that's generated by iterrows() on every run is a Pandas Series. This format is not very convenient to print out. Luckily, you can easily select variables from the Pandas Series using square brackets:
for lab, row in brics.iterrows() :
    print(row['country'])
Instructions
100 XP
•	Using the iterators lab and row, adapt the code in the for loop such that the first iteration prints out "US: 809", the second iteration "AUS: 731", and so on.
•	The output should be in the form "country: cars_per_cap". Make sure to print out this exact string (with the correct spacing).
o	You can use str() to convert your integer data to a string so that you can print it in conjunction with the country label.
Take Hint (-30 XP)
Codes:
# Import cars data
import pandas as pd
cars = pd.read_csv('cars.csv', index_col = 0)

# Adapt for loop
for lab, row in cars.iterrows() :
    print(lab + ": " + str(row['cars_per_cap']))

Outcomes:
 US: 809
AUS: 731
JPN: 588
IN: 18
RU: 200
MOR: 70
EG: 45
+100 XP
Solid!
Exercise
Add column (1)
In the video, Filip showed you how to add the length of the country names of the brics DataFrame in a new column:
for lab, row in brics.iterrows() :
    brics.loc[lab, "name_length"] = len(row["country"])
You can do similar things on the cars DataFrame.
Instructions
100 XP
•	Use a for loop to add a new column, named COUNTRY, that contains a uppercase version of the country names in the "country" column. You can use the string method upper() for this.
•	To see if your code worked, print out cars. Don't indent this code, so that it's not part of the for loop.
Take Hint (-30 XP)
Codes:
# Import cars data
import pandas as pd
cars = pd.read_csv('cars.csv', index_col = 0)

# Code for loop that adds COUNTRY column
for lab, row in cars.iterrows() :
    cars.loc[lab, "COUNTRY"] = row["country"].upper()
   # Print cars
print(cars)
    cars_per_cap        country  drives_right        COUNTRY
US            809  United States          True  UNITED STATES
AUS           731      Australia         False      AUSTRALIA
JPN           588          Japan         False          JAPAN
IN             18          India         False          INDIA
RU            200         Russia          True         RUSSIA
MOR            70        Morocco          True        MOROCCO
EG             45          Egypt          True          EGYPT
+100 XP
Great, but you might remember that there is also an easier way to do this.

Exercise
Add column (2)
Using iterrows() to iterate over every observation of a Pandas DataFrame is easy to understand, but not very efficient. On every iteration, you're creating a new Pandas Series.
If you want to add a column to a DataFrame by calling a function on another column, the iterrows() method in combination with a for loop is not the preferred way to go. Instead, you'll want to use apply().
Compare the iterrows() version with the apply() version to get the same result in the brics DataFrame:
for lab, row in brics.iterrows() :
    brics.loc[lab, "name_length"] = len(row["country"])

brics["name_length"] = brics["country"].apply(len)
We can do a similar thing to call the upper() method on every name in the country column. However, upper() is a method, so we'll need a slightly different approach:
Instructions
100 XP
•	Replace the for loop with a one-liner that uses .apply(str.upper). The call should give the same result: a column COUNTRY should be added to cars, containing an uppercase version of the country names.
•	As usual, print out cars to see the fruits of your hard labor
Take Hint (-30 XP)


Codes:
# Import cars data
import pandas as pd
cars = pd.read_csv('cars.csv', index_col = 0)
# Use .apply(str.upper)
cars["COUNTRY"] = cars["country"].apply(len)
print(cars)

    outcomes:
# Import cars data
import pandas as pd
cars = pd.read_csv('cars.csv', index_col = 0)

# Use .apply(str.upper)
cars["COUNTRY"] = cars["country"].apply(str.upper)
print(cars)
outcomes:
    cars_per_cap      ...              COUNTRY
US            809      ...        UNITED STATES
AUS           731      ...            AUSTRALIA
JPN           588      ...                JAPAN
IN             18      ...                INDIA
RU            200      ...               RUSSIA
MOR            70      ...              MOROCCO
EG             45      ...                EGYPT

[7 rows x 4 columns]
+100 XP
Great job! It's time to blend everything you've learned together in a case-study. Head over to the next chapter!

Chapter-5 video on Random numbers:
Exercise
Random float
Randomness has many uses in science, art, statistics, cryptography, gaming, gambling, and other fields. You're going to use randomness to simulate a game.
All the functionality you need is contained in the random package, a sub-package of numpy. In this exercise, you'll be using two functions from this package:
•	seed(): sets the random seed, so that your results are reproducible between simulations. As an argument, it takes an integer of your choosing. If you call the function, no output will be generated.
•	rand(): if you don't specify any arguments, it generates a random float between zero and one.
Instructions
100 XP
•	Import numpy as np.
•	Use seed() to set the seed; as an argument, pass 123.
•	Generate your first random float with rand() and print it out.
Take Hint (-30 XP)

Codes:
# Import numpy as np
import numpy as np
# Set the seed
np.random.seed(123)
# Generate and print random float
print(np.random.rand())
Outputs: 0.6964691855978616
+100 XP Great! Now let's simulate a dice.
Exercise
Roll the dice
In the previous exercise, you used rand(), that generates a random float between 0 and 1.
As Filip explained in the video you can just as well use randint(), also a function of the random package, to generate integers randomly. The following call generates the integer 4, 5, 6 or 7 randomly. 8 is not included.
import numpy as np
np.random.randint(4, 8)
Numpy has already been imported as np and a seed has been set. Can you roll some dice?
Instructions
100 XP
•	Use randint() with the appropriate arguments to randomly generate the integer 1, 2, 3, 4, 5 or 6. This simulates a dice. Print it out.
•	Repeat the outcome to see if the second throw is different. Again, print out the result.
Take Hint (-30 XP)
# Import numpy and set seed
import numpy as np
np.random.seed(123)

# Use randint() to simulate a dice
dice=np.random.randint(1,7)
print(dice)
# Use randint() again
dice=np.random.randint(1,7)
print(dice)
Outcomes: 6
                     3 

+100 XP
Alright! Time to actually start coding things up!

Exercise
Determine your next move
In the Empire State Building bet, your next move depends on the number of eyes you throw with the dice. We can perfectly code this with an if-elif-else construct!
The sample code assumes that you're currently at step 50. Can you fill in the missing pieces to finish the script? numpy is already imported as np and the seed has been set to 123, so you don't have to worry about that anymore.
Instructions
100 XP
•	Roll the dice. Use randint() to create the variable dice.
•	Finish the if-elif-else construct by replacing ___:
•	If dice is 1 or 2, you go one step down.
•	if dice is 3, 4 or 5, you go one step up.
•	Else, you throw the dice again. The number of eyes is the number of steps you go up.
•	Print out dice and step. Given the value of dice, was step updated correctly?
Take Hint (-30 XP)





Codes:
# Numpy is imported, seed is set
# Starting step
step = 50
# Roll the dice
dice=np.random.randint(1,7)
# Finish the control construct
if dice <= 2 :
    step = step - 1
elif dice<=5 :
    step=step + 1
else :
    step = step + np.random.randint(1,7)

# Print out dice and step
print(dice)
print(step)
Outcomes:5
                  51
Every time it is going to be different  random numbers but here whatever I got once:

+100 XP
Cool! You threw a 6, so the code for the else statement was executed. You threw again, and apparently you threw 3, causing you to take three steps up: you're currently at step 53.


                       Second video was on random walk:
Exercise
The next step
Before, you have already written Python code that determines the next step based on the previous step. Now it's time to put this code inside a for loop so that we can simulate a random walk.
Instructions
100 XP
Instructions
100 XP
•	Make a list random_walk that contains the first step, which is the integer 0.
•	Finish the for loop:
•	The loop should run 100 times.
•	On each iteration, set step equal to the last element in the random_walk list. You can use the index -1 for this.
•	Next, let the if-elif-else construct update step for you.
•	The code that appends step to random_walk is already coded.
•	Print out random_walk.
Take Hint (-30 XP)
Codes:
# Numpy is imported, seed is set
# Initialize random_walk
random_walk=[0]
# Complete the for loop
for x in range(100) :
    # Set step: last element in random_walk
   step = random_walk[-1]
    # Roll the dice
    dice = np.random.randint(1,7)
    # Determine next step
    if dice <= 2:
        step = step - 1
    elif dice <= 5:
        step = step + 1
    else:
        step = step + np.random.randint(1,7)

    # append next_step to random_walk
    random_walk.append(step)

# Print random_walk
print(random_walk)
Outcomes is random every time:
[0, 4, 3, 2, 4, 3, 4, 6, 7, 8, 13, 12, 13, 14, 15, 16, 17, 16, 21, 22, 23, 24, 23, 22, 21, 20, 19, 20, 21, 22, 28, 27, 26, 25, 26, 27, 28, 27, 28, 29, 28, 33, 34, 33, 32, 31, 30, 31, 30, 29, 31, 32, 35, 36, 38, 39, 40, 41, 40, 39, 40, 41, 42, 43, 42, 43, 44, 45, 48, 49, 50, 49, 50, 49, 50, 51, 52, 56, 55, 54, 55, 56, 57, 56, 57, 56, 57, 59, 64, 63, 64, 65, 66, 67, 68, 69, 68, 69, 70, 71, 73]
+100 XP
Good job! There's still something wrong: the level at index 15 is negative!

Exercise
How low can you go?
Things are shaping up nicely! You already have code that calculates your location in the Empire State Building after 100 dice throws. However, there's something we haven't thought about - you can't go below 0!
A typical way to solve problems like this is by using max(). If you pass max() two arguments, the biggest one gets returned. For example, to make sure that a variable x never goes below 10 when you decrease it, you can use:
x = max(10, x - 1)
Instructions
100 XP
•	Use max() in a similar way to make sure that step doesn't go below zero if dice <= 2.
•	Hit Submit Answer and check the contents of random_walk.
Take Hint (-30 XP)
Codes:
# Numpy is imported, seed is set
# Initialize random_walk
random_walk = [0]
for x in range(100) :
    step = random_walk[-1]
    dice = np.random.randint(1,7)
    if dice <= 2:
        # Replace below: use max to make sure step can't go below 0
        step = max(0, step - 1)
    elif dice <= 5:
        step = step + 1
    else:
        step = step + np.random.randint(1,7)
    random_walk.append(step)
print(random_walk)

Outcomes:
[0, 3, 4, 5, 4, 5, 6, 7, 6, 5, 4, 3, 2, 1, 0, 0, 1, 6, 5, 4, 5, 4, 5, 6, 7, 8, 9, 8, 9, 8, 9, 10, 11, 12, 11, 15, 16, 15, 16, 15, 16, 17, 18, 19, 20, 21, 22, 25, 26, 27, 28, 33, 34, 38, 39, 38, 39, 40, 39, 40, 41, 43, 44, 45, 44, 43, 44, 45, 44, 43, 44, 45, 47, 46, 45, 46, 45, 46, 47, 48, 50, 49, 50, 51, 52, 53, 54, 53, 52, 53, 52, 53, 54, 53, 56, 57, 58, 59, 58, 59, 60]
Notice this time we do not have values in negative because we set it so loop does not go beyond zero!
 +100 XP
If you look closely at the output, you'll see that around index 15 the step stays at 0. You're not going below zero anymore. Great!

Exercise
Visualize the walk
Let's visualize this random walk! Remember how you could use matplotlib to build a line plot?
import matplotlib.pyplot as plt
plt.plot(x, y)
plt.show()
The first list you pass is mapped onto the x axis and the second list is mapped onto the y axis.
If you pass only one argument, Python will know what to do and will use the index of the list to map onto the x axis, and the values in the list onto the y axis.
Instructions
100 XP
Add some lines of code after the for loop:
•	Import matplotlib.pyplot as plt.
•	Use plt.plot() to plot random_walk.
•	Finish off with plt.show() to actually display the plot.
Take Hint (-30 XP)

# Numpy is imported, seed is set
# Initialization
random_walk = [0]
for x in range(100) :
    step = random_walk[-1]
    dice = np.random.randint(1,7)
    if dice <= 2:
        step = max(0, step - 1)
    elif dice <= 5:
        step = step + 1
    else:
        step = step + np.random.randint(1,7)
    random_walk.append(step)
# Import matplotlib.pyplot as plt
import matplotlib.pyplot as plt
# Plot random_walk
plt.plot(random_walk)
# Show the plot
plt.show()
+100 XP
This is pretty cool! You can clearly see how your random walk progressed.

                          Video was on distribution of a random walk

Exercise
Simulate multiple walks
A single random walk is one thing, but that doesn't tell you if you have a good chance at winning the bet.
To get an idea about how big your chances are of reaching 60 steps, you can repeatedly simulate the random walk and collect the results. That's exactly what you'll do in this exercise.
The sample code already sets you off in the right direction. Another for loop is wrapped around the code you already wrote. It's up to you to add some bits and pieces to make sure all of the results are recorded correctly.
Note: Don't change anything about the initialization of all_walks that is given. Setting any number inside the list will cause the exercise to crash!
Instructions
100 XP
•	Fill in the specification of the for loop so that the random walk is simulated 10 times.
•	After the random_walk array is entirely populated, append the array to the all_walks list.
•	Finally, after the top-level for loop, print out all_walks.
Take Hint (-30 XP)
Codes:
# Numpy is imported; seed is set
# Initialize all_walks (don't change this line)
all_walks = []
# Simulate random walk 10 times
for i in range(10) :
    # Code from before
    random_walk = [0]
    for x in range(100) :
        step = random_walk[-1]
        dice = np.random.randint(1,7)
        if dice <= 2:
            step = max(0, step - 1)
        elif dice <= 5:
            step = step + 1
        else:
            step = step + np.random.randint(1,7)
        random_walk.append(step)
    # Append random_walk to all_walks
    all_walks.append(random_walk)
# Print all_walks
print(all_walks)
+100 XP
Well done!

Exercise
Visualize all walks
all_walks is a list of lists: every sub-list represents a single random walk. If you convert this list of lists to a Numpy array, you can start making interesting plots! matplotlib.pyplot is already imported as plt.
The nested for loop is already coded for you - don't worry about it. For now, focus on the code that comes after this for loop.
Instructions
100 XP
•	Use np.array() to convert all_walks to a Numpy array, np_aw.
•	Try to use plt.plot() on np_aw. Also include plt.show(). Does it work out of the box?
•	Transpose np_aw by calling np.transpose() on np_aw. Call the result np_aw_t. Now every row in np_all_walks represents the position after 1 throw for the 10 random walks.
•	Use plt.plot() to plot np_aw_t; also include a plt.show(). Does it look better this time?
Take Hint (-30 XP)
Codes:
# numpy and matplotlib imported, seed set.
# initialize and populate all_walks
all_walks = []
for i in range(10) :
    random_walk = [0]
    for x in range(100) :
        step = random_walk[-1]
        dice = np.random.randint(1,7)
        if dice <= 2:
            step = max(0, step - 1)
        elif dice <= 5:
            step = step + 1
        else:
            step = step + np.random.randint(1,7)
        random_walk.append(step)
    all_walks.append(random_walk)
# Convert all_walks to Numpy array: np_aw
np_aw=np.array(all_walks)
# Plot np_aw and show
plt.plot(np_aw)
plt.show()
# Clear the figure
plt.clf()
# Transpose np_aw: np_aw_t
np_aw_t=np.transpose(np_aw)
# Plot np_aw_t and show
plt.plot(np_aw_t)
plt.show()

+100 XP
Good job! You can clearly see how the different simulations of the random walk went. Transposing the 2D Numpy array was crucial; otherwise Python misunderstood.

Exercise
Implement clumsiness
With this neatly written code of yours, changing the number of times the random walk should be simulated is super-easy. You simply update the range() function in the top-level for loop.
There's still something we forgot! You're a bit clumsy and you have a 0.1% chance of falling down. That calls for another random number generation. Basically, you can generate a random float between 0 and 1. If this value is less than or equal to 0.001, you should reset step to 0.
Instructions
100 XP
•	Change the range() function so that the simulation is performed 250 times.
•	Finish the if condition so that step is set to 0 if a random float is less or equal to 0.001. Use np.random.rand().
Take Hint (-30 XP)

Codes:
# numpy and matplotlib imported, seed set
# Simulate random walk 250 times
all_walks = []
for i in range(250) :
    random_walk = [0]
    for x in range(100) :
        step = random_walk[-1]
        dice = np.random.randint(1,7)
        if dice <= 2:
            step = max(0, step - 1)
        elif dice <= 5:
            step = step + 1
        else:
            step = step + np.random.randint(1,7)
        # Implement clumsiness
        if np.random.rand() <= 0.001 :
            step = 0
        random_walk.append(step)
    all_walks.append(random_walk)
# Create and plot np_aw_t
np_aw_t = np.transpose(np.array(all_walks))
plt.plot(np_aw_t)
plt.show()

+100 XP
Superb! Look at the plot. In some of the 250 simulations you're indeed taking a deep dive down!


Exercise
Plot the distribution
All these fancy visualizations have put us on a sidetrack. We still have to solve the million-dollar problem: What are the odds that you'll reach 60 steps high on the Empire State Building?
Basically, you want to know about the end points of all the random walks you've simulated. These end points have a certain distribution that you can visualize with a histogram.
Note that if your code is taking too long to run, you might be plotting a histogram of the wrong data!
Instructions
100 XP
•	To make sure we've got enough simulations, go crazy. Simulate the random walk 500 times.
•	From np_aw_t, select the last row. This contains the endpoint of all 500 random walks you've simulated. Store this Numpy array as ends.
•	Use plt.hist() to build a histogram of ends. Don't forget plt.show() to display the plot.
Take Hint (-30 XP)
Codes:
# numpy and matplotlib imported, seed set

# Simulate random walk 500 times
all_walks = []
for i in range(500) :
    random_walk = [0]
    for x in range(100) :
        step = random_walk[-1]
        dice = np.random.randint(1,7)
        if dice <= 2:
            step = max(0, step - 1)
        elif dice <= 5:
            step = step + 1
        else:
            step = step + np.random.randint(1,7)
        if np.random.rand() <= 0.001 :
            step = 0
        random_walk.append(step)
    all_walks.append(random_walk)

# Create and plot np_aw_t
np_aw_t = np.transpose(np.array(all_walks))
# Select last row from np_aw_t: ends
ends = np_aw_t[-1,:]
# Plot histogram of ends, display plot
plt.hist(ends)
plt.show()
+100 XP
Great job! Have a look at a histogram; what do you think your chances are?
Exercise
Calculate the odds
The histogram of the previous exercise was created from a Numpy array ends, that contains 500 integers. Each integer represents the end point of a random walk. To calculate the chance that this end point is greater than or equal to 60, you can count the number of integers in ends that are greater than or equal to 60 and divide that number by 500, the total number of simulations.
Well then, what's the estimated chance that you'll reach 60 steps high if you play this Empire State Building game? The ends array is everything you need; it's available in your Python session so you can make calculations in the IPython Shell.
Instructions
50 XP
Possible Answers
•	 
48.8%
•	 
73.9%
•	 
78.4%
•	 
95.9%
Submit Answer
Take Hint (-15 XP)
+50 XP
Correct! Seems like you have a pretty high chance of winning the bet!


