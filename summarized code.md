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

