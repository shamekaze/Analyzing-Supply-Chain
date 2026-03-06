E-Commerce Brand Strategy & Stockout Analysis

Brand Strategy & Stockout Analysis
1. Project Overview
This project identifies high-value inventory gaps by analyzing product descriptions and size availability to calculate potential lost revenue across major fashion brands. By quantifying stockouts, the analysis helps businesses prioritize which brands require immediate restocking to recover "Phantom Revenue".

2. Project Structure
brand_analysis.ipynb: The main Jupyter Notebook containing the data cleaning, brand extraction, and strategic visualization logic.
data/: Directory containing the raw product CSV files.
images/: Static exports of the Brand Strategy Analysis plots for quick reference.

3. Key FeaturesUnstructured Data Parsing: Scans product descriptions to isolate brand names using keyword anchors.Stockout Quantification: Converts text strings (e.g., "UK 8 - Out of stock") into numerical stockout rates.Revenue Impact Estimation: Calculates potential lost revenue based on price and the number of unavailable sizes.Strategic Visualization: Identifies high-priority brands using a Price vs. Stockout Rate scatterplot.

4. Logic & Methodology1. Brand ExtractionThe script uses a custom function to find the keyword "by" in descriptions and extract the immediate brand name. It then cleans this data using a mapping dictionary to fix multi-word names like "River Island" or "New Look".2. Phantom Revenue CalculationThe calculate_phantom_revenue function performs the following steps:Splits size availability strings into lists.Counts every instance of "Out of stock".Calculates the Stockout Rate as a percentage of the total size range.3. Financial ImpactLost revenue is estimated using this formula:$$Lost\_Revenue = Price \times Stockout\_Count$$4. Strategic Analysis MatrixThe final analysis groups brands to find "Winners":Criteria: Brands with an average Price > 40 and a Stockout Rate > 0.4.Visualization: A scatterplot where bubble size represents total Lost Revenue, making it easy to see which brands offer the biggest opportunity for recovery.

5.library and programming language
i. Technologies UsedPython: Core data processing.
ii. Pandas: Data manipulation and cleaning.
iii. Matplotlib & Seaborn: Data visualization and trend analysis.
