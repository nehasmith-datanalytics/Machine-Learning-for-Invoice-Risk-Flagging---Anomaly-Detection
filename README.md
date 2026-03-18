# Machine-Learning-for-Invoice-Risk-Flagging---Anomaly-Detection

## 📌 Description
This project develops a data-driven system to automatically identify vendor invoices that require **manual review**. By analyzing patterns in pricing, freight costs, and delivery timelines, the solution flags potentially risky invoices and streamlines the approval workflow.

The approach replaces inefficient manual processes with an intelligent system that prioritizes high-risk invoices while allowing low-risk invoices to be processed automatically.

---

## 🎯 Objective
- Predict whether an invoice should be flagged for manual approval  
- Detect anomalies in:
  - Freight charges  
  - Invoice amounts  
  - Delivery delays  
- Reduce dependency on manual review processes  
- Enable scalable invoice processing  

---

## 📊 Key Performance Indicators (KPIs)

- **Flagging Accuracy**  
  Measures how accurately the model identifies risky invoices  

- **Reduction in Manual Reviews**  
  Percentage decrease in invoices requiring human intervention  

- **False Positive Rate**  
  Low-risk invoices incorrectly flagged  

- **False Negative Rate**  
  High-risk invoices missed by the system  

- **Processing Time per Invoice**  
  Time saved compared to manual workflows  

- **Anomaly Detection Rate**  
  Number of irregularities detected in cost, freight, or delivery  

---

<img width="443" height="191" alt="image" src="https://github.com/user-attachments/assets/14307dc3-5cb7-42be-9e5d-8f70022802e7" />

## 📊 Correlation Analysis: Quantity, Freight, and Dollars

The heatmap above shows the correlation between **Quantity**, **Freight**, and **Dollars**, revealing very strong positive relationships across all variables:

- **Quantity vs Freight (0.95)**  
  Indicates that as the number of items increases, freight costs also rise significantly.

- **Quantity vs Dollars (0.96)**  
  Suggests that higher quantities are strongly associated with higher total invoice values.

- **Freight vs Dollars (0.99)**  
  Nearly perfect correlation, implying that freight cost scales almost directly with total invoice value.
  
### 🔍 Key Insight
All three variables are **highly collinear**, meaning they move together. This suggests:
- Freight cost is largely driven by order size and value  
- There may be redundancy in features for modeling  
- Feature selection or dimensionality reduction may improve model performance  

---

<img width="647" height="442" alt="image" src="https://github.com/user-attachments/assets/b24b5b59-5f65-422b-8fc5-0e38a028be0c" />
## 📈 Scatter Plot Analysis: Freight vs Quantity & Dollars

The scatter plot visualizes how **Freight Cost** relates to both **Quantity** and **Dollars**:

### 🟠 Quantity vs Freight
- Displays a **positive but more dispersed relationship**  
- Freight increases with quantity, but with noticeable variability  
- Indicates that quantity alone does not fully explain freight cost  

### 🟣 Dollars vs Freight
- Shows a **strong linear relationship**  
- Points are tightly clustered along a line  
- Confirms that freight cost is closely tied to total invoice value  

---
<img width="650" height="442" alt="image" src="https://github.com/user-attachments/assets/a68e3e3f-dfe9-4338-be5b-7cac0f9981e9" />

## 📈 Model Performance: Predicted vs Actual

The scatter plot above compares **Predicted Freight Cost** against **Actual Freight Cost**, providing a visual assessment of model performance.

---

## 🔍 Key Observations

- **Strong Linear Alignment**  
  Most data points lie close to the diagonal trend, indicating that the model predictions closely match actual values.

- **High Accuracy in Mid-Range Values**  
  Predictions are particularly accurate for invoices with moderate freight costs, where points are tightly clustered.

- **Presence of Outliers**  
  A few points deviate significantly from the main trend:
  - Some invoices are **underpredicted** (actual much higher than predicted)  
  - Others are **overpredicted**  

- **Slight Variability at Higher Values**  
  As freight cost increases, prediction variance also increases slightly, which is common in regression models.

---

## 📊 Interpretation

- The model demonstrates **strong predictive capability**, capturing the overall relationship between input features and freight cost.
- Errors are relatively small for most observations, suggesting the model is reliable for general use.
- Outliers may represent:
  - Unusual shipping conditions  
  - Data quality issues  
  - Potential anomalies worth investigating  

---

<img width="1125" height="527" alt="image" src="https://github.com/user-attachments/assets/3176a2d2-4b01-45ed-80a0-23bce93fdb9d" />


## 💼 Business Value

- **Operational Efficiency**  
  Reduces manual workload for finance teams  

- **Risk Mitigation**  
  Detects pricing discrepancies and unusual delivery delays  

- **Cost Savings**  
  Minimizes financial losses due to errors or overpayments  

- **Scalability**  
  Handles increasing invoice volumes without additional resources  

- **Data-Driven Insights**  
  Enables better vendor evaluation and financial decision-making  

---

## ✅ Outcomes

- Automated identification of high-risk invoices  
- Faster and more efficient invoice processing  
- Improved anomaly detection in financial data  
- Reduced manual intervention  
- Better allocation of human effort to complex cases  
- Enhanced financial control and compliance  
