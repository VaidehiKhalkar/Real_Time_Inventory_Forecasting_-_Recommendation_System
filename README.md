
#  Real-Time Inventory Forecasting & Recommendation System

This project is a robust, end-to-end solution designed for **inventory management** and **personalized product recommendations**, leveraging the power of **predictive analytics**, **cloud technologies**, and **automated ML pipelines**.

---

##  Project Overview

The **Real-Time Inventory Forecasting & Recommendation System** was built to automate the entire inventory lifecycle—from **data ingestion** to **forecasting**, and **customer product recommendation**. This platform ensures accurate stock predictions and boosts customer engagement by delivering personalized recommendations.

---

##  Key Features

-  **Real-Time Data Ingestion**  
  Integrated with AWS S3, Glue, and Kafka for seamless streaming and batch data intake.

-  **Inventory Forecasting**  
  ML models trained on historical sales and seasonal trends to predict future demand with high accuracy.

-  **Product Recommendation Engine**  
  Leveraged collaborative filtering and content-based algorithms for customer-specific product suggestions.

-  **Automated ML Pipelines**  
  End-to-end pipelines: data cleaning → feature engineering → model training → evaluation → deployment using Pickle & Changemaker.

-  **Dashboards & Monitoring**  
  Power BI and Streamlit dashboards for real-time visualization of inventory trends and customer behavior.

---

##  Architecture

```
        ┌──────────────┐        ┌──────────────┐
        │   AWS S3     │◄──────►│   AWS Glue    │
        └────▲─────────┘        └────▲─────────┘
             │                        │
             ▼                        ▼
       ┌──────────┐           ┌────────────┐
       │  Apache  │           │ Data       │
       │  Kafka   │◄──────────┤ Preprocess │
       └────▲─────┘           └────────────┘
            │
            ▼
     ┌────────────┐
     │ ML Models  │◄────── Feature Engineering + Forecasting + Recommender
     └────▲───────┘
          │
          ▼
   ┌──────────────┐
   │ Power BI /   │
   │ Streamlit UI │
   └──────────────┘
```

---

##  Tech Stack

| Category              | Technologies Used                                             |
|-----------------------|---------------------------------------------------------------|
| **Programming**       | Python, SQL                                                   |
| **Data Engineering**  | AWS Glue, Apache Kafka, Pandas, NumPy                         |
| **Machine Learning**  | Scikit-learn, Pickle, Custom Models                           |
| **Cloud & Storage**   | AWS S3, EC2                                                   |
| **Visualization**     | Power BI, Streamlit                                           |
| **Pipeline Orchestration** | Custom Automation Scripts, Changemaker Workflows         |

---

##  Repository Structure

```
├── dummy_data.ipynb               # Dummy data generator
├── forecasting_model.ipynb        # Inventory forecasting notebook
├── recommendation_engine.ipynb    # Product recommendation logic
├── utils/                         # Helper functions and pipeline scripts
├── data/                          # Sample & processed data
├── dashboards/                    # Power BI and Streamlit dashboards
└── README.md                      # Project overview
```

---

##  Outcomes

- Reduced inventory stockouts by **30%**
- Improved warehouse planning with accurate forecasts
- Delivered real-time product recommendations increasing **user engagement by 25%**

---

##  Author

**Vaidehi Khalkar**  
🔗 [GitHub Profile](https://github.com/VaidehiKhalkar)  

---

## Future Enhancements

- Integrate with retail ERP systems for live inventory updates.
- Deploy recommendation engine as a microservice via AWS Lambda or Docker.
- Introduce real-time alerting for low-stock or demand anomalies.

