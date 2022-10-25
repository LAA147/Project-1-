# Interpretation of Oregon State Data in 2020-
I worked with Oregon state data for my project. I wanted to analyze how different parameters were effected during the first year of the Covid-19 pandemic (2020). I picked per capita annual income and birth rate as my two parameters to compare with my Covid-19 data and check the differences. 

I collected the following data sets:
    1. SARS Covid-19 cases (2020 year)
    2. Number of births in each county (2020 year)
    3. Annual per capita income (2020 year)

Using the collected data, the following questions can be framed:
    1. How did the covid 19 pandemic effect the annual income in each county?
    2. How did the covid 19 pandemic effect the number of births in each county?
    3. Were there less number of births in counties where there was less annual income, during the pandemic?

I checked if my data was normally distributed or not using the "Shapiro-Wilk" test. The alpha value obtained from the test is much less than 0.05. Hence I used U-test to compare my data for the first two questions. I used linear regression model to fit the data 
