# Bank-customer-churn-prediction

I worked on this project for an end-to-end analytics in a banking context, combining machine learning with AI tools to generate insights that  a retention team could use. 

## Project overview
This project predicts which bank customers are likely to churn (leave the bank). Here i am making use of machine learning, and translates model outputs into executive-ready business intelligence. It is designed to mirror a real-world analytics workflow inside a retail bank; from raw data ingestion through to a boardroom-ready through Python visualization libraries like Matplotlib, Seaborn, Plotly, Streamlit with AI-generated narrative commentary. Future improvements include migrating the visualizations to Power BI or Tableau to provide a more interactive business-facing dashboard experience.

This project demonstrates how modern data analytics professionals can combine traditional BI skills with AI prompt engineering to dramatically accelerate the insight cycle and enable a quicker and better decision making.

## What Business problem i'm i solving here?

Acquiring a new bank customer costs 5–7x more than retaining an existing one. A retail bank with 10,000+ customers and a 20% annual churn rate needs a proactive, data driven system to identify at risk customers before they leave; not after the have left. This project builds that system.

**Key business questions answered:**
- Which customers are most likely to churn in the next period?
- What are the strongest behavioural and demographic drivers of churn?
- Which customer segments represent the highest revenue risk?
- What retention actions should the bank prioritise?

## The Dataset used

| Property | Detail |
|---|---|
| Source | Kaggle — Bank Customer Churn Prediction |
| Records | 10,000 customers |
| Features | 14 columns (demographics, account behaviour, product usage) |
| Target variable | `Exited` (1 = churned, 0 = retained) |
| Class imbalance | ~20% churn rate |

## Tech stack

| Layer | Tools used |
|---|---|
| Data processing | Python, pandas, NumPy |
| Visualisation (EDA) | matplotlib, seaborn, Google Colab, Plotly, Streamlit |
| Machine learning | scikit-learn, XGBoost |
| Explainability | SHAP (SHapley Additive exPlanations) |
| Feature engineering | Custom ratio features (BalanceToSalary, ProductsPerTenure) |
| BI Dashboard | Interactive Dashboard — Python (Matplotlib), Microsoft Power BI (3-page executive dashboard), |
| AI tools | Claude, ChatGPT — prompt engineering for insight interpretation |
| Export | openpyxl (Excel export for Power BI ingestion) |

## Methodology

### 1. Exploratory data analysis
I Analysed churn patterns across age, geography, product count, balance, and activity status. After this analysis, the Key findings were: Germany shows 32.4% churn vs a 16.4% average, and customers holding 3+ products churn at an alarming 82.7%. Can be seen on the different generatedted charts below.

<img width="1790" height="1116" alt="Exploratory Data Analysis" src="https://github.com/user-attachments/assets/b0ed4067-f811-4c5c-8679-dac9e105f458" />


### 2. Feature engineering
I Created domain-informed features including balance-to-salary ratio, products-per-tenure, and age group buckets to improve model signal.

### 3. Model comparison
I Trained and compared three models — Logistic Regression, Random Forest, and XGBoost — evaluating on AUC, F1, Precision, and Recall.
See screenshots below

<img width="592" height="297" alt="MODEL LR" src="https://github.com/user-attachments/assets/15a63a06-df0c-4889-a574-aa091fb7fc2f" />
<img width="596" height="313" alt="MODEL RF" src="https://github.com/user-attachments/assets/af4085e1-ec7f-4141-9222-fc52d3127b98" />
<img width="601" height="307" alt="MODEL XGBOOST" src="https://github.com/user-attachments/assets/5e78ec42-18be-4084-8454-f4c156fdfe7f" />
<img width="705" height="183" alt="FINAL RESULTS" src="https://github.com/user-attachments/assets/f1b58378-1c22-49f3-9e38-d2487982653f" />


### 4. Explainability with SHAP
Used and Applied SHAP (SHapley Additive exPlanations) to interpret model predictions and identify the factors driving customer churn. Generated both global feature importance insights and customer-level explanations, enabling business stakeholders to understand and trust the model's recommendations.

**Top 5 churn drivers:**
1. Age (40–60 segment highest risk)
2. Number of products held
3. Active member status
4. Account balance
5. Geography (Germany segment)

### 5. AI-augmented insight generation
After analyzing the customer data, I used AI tools such as ChatGPT and Claude to help transform technical analysis into business-friendly insights. After completing the data analysis and building the churn prediction model, I used structured prompts to summarize key findings, explain the factors driving customer churn in simple banking terms, generate customer retention recommendations, and create commentary for Power BI dashboards. This helped present the results in a way that business stakeholders could easily understand and act upon.
### Generate executive insight summaries from EDA findings

After exploring the data, I used AI to summarize the most important patterns and trends for managers who don't have time to review charts and technical details.

### Interpret SHAP feature importance in plain banking language

I used AI to explain the model's results in simple terms, showing which customer characteristics were increasing the likelihood of churn and why that matters to the bank.

### Write retention strategy recommendations for the Head of Retail Banking

Based on the analysis, I used AI to help create practical suggestions that the bank could use to reduce customer churn and improve customer retention.

### 3 professional dashboard images directly in Google Colab using Python dashboard commentary text

I used AI to generate short explanations and insights that accompany charts and KPIs in the dashboard, making the reports easier for decision-makers to understand.

## Interactive Dashboard — Python (Matplotlib)

The analysis is presented across 3 professional dashboard pages
generated entirely in Python — no BI tool required. Each page
was designed to mirror an executive reporting workflow inside
a retail bank.

**Page 1 — Executive Overview**
KPI cards (total customers, churn rate, high-risk count, avg
churn probability), churn breakdown by geography, product count,
and active vs inactive member status.

![Executive Overview](images/dashboard_page1_executive_overview.png)

**Page 2 — Customer Risk Segmentation**
Scatter plot of all 10,000 customers mapped by Age vs Balance
and coloured by risk tier (High / Medium / Low), alongside a
ranked table of the 15 highest-risk customers with their
churn probabilities.

![Risk Segmentation](images/dashboard_page2_risk_segmentation.png)

**Page 3 — AI Model Insights**
XGBoost feature importance chart showing the top 10 churn
drivers, a model performance comparison table across all 3
models, and an AI-generated executive summary with retention
strategy recommendations.

![AI Model Insights](images/dashboard_page3_ai_model_insights.png)










