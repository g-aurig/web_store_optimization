# Analytics project - Web Store Optimization

- [Introduction](#Introduction)
- [Objectives](#Objectives)
- [Benchmarks](#Benchmarks)
- [Results](#Results)
- [Insights](#Insights)
- [Recommendations](#Recommendations)
- [Further steps](#Further-steps)
- [Resources](#Resources)

# Introduction
Data is coming from the Google Merchandise Store e-commerce dataset. The dataset is called "bigquery-public-data.ga4_obfuscated_sample_ecommerce.events" and contains data from 1/11-2020 until 31/01/2021. 

![Screenshot 2023-08-24 at 16 04 05](https://github.com/g-aurig/web_store_optimization/assets/138019708/8230bb31-ee40-4faf-a162-2d76188edae0)

# Objectives
The objective of this analytics project is to gain insights of the data with the help of BigQuery &amp; to provide actionable recommendations based on the insights with the aim of reaching business growth.

# Benchmarks
The Average Order Value (AOV) is the average amount customers spend per purchase. The improvement of the AOV to increase the total revenue is one essential pillar for a web shop. For the considered time period the AOV is 69.38 USD.

![Screenshot 2023-09-05 at 10 23 36](https://github.com/g-aurig/web_store_optimization/assets/138019708/d6878c8d-1e40-4593-8849-c0ab47dfe977)

The bars are showing the distribution of the values for each order. The majority of orders are between 10–60 USD, and a very long tail of orders that are more than 150 USD.
The strong dark line shows the share of orders on the total number of orders. 91% of our orders have a value between 0 and 150 USD which is helpful to know when a long tail of order values occurs.

![Screenshot 2023-09-12 at 10 13 37](https://github.com/g-aurig/web_store_optimization/assets/138019708/7b404e20-4e0f-4581-b926-840c1913ed28)

An additional benchmark value can be the Cart Abandonment Rate which indicates how many users initialized the checkout without completing their purchase. For the Google Merchandise shop this rate is 85.31%.

![Screenshot 2023-09-05 at 14 38 13](https://github.com/g-aurig/web_store_optimization/assets/138019708/59ce1abe-3a78-4837-a585-d1610a35f246)

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

![Screenshot 2023-08-29 at 11 18 19](https://github.com/g-aurig/web_store_optimization/assets/138019708/cbd37902-581c-4e78-a55e-d04feb110997)

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
- Do a deep dive into analysing the checkout process steps to discover optimisation potential.

## Resources
The analysis has been done with the help of the following online resources.
- [Median, Mode, and Average Order Value in BigQuery using SQL by Romain Granger](https://towardsdatascience.com/median-mode-and-average-order-value-in-bigquery-using-sql-8952bfbc288a)




