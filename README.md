# Data 115 Personal Project
# Personal Data Set 
I set out to learn more about the relationship between Union Membership and Income Inequality in the United States. More specifically, this dataset looks to answer whether Union Membership in the Private Sector or in the Public Sector has a larger effect on the share of income going to the top 5% and middle 60% of the country.  Data on Union membership were gathered from the U.S. Historical Tables on Union Membership, Coverage, Density and Employment found on Unionstats.com. Data on income inequality are from the U.S Census Historical Income Tables (Table H-2). 


For Income Inequality data, columns displaying the number of observations (in thousands) were deleted, as they were not relevant for the analysis. Data from unionstats was cleaned to only include the percentage of Private sector workers that were unionized, excluding data on the overall number of members, number of observations, raw number of individuals covered, and the percent of individuals covered. These steps were repeated with the data for Public sector workers. Income inequlity data for years 1967-1976 and the year 2020 were excluded because there was no matching data on overall Union membership for those years. Union membership rate in 1982 were missing completely at random. Mean substitution was employed, using data from the years 1981 and 183. To create the column showing the share of aggregate income recieved by the middle 60%, numbers for the second, third, and fourth fifths on the population were summed. 


Column names one, two, three, four, and five refer to the share of aggregate income recieved by the each fifth of the population. One5 shows the share for the bottom 5th and five5 contains the share of income recieved by the top 5th of the country. fivepercent shows the shae of income recieved by the top 5% of earners. midsixty shows the sum of the middle 3/5ths of the population, representing the share of income recieved by the middle 60% of the country. 

<img src="file:///Users/timpendry/Desktop/Data%20Analysis/data-plot.html"
This is a plot of decreasing union membership over time. Data is pulled from unionstats.com and the Institute for Economic Policy. 
