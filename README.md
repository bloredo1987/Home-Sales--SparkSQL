# Home-Sales--SparkSQL

### Analysis:
---
<b>What worked:</b><br>

* Average Price for 4-Bedroom Houses by Year:

This query efficiently calculates the average price for four-bedroom houses sold each year. It appropriately uses a GROUP BY clause to aggregate data by year and a WHERE clause to filter for four-bedroom houses. The results are sorted by year, providing a clear summary.
Runtime: Approximately 1.5 seconds.

* Average Price for 3-Bedroom, 3-Bathroom Houses by Year Built:

The query effectively computes the average price for homes with three bedrooms and three bathrooms, grouped by their year of construction. The use of GROUP BY and WHERE clauses is appropriate for the analysis. The results are sorted by year built.
Runtime: Around 0.83 seconds.

* Average Price for 3-Bedroom, 3-Bathroom, 2-Floor, ≥ 2,000 Sqft Homes by Year Built:

This query successfully filters homes based on specific criteria and then calculates the average price for each year they were built. The results are rounded to two decimal places and sorted by year built. This provides valuable insights into a specific segment of the housing market.
Runtime: About 0.54 seconds.

* View Rating for Average Price ≥ $350,000:

The query effectively determines the view rating for homes with an average price greater than or equal to $350,000. Proper use of GROUP BY and HAVING clauses is applied for this analysis.
Runtime: Approximately 0.81 seconds.

* Caching and Uncaching of Data:

Caching the home_sales table was a strategic move to speed up subsequent queries. It's especially effective when queries are repeatedly executed. The check for cached status and uncaching at the end of the script shows a good understanding of Spark's caching mechanism.

* Handling Parquet Data:

The code efficiently writes data in Parquet format, partitioned by the date_built field. Reading and creating a temporary view for the Parquet data demonstrates proficiency in handling different data formats.


---
<b>What didn't work:</b><br>

There are no major issues with the provided code. However, it's important to consider the following recommendations for future improvement:

* Optimizing Performance:

The code already shows good performance, but for larger datasets or more complex queries, it might be beneficial to explore further optimization techniques like using indexes, optimizing joins, or considering data distribution strategies.

* Error Handling:

While the code seems robust, it's always a good practice to include error handling mechanisms, especially when dealing with data operations.

* Comments and Documentation:

Adding comments to the code can help in understanding the logic, especially for complex operations. Additionally, providing documentation on the purpose of each query and any assumptions made about the data would be beneficial for future reference.

* Scalability Considerations:

If the dataset is expected to grow significantly, it might be worth considering distributed computing frameworks like Apache Spark to handle larger volumes of data.

* Testing on Diverse Datasets:

Testing the code on different datasets, including edge cases, can help ensure its robustness and effectiveness across various scenarios.


---
Overall, the provided code exhibits good practices in data manipulation and querying using SparkSQL. With the recommended enhancements, it can be even more versatile and reliable for handling diverse real-world datasets.
