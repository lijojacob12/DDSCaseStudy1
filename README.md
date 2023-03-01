# Doing Data Science Craft Beer Case Study  

The case study includes the following topics   
  a. Number of breweries across each State  
  b. How are we handling the Missing values and duplicates in the datasets  
  c. Some stats on ABV and IBU variables and their relationship  
  d. Recommendation for new beer  

  ## Number of breweries across each State  
  Most of the breweries seems to be clustered along the west cost, northeast and eastern Midwest US.  
  Top 5 States are Colorado, Calfornia, Michigan, Oregon and Texas  

  ## How are we handling the Missing values and duplicates in the datasets  
  Many missing ABV and IBU values were in the data as best we could using external resources(https://www.brewerydb.com/  and  https://untappd.com/home)  
  Missing data was highly correlated to certain breweries so imputation and exclusion would not be a valid option.  
  After filling in most of  ABV data we dropped N/A’s and then imputed the mean for remaining IBU if it was missing based on beer style.  
  Total number of dropped beers is 23 or ~ 1% of total  
  
  Note: Commented code in the missing value section is to determine the breweries or style not missing at random.

  ## Some stats on ABV and IBU variables and their relationship  
  ### Median ABV  
  Kentucky and Delaware are on the top. NJ and UTAH at the bottom. (UTAH has state regulation on maximum ABV)  
  The overall Median ABV is 5.6%  

  ### Median IBU  
  West Virginia has high median IBU since sample data set contains only two beers for this state and with higher IBU values.
  Some of the beers in New Hampshire has very low IBU values(below 20)
  The overall median IBU is 33

  ### Maximum ABV  
  Colorado - 12.8% Alcohol Content
  Lee Hill Series Vol. 5 - Belgian Style Quadrupel Ale by Upslope Brewing Company in Boulder, Colorado has maximum ABV(12.8%)
  State Colorado has the lack of legal restrictions, the high altitude, and the state's brewing culture which are some of the reasons why ABV is high in their beers  

  ### Maximum IBU 
  Bitter Bitch Imperial IPA by Astoria Brewing Company in Astoria, Oregon is the most bitter beer(IBU - 138)  
  The bitterness in this beer is achieved through the use of a blend of six different hops, which are added to the beer during the brewing process.  

  ### ABV summary  

  Mean is 5.97% and Median is 5.6%.  
  Since mean is greater than median,  ABV data is right skewed  
  We created a variable called Beer Type("Typ") which holds three values('IPA', 'Other Ales', 'Other Beers').  
  By looking at different types of beers the distribution shows that Ales other than IPA and Other type of beers are causing right skewness. Distribution IPA seems to be reasonably normal  

  ### ABV-IBU Relationship

  The evidence suggest that there is a positive relationship between IBU and ABV.  
  Soft cap on ABV at 10% which might be due to state regulations in some of the states.  
  By looking at the data based on Type of beers, IPA tent to have more bitterness for same Alcohol content when compared with other Ales and other type of beers.  

  ### KNN Model  
  We iterated 200 times for values of K ranging from 1-20 and found that the optimal value for K is 5.  
  As part of implementing a KNN model to predict beer types('IPA' and 'Other Ales'), the variables ABV and IBU are used.
  Looking at the results of our model it seems to be doing a great job classifying the IPAs vs. Other Ales with an accuracy of ~ 90%, sensitivity ~ 89.5% and specificity ~ 91% with a K value of 5. 

  IPAs tend to be somewhere above 50 IBU’s and ales tend to fall below 50 IBU’s.

  ### Recommendation for new beer  

  Low concentration of IPAs & Ales in southern part of the US  
  Florida has the 3rd largest population and Georgia has the 8th highest population in the US  
  Our recommendation is to release a new beer IPA or Ale in the Florida/Georgia as there is the most opportunity in the state based on our analysis.  

 ### Summary  
  Breweries seems to be clustered along the west cost, northeast and eastern Midwest US.  
  The evidence suggest as IBU goes up so does ABV.  
  The evidence suggest that a common defining factor between IPAs and Other Ales is IBU  
  To introduce new beers, Budweiser should look to release a new IPA or Ale in Florida and/or Georgia.  

## Files  
Files included as part of this documentation are  

1. CraftBeerCaseStudy.Rmd  
2. CraftBeerKinit.html  
3. berweries.csv  
4. beer.csv  
5. ReadMe.md  
6. CRAFT_BEER_CASE_STUDY_FINAL.ppt  
