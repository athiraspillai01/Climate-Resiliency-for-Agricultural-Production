# **Climate Resiliency Assessment for Agricultural Production in Maharashtra \& Madhya Pradesh**



## **1.Project Overview**


This case study assesses the climate resiliency of agricultural production in two different states, Maharashtra (MH) and Madhya Pradesh (MP). These are the two agriculturally critical Indian states. The research includes historical climate information, crop performance, economic effects, policy analysis, and technology utilization to gain insights and develop resilient climate indicators.

## 

## **2.Contents**

* `main\_program\_python\_file.py`: Python source file.
* `program\_notebook.ipynb`: Main implementation notebook (Jupiter file).
* `/data/`: Folder containing climate and crop data (temperature, precipitation, NDVI, yield).
* `README.md`: Project documentation.
* `outputs/`: Folder for graphs.

## 

## **3.Project Architecture Overview**



Climate\_Resilience\_Assessment/

data/
MH\_temperature.csv,
MH\_precipitation.csv,
MP\_temperature.csv,
MP\_precipitation.csv

notebooks/
program\_notebook.ipynb

outputs/
trend\_graphs/
anomaly\_flags/


## 

## **4.Key Modules in Notebook**



1. Data Loading \& Preprocessing
2. Trend Detection using Rolling Average
3. Anomaly Detection (Z-score based)
4. Crop Performance \& NDVI Trend Analysis
5. Economic Impact Assessment
6. Policy \& Infrastructure Review
7. Resiliency Indicator Framework Proposal
8. Recommendations



## **5.Climate Anomaly Detection Logic**

-Technique Used: Z-score Method
-Thresholds: Values with |z| > 2 are flagged as anomalies
-Features Analyzed: Monthly Avg. Temperature, Precipitation
-Purpose: Identify abnormal patterns like heatwaves, droughts, and floods.



```python
z_scores = np.abs(stats.zscore(df\\\\\\\\\\\\\\\['temperature']))
df['anomaly'] = np.where(z\\\\\\\\\\\\\\\_scores > 2, 1, 0)
```

## **Climate Resilience Indicators**

| Indicator                         | Description                                              | Frequency |
|----------------------------------|----------------------------------------------------------|-----------|
| NDVI Variability Index           | Measures vegetation health fluctuations                  | Monthly   |
| Yield Deviation Index            | Compares actual vs expected yield                        | Seasonal  |
| Rainfall Reliability Coefficient | Degree of rainfall consistency                           | Monthly   |
| Climate Anomaly Frequency Index | % of months with anomalies over last 3 years             | Quarterly |
| Tech Adoption Index              | Use of irrigation, weather apps, resilient seed varieties| Yearly    |



6. ## **Sample Data Quality Report**



| Feature        | Nulls (%) | Outliers Detected | Notes                         |
|----------------|-----------|-------------------|-------------------------------|
| Temperature    | 0.0%      | 2.3%              | Some high-temp spikes in MH   |
| Precipitation  | 1.2%      | 4.5%              | Gaps during monsoon months    |
| NDVI           | 0.0%      | 1.0%              | Acceptable variation          |
| Crop_Yield     | 3.1%      | 2.7%              | Imputed via linear regression |







7. ## **Instructions to Run**

   1. Clone the repository or upload files to your Colab environment.
   2. Install dependencies if using locally:

 	`bash pip install pandas numpy matplotlib seaborn scipy `

   3.Open the notebook `Untitled32 (1).ipynb` and execute cells in order.

   4.View results in `outputs/` folder or within Colab cells.



## 8\. Recommendations Summary

* **Adopt resilient crop varieties**: SB and WH showed better yield stability.
* **Promote drip irrigation \& moisture sensors** to counter rainfall unpredictability.
* **Implement climate-index insurance schemes** to reduce economic shocks.
* **Expand training on digital tools** for early warning systems.
* **Refine government subsidies** to target vulnerable regions based on resiliency indicators.

## References

* IMD (India Meteorological Department)
* GEE (Google Earth Engine) for NDVI
* MoAFW \& ICAR reports
* State-specific agriculture departments
