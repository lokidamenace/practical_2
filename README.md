## Executive Summary

This analysis aimed to identify the key factors driving used car prices to provide actionable insights for a used car dealership. By analyzing a large dataset of used car listings, we built and evaluated several regression models to predict car prices. The Random Forest Regressor model performed best, and its feature importance analysis revealed that **car age, odometer reading, vehicle condition, and region are the most significant predictors of used car prices.** These findings confirm that depreciation, quality, and local market conditions play crucial roles in determining a used car's value.

## Analysis and Model Performance

The used-car price analysis examined 426,000 listings across the United States to identify the main factors influencing vehicle resale value. After cleaning and preparing the data, including handling missing values, creating new features like 'car_age' and 'odometer_per_year', and encoding categorical variables, three regression models were used: Linear Regression, Random Forest Regressor, and Gradient Boosting Regressor. The performance of these models was evaluated using Mean Absolute Error (MAE), Mean Squared Error (MSE), and Root Mean Squared Error (RMSE).

| Model             | MAE            | MSE             | RMSE           |
|-------------------|----------------|-----------------|----------------|
| Linear Regression | 169,262.52     | 5.33e+13        | 7,297,692.52   |
| Random Forest     | 75,596.36      | 5.59e+13        | 7,474,759.16   |
| Gradient Boosting | 255,159.91     | 6.24e+13        | 7,900,003.86   |

The Random Forest model exhibited the lowest MAE, indicating that its predictions were, on average, closest to the actual prices among the other models. While the MSE and RMSE were high across all models due to outliers and the nature of the data, the MAE provides a more robust measure for this context.

## Key Findings and Drivers of Price

The feature importance analysis from the Random Forest model highlighted the following as the most influential factors in determining used car prices:

*   **Region:** The geographic location significantly impacts price, reflecting variations in local market demand, taxes, and availability.
*   **Odometer:** Higher mileage generally leads to lower prices due to wear and tear and perceived remaining lifespan.
*   **Car Age:** Older cars depreciate more, resulting in lower market values.
*   **Condition:** Cars in better condition ('excellent', 'like new') command higher prices.
*   **Odometer per Year:** This feature, a derivative of odometer and age, also contributes to price prediction, indicating average annual usage.
*   **Manufacturer and Model:** Brand reputation, popularity, and model-specific factors influence pricing.

Other factors like paint color, type, and state also have some influence but are less impactful than the primary drivers.

<img width="2560" height="1385" alt="features" src="https://github.com/user-attachments/assets/42cdd6ef-78cc-4bbf-94c2-10a52df0092f" />

## Recommendations for the Dealership

Based on these findings, the following recommendations are made to the used car dealership:

1.  **Focus on Inventory with Lower Age and Odometer:** Prioritize acquiring and stocking newer cars with lower mileage, as these are in higher demand and command better prices.
2.  **Assess and Highlight Vehicle Condition:** Invest in thoroughly inspecting and reconditioning vehicles to improve their condition. Clearly communicate the excellent or like-new condition of cars to justify higher price points.
3.  **Understand Regional Market Dynamics:** Analyze pricing trends and demand in different regions to optimize inventory sourcing and pricing strategies for specific locations.
4.  **Leverage Brand and Model Popularity:** Stock popular and reputable makes and models that have consistently shown higher resale values.
5.  **Consider Drive Type in Pricing:** Price AWD/4WD vehicles competitively, especially in regions where these are in high demand.
6.  **Use Data-Driven Pricing:** Utilize the insights from this analysis and potentially the trained model to inform pricing decisions for individual vehicles, ensuring competitive yet profitable pricing.
7.  **Target Marketing Efforts:** Tailor marketing campaigns to highlight the key attributes that consumers value most, such as low mileage, excellent condition, and popular models.


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
