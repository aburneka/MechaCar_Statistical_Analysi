
# MechaCar_Statistical_Analysis

AutosRUs’ newest prototype, the MechaCar, is suffering from production troubles that are blocking the manufacturing team’s progress. 

We performed the following statistical analysis for the MechaCar:

* Perform multiple linear regression analysis to identify which variables in the dataset predict the mpg of MechaCar prototypes
* Collect summary statistics on the pounds per square inch (PSI) of the suspension coils from the manufacturing lots
* Run t-tests to determine if the manufacturing lots are statistically different from the mean population
* Design a statistical study to compare vehicle performance of the MechaCar vehicles against vehicles from other manufacturers. 

## Linear Regression to Predict MPG

Image 1: MechaCar multiple linear regression to predict MPG summary statistics
<img width="523" alt="multiple linear regression for MPG " src="https://user-images.githubusercontent.com/79999761/130334891-0d13bcd2-140b-4ccd-b164-9bd81c556edf.png">

## MechaCar multiple linear regression summary

From the summary statistics for the model, vehicle length and ground clearance are both below the siginficance level of 0.05 and can be inferred as to having an statistically significant impact on MPG. It also shows statistical significance for the intercept implying there are features that may need enhancing in order to improve the model.

While the r-squared value for the multiple linear regression model is 0.71 and our p-value is below the significance level of 0.05, which means the slope of our line is not zero, but the null hypothesis cannot be rejected because there are fewer variables that show statistical significance than those that don't in the current model.

While our model's statistics pass our r-squared (>0.7) and p-value (<0.05>) test, we can state that this model does not effectively predict mpg of the MechaCar prototypes as the statisitcal significance of the intercept implies this model is subject to over fitting. Additionally, it tells us there may be other variables that explain the variability not included in this specific model.

## Summary Statistics on Suspension Coils

Image 2: PSI Summary Statistics for all Suspension Coil Manufacturing Lots
<img width="430" alt="PSI summary stats" src="https://user-images.githubusercontent.com/79999761/130334897-060c1142-efcc-4d00-b64b-09d62edb4469.png">


Based on the summary data in image 2 we can conclude the overall manufacturing lots in total meet the current specification requirements because the variance is less than 100 PSI.

Image 3: PSI Summary Statistics by Suspension Coil Manufacturing Lots

<img width="571" alt="PSI summary stats by lot " src="https://user-images.githubusercontent.com/79999761/130334907-e93a5846-baac-4310-8f00-959b74339e1e.png">


Based on the summary data in image 3, we can conclude Lots 1 and 2 meet the design specification for the MechaCar suspension coils because the statistical variance of the data in those lots does not exceed 100 PSI. Additionally, we can conclude manufacturing Lot 3 does not meet the design specifications as the statistical variance of 170 PSI for the lot exceeds the minimum variance of 100 PSI.

T-Tests on Suspension Coils

Total Lot
Image 4: T-test for all manufacturing lots for all manufacturing lots 

<img width="444" alt="t-teswt for all manufacturing lots to pop  mean (1500 PSI)" src="https://user-images.githubusercontent.com/79999761/130334930-629661f5-ad93-4782-9a06-2f5c9a41f7ba.png">


Assuming a significance level of 0.05 and a  p-value of 0.06 in the t-test data from image 4, we can conclude that the overall manufacturing lot does not provide enough evidence to eliminate the null hypotheses of the production population being similar to the mean assumption of 1500 PSI.

Lot 1
Image 5: T-test for Lot 1 to population mean (1500 PSI) T-test for Lot 1 to population mean (1500 PSI)
<img width="501" alt="lot 1 t-test" src="https://user-images.githubusercontent.com/79999761/130334916-ddb3ae4b-c578-40a9-b154-e1027098e0ad.png">

Based on p-value of 1 in the t-test data above, we can conclude that the overall manufacturing lot does not provide enough evidence to eliminate the null hypotheses of the production population being similar to the mean assumption of 1500 PSI.

Lot 2
Image 6: T-test for Lot 2 to population mean (1500 PSI) T-test for Lot 2 to population mean (1500 PSI)
<img width="429" alt="lot 2 t-test" src="https://user-images.githubusercontent.com/79999761/130334946-5d53a010-ffb0-4879-b563-6552fbe2e44c.png">

Based on p-value of 0.6 in the t-test data above, we can conclude that the overall manufacturing lot does not provide enough evidence to eliminate the null hypotheses of the production population similar to the mean assumption of 1500 PSI.

Lot 3
Image 7: T-test for Lot 3 to population mean (1500 PSI) T-test for Lot 3 to population mean (1500 PSI)
<img width="421" alt="t-test lot 3" src="https://user-images.githubusercontent.com/79999761/130334948-364436c1-3e27-446a-8d86-eb2e6768923b.png">


Based on p-value of 0.04 in the t-test data above, we can conclude that the overall manufacturing lot allows us to reject the null hypotheses of the production population being similar to the mean assumption of 1500 PSI. This would indicate an issue with this specific production lot.

### Conclusions for Lots
While the total lot may be within the statistical range of the assumption of 1500 PSI, it is clear that unlike Lots 1 and 2, Lot 3 has a production issue that should be looked at.

## Study Design: MechaCar vs. Competition
Consumers typically value the vehicle's price when selecting from similar vehicle offerings.

### Assumptions
Vehicle class, add-on packages, and engine type are similar across vehicle prices being compared.

### Metrics to test
price = vehicle MSRP ($) - Consumers value a vehicle's cost as it is typically one of the largest monetary purchases made in a person's lifetime.

### Hypotheses
Null: MechaCar's market price is priced the same as similar vehicles on the market.
Alternative: MechaCar's market priced is over-priced compared to similar vehicles on the market.
### Statistical testing
To test the above hypotheses we would perform a two-sample t-test using sales data for the MechaCar as one dataset and a random sample of the larger sales data for the rest of similar cars on the market.

### Data needed for statistical testing
We would need a dataset for MechaCar's sales prices and one separate sales price dataset for all similar vehicles.
