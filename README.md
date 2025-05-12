# Women's Safety Analysis in India (2001–2014)
Welcome to the Women's Safety Analysis in India repository! This project dives into crime data from 2001 to 2014 to assess the safety of women across Indian states and union territories. Using data analysis, visualization, and clustering, we identify which regions are safer for women and highlight areas needing attention. This README is designed to be clear, engaging, and easy to navigate, so let's explore!

# 🌟 Project Overview
This repository analyzes crimes against women in India, sourced from a Kaggle dataset. With over 10,000 records, the project uncovers patterns in crimes like rape, kidnapping, and domestic violence, classifying states as "safe" or "unsafe" using K-means clustering. Whether you're a data enthusiast, researcher, or policymaker, this project offers valuable insights into women's safety trends.

# 📊 Dataset Description

Source: Kaggle dataset on crimes against women (2001–2014).
Size: 10,677 records, originally 11 columns (reduced to 10 after preprocessing).
Key Columns:
STATE/UT: State or Union Territory.
DISTRICT: District within the state.
Year: Year of data (2001–2014).
Rape: Number of rape cases.
Kidnapping and Abduction: Kidnapping cases.
Dowry Deaths: Dowry-related deaths.
Assault on Women: Assault cases with intent to outrage modesty.
Insult to Modesty: Cases of insult.
Cruelty by Husband: Domestic violence cases.
Importation of Girls: Trafficking cases.


# Preprocessing Steps:
Dropped irrelevant column (Unnamed: 0).
Standardized state names (e.g., uppercase, unified "A&N Islands").
Aggregated data by state for total crime counts.
Added a Total column summing all crimes per state.




# 🔍 Analysis and Findings
Data Summary

Total Crimes: 5.32 million crimes against women recorded from 2001–2014.
Dominant Crime: "Cruelty by Husband or His Relatives" (2.23 million cases).
Other Major Crimes:
Assault on Women: 1.21 million cases.
Kidnapping and Abduction: 746,198 cases.


Least Common Crime: Importation of Girls (1,872 cases).

# Key Insights

Highest Crime States:
Uttar Pradesh: 582,398 cases (high in kidnapping: 135,906).
Andhra Pradesh: 575,354 cases (domestic cruelty: 280,906).
West Bengal: 537,976 cases (domestic cruelty: 344,124).


# Safest Regions:
Lakshadweep: 54 cases.
D&N Haveli: 80 cases.
A&N Islands: 204 cases.


# Crime Patterns:
Domestic cruelty dominates, reflecting widespread domestic violence issues.
Dowry deaths are prominent in Uttar Pradesh and Bihar.
Importation of girls is rare but notable in Bihar (904 cases).



# Clustering Analysis

Goal: Classify states as "safe" or "unsafe" using K-means clustering.
Approach:
Normalized crime data using MinMaxScaler.
Used K-means with 2 clusters (safe vs. unsafe), based on mean total crimes (136,451).
States above the mean were "unsafe"; below were "safe".


# Accuracy: 100% correct labeling for all 39 states/UTs.
Results:
Unsafe States (14):
Andhra Pradesh, Assam, Bihar, Gujarat, Haryana, Karnataka, Kerala, Madhya Pradesh, Maharashtra, Odisha, Rajasthan, Tamil Nadu, Uttar Pradesh, West Bengal.


# Safe States (25):
A & N Islands, Arunachal Pradesh, Chandigarh, Chhattisgarh, D & N Haveli, Daman & Diu, Delhi, Delhi UT, Goa, Himachal Pradesh, Jammu & Kashmir, Jharkhand, Lakshadweep, Manipur, Meghalaya, Mizoram, Nagaland, Puducherry, Punjab, Sikkim, Telangana, Tripura, Uttarakhand.




# Why These Results?
Unsafe states often have larger populations and higher domestic violence rates.
Safe states include smaller regions or those with stronger law enforcement.




# 🗂 Repository Structure

data/:
crimes_against_women_2001-2014.csv: Raw dataset.


# notebooks/:
women_safety_analysis.ipynb: Jupyter notebook with full analysis code.


# README.md: You're reading it! A user-friendly guide to the project.


# 🚀 How to Use

Clone the Repository:git clone https://github.com/your-username/womens-safety-india.git


Install Dependencies:pip install pandas numpy seaborn matplotlib plotly scikit-learn


# Run the Analysis:
Open notebooks/women_safety_analysis.ipynb in Jupyter Notebook.
Place the dataset in the data/ folder.
Run the notebook to explore the analysis and results.




# 🎯 Conclusion
This project reveals stark regional differences in women's safety in India from 2001 to 2014. Uttar Pradesh, Andhra Pradesh, and West Bengal stand out as high-risk areas, driven by domestic violence and kidnapping. Smaller regions like Lakshadweep and Sikkim are notably safer. The K-means clustering effectively categorizes states, offering a foundation for policy recommendations. Future analyses could normalize data by population or include newer datasets for updated insights.

# 🙌 Acknowledgments

Dataset: Kaggle Crimes Against Women Dataset.
Tools: Python, Pandas, Plotly, Scikit-learn.


