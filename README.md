Women's Safety Analysis in India (2001-2014)
Project Overview
This repository contains a comprehensive data analysis project focused on evaluating the safety of women across Indian states and union territories, based on crime data from 2001 to 2014. The dataset, sourced from Kaggle, includes 10,677 records detailing various crimes against women, such as rape, kidnapping, dowry deaths, and domestic cruelty. The analysis employs data preprocessing, visualization, and K-means clustering to classify states as "safe" or "unsafe" for women, providing insights into regional safety patterns.
Dataset Description

Source: Kaggle dataset on crimes against women in India (2001-2014).
Size: 10,677 rows and 11 columns (reduced to 10 after preprocessing).
Columns:
STATE/UT: State or Union Territory.
DISTRICT: District within the state.
Year: Year of crime data (2001–2014).
Rape: Number of rape cases.
Kidnapping and Abduction: Number of kidnapping cases.
Dowry Deaths: Number of dowry-related deaths.
Assault on Women with Intent to Outrage Her Modesty: Assault cases.
Insult to Modesty of Women: Cases of insult.
Cruelty by Husband or His Relatives: Domestic violence cases.
Importation of Girls: Cases of girl trafficking.


Preprocessing:
Removed irrelevant column (Unnamed: 0).
Standardized state names (e.g., converted to uppercase, unified variations like "A&N Islands" and "A & N Islands").
Aggregated data by state to compute total crimes.
Added a Total column summing all crime categories per state.



Analysis and Findings
Data Summary

Total Crimes: Over 5.32 million crimes against women were recorded across India from 2001 to 2014.
Most Prevalent Crime: "Cruelty by Husband or His Relatives" accounted for the highest number of cases (2.23 million), followed by "Assault on Women" (1.21 million) and "Kidnapping and Abduction" (746,198).
Least Prevalent Crime: "Importation of Girls" had the fewest cases (1,872).

Key Insights

States with Highest Crime Rates:
Uttar Pradesh: 582,398 total cases, with high instances of kidnapping (135,906) and dowry deaths (57,256).
Andhra Pradesh: 575,354 cases, notably high in domestic cruelty (280,906).
West Bengal: 537,976 cases, with significant domestic cruelty (344,124).


States with Lowest Crime Rates:
Lakshadweep: 54 cases, the safest region.
D&N Haveli: 80 cases.
A&N Islands: 204 cases.


Crime Distribution:
Domestic cruelty is the dominant crime in most states, reflecting systemic issues in domestic violence.
Dowry deaths are notably high in states like Uttar Pradesh and Bihar, indicating cultural challenges.
Importation of girls is minimal but concentrated in states like Bihar (904 cases).



Clustering Analysis

Objective: Classify states as "safe" or "unsafe" using K-means clustering.
Methodology:
Used crime data normalized via MinMaxScaler.
Applied K-means with 2 clusters (safe vs. unsafe), based on the mean total crime value (136,451).
States with total crimes above the mean were labeled "unsafe" (cluster 1); below were "safe" (cluster 0).


Accuracy: The clustering model correctly labeled all 39 states/UTs compared to a predefined threshold.
Results:
Unsafe States (14): Andhra Pradesh, Assam, Bihar, Gujarat, Haryana, Karnataka, Kerala, Madhya Pradesh, Maharashtra, Odisha, Rajasthan, Tamil Nadu, Uttar Pradesh, West Bengal.
Safe States (25): A & N Islands, Arunachal Pradesh, Chandigarh, Chhattisgarh, D & N Haveli, Daman & Diu, Delhi, Delhi UT, Goa, Himachal Pradesh, Jammu & Kashmir, Jharkhand, Lakshadweep, Manipur, Meghalaya, Mizoram, Nagaland, Puducherry, Punjab, Sikkim, Telangana, Tripura, Uttarakhand.


Reasoning:
Unsafe states typically have larger populations and higher incidences of domestic cruelty and kidnapping, correlating with urban density and socio-economic factors.
Safe states include smaller regions (e.g., Lakshadweep, Sikkim) or areas with lower reported crime rates, possibly due to better law enforcement or cultural factors.



Visualizations

Bar Plots:
Total crimes by state, highlighting Uttar Pradesh, Andhra Pradesh, and West Bengal as high-risk areas.
Domestic cruelty cases, showing West Bengal and Andhra Pradesh as outliers.


Pie Chart:
Distribution of "Importation of Girls" cases, with Bihar and West Bengal as key contributors.


Tools Used: Plotly Express for interactive visualizations, saved as total_crimes.png, cruelty_cases.png, and importation_pie.png.

Repository Structure

data/crimes_against_women_2001-2014.csv: Raw dataset.
notebooks/women_safety_analysis.ipynb: Jupyter notebook with the full analysis code.
visualizations/:
total_crimes.png: Bar plot of total crimes by state.
cruelty_cases.png: Bar plot of domestic cruelty cases.
importation_pie.png: Pie chart of girl importation cases.


README.md: This file, providing an overview and analysis summary.

How to Use

Clone the Repository:git clone https://github.com/your-username/womens-safety-india.git


Install Dependencies:pip install pandas numpy seaborn matplotlib plotly scikit-learn


Run the Notebook:
Open notebooks/women_safety_analysis.ipynb in Jupyter Notebook.
Ensure the dataset is in the data/ folder.
Execute cells to reproduce the analysis and visualizations.


Explore Visualizations:
View generated plots in the visualizations/ folder or regenerate them via the notebook.



Conclusion
This analysis highlights significant regional disparities in women's safety in India from 2001 to 2014. States like Uttar Pradesh and Andhra Pradesh emerge as high-risk areas, primarily due to domestic violence and kidnapping. Conversely, smaller regions like Lakshadweep and Sikkim are notably safer. The clustering model provides a clear classification of safe and unsafe states, which can inform policy-making and targeted interventions. Future work could incorporate population normalization and more recent data to refine these insights.
Acknowledgments

Dataset provided by Kaggle.
Built with Python, Pandas, Plotly, and Scikit-learn.

Suggested Repository Title
"Womens-Safety-India-2001-2014"
This title is concise, descriptive, and clearly indicates the focus on women's safety analysis in India over the specified period, making it easily understandable for anyone visiting the repository.
