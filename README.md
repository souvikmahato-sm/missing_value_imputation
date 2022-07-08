# Motivation
Data plays a very important role in decision making. Data are characteristics or information that are collected through observation. High accuracy data analysis model is required to perform on data to make real world decision. However in real world, we often encounter with missing data : users may not share complete data due to privacy reasons. These missing data affect the accuracy of data analysis and thereby the inference obtained from the data. Hence, imputing these missing values is an important task before the analysis. Many studies have been attempted to device models and algorithm to impute these missing data.
<br>

[Doc](https://drive.google.com/file/d/1Iv5O3cFlVcmEkbwfoa3S8FgYHHTK4nN2/view?usp=sharing)

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
Now we calculate a range $R$ such that $R$ comes maximum overlaps in $\{R_1 ,R_2 , R_3 , ...\}$ <br>

For example :
Let say we have 4 samples,

![image](https://user-images.githubusercontent.com/58760297/127728382-da9d005c-a310-42b7-8038-ac859406a650.png) <br>

Here, $R = [x,y]$ is the required range as it contains maximum overlaps. Now, we impute the missing values with $\frac{x+y}{2}$.