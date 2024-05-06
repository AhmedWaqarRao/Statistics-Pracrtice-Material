Import Libraries: The code begins by importing necessary libraries: numpy for numerical operations, matplotlib.pyplot for plotting graphs, %matplotlib inline for inline plotting in Jupyter notebooks, and seaborn for enhanced visualization.
Define Dataset: The dataset is defined as a list of numerical values. This dataset contains some outlier values.
Histogram Plot: The plt.hist() function is used to create a histogram plot of the dataset. This plot helps visualize the distribution of data and identify any outliers visually. Each bar represents the frequency of values within a certain range.
Z-Score Outlier Detection: The detect_outliers() function is defined to detect outliers using the Z-score method. The Z-score of each data point is calculated based on the mean and standard deviation of the dataset. If the absolute Z-score of a data point exceeds a threshold (typically set to 3), it is considered an outlier and appended to the outliers list.
Interquartile Range (IQR) Method: The code then implements outlier detection using the IQR method. Here's the breakdown:
The dataset is sorted in ascending order.
The first and third quartiles (Q1 and Q3) are calculated using np.percentile() function with 25th and 75th percentiles, respectively.
The interquartile range (IQR) is calculated as the difference between Q3 and Q1.
The lower and upper fences are determined as Q1 - 1.5 * IQR and Q3 + 1.5 * IQR, respectively. Any data point outside these fences is considered an outlier.
Boxplot Visualization: A boxplot is created using sns.boxplot() to visually represent the dataset's distribution, including outliers. The boxplot displays the median, quartiles, and any outliers present in the dataset.
This code provides a comprehensive approach to outlier detection using both Z-score and IQR methods, accompanied by visualizations to aid in understanding the dataset's characteristics.
