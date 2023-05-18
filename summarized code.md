 #Switching between styles

<h3> Importing essential libraries </h3> :

```
import matplotlib.pyplot as plt
import seaborn as sns
import pandas as pd
import numpy as np

```
<h2> Selcting the "ggplot" </h2> 

```
# Use the "ggplot" style and create new Figure/Axes
plt.style.use('ggplot')
fig, ax = plt.subplots()
ax.plot(seattle_weather["MONTH"], seattle_weather["MLY-TAVG-NORMAL"])
plt.show()

```

<h2> Select the 'Solarize_Light2' style, create a new Figure called fig, and a new Axes object called ax with plt.subplots
</h2> 

```
# Use the "Solarize_Light2" style and create new Figure/Axes
plt.style.use("Solarize_Light2")
fig,ax = plt.subplots()
ax.plot(austin_weather["MONTH"], austin_weather["MLY-TAVG-NORMAL"])
plt.show()

```
<h1> Saving a file several times : </h1>
1 Examine the figure by calling the plt.show() function.

2 Save the figure into the file my_figure.png, using the default resolution.

3 Save the figure into the file my_figure_300dpi.png and set the resolution to 300 dp

```
# 1 Show the figure
plt.show()

# 2 Save as a PNG file
fig.savefig('my_figure.png')

# 3  Save as a PNG file with 300 dpi
fig.savefig("my_figure_300dpi.png",dpi=300)

```
<h2> Save a figure with different sizes
</h2>


Set the figure size as width of 3 inches and height of 5 inches and save it as 'figure_3_5.png' with default resolution.

Set the figure size to width of 5 inches and height of 3 inches and save it as 'figure_5_3.png' with default settings.


```

# Set figure dimensions and save as a PNG
fig.set_size_inches([3 , 5])
fig.savefig('figure_3_5.png')

# Set figure dimensions and save as a PNG
fig.set_size_inches( [5 , 3])
fig.savefig('figure_5_3.png')

```


<h2> Unique values of a column
 </h2>
 
Create a variable called sports_column that holds the data from the "Sport" column of the DataFrame object.
Use the unique method of this variable to find all the unique different sports that are present in this data, and assign these values into a new variable called sports.
Print the sports variable to the console.


```

# Extract the "Sport" column
sports_column = summer_2016_medals["Sport"]

# Find the unique values of the "Sport" column
sports = summer_2016_medals["Sport"].unique()

# Print out the unique sports values
print(sports)
```

<h2> Automate your visualization
</h2>

<h3> INSTRUCTIONS : </h2>

Iterate over the values of sports setting sport as your loop variable.
In each iteration, extract the rows where the "Sport" column is equal to sport.
Add a bar to the provided ax object, labeled with the sport name, with the mean of the "Weight" column as its height, and the standard deviation as a y-axis error bar.
Save the figure into the file "sports_weights.png".

```

fig, ax = plt.subplots()

# Loop over the different sports branches
ax.set_xticklabels(sports, rotation=90)
for sport in sports:
  # Extract the rows only for this sport
  sport_df = summer_2016_medals[summer_2016_medals["Sport"] == sport]
  # Add a bar for the "Weight" mean with std y error bar
  ax.bar(sport, sport_df["Weight"].mean(),yerr = sport_df["Weight"].std())

ax.set_ylabel("Weight")


# Save the figure to file
fig.savefig("sports_weights.png")

```

