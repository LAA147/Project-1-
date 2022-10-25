# Interpretation of Oregon State Data in 2020
**Introduction** - 
I worked with Oregon state data for my project. I wanted to analyze how different parameters were effected during the first year of the Covid-19 pandemic (2020). I picked per capita annual income and birth rate (county-wise) as my two parameters to compare with my Covid-19 data and check the differences. 

**Data Collection** - 
I collected the following data sets:
* 1. SARS Covid-19 cases (2020 year) (Collected from the GITHUB folder provided in the class)
* 2. Number of births in each county (2020 year) (https://www.oregon.gov/oha/ph/birthdeathcertificates/vitalstatistics/birth/pages/index.aspx)
* 3. Annual per capita income (2020 year) (https://fred.stlouisfed.org/release/tables?rid=175&eid=268359)

Using the collected data, the following questions can be framed:
* 1. How did the covid 19 pandemic effect the annual income in each county?
* 2. How did the covid 19 pandemic effect the number of births in each county?
* 3. Were there less number of births in counties where there was less annual income, during the pandemic?

The following figures represent the scatter plots of the data:
![download (1)](https://github.com/LAA147/Project-1-/blob/main/download%20(1).png)
![download (2)](https://github.com/LAA147/Project-1-/blob/main/download%20(2).png)
![download (3)](https://github.com/LAA147/Project-1-/blob/main/download%20(3).png)

The followinf figures represent the bar plots of the collected data (county-wise):
![download (4)](https://github.com/LAA147/Project-1-/blob/main/download%20(4).png)
![download (5)](https://github.com/LAA147/Project-1-/blob/main/download%20(5).png)
![download (6)](https://github.com/LAA147/Project-1-/blob/main/download%20(6).png)

**Method** - 
I checked if my data was normally distributed or not using the "Shapiro-Wilk" test. The alpha value obtained from the test is much less than 0.05. Hence I used U-test to compare my data for the first two questions. I discretized my paramerters to do the U-test with covid-19 data. Discretization for the Per-capita income parameter was done based on the two economic levels in the society. They are:
* Lower-class - Per capita income < $48000
* Upper/Middle class - Per capita income >= $48000
Discretization for the birth rate parameter was done based on the average number of births in a county in the United States. They are:
* Less than the average number of births (<500)
* More than the average number of births (>=500)


**Results** -

First U-test:
Null Hypothesis - "More number of Covid-19 Cases in counties with less per capita income"
* Result : p value = 0.176042

Second U-test:
Null Hypothesis - "More number of Covid-19 Cases in counties with less number of births"
* Result : p value = 0.00000332


I used linear regression model to fit the collected data with the selected parameters. Interaction effects between the birth rate parameter and the income parameter were evaluated as follows:
* Intercept : 762.5999
* New births dependence parameter : 1657.8
* Income dependence parameter : -298.0007
* Interaction slope : 6015.4272
The following figure represents the interaction plot:
![download (7)](https://github.com/LAA147/Project-1-/blob/main/download%20(7).png)

**Conclusions** - 
Both my null hypothesis should be rejected because of the obtained p-value. From the linear regression analysis, a positive dependence of births data is observed, a negative dependence of income data is observed and a positive dependence of their interaction is noted.


**Next steps** - 
For a better analysis/fit, a non-linear model can be used. Also, more data points can be incorporated to analyze the above mentioned parameters. For example, data from 2021, 2022 years can be collected and analyzed accordingly.
