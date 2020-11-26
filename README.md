# Phase 2 Project

![Film_Crew](/images/KingCountyRealty.png)

# King County Realty - Increasing Revenue From Seller Commisions

**Authors**:[Russell Pihlstrom](mailto:rgpihlstrom@yahoo.com)

## Overview

This project is focused on leveraging Multiple Linear Regression to make predictions on the prices of homes.  It features data captured between 2014 - 2015 of the actual sales prices of homes sold in King County Seattle between this timeframe.  It also features ancillary supporting data scraped from several sources include the King County Assessor’s office along with King County School District data.

The goal of the project is to accurately predict the price in which each home sold using the attributes(features) associated with each home.  The generated model was able to achieve a “Predictive Power” of 82% prices (R^2 = .82).  The following 6 features had the greatest weights within the model: Previous Year Appraisals Values: School District Rank : Number of Fortune 500 Companies within 10 miles: Grade Of Home: and Above Square Footage.

The Model will be used by Real Estate agents in two capacities: 

1: Making recommendations to potential home sellers on the features they should focus on improving prior to sale

2:  Setting "better" or more informed prices.  

Ultimately, this model will help the King County Reality Co. increase revenue from seller commissions as more informed agents and smarter prices will facilitate higher home sales prices and higher home sales prices will translate into higher seller commissions.  The model can be used as both a tool by itself to ensure sellers achieve true Market Value as well as a educational tool to improve agent acumen.  This will give King County Reality the tools it needs to be more successful as it faces predicted trends in higher home prices along with higher levels of new construction.




## Business Problem

The king County Realty company is looking to increase its revenue from seller commissions.  Housing market experts predict a spike in the prices of homes along with increases in housing inventory due to new construction.  The CEO wants to ensure the firm is prepared to appropriately meet the challenges of this new housing market and believes his firm needs to be more data driven in its approach to helping customers buy and sell homes.  The CEO has hired me to help leverage its current data sources along with finding additional data sources required to help agents in two primary areas

1.	 Better understand and predict the relationship between home improvement projects and their impact on final sales price.  
2.	Understand if there are other data sources that agents can use to help set smarter prices.

Historically prices are set using several sources of data that is presented to agents in the form of a Comparative Market Analysis (CMA) report.  
Pressures are mounting as home prices along with the number of building permits issued is expected to rise over the next five years.  Customer expectations are increasing as is the pressures to stay competitive.


## Data
1.	Houses sold between May 2014 – May 2015 in King County in the state of Washington, along with the homes basic attributes: This was the intial data provided to begin the project

2.	Home Tax data collected by King County Tax Assessor’s Office:  This data contains several years of past apprasal information used to justify taxes levied per house.  Includings additional physical attributes as well as school district

3.	King County School District Ranks:  This data is used to get the ranking of the school district associated with each of the homes in the initial dataset discussed above


<ol>
    <li>Box Office Mojo: Reporting & analysis service that tracks box office receipts. Data includes         daily, weekly, weekend, monthly, yearly, seasonal, and holiday box-office grosses & is linked         by movie title and year of release. </li>
    <li>IMDB : Database with information related to films, including cast, crew, fan and critical             reviews & ratings.  Data is linked through unique movie keys (tconst) & person keys (nconst).     </li>
    <li> Rotten Tomatoes:  The leading online aggregator of movie and TV show reviews. Data linked by          rotten tomatoes ID. </li>
    <li> The Numbers:  Detailed financial analysis, from box office to Blu-ray sales. Data linked by movie name, release year, person name & birthday</li>
</ol>



## Methods



This project uses the Crisp DM methodology to generate a Multiple Linear Regression model optimized to predict the sales prices for each of the homes sold within the aforementioned timeframe.  The model developed provides the opportunity to use a homes features (physical and or location based) as well as other information collected by the assessors office including the home appraisal tax data.  The top 6 features (attributes) that had the heaviest weights (coefficients) in predicting a homes price includes : Previous Year Appraisals Values: School District Rank : Number of Fortune 500 Companies within 10 miles: Grade Of Home: and Above Square Footage. 

The methodology for model development was very interactive.  I began by doing secondary research around the basic drivers of the real estate industry, more specifically is researched what features are most attractive to buyers and sellers along with the methods used by real estate agents to set home prices.  Early on in the iterative research/ modeling process it was obvious the model was missing key elements to determine the attractiveness of the location of each home.  I rectified this gap by scraping several location riches sources of data.  Unfortunately, only a handful of these sources were present in the final model as the VIF and correlation tests resulted in many of them being excluded.  

The assumption requirements associated with using multiple linerar regression to make predictions were followed during model development.  The assumptions include: linearity, multicollinearity, homoscedastic, and error normality.

In terms of data collection I primarily scraping, downloading, cleaning & linking via provided or created keys.


## Results

The final model generated a predictive power (Adj R^2) of .82

![Movie_Genres](/images/Movie_Genre.png)


The features that had the most influence/ wieghts include: 1.2 x Previous Year Appraisals Values : School District Rank : Number of Fortune 500 Companies within 10 miles: Grade Of Home: and Above Square Footage.


![A_Players](/images/A_Players.png)

Based on the model usings hypothetical changes in the average home features in the model resulted in the following

![A_Players](/images/Critics_ROI.png)
![A_Players](/images/Critics_Popularity.png)

## Extra Credit

Given the greater than 200% greater weight of Assesor Apprasail Value feature had above the next most impactful feature, above square footable, I thought iit would be interesting to see how well our model would predict Assesor Apprasail Values, more specifically I changed the target value of the original model from a homes sales price I used it to predict the Assesor Apprasail Value.  Interesting our model predicted/ explained the Assesor Apprasail Value with greater strenght than our second model generated, which did not include the Assesor Apprasail Value as a feature.   The Assesor Apprasail Value features was not added until my third and forth models.  See below.


![A_Players](/images/Critics_ROI.png)


What this suggestes is the factors that the assesors use to create their appraisal is very simliar to those that were provided in our inital dataset.  The fact that our model explained more variablilyt in the data of the Assesors Apprasal value suggests that assesor use more tanggible features when creating appraisals and then final price buyers pay for a home has factors that are not as tangabli in nature, ie. subject preference



## Conclusions

This analysis leads to three recommendations helping King County Reality acheive higher seller commisions:

- **Physical "Controllable Features**  As real estate agents look to coach prospective sellers on features to improve to maximize sales price they should focus on Square Foot Main Level, as well as increasing Grade related features such as custom cabinets, and other various customozizations that make home less basic and more custom
- **Location "Influencable" Features”** WHile the above "controllable" features allow sellers to make short-term efforts and realize instant benefits, location based features such as the ranking of the school district in which a home resides or the number of attractions within close proximity to a home is very difficult to impact in a direct manner.  However, over the course of several years a home owner can look to invest in efforts and finances to improve school performance and or influence political decisions related to politicians who believe in bringing more attractions to the area in which a home resides.

- **Setting "bBtter" More Informed Prices**  Based on the 200% delta between the Assesor Apraisal feature and the next biggest feature suggests that this feature could be very intrumental in augmenting the current processes real estate agents use in setting prices.  This could be especially true in situation where CMA data is either not available or not as applicable as desired.

### Next Steps

Further analyses could yield additional insights to help King County Reality Increase Revenue From Sales Commisions

- **Augment the Current Model** Look to add prediction accuracy by studying the homes that showed the largest difference between the predicted and the actual values of a the sold home.  Additionally looking to features requiring interactivity could be explored as many factors that would seem to be impactful were elimnated due to VIF.
- **Creating Additional Models**  The model created was optimized for the most frequent "Common/ Main stream" home prices, quantity of square footage, number of bathroom/ rooms, lot size and several other realated features were honed to predict homes that would be foound in the middle of the bell curve for normalized data.  Additional models could be created focused on homes <$200k, >$900k, Waterfront, large Lot Size, etc 
- **Deployment** Once we have optimized our models and or generated enough model to account for the wide variety of home features that are present in the King County district look to automate and deploy via a web based interface and made available to the larger public for impromptu consumption

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
