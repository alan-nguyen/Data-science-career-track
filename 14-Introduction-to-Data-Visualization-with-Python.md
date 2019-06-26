## Course 14: Introduction to Data Visualization with Python

### Content
#### 1. Customizing Plots
#### 2. Plotting 2D arrays
#### 3. Statistical plots with Seaborn
#### 4. Analyzing time series and images
--------------------------------------------------------------------------------------------------------------------
### 1. Customizing Plots

### 2. Plotting 2D arrays

### 3. Statistical plots with Seaborn
**Simple linear regressions**
```python
# Import plotting modules
import matplotlib.pyplot as plt
import seaborn as sns

# Plot a linear regression between 'weight' and 'hp'
sns.lmplot(x='weight', y='hp', data=auto)

# Display the plot
plt.show()
```
**Plotting resisuals of a regression**
```python
# Import plotting modules
import matplotlib.pyplot as plt
import seaborn as sns

# Generate a green residual plot of the regression between 'hp' and 'mpg'
sns.residplot(x='hp', y='mpg', data=auto, color='green')

# Display the plot
plt.show()
```

```python
# Generate a scatter plot of 'weight' and 'mpg' using red circles
plt.scatter(auto['weight'], auto['mpg'], label='data', color='red', marker='o')

# Plot in blue a linear regression of order 1 between 'weight' and 'mpg'
sns.regplot(x='weight', y='mpg', data=auto, scatter=None, color='blue', label='order 1')

# Plot in green a linear regression of order 2 between 'weight' and 'mpg'
sns.regplot(x='weight', y='mpg', data=auto, scatter=None, order=2, color='green', label='order 2')

# Add a legend and display the plot
plt.legend(loc='upper right')
plt.show()
```

### 4. Analyzing time series and images
