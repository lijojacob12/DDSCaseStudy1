# Doing Data Science Craft Beer Case Study  

The case study includes the following topics   
  a. Number of breweries across each State  
  b. How are we handling the Missing values and duplicates in the datasets  
  c. Some stats on ABV and IBU variables and their relationship  
  d. Recommendation for new beer  

## Number of breweries across each State  
Most of the breweries seems to be clustered along the west cost, northeast and eastern Midwest US.  
Top 5 States are Colorado, Calfornia, Michigan, Oregon and Texas  

##How are we handling the Missing values and duplicates in the datasets  
Many missing ABV and IBU values were in the data as best we could using external resources.  
Missing data was highly correlated to certain breweries so imputation and exclusion would not be a valid option.  
After filling in most of  ABV data we dropped N/A’s and then imputed the mean for remaining IBU if it was missing based on beer style.  
Total number of dropped beers is 23 or ~ 1% of total  

## Some stats on ABV and IBU variables and their relationship  
### Median ABV  
Kentucky and Delaware are on the top. NJ and UTAH at the bottom. (UTAH has state regulation on maximum ABV)  
The overall Median ABV is 5.6%  

### Median IBU  
West Virginia has high median IBU since sample data set contains only two beers for this state and with higher IBU values.
Some of the beers in New Hampshire has very low IBU values(below 20)
The overall median IBU is 33

### Max ABV  
Colorado - 12.8% Alcohol Content
Lee Hill Series Vol. 5 - Belgian Style Quadrupel Ale by Upslope Brewing Company in Boulder, Colorado has maximum ABV(12.8%)



### KNN Model  
We created a variable called Beer Type("Typ") which holds three values('IPA', 'Other Ales', 'Other Beers').
As part of implementing a KNN model to predict beer types('IPA' and 'Other Ales'), the variables ABV and IBU are used.
Looking at the results of our model it seems to be doing a great job classifying the IPAs vs. Other Ales with an accuracy of ~ 90%, sensitivity ~ 89.5% and specificity ~ 91% with a K value of 5. 

Files included as part of this documentation are  

1. CraftBeerCaseStudy.Rmd  
2. CraftBeerKinit.html  
3. berweries.csv  
4. beer.csv  
5. ReadMe.md  
6. CRAFT_BEER_CASE_STUDY_FINAL.ppt  
