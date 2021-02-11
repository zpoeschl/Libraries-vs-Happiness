# Project-1
Project 1 for UMN Data Analytics bootcamp.

##Happiness and libraries
Our project will look at a database of libraries and happiness ratings to see if the availability and use of libraries has any correlation to happiness scores. 
Both datasets have missing countries. We'll have to clean the data to remove missing countries. We'll need to drop countries that aren't in both lists and focus on the public libraries. 

##Methodology
#Hypothesis
We need an independent variable and a dependent. Libraries (x axis) and happiness (y axis). Our assumption is that libraries cause happiness (the more libraries the happier people are). 
#Questions
Are there more libraries in happier countries? (number of libraries)
Does usage of libraries correlate with happiness rankings? (multiple user proxies available)

#Visualizations
Number of libraries in countries with happiness overlay (heat maps)
Happiness by country (bar graph)
Libraries per country (bar graph) 
Scatter plot of physical visits and happiness
Scatter plot of loans and happiness
Is there a correlation, if so how strong is the correlation? (a bit of stat analysis)

#Source of data
Happiness data https://www.kaggle.com/unsdsn/world-happiness
Library data https://librarymap.ifla.org/map

#Jupyter notebook one: data cleaning
Use pandas to clean and format datasets:
Read both CSVs
Add the year (2017) to the happiness data set  
Merge on year and country to drop the data that isn’t in both
Export a clean CSV to upload into the second jupyter notebook and save it as a dataframe

#Jupyter notebook two: visualizations and write up
Jupyter notebook to create the visualizations and do the analysis (6-8 visualizations, ideally two per question)
Write up of findings (preferably within the jupyter notebook as markup cells) 
