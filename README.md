# Morivation
Data plays a very important role in decision making. Data are characteristics or information that are collected through observation. High accuracy data analysis model is required to perform on data to make real world decision. However in real world, we often encounter with missing data : users may not share complete data due to privacy reasons. These missing data affect the accuracy of data analysis and thereby the inference obtained from the data. Hence, imputing these missing values is an important task before the analysis. Many studies have been attempted to device models and algorithm to impute these missing data.
<br>

# Method
Here I will use the idea of *Confidence Interval*, to impute missing values and get inference from a Dataset.

![image](https://user-images.githubusercontent.com/58760297/127699342-3d9184af-7ab8-4e75-bca4-9fae42d299e5.png)
<br>
> $$\bar{x} - z\sigma_{\bar{x}} \le \bar{\mu} \le \bar{x} + z\sigma_{\bar{x}}$$
>- $\bar{\mu}$ *= estimated mean of population*
>- $\bar{x}$ *= mean of sample*
>- $\sigma_{\bar{x}}$ *= standard deviation of sample*
>- $z$ *= confidence level*

<br>

# Calculation

$\forall$ $sample_i$ : we calculate ${\bar{x_i}}$ , $\sigma_{\bar{x_i}}$
Thus we can find a plausible range for $\mu_i$= $R_i$
Now we calculate a range $R$ such that $R$ comes maximum number of times in $\{R_1 ,R_2 , R_3 , ...\}$