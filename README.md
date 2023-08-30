# Analytics project - Web Store Optimization
![Screenshot 2023-08-24 at 16 04 05](https://github.com/g-aurig/web_store_optimization/assets/138019708/7973626b-94b7-43e0-9d7e-a036bc222ccb)

# Introduction
Data is coming from the Google Merchandise Store e-commerce dataset. The dataset is called "bigquery-public-data.ga4_obfuscated_sample_ecommerce.events" and contains data from 1/11-2020 until 31/01/2021. 

# Objectives
The objective of this analytics project is to gain insights of the data with the help of BigQuery &amp; to provide actionable recommendations based on the insights with the aim of reaching business growth.

# Results
## Items ecommerce funnel with conversion ratios
The ecommerce funnel for items is highly valuable for an online business because it provides a better understanding of how interactions with products occur on the website.
When looking at the ecommerce steps & ratios based on **session scope** the following questions can be examined:
- What frequency are specific products looked at?
- What products were added to the cart?
- What products were removed from the cart?
- How many of these products end up being purchased?
  
By answering these questions, data-informed decisions can be taken to strive for the web store goals in order to achieve the e-commerce strategy.

The screenshot below shows the visualisation of the "item_name" with the ecommerce funnel steps "view_item", "add_to_cart", "begin_checkout" & "purchase" in Looker Studio. Besides, the ratios for "cart_to_view", "checkout_to_view" & "purchase_to_view" are shown.
In the original state, the table is sorted by the "purchase" column, but can easily be sorted by other metrics. The visible end result is limited to ten rows to keep clarity.

![Screenshot 2023-08-29 at 11 18 19](https://github.com/g-aurig/web_store_optimization/assets/138019708/c6b50ceb-de9c-4bcb-8ab1-2e3d3ee45dcc)

## Insights:
- Overall, the item ecommerce funnel looks healthy, i.e. the number is decreasing between the different steps. One exception is row six where "begin_checkout" is lower than "purchase". There could be technical glitches or tracking inaccuracies that result in the "begin_checkout" event not being recorded accurately for all sessions.
- The "cart_to_view" ratio remains in a sound range (0.221-0.338) when looking at the ten top sellers. 
- The "checkout_to_view" ratio depicts substantial differences (0.015-0.060, with the originally lowest value of 0.012 potentially being inaccurate) when looking at the ten top sellers.
- The "purchase_to_view" ratio ranges between 0.012-0.057 when looking at the ten top sellers. 

## Recommendations:
- Make sure that the best selling items are sorted on top of the product page(s) so that they are simple to access for the user.
- Think about actions that increase the "cart_to_view" ratio, e.g. a clear call to action, detailed product descriptions, product reviews & ratings.
- Overview the checkout to increase the "begin_checkout_to_view" ratio. Examine whether the checkout process can be steamlined, if multiple payment options are needed or progress indicators are helpful for users.
- The "purchase_to_view" ratio provides knowledge about where to focus marketing efforts on. 
- Investigate into the root causes for the discrepancy between "begin_checkout" & "purchase" step. In addition do a proper crosscheck of the remaining rows in order to find out if this is a bigger issue.

## Further steps
- Do data comparisons between different date ranges to see developments and trends over time, e.g. seasonal variations.
- Do the same analysis in the opposite direction, i.e. investigating into products considered as "flops" that might need attention in form of improved descriptions, images, or pricing information.
- Do a deep dive into analysing the checkout process to discover optimisation potential.




