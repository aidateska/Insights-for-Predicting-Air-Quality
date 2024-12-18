# **Air Quality Analysis Project**

## **Project Overview**  
This project analyzes air quality across various regions using a dataset with 5,000 samples. The dataset contains environmental and demographic variables that influence pollution levels. The analysis involves:  
1. **Uploading the data into a SQL database** for structured querying.  
2. **Performing advanced analyses with Python**, including predictive modeling and exploratory data analysis (EDA).  
3. **Visualizing key insights in Power BI** to create dynamic and interactive dashboards.  

---

## **Dataset Features**  
The dataset includes the following variables:  

| **Feature**                         | **Description**                                                                                  |  
|-------------------------------------|--------------------------------------------------------------------------------------------------|  
| **Temperature (°C)**                | Average temperature of the region.                                                              |  
| **Humidity (%)**                    | Relative humidity recorded in the region.                                                       |  
| **PM2.5 Concentration (µg/m³)**     | Levels of fine particulate matter (diameter ≤ 2.5µm).                                           |  
| **PM10 Concentration (µg/m³)**      | Levels of coarse particulate matter (diameter ≤ 10µm).                                          |  
| **NO2 Concentration (ppb)**         | Nitrogen dioxide levels.                                                                        |  
| **SO2 Concentration (ppb)**         | Sulfur dioxide levels.                                                                          |  
| **CO Concentration (ppm)**          | Carbon monoxide levels.                                                                         |  
| **Proximity to Industrial Areas (km)** | Distance to the nearest industrial zone.                                                       |  
| **Population Density (people/km²)** | Number of people per square kilometer in the region.                                            |  
| **Air Quality Levels (Target)**     | Categorical classification of air quality: `Good`, `Moderate`, `Poor`, `Hazardous`.            |  

---

## **Goals and Objectives**  
### **Key Objectives**:  
1. **Exploratory Data Analysis (EDA)**:  
   - Understand the distribution of pollutants like PM2.5, PM10, and NO2.  
   - Analyze the relationship between population density and air quality.  
2. **Data Modeling**:  
   - Use Python and machine learning techniques to predict air quality levels.  
   - Identify key factors influencing air pollution using feature importance analysis.  
3. **SQL Integration**:  
   - Store and query data efficiently using SQL.  
   - Perform advanced queries like filtering regions with hazardous air quality.  
4. **Power BI Visualization**:  
   - Create interactive dashboards to present trends, comparisons, and key metrics.  

---

## **Executed Analyses**  
 

### **1. Descriptive Analysis**  
- Calculate average levels of PM2.5, PM10, NO2, SO2, and CO across all regions.  
- Identify the regions with the highest and lowest pollution levels.  
- Evaluate seasonal trends (if time data is available).  

### **2. Correlation Analysis**  
- Analyze correlations between temperature, humidity, and pollutant levels.  
- Visualize relationships between proximity to industrial areas and pollutant levels using scatterplots.  

### **3. Population Impact Analysis**  
- Investigate how population density impacts air quality levels.  
- Compare air quality in urban, suburban, and rural areas.  

### **4. Predictive Modeling**  
- Use machine learning algorithms (e.g., Random Forest, Logistic Regression) to classify air quality levels.  
- Evaluate model performance using accuracy, precision, recall, and F1-score.  

### **5. SQL Queries**  
- Identify regions with hazardous air quality and high population density using SQL queries.  
- Aggregate data by air quality category to understand overall trends.  

### **6. Power BI Dashboards**  
- **Dynamic Maps**: Show pollution levels across regions using heatmaps.  
- **Time Series Analysis**: Visualize trends in pollutant levels over time.  
- **Interactive Filters**: Allow users to filter by air quality category, pollutant, or region.  

---

## **Technologies Used**  
- **SQL**: For storing and querying large datasets.  
- **Python**: For data analysis, visualization, and modeling.  
  - Libraries: `Pandas`, `Matplotlib`, `Seaborn`, `Scikit-learn`.  
- **Power BI**: For creating professional and interactive dashboards.  

---

## **Installation and Setup**  

### **1. Upload Dataset to SQL Database**  
1. Set up your SQL database.  
2. Use the provided script to create tables and upload data:  
   ```sql  
   CREATE TABLE air_quality (  
       id INT PRIMARY KEY,  
       temperature FLOAT,  
       humidity FLOAT,  
       pm25 FLOAT,  
       pm10 FLOAT,  
       no2 FLOAT,  
       so2 FLOAT,  
       co FLOAT,  
       industrial_proximity FLOAT,  
       population_density INT,  
       air_quality_level VARCHAR(20)  
   );  
   ```  
3. Insert data into the database using Python:  
   ```python  
   import pandas as pd  
   from sqlalchemy import create_engine  

   # Load dataset  
   df = pd.read_csv('air_quality.csv')  

   # Create SQL connection  
   engine = create_engine('mysql+pymysql://user:password@host/db_name')  

   # Upload data  
   df.to_sql('air_quality', engine, if_exists='replace', index=False)  
   ```  

### **2. Python Environment Setup**  
1. Clone this repository:  
   ```bash  
   git clone https://github.com/your-username/air-quality-analysis.git  
   ```  
2. Install dependencies:  
   ```bash  
   pip install -r requirements.txt  
   ```  

### **3. Power BI Integration**  
1. Connect Power BI to your SQL database.  
2. Import the tables and start building visualizations.  

---

## **Folder Structure**  
```plaintext  
project/  
│  
├── data/                # Dataset files  
├── scripts/             # Python scripts for analysis  
├── sql/                 # SQL queries and schema  
├── visualizations/      # Power BI dashboard files  
├── images/              # Placeholder for images  
├── README.md            # Project documentation  
└── requirements.txt     # Python dependencies  
```  

---

## **Examples of Visualizations**  

### **1. Pollution Trends Over Regions**  
![Placeholder for Regional Trends](images/region_trends.png)  

### **2. Correlation Heatmap**  
![Placeholder for Correlation Heatmap](images/correlation_heatmap.png)  

### **3. Power BI Dashboard**  
![Placeholder for Power BI Dashboard](images/powerbi_dashboard.png)  

---

## **Contributing**  
Contributions are welcome! To contribute:  
1. Fork the repository.  
2. Create a new branch for your feature or fix:  
   ```bash  
   git checkout -b feature-name  
   ```  
3. Commit your changes and push to your branch.  
4. Submit a pull request for review.  

---

## **Contact**  
Author: **Aida T**  
Email: aida.teskeredzic@fhmzbih.gov.ba  
GitHub: [Aida T](https://github.com/aidateska)  

---
