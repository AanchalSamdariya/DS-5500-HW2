# DS-5500-HW2

## Problem 2

#### Choose and critique one of the visualization by one of your fellow classmates for HW 1 Problem 2 (distribution of income across countries and continents over time). Include a link to the original.
#### Describe the visualization and how it is similar and/or different from yours. Is it easy to interpret? Does it effectively visualize what is being asked? Why or why not?

To critique the visualization for distribution of income across countries and continents over time, I have chosen the graphs shown in the following link:
https://github.com/philip-johnson-2/ds5500-hw1/blob/master/README.md

Here, the distribution of income for a specific year is shown over a world map with a shade card of blue represting different shades of blue for different ranges of income. A slider for selecting a particular time of the year was to be implemented which would definitely make it feasible to view the changes across different years. 
This is very different from my visualization which is a line plot of income over time where each line represents a different country and all countries belonging to the same continent have the same line colour. On hovering over a line, the specific details of the income, year, country and continent can be viewed. However, it is not possible to get the country/continent names without hovering, which is much more convenient in the above (Johnson's) visualization.

The graphs I have chosen to critique is easy to interpret when you need to visualize the distribution of income across continents and contries for a specific year at a time, but not across different years. It is not possible to see the change in income across countries and continents over time. Hence, it does not visualize all the aspects of the question effectively. 

## Problem 3

#### Choose and critique one of the visualization by one of your fellow classmates for HW 1 Problem 3 (relationship between income, life expectancy, and child mortality over time). Include a link to the original.
#### Describe the visualization and how it is similar and/or different from yours. Is it easy to interpret? Does it effectively visualize what is being asked? Why or why not?

To critique the visualization for distribution of income, life expectancy and child mortality within continents over time, I have chosen the graphs shown in the following link:
https://github.com/ethanyangxlg/DS5500_HW1/blob/master/DS5500_HW1.pdf

Here, income, life expectancy and child mortality were plotted in different line plots to show their relationship within continents over time. Moreover, the visualization for each continent was present in a separate graph. Therefore, total number of graphs was large.
This is similar to my visualization except for the fact that the visualziation for all continents was present in a single graph for a particular variable. So, there were just 3 graphs in m y visualization - Income over time, Child mortality over time, Life expectancy over time.

The visualization I chose to critique is easy to interpret the relationship between income, life expectancy and child mortality over time for each continent separately. It would only take a little more effort to visualize the difference in relationship of these variables across different continents as we need to look at different graphs and understand the change. Since number of continents are limited and low, we could plot all continents in a single graph to visualize the difference in income, life expectancy or child mortality at any given time (year). However, since the relationship between income, life expectancy and child mortality against time is still shown clearly, this visualization is effective in providing what has been asked for. 

## Problem 4

#### Choose and fit one or more models to quantify the relationship betweem income (GDP per capita) and life expectancy over time. Justify your choice of model and comment on its appropriateness. (You are not required to handle the autocorrelation of time series, but should comment on how this impacts your analysis.) 
#### Visualize the model(s) and comment on what they tell you about the relationship between income and life expectancy over time.

To visualize the income and life expectancy over time, the mean of income was taken over time for all countries and the same was done with life expectancy. This aggregation would show the change in income and life expectancy over time.
These are the correlations between the different variables : mean(gdp_per_capita), mean(life_expectancy) and time:

![Correlation between gdp_per_capita, life_expectancy, time](images/income_life_corr.png)

There is no linear relationship between gdp_per_capita and time or between life_expectancy and time, but there is a slight positive correlation between them. Nevertheless, gdp_per_capita and life_expectancy were fitted in a Linear Regression model to observe a baseline. This is shown in the figure below:

Regression of life_expectancy over gdp_per_capita (Baseline):
![](images/reg_income_life.png)

The above baseline model was fitted as Y = B0*X + C where Y is the response variable (life_expectancy), B0 is the coffecient of X which is 0.0026, X is the dependent variable (gdp_per_capita), C is the Constant which is 30.5282.
Therefore, the model is represented as: Y = 0.0026*X + 30.5282.
This model gave an R-squared of 0.921 which indicates that the model explains well the variability of the respone data around its mean, but can do better. Since this relationship looks logarithmic, log transformation was done over gdp_per_capita. The regression plot of life_expectancy over log(gdp_per_capita) is shown below:

Regression of life_expectancy over log(gdp_per_capita):
![](images/reg_ln_income_life.png)

The above model was fitted as Y = B0*X + C where B0 is 14.4227 and C is -71.4284.
Therefore, the model is represented as: Y = 14.4227*log(X) + -71.4284
This shows a better fit of the model with a high positive correlation between life_expectancy and log(gdp_per_capita) over time. The relationship between life_expectancy and gdp_per_capita over time explains that as gdp_per_capita increases with time, the life_expectancy rate also increases. This is an expected observation and is thus shown in the above results. With higher gdp, better health facilities can be provided to the citizens and in turn help increase their lifespan.
The statistics of the regression model is shown below:

![](images/income_life_summary.png)

The R-squared of the new model has increased to 0.960 which indicated that the model explains the variability of the response data around its mean better than previously. Further transormations might help fit the data better, but there are chances that it would also lead to overfitting.

## Problem 5

#### Choose and fit one or more models to quantify the relationship betweem income (GDP per capita) and child mortality over time. Justify your choice of model and comment on its appropriateness. (You are not required to handle the autocorrelation of time series, but should comment on how this impacts your analysis.) 
#### Visualize the model(s) and comment on what they tell you about the relationship between income and child mortality over time.

To visualize the income and child mortality over time, the mean of income was taken over time for all countries and the same was done with child mortality. This aggregation would show the change in income and child mortality over time.
These are the correlations between the different variables : mean(gdp_per_capita), mean(child_mortality) and time:

![Correlation between gdp_per_capita, child_mortality, time](images/income_mortality_corr.png)

There is no linear relationship between gdp_per_capita and time or between child_mortality and time, but there is a correlation between them. Nevertheless, gdp_per_capita and child_mortality were fitted in a Linear Regression model to observe a baseline. This is shown in the figure below:

Regression of child_mortality over gdp_per_capita (Baseline):
![](images/reg_income_mortality.png)

The above baseline model was fitted as Y = B0*X + C where Y is the response variable (child_mortality), B0 is the coffecient of X which is -0.0244, X is the dependent variable (gdp_per_capita), C is the Constant which is 408.2029.
Therefore, the model is represented as: Y = -0.0244*X + 408.2029.
This model gave an R-squared of 0.889 which indicates that the model explains well the variability of the respone data around its mean, but can be improved. The plot shows a negative correlation between income and child mortality rate upto income of 12500 after which the child mortality rate remains almost constant at 0. As the above plot shows a relationship that looks logarithmic, log transformation was applied over gdp_per_capita. The regression plot of child_mortality over log(gdp_per_capita) is shown below:

Regression of child_mortality over log(gdp_per_capita):
![](images/reg_ln_income_mortality.png)

The above model was fitted as Y = B0*X + C where B0 is -139.6825 and C is 1399.1926.
Therefore, the model is represented as: Y = -139.6825*log(X) + 1399.1926.
This shows a better fit of the model with a negative linear correlation between child_mortality and log(gdp_per_capita). The statistics of the regression model is shown below:

![](images/income_mortality_summary.png)

The R-squared of the new model has increased to 0.983 which indicates a much better representation of the model. 
The relationship between child mortality and gdp_per_capita over time explains that as gdp_per_capita increases with time, the child death rate reduces. This is an expected observation and is thus shown in the above results. With high gdp_per_capita, the government can provide better care and facilities for children which would help in healthy lifestyles and low death rates.
