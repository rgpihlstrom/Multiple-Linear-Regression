# Phase 2 Project

![Film_Crew](/images/KingCountyRealty.png)

# King County Realty - Increasing Revenue From Seller Commisions

**Authors**:[Russell Pihlstrom](mailto:rgpihlstrom@yahoo.com)

## Overview

This project uses Multiple Linear Regression to make predictions on potential future prices of homes sold in King County Washington and potentially surrounding areas.  By analyzing past actual prices for homes sold against the features of each respective home I developed a predictive model that explains 82% (R^2 = .82) of the variability in price.  This algorithm,“model”, can be used to predict the value each feature contributes to the final sales price of a home along with predicting potential future sales prices for homes where required data to run the model are available.  The following 6 features had the greatest weights within the model: Previous Year Appraisals Values: School District Rank : Number of Fortune 500 Companies within 10 miles: Grade Of Home: and Quantity of Finishd Above Square Footage.

The model was developed using actual sales transactions from homes sold between May 2014 – May 2015 in the County of King in the state of Washington.  The model was developed to help a hypothetical real estate firm called King County Reality increase revenue from seller commissions by addressing two areas the CEO of King County Reality believes were gaps in current business processes:

1: Help agents make more valuable recommendations to potential home sellers on the features in which to focus improving upon in order to maximize sales price


2:  Setting "better" or more informed sales prices  

Ultimately, the model can be used as both a tool by itself to ensure sellers achieve true Market Value upon sale as well as an educational tool to improve agent acumen.  This will give King County Reality the sophistication it needs to be more successful as it faces challenging predicted trends in higher home prices along with higher levels of inventory in the form of new construction.




## Business Problem

The King County Realty company is looking to increase its revenue from seller commissions.  Housing market experts are predicting a sharp increase in the prices of homes along with increases in housing inventory due to new construction.  The CEO wants to ensure the firm is prepared to appropriately meet the challenges of this new housing market and believes his firm needs to be more data driven in its approach to helping customers buy and sell homes.  The CEO has hired me to help leverage its current data sources along with finding new data sources to help agents in two primary areas

1.	 Better understand and predict the relationship between home improvement projects/ features and there impact on final sales price 
2.	Understand if there are other data sources that agents can use to help set smarter prices

Historically prices are set using several sources of data that is presented to agents in the form of a Comparative Market Analysis (CMA) report.  The CEO is wondering if there are other sources of data to help triangulate the prices set for newly listed homes.

Pressures are mounting as home prices along with the number of building permits issued is expected to rise over the next five years.  Furthermore, customer expectations are increasing as is the pressures to stay competitive with other boutique reality firms.


## Data
1.	Provided Data: The initial source of data entailed approximately 21k sales transactions for houses sold between May 2014 – May 2015 in King County in the state of Washington, along with the actual agreed to sales prices, other homes basic attributes were provided: Home dimensions (Square Foot Lot, Square Foot Upper, Square Foot Basement, Grade of Home, Condition of Home, Views Available, Other misc features)

2.	Scraped Data: Home Tax data collected by King County Tax Assessor’s Office:  This data contains several years of past appraisal information used to justify taxes levied per house.  Including additional physical attributes as well as school district

3.	Scraped Data: King County School District & Rank:  This data is used to get the ranking of the school district associated with each of the homes in the initial dataset discussed above
3.	Downloaded Data: I downloaded a variety of other data such as “Hot Zip Code” data, Attraction data, as well as creating custom bins/ groupings of data that was used in supporting model development

## Methods



This project uses the Crisp DM methodology to generate and optimized the final Multiple Linear Regression model.  The model developed provides the opportunity to use a home’s features (physical and or location based) as well as other information scraped from the assessor’s office including the home appraisal tax data.  The top 6 features, attributes that had the heaviest weights (coefficients), in predicting a home’s price were : Previous Year Appraisals Values: School District Rank : Number of Fortune 500 Companies within 10 miles: Grade Of Home: and Above Square Footage.  In addition to those listed several other features were used in explaining variability in home prices.  

As prescribed by the Crisp DM methodology, model development was very iterative.  I began by doing secondary research around the basic business drivers of the real estate industry, more specifically I researched what features are most attractive to buyers and sellers along with the methods used by real estate agents to set home prices.  Early in the iterative research/ modeling process it was obvious the model was missing key elements to determine the attractiveness of the home’s location.  I addressed this gap by scraping several sources that would allow me to ascertain the richness of a home’s location (School District & Ranking, Proximity to Attractions & Corporate Headquarters of the 12 fortune 500 companies located in King County, Zip Code Hotness Scores, and other misc information).  Unfortunately, only a handful of these sources were present in the final model as the VIF and correlation tests resulted in many of them being excluded.  
Adhering to Linear Regression Assumptions: The assumption requirements associated with using multiple linear regression to make predictions were followed during model development and certainly added to the number of iterations required to find the optimum combination of data & features.  The assumptions include: linearity, multicollinearity, homoscedastic, and error normality.

In terms of data collection, I primarily used scraping, downloading, cleaning & linking via Parcel ID or created keys.
## Results

The final model generated a predictive power (Adj R^2) of .82

![Movie_Genres](/images/Movie_Genre.png)


The features that had the most influence/ weights include: 1.2 x Previous Year Appraisals Values : .34 x Above Square Footage: .22 x School District Rank : .15 Number of Fortune 500 Companies.  Several other features were used in making predictions.  See Power Point Presentation or Jupyter Notebook “Models” for details


![A_Players](/images/A_Players.png)

Based on the model,  using hypothetical changes in the average home features, the model predicted the following results:

![A_Players](/images/Critics_ROI.png)
![A_Players](/images/Critics_Popularity.png)


Greatest Insight:  The weight “Assessor Appraisal Value” had relative to the second most heavy feature “Above Square Footage”.  The reason this was so insight was the lack of reference to this variable in all my research in regards to determining a home’s sales price.  Research suggested the agents use CMA (Comps) to set pricings and while I did not have a feature related to CMA I would hypothesize it would be stronger than “Assessor Appraisal Value” in predictive power, no where in my research did I see anyone recommend using “Assessor Appraisal Value” as a potential feature.  Given it was the heaviest feature in my model I would recommend it be added as a potential attribute to all home predictive models.  Most research suggest the more common features 
“Location, Location, Location” as well as “Above Square Footage” are most helpful in predicting a homes price not “Assessor Appraisal Value
## Extra Credit
Given the greater than 200% greater weight of “Assessor Appraisal Value” feature had above the next most impactful feature, “Above Square Footage”, I thought it would be interesting to see how well our model would predict Assessor “Appraisal Values”, more specifically, I changed the target value of the original model from a homes sales price to  “Assessor Appraisal Value”.  Interesting our model predicted/ explained the Assessor Appraisal Value with greater strength than our second model was able to explain the actual sales price reached, which did not include the “Assessor Appraisal Value” as a feature.   The “Assessor Appraisal Value” features was not added until later models.  See below


![A_Players](/images/Critics_ROI.png)


What this suggests is the factors that the assessors use to create their appraisal is very similar to those that were provided in our initial dataset.  The fact that our model explained more variability in the data of the Assessors Appraisal Value suggests that assessor use more tangible features when creating appraisals, which were present in our initial dataset, than buyers and sellers use to reach final sales price.  More specifically, Assessors rely more heavily on the tangible features when developing appraisals than buyers and seller use to achieve final prices which certainly has an element of intangibility (i.e.. buyer preference, which is entirely subjective)



## Conclusions

This analysis leads to three recommendations helping King County Reality achieve higher seller commissions:

- **Physical "Controllable Features**  As real estate agents look to coach prospective sellers on features to improve to maximize sales price they should focus on “Above Square Footage”, as well as increasing “Grade” which is related to features such as custom cabinets, and other various customizations that make home less basic and more designer/ custom
- **Location "Influenceable" Features”** While the above "controllable" features allow sellers to make short-term efforts and realize instant benefits, location based features such as the ranking of the school district in which a home resides or the number of attractions within close proximity to a home is very difficult to impact in a direct manner.  However, over the course of several years a home owner can look to invest in efforts and finances to improve school performance and or influence political decisions related to politicians who believe in bringing more attractions to the area in which a home resides.
- **Setting "Better" More Informed Prices**  Based on the 200% delta between the “Assessor Appraisal Value” feature and the next biggest feature suggests that this feature could be very instrumental in augmenting the current processes real estate agents use in setting prices.  This could be especially true in situation where CMA data is neither not available, nor as applicable as desired.

### Next Steps

Further analyses could yield additional insights to help King County Reality Increase Revenue from Sales Commissions
- **Augment the Current Model** Look to add prediction accuracy by studying the homes that showed the largest difference between the predicted and the actual prices of homes sold.  Additionally, looking to add features requiring interactivity could be explored as many factors that would seem to be impactful were eliminated due to VIF.
- **Creating Additional Models**  The model created was optimized for the most frequent "Common/ Main stream" home prices, quantity of square footage, number of bathroom/ rooms, lot size and several other related features were used to predict homes that would be found in the middle of the bell curve of a normalized dataset (Homes between ~$300-~$900k, Bedrooms between 1-4, Lot Size 4,000 – 12,000, Other).  Additional models could be created focused on homes <$200k, >$900k, Waterfront, large Lot Size, etc 
- **Deployment** Once we have optimized our models and or generated enough models to account for the wide variety of home present in the King County district I would look to automate and deploy the models via a web based interface and make it available to the larger public for impromptu consumption and a potential Marketing tool to generate web traffic and brand awareness

## For More Information

See the full analysis in the [Jupyter Notebooks](folder) or review our <a href="https://github.com/mattielips/movie-data-analysis/blob/master/Presentation.pdf">Presentation</a>.

For additional info, contact me here: [ Russell Pihlstrom](mailto:rgpihlstrom@yahoo.com)


## Repository Structure

```
├── CastandCrew_Analysis.ipynb
├── Critics_Analysis.ipynb
├── debug.log
├── images
    ├── Windows_Background.png
    ├── ProfitsByPlayers.png
    ├── Film_Set.png
    ├── Movie_Genre.png
    ├── Critics_Popularity.png
    ├── Critics_ROI.png
    ├── BoxPlot-Average$.pdf
    ├── BoxPlot-Average$.png
    ├── BoxPlot-#OfMovies.png
    └── A_Players.pngnotebooks
├── Presentation.pdf
├── ProductionStudios_Analysis.ipynb
├── README.md
├── Webscraping
    ├── CreatingMasterFinanceTable.ipynb
    ├── CreatingMasterMovieCatalog_DF.ipynb
    ├── Get_Known_For_MoviesData.ipynb
    ├── Get_MetaData_FromFinanceTables.ipynb
    ├── Preping_StarPlayer_Dfs_10_10.ipynb
    ├── Preping_StarPlayer_Dfs.ipynb
    └── ScrapingIMDB.ipynb
└── zippedData
    ├── bom.movie_gross.csv.gz
    ├── df_Financials_SummaryAndDetail_Imdb_Dom.xlsx
    ├── df_Generes_With_tconst.xlsx
    ├── df_IMDB_Akas_english.xlsx
    ├── df_IMDB_MovieCatalog.xlsx
    ├── df_MasterFinancials_MetaData.xlsx
    ├── df_MasterFinancials.xlsx
    ├── df_Movie_Financials.xlsx
    ├── df_StarActors_KnownForWithTconst.xlsx
    ├── df_StarActors_NoDups.xlsx
    ├── df_StarActors_With_nconst_tconst.xlsx
    ├── df_StarActors_With_nconst.xlsx
    ├── df_starsplayers_WithContribution.xlsx
    ├── df_Studio_x_ref_For_import.xlsx
    ├── imdb.name.basics.csv.gz
    ├── imdb.title.akas.csv.gz
    ├── imdb.title.basics.csv.gz
    ├── imdb.title.crew.csv.gz
    ├── imdb.title.principals.csv.gz
    ├── imdb.title.ratings.csv.gz
    ├── InflationAdjuster.xlsx
    ├── rt.movie_info.tsv.gz
    ├── rt.reviews.tsv.gz
    ├── tmdb.movies.csv.gz
    ├── tn.movie_budgets.csv.gz
    └── Top_10_By_Genre_Top_Players_new.xlsx
