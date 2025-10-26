# Summary and Analysis

The used-car price analysis examined 426,000 listings across the United States to identify the main factors influencing vehicle resale value. After cleaning the data to remove duplicates, outliers, and unrealistic values, key predictors such as vehicle age, mileage, condition, manufacturer, model, fuel type, and region were analyzed. A machine learning pipeline was developed using Linear Regression and a Random Forest Regressor. The results showed that Random Forest performed better. The most influential factors included vehicle age, odometer reading, and condition, which together explained most of the observed depreciation pattern in the data. Other contributors, such as manufacturer reputation, drivetrain type, and region, also played meaningful roles. Overall, the analysis shows that used-car prices are primarily driven by depreciation (age and mileage), quality indicators (condition and brand), and market factors (location and vehicle type).




| Factor                   | Direction of Effect | Explanation                                        |
| ------------------------ | ------------------- | -------------------------------------------------- |
| **Age**                  | ↓ Negative          | Older cars lose value rapidly                      |
| **Odometer (log)**       | ↓ Negative          | Higher mileage lowers resale price                 |
| **Condition**            | ↑ Positive          | “Excellent” or “Like New” cars command premiums    |
| **Manufacturer / Model** | Mixed               | Brand and model reputation drive price differences |
| **Drive (AWD/4WD)**      | ↑ Positive          | All-wheel drive vehicles often priced higher       |
| **Transmission**         | ↑ (Automatic)       | Automatics typically more desirable                |
| **Fuel type**            | ↑ (Hybrid/Electric) | Green vehicles fetch higher resale                 |
| **Region/State**         | Mixed               | Reflects local demand and weather-related wear     |
