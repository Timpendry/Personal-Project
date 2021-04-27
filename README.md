# Data 115 Personal Project
# Personal Data Set 
In the past several months, much attention has been devoted to the efforts of an Alabama Amazon warehouse to form Amazon's first Union. While unions were instrumental to shaping labour law standards in the United States in the early and mid 20th century, in recent years Union membership has declined, partly due to legal restrictions which have been passed in many areas making it harder for workers to unionize. I set out to learn more about the relationship between Union Membership and Income Inequality in the United States, hypothesizing that Unions have a positive relationship with the share of income going to middle class workers. The data I gathered are from the U.S. Historical Tables on Union Membership, Coverage, Density and Employment found on Unionstats.com, an internet resource providing extensive data on union membership rates. To explore income inequality, I gathered data from the U.S Census Historical Income Tables (Table H-2), which show the aggregate share of income recieved by each fifth of the population, and the top five percent. Together, the data I compiled are ideally suited to explore how union membership - public sector, private sector, and overall rates- affect income inequality, measured as the share of income going to the top 5% and middle 60% of the country.

The data cleaning process was relatively simple. Data were imported from Unionstats.com and Census.gov to excel. For the Income Inequality data, columns displaying the number of observations (in thousands) were deleted, as they were not relevant for the analysis. Data from unionstats was cleaned to only include the percentage of Private sector workers that were unionized, excluding data on the overall number of members, number of observations, raw number of individuals covered, and the percent of individuals covered. These steps were repeated with the data for Public sector workers and all wage and salary workers. Income inequlity data for years 1967-1976 and the year 2020 were excluded because there was no matching data on overall Union membership for those years. Union membership rates in 1982 were missing completely at random. Mean substitution was employed, using data from the years 1981 and 1983. To create the column showing the share of aggregate income recieved by the middle 60%, numbers for the second, third, and fourth fifths on the population were summed together. 


Column names "one", "two", "three", "four", and "five" refer to the share of aggregate income recieved by the each fifth of the population. "One" shows the share for the bottom 5th and "five" contains the share of income recieved by the top 5th of the country. "fivepercent" shows the share of income recieved by the top 5% of earners. "midsixty" shows the sum of the middle 3/5ths of the population, representing the share of income recieved by the middle 60% of the country. "priv" shows the rate of union membership among workers in the private sector, "pub" shows the rate of union membership among workers in the public sector, and "All" shows the rate of union membership for all wage and salary workers combined. 


Visualization - The best visualization to summarize and describe my dataset is simple line plot. On it, one can see that the overall rate of union membership(shown in blue) has fallen steadily since 1973, when observations begin. Similarly, the share of income recieved by the middle 60% of the nation (shown in brown) also declined steadily. Displaying the opposite trend, the share of income going to the top 5% of earners (shown in red) trends steadily upward. 
![](Visualization.png)


Analysis - The line plot captures the overall relationship very well, but I was curious whether private sector union membership or public sector union membership had a larger effect on earnings, both for the top 5% and the middle 60%. To test this, I ran several bivariate regression models. I ran six bivariate regressions, testing the effect of Union membership - private sector, public sector, and all workers - on the share of income recieved by the top 5% and the middle 60%. The overall union membership was strongly correlated with higher earnings by the middle 60% of the population and strongly correlated with a lower share of income going to the top 5%. A 1% increase in overall union membership is correlated with an increase in the aggregate income recieved by the middle 60% of .47%. The same increase in Union membership is correlated with the top 5% of earners recieving .46% less of aggregate income. 
While these results are interesting, they are unsurprising. I was more curious what the effect of Private sector versus Public sector Unionization would be. Running the regression models showed that Private union membership had nearly the same effect as overall union membership, an increase in the middle 60%'s share of the aggregate income (+.46%) and a decrease of the top 5%'s share of aggregate income (-.45%). Public sector unionization had an opposite relationship. A 1% increase in Public sector Unionization was correlated with the middle 60% recieving .37% less of aggregate income, while being correlated with the top 5% recieving .37% more. 


