Project Goal: To analyze a dataset of over 66,000 startups to identify factors (funding, sector, country, year) associated with startup failure, defined as having a 'closed' status
Key Findings
Funding Impact: The failure rate is highest for startups with <$100K in total funding (approx. 10%). It is lowest for those with >$100M (close to 0%).
Sectors: Top sectors with the highest failure rates (requiring >=50 total startups) include Coupons, Facebook Applications, and Curated Web.
Countries: The top countries with the highest failure rates (requiring >=50 total startups) are RUS (Russia), BRA (Brazil), and NZL (New Zealand).
Correlation: Total funding (funding_total_usd) shows a very weak negative correlation (-0.07) with failure status. The number of funding rounds (funding_rounds) also shows a very weak negative correlation (-0.05).
Founding Year: The failure rate has fluctuated, showing peaks around 2010 and then decreasing sharply for the most recent years (2014-2015).
Data Processing Highlights
Initial Data: The dataset contained 66,368 entries and 14 columns.
Missing Value Handling: Columns with high non-null counts, like permalink and homepage_url, were dropped. Missing numerical values were filled with 0, and missing categorical values were filled with "Unknown".
Feature Engineering:
A binary feature is_failed was created (1 if status is 'closed', 0 otherwise).funding_total_usd was converted to numeric and categorized into the funding_bin column.The first category in category_list was extracted into primary_category.Date columns were converted to datetime objects, and their corresponding year fields were extracted.
