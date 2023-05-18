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
