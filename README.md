# Phase 2 Project

![Film_Crew](/images/KingCountyRealty.png)

# King County Realty - Increasing Revenue From Seller Commisions

**Authors**:[Russell Pihlstrom](mailto:rgpihlstrom@yahoo.com)

## Overview

This project uses Multiple Linear Regression to make predictions on potential future prices of homes sold in King County Washington and potentially surrounding areas.  By analyzing past actual prices for homes sold against the features of each respective home I developed a predictive model that explains 82% (R^2 = .82) of the variability in price.  This algorithm,“model”, can be used to predict the value each feature contributes to the final sales price of a home along with predicting potential future sales prices for homes where required data to run the model are available.  The following 6 features had the greatest weights within the model: Previous Year Appraisals Values: School District Rank : Number of Fortune 500 Companies within 10 miles: Grade Of Home: and Quantity of Finishd Above Square Footage.

The model was developed using actual sales transactions that took place between May 2014 – May 2015 in the County of King in the state of Washington.  The model was developed to help a hypothetical real estate firm called King County Reality increase revenue from seller commissions by addressing two areas the CEO of King County Reality believes were gaps in current business processes:

1: Help agents make more valuable recommendations to potential home sellers on the features in which to focus improving upon in order to maximize sales price.  The model allowed me to advise agents to reccomend focusing potential sellers in the following areas: **Above Square Footable, Grade of Home, Improving School District, Inviting Fortune 500 expansion/ addition**


2:  Setting "better" or more informed sales prices.  Beyond simply analyzing the impact features can have on predicting sales prices, my research suggestion adding **Assesor Apprasal Value** as a future feature to make more acurate predictions.  This is a feature that had no mentions as a vaulable predictor previous to my discovery through final model creation.

Ultimately, the model can be used as both a tool by itself to ensure sellers achieve true Market Value upon sale as well as an educational tool to improve agent acumen.  This will give King County Reality the sophistication it needs to be more successful as it faces challenging predicted trends in higher home prices along with higher levels of inventory in the form of new construction.




## Business Problem

The King County Realty company is looking to increase its revenue from seller commissions.  Housing market experts are predicting a sharp increase in the prices of homes along with increases in housing inventory due to new construction.  The CEO wants to ensure the firm is prepared to appropriately meet the challenges of this new housing market and believes his firm needs to be more data driven in its approach to helping customers buy and sell homes.  The CEO has hired me to help leverage its current data sources along with finding new data sources to help agents in two primary areas

1.	Better understand and predict the relationship between home improvement projects/ features and there impact on final sales price 
2.	Understand if there are other data sources that agents can use to help set smarter prices

Historically prices are set using several sources of data that is presented to agents in the form of a Comparative Market Analysis (CMA) report.  The CEO is wondering if there are other sources of data to help triangulate the prices set for newly listed homes.

Overall, pressures is mounting as home market dynamics are increasing as well as customer expectations and competition faced from other boutique reality firms.


## Data
1.	Provided Data: The initial source of data entailed approximately 21k sales transactions that took place between May 2014 – May 2015 in the count of King in the state of Washington.  In addition to providing the actual sales price reached for each home, the provided data also included metadata for each home sold such as: Square Footage of Lot, Square Footage Above, Square Footage of Basement, Grade of Home, Condition of Home, Views Available, Other misc features.

2.	**Scraped Data**:King County Tax Assessor Data:  This data contains several years of past appraisal information used to justify taxes levied per house.  The data from the Tax Assesor Office also include additional physical attributes as well as school district associated with each Parcel ID.  Example: https://blue.kingcounty.com/Assessor/eRealProperty/Dashboard.aspx?ParcelNbr=7338200240


3.	**Scraped Data**: King County School District & Rank:  This data is used to get the ranking of the school district associated with each of the homes in the initial dataset discussed above.   Example: https://backgroundchecks.org/top-school-districts-in-washington-2018.html

3.	**Downloaded Data**: I downloaded a variety of other data such as “Hot Zip Code” data, Attraction data, as well as creating custom bins/ groupings of data that was used in supporting model development.  Example: https://www.realtor.com/research/reports/hottest-markets/

## Methods
This project uses the Crisp DM methodology to generate and optimized the final Multiple Linear Regression model.  The model developed provides the opportunity to use a home’s features (physical and or location based) as well as other information scraped from the assessor’s office including the home appraisal tax data.  The top 6 features, attributes that had the heaviest weights (coefficients), in predicting a home’s price were : Previous Year Appraisals Values: School District Rank : Number of Fortune 500 Companies within 10 miles: Grade Of Home: and Above Square Footage.  In addition to those listed several other features were used in explaining variability in home prices.  

As prescribed by the Crisp DM methodology, model development was very iterative.  I began by doing secondary research around the basic business drivers of the real estate industry, more specifically I researched what features are most attractive to buyers and sellers along with the methods used by real estate agents to set home prices.  Early in the iterative research/ modeling process it was obvious the model was missing key elements to determine the attractiveness of the home’s location.  I addressed this gap by scraping several sources that would allow me to ascertain the richness of a home’s location (School District & Ranking, Proximity to Attractions & Corporate Headquarters of the 12 fortune 500 companies located in King County, Zip Code Hotness Scores, and other misc information).  Unfortunately, only a handful of these sources were present in the final model as the VIF and correlation tests resulted in many of them being excluded.

**Adhering to Linear Regression Assumptions**: The assumption requirements associated with using multiple linear regression to make predictions were followed during model development and certainly added to the number of iterations required to find the optimum combination of data & features.  The assumptions include: linearity, multicollinearity, homoscedastic, and error normality.

## Results
The final model generated a predictive power (Adj R^2) of .82

<img src="/images/Model_Final_Results.png" width="400" height="300" align="left">

**The features that had the most influence/ weights include:** 

    - 1.2 x (Previous Year Appraisals Values)

    - .34 x (Above Square Footage)

    - .22 x (School District Rank)

     - .15 x (Number of Fortune 500 Companies)

     - Other x (See Power Point Presentation or Jupyter Notebook “Models” for details)



  


![A_Players](/images/ChangesInAveargeHome.png)

**Greatest Insight**:  The weight “Assessor Appraisal Value” had relative to the second most heavy feature “Above Square Footage”.  The reason this was so insightful was the lack of reference to this variable in all my research in regards to determining a homes sales price.  Research suggested the agents use CMA (Comps) to set pricings and while I did not have a feature related to CMA in my model I would hypothesize it would be stronger than “Assessor Appraisal Value” in predictive power.  That being said, I hypothesize that "Assessor Appraisal Value" would be the second most heavy feature in a model that contained both "Comp Prices" and "“Assessor Appraisal Value". Given this hypothesis I would recommend it be added as a potential attribute to all home predictive models.  Most research suggest the more common features “Location, Location, Location” as well as “Above Square Footage” as the most helpful, “Assessor Appraisal Value" is currently being overlooked.

## Extra Credit
Given the greater than 200% difference in wieght between the “Assessor Appraisal Value” feature had the next most impactful feature, “Above Square Footage”, I thought it would be interesting to see how well our model would predict "Assessor Appraisal Values”, more specifically, used the orginal model and changed the target value  predicted "Homes Sales Price to predicted “Assessor Appraisal Value”.  Interestingly my model predicted/ explained the "Assessor Appraisal Value" with greater strength than "Homes Sales Price".  Keep in mind my second model did not include the “Assessor Appraisal Value” as a feature. See below for a comparison of the same model predicting both "Home Price" and "Assesors Appraisal Value"





![NA](/images/Original_vs_Assesor_Value.png)


**INSIGHT** What this suggests is the factors that the assessors use to create appraisals are very similar to those that were provided in our initial dataset and using to build our early models.  The fact that our model explained more variability in "Assessors Appraisal Value" suggests that assessor use more tangible features when creating appraisals vs. intangilble features.  This conclusion can be drawn given the heavy presence of tangible featrues in the dataset.  More specifically, Assessors rely more heavily on the tangible features (Above Sqr Ft, Lot Size, Grade, Etc.) when developing appraisals than buyers and seller use to achieve in reaching final prices.  Hypothesized intangibility features buyer and sellers use to reach final sales price are skewed toward and or incorporate buyer preference, which is entirely subjective.



## Conclusions/ Reccomendations
This analysis leads to three recommendations helping King County Reality achieve higher seller commissions:

**Physical "Controllable Features**  As real estate agents look to coach prospective sellers on features to improve to maximize sales price they should focus on “Above Square Footage”, as well as increasing “Grade” which is related to features such as custom cabinets, and other various customizations that make home less basic and more designer/ custom
<br>
<img src="/images/ControlableFeatures.png" width="500" height="300"></image>
<br>  
**Location "Influenceable" Features”** While the above "controllable" features allow sellers to make short-term efforts and realize instant benefits, location based features such as the ranking of the school district in which a home resides or the number of attractions within close proximity to a home is very difficult to impact in a direct manner.  However, over the course of several years a home owner can look to invest in efforts and finances to improve school performance and or influence political decisions related to politicians who believe in bringing more attractions to the area in which a home resides.
<br>
<img src="/images/InfluencableFeatures.png" width="500" height="300"></image>
<br>
**Setting "Better" More Informed Prices**  Based on the 200% delta between the “Assessor Appraisal Value” feature and the next biggest feature suggests that this feature could be very instrumental in augmenting the current processes real estate agents use in setting prices.  This could be especially true in situation where CMA data is neither not available, nor as applicable as desired.
<br>
<img src="/images/taxAssesorValues.png" width="500" height="300"></image>

## Next Steps

Further analyses could yield additional insights to help King County Reality Increase Revenue from Sales Commissions
- **Augment the Current Model** Look to add prediction accuracy by studying the homes that showed the largest difference between the predicted and the actual prices of homes sold.  Additionally, looking to add features requiring interactivity could be explored as many factors that would seem to be impactful were eliminated due to VIF.
- **Creating Additional Models**  The model created was optimized for the most frequent "Common/ Main stream" home prices, quantity of square footage, number of bathroom/ rooms, lot size and several other related features were used to predict homes that would be found in the middle of the bell curve of a normalized dataset (Homes between ~$300k - ~$900k, Bedrooms between 1-4, Lot Size 4,000 – 12,000, Other).  Additional models could be created focused on homes <$200k, >$900k, Waterfront, large Lot Size, etc 
- **Deployment** Once we have optimized our models and or generated enough models to account for the wide variety of home present in the King County district I would look to automate and deploy the models via a web based interface and make it available to the larger public for impromptu consumption and a potential Marketing tool to generate web traffic and brand awareness

## For More Information

See the full analysis in the [Jupyter Notebooks](folder) or review our <a href="https://github.com/mattielips/movie-data-analysis/blob/master/Presentation.pdf">Presentation</a>.

For additional info, contact me here: [ Russell Pihlstrom](mailto:rgpihlstrom@yahoo.com)
