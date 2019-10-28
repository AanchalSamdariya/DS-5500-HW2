# DS-5500-HW2

## Problem 4

These are the correlations between the different variables : gdp_per_capita, life_expectancy and time:

![Correlation between gdp_per_capita, life_expectancy, time](images/income_life_corr.png)

There is no linear relationship between gdp_per_capita and time, but there is a slight positive correlation between life_expectancy and time. Nevertheless, gdp_per_capita and life_expectancy were fitted in a Linear Regression model to observe a baseline. This is shown in the figure below:

Regression of life_expectancy over gdp_per_capita (Baseline):
![](images/reg_income_life.png)

The above baseline model gave an R-squared of just 0.336 which indicated that the model does not explain well the variability of the respone data around its mean. Since this relationship looks logarithmic, log transformation was done over gdp_per_capita. The regression plot of life_expectancy over log(gdp_per_capita) is shown below:

Regression of life_expectancy over log(gdp_per_capita):
![](images/reg_ln_income_life.png)

This shows a better fit of the model with a positive correlation between life_expectancy and log(gdp_per_capita). The relationship between life_expectancy and gdp_per_capita explains that as gdp_per_capita increases, the life_expectancy rate increases. This is an expected observation and is thus shown in the above results. With higher gdp, better health facilities can be provided to the citizens and in turn help increase their lifespan.
The statistics of the regression model is shown below:

![](images/income_life_summary.png)

The R-squared of the new model has increased to 0.681 which indicated that the model explains the variability of the response data around its mean better than previously. Further transormations might help fit the data better, but there are chance that it would also lead to overfitting.

## Problem 5

These are the correlations between the different variables : gdp_per_capita, child_mortality and time:

![Correlation between gdp_per_capita, child_mortality, time](images/income_mortality_corr.png)

There is no linear relationship between gdp_per_capita and time, but there is a negative correlation between child_mortality and time. Nevertheless, gdp_per_capita and child_mortality were fitted in a Linear Regression model to observe a baseline. This is shown in the figure below:

Regression of child_mortality over gdp_per_capita (Baseline):
![](images/reg_income_mortality.png)

The above baseline model gave an R-squared of just 0.264 which indicates that the model does not explain well the variability of the respone data around its mean. Since this relationship looks logarithmic, log transformation was done over gdp_per_capita. The regression plot of child_mortality over log(gdp_per_capita) is shown below:

Regression of child_mortality over log(gdp_per_capita):
![](images/reg_ln_income_mortality.png)

The above plot does not display a very distinct correlation between the variables and requires further transformation. Therefore, log(child_mortality) was also taken to observe a better relationship between the variables.

Regression of log(child_mortality) over log(gdp_per_capita):
![](images/reg_ln_income_ln_mortality.png)

This shows a better fit of the model with a negative correlation between log(child_mortality) and log(gdp_per_capita). The statistics of the regression model is shown below:

![](images/income_mortality_summary.png)

The R-squared of the new model has increased to 0.708 which indicates a better representation of the model. 
The relationship between child mortality and gdp_per_capita explains that as gdp_per_capita increases, the child death rate reduces. This is an expected observation and is thus shown in the above results. With high gdp_per_capita, the government can provide better care and facilities for children which would help in healthy lifestyles and low death rates.
