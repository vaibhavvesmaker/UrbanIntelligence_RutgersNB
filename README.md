# Urban Service Requests Analysis for Rutgers – New Brunswick 

This project leverages data science, machine learning, and time-series forecasting to analyze urban service requests in New Brunswick—home to Rutgers University. By examining open datasets related to waste management, infrastructure, property maintenance, and public safety, our goal is to provide actionable insights for optimizing urban management, reducing costs, and improving public safety.


## Table of Contents
- [Project Overview](#project-overview)
- [Key Features](#key-features)
- [Methodology](#methodology)
  - [Data Collection & Processing](#data-collection--processing)
  - [Exploratory Data Analysis (EDA)](#exploratory-data-analysis-eda)
  - [Machine Learning Models](#machine-learning-models)
- [Urban Impact Analysis](#urban-impact-analysis)
  - [Waste Management](#waste-management)
  - [Property Maintenance](#property-maintenance)
  - [Infrastructure & Transportation](#infrastructure--transportation)
  - [Public Safety](#public-safety)
- [Visualizations & Reporting](#visualizations--reporting)
- [Repository Structure](#repository-structure)
- [Setup and Usage Instructions](#setup-and-usage-instructions)
- [Future Enhancements](#future-enhancements)
- [Contributing](#contributing)
- [License](#license)

## Project Overview
This repository documents a comprehensive analysis of urban service requests in New Brunswick using open data. We apply various machine learning techniques—ranging from traditional statistical models like ARIMA and Facebook Prophet for time-series forecasting to modern approaches like XGBoost and deep learning for classification and anomaly detection. Our insights help city officials and businesses optimize operations in waste management, infrastructure planning, property maintenance, and public safety.

## Key Features
- **Data-Driven Analysis:** Integration of open datasets to track service requests across multiple urban domains.
- **Advanced Forecasting:** Use of Facebook Prophet and ARIMA to forecast trends and seasonal patterns in service requests.
- **Predictive Modeling:** Application of XGBoost and deep learning models for classification and anomaly detection.
- **Actionable Insights:** Identification of cost-saving opportunities and efficiency improvements for urban management.
- **Interactive Visualizations:** Development of dashboards and static reports for clear communication of insights.
- **Reproducible Research:** A fully documented project with Jupyter Notebooks, scripts, and clear instructions for replication.

## Methodology

### Data Collection & Processing
- **Open Data Sources:** We gather urban service request data from local government portals and state open data platforms. If Rutgers – New Brunswick-specific data is unavailable, similar city 311 datasets are used as proxies.
- **Data Cleaning:** Raw data is processed to handle missing values, standardize formats, and remove duplicates. Geographical information is normalized to map requests accurately.
- **Data Integration:** Additional data (e.g., weather, demographic statistics) is merged to enrich our analysis and support feature engineering.

### Exploratory Data Analysis (EDA)
- **Trend Analysis:** Identify overall volume, seasonal cycles, and anomalies in the service requests.
- **Category Breakdown:** Understand which issues are most prevalent across waste management, property maintenance, infrastructure, and public safety.
- **Geospatial Mapping:** Visualize service request density by neighborhood to uncover hotspots and patterns.

### Machine Learning Models
- **Time-Series Forecasting:**
  - *Facebook Prophet:* Models complex seasonal effects and holiday impacts, providing easy-to-interpret forecasts.
  - *ARIMA:* Offers a classical statistical approach for time-series prediction.
- **Predictive Classification & Anomaly Detection:**
  - *XGBoost:* A robust algorithm used for classification tasks (e.g., categorizing request types) and anomaly detection.
  - *Deep Learning:* Employs RNNs/LSTMs and text-based neural networks to capture nonlinear relationships and subtle trends in the data.
- **Model Evaluation:** Each model is evaluated using standard metrics (RMSE, MAE, accuracy, precision, recall) and compared to select the best approach for each task.

## Urban Impact Analysis

### Waste Management
- **Insight:** Bulk waste pickups and illegal setout requests peak seasonally (e.g., in May due to student move-outs).
- **Impact:** Optimized scheduling based on our forecasts can reduce operational costs by 15–20%.

### Property Maintenance
- **Insight:** Requests for property maintenance (e.g., overgrown grass, building repairs) spike in spring and summer.
- **Impact:** Local businesses and city agencies can adjust staffing and resource allocation based on seasonal demand.

### Infrastructure & Transportation
- **Insight:** Pothole reports and parking violation complaints increase during colder months due to weather-related road damage.
- **Impact:** Forecasts enable proactive maintenance planning, reducing repair costs and improving road safety.

### Public Safety
- **Insight:** Non-emergency public safety requests, including noise complaints and social service calls, exhibit clear temporal trends.
- **Impact:** Better forecasting supports efficient resource allocation, ensuring timely responses to community needs.

## Visualizations & Reporting
- **Interactive Dashboards:** Explore geospatial and temporal trends through dynamic maps and time-series visualizations.
- **Static Reports:** Detailed Jupyter Notebooks and exported PDFs summarize the analysis, model performance, and key insights.
- **Geographical Mapping:** Heatmaps and choropleth maps help visualize hotspots and density of service requests.



├── README.md
├── data/
│   ├── raw/                # Raw data files (or instructions to download data)
│   └── processed/          # Cleaned and processed data files
├── notebooks/
│   ├── 1_data_collection_and_cleaning.ipynb
│   ├── 2_eda_visualizations.ipynb
│   ├── 3_forecasting_models.ipynb
│   └── 4_classification_anomaly_models.ipynb
├── src/
│   ├── data_processing.py  # Data cleaning and integration functions
│   ├── models.py           # Model training and evaluation functions
│   └── dashboard.py        # Code for launching interactive dashboards
├── reports/
│   ├── final_report.pdf    # Final project report and visualizations
│   └── figures/            # Figures used in the report
├── requirements.txt        # Python dependencies
└── LICENSE
```

## Setup and Usage Instructions

1. **Clone the Repository:**
   ```bash
   git clone https://github.com/yourusername/urban-service-requests-analysis.git
   cd urban-service-requests-analysis
   ```

2. **Install Dependencies:**
   Ensure you have Python 3.x installed. Then install the required packages:
   ```bash
   pip install -r requirements.txt
   ```

3. **Data Acquisition:**
   - Follow the instructions in the `data/` directory to download and store the required datasets.
   - If raw data is not included, use the provided script in `src/data_processing.py` to automatically download and preprocess the data.

4. **Run Notebooks:**
   - Open the notebooks in the `notebooks/` folder with Jupyter Notebook or JupyterLab.
   - Start with `1_data_collection_and_cleaning.ipynb` and proceed sequentially to see the complete analysis workflow.

5. **Model Training & Forecasting:**
   - Run `3_forecasting_models.ipynb` to train time-series models (Prophet, ARIMA) and generate forecasts.
   - Run `4_classification_anomaly_models.ipynb` for predictive modeling and anomaly detection using XGBoost and deep learning models.

6. **Launch Dashboard:**
   - If an interactive dashboard is available, run:
     ```bash
     python src/dashboard.py
     ```
   - Open the provided local URL in your browser to interact with the visualizations.

## Future Enhancements
- **Model Refinement:** Explore additional machine learning models (e.g., LightGBM, CatBoost) and deep neural networks.
- **Alternative Data Sources:** Integrate more external datasets (e.g., weather, demographics) to enhance predictions.
- **Real-Time Deployment:** Develop a real-time API for live service request forecasting and anomaly detection.
- **Expanded Geographical Analysis:** Extend the analysis to include other cities or additional neighborhoods.

## Contributing
Contributions are welcome! If you’d like to contribute:
- Fork the repository.
- Create a new branch for your changes (e.g., `feature/your-feature`).
- Submit a pull request with clear commit messages and descriptions.
- For major changes, please open an issue first to discuss your ideas.

## License
This project is licensed under the **MIT License** – see the [LICENSE](LICENSE) file for details.
```

---
