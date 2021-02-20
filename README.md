# Project-1
Project 1 for UMN Data Analytics bootcamp.

Mallory Anderson, Ellie Bunz, Pam Meyer, and Zoe Poeschl completed this project.

## Project Requirements
This project required the team to use pandas to clean and format datasets, use a Jupyter Notebook to describe the data exploration and cleanup process, and a second Jupyter Notebook to illustrate the final data analysis. Use Matplotlib to create visualizations of the data.

# Happiness and libraries
Our project looked at library data and happiness data to evaluate two central questions:
- Are there more libraries in happier countries?
- Does usage of libraries correlate with happiness rankings? 

## Questions
- What percent of libraries are public?
    - Library visits per library type (pie chart)
    - Amount of libraries per library type (pie chart)
- What are some of the happiest countries?
    - Top 20 happiest countries (bar chart)
    - Top 20 happiest countries with library usage data (bar chart)
    - Map of overall happiness (heatmap using gmaps)
- Are there more libraries in happier countries?
    - Libraries per country (bar chart)
    - Libraries per capita (heatmap and markers using gmaps)
- Does library use make a happier country?
    - Number of physical loans versus country happiness scores (scatter plot)
    - Number of library visits versus country happiness socres (scatter plot)
    - Count of library visits overlaid with happiness (heatmap and markers using gmaps)
    - Library visits per country (bar graph)

## Methodology
### Data
To answer the questions we identified data sources: 

Happiness data https://www.kaggle.com/unsdsn/world-happiness
Library data https://librarymap.ifla.org/map
Population data https://data.worldbank.org/indicator/SP.POP.TOTL
Capitals data https://www.kaggle.com/nikitagrec/world-capitals-gps

We used one year of data for library, happiness, and population datasets: 2017

### Cleanup and exploration
Each data set was imported into a Jupyter Notebook and put into a dataframe. Then we cleaned the data and ran a series of visualizations to explore our data. Initially we had intended to focus on public libraries, but after completing the library visits per library type and amount of libraries per library type we determined it was best to evaluate all libraries. 

We identified that the library dataset needed to be normalized by population. 

The first step in data cleanup was to combine our dataframes using merge and drop countries with incomplete data. 
To summarize our data for visualizations we used loc to narrow our dataframes to a particular metric: visits, physical loans, and libraries. These new dataframes were grouped using groupby for visualization. 

We generated several maps to illustrate our data. This required latitude and longitude data. Capitol city latitude and longitude were used for the maps. This data was from the World Bank. 

### Data analysis
To answer our central question: Does usage of libraries correlate with happiness ratings we used linear regression to identify if there was a correlation usage and happiness. Two linear regression were completed: 
- number of physical loans at libraries versus country happiness scores 
    - rvalue of -0.295 which is a weak correlation
- number of library visits versus country happiness scores
    - rvalue of 0.39 which is a weak correlation

### Summary
We determined that there was not a strong correlation between library usage and happiness scores. This likely means that happiness scores are influenced by many other variables that were not evaluated within our analysis.

### Post mortem
Many countries had incomplete library data resulting in only a small number of countries being used within our sample. Exploring options for additional library datasets or expanding from only one year of analsyis (2017) and including more years could have increased the size of our sample, which may have had an impact on our results. 

Instead of using the capital latitude and longitude the maps may have been more accurately displayed if location was set on the centerpoint of the country instead. 

To better explore our question we could have completed additional tests. A hypothesis and null hypothesis were developed and it was determined that and ANOVA would have been a good test to run to test library usage and happiness.
