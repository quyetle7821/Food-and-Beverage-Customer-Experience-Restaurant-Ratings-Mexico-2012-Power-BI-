# Restaurant Ratings & Customer Experience For Mexico’s F&B Market (2012) | Power BI

  <img width="1353" height="885" alt="image" src="https://github.com/user-attachments/assets/3686d741-b123-4b48-b338-2f2f8b5221a1" />



Author: Lê Trường Quyết

Date: 2025 - 09

Tools Used: Power BI

## 📑 Table of Contents  
1. [📌 Background & Overview](#-background--overview)  
2. [📂 Dataset Description & Data Structure](#-dataset-description--data-structure)  
3. [🧠 Design Thinking Process](#-design-thinking-process)  
4. [📊 Key Insights & Visualizations](#-key-insights--visualizations)  
5. [🔎 Final Conclusion & Recommendations](#-final-conclusion--recommendations)

---

## 📌 Background & Overview  

### Objective:
### 📖 What is this project about? 
This project builds a **Power BI dashboard** to analyze **restaurant ratings in Mexico (2012**) using customer feedback data **(Overall / Food / Service ratings)**. The goal is to provide data-driven insights to help stakeholders understand customer satisfaction and make better **market and expansion decisions**, including:

  - **Assess overall satisfaction** and identify key gaps between Food vs Service quality
  - **Compare performance across cities** to prioritize high-potential markets
  - **Evaluate restaurant attributes** (cuisine, price tier, facilities) that correlate with higher ratings
  - **Support investment and expansion planning** for F&B concepts based on volume vs quality

### 👤 Who is this project for?  
✅ **Business analysts / data analysts** looking to turn rating data into actionable insights

✅ **F&B operators / restaurant managers** aiming to improve customer experience and service quality

✅ **Expansion & strategy teams / investors** prioritizing cities and concepts for scalable growth


### ❓ Business Questions:
✅ What is the overall customer satisfaction level for restaurants in Mexico (2012) based on **Overall / Food / Service** ratings?

✅ Which cities show the best combination of **high rating quality and sufficient review volume** for market prioritization?

✅ Which restaurant attributes **(cuisine, price tier, facilities)** are most associated with higher ratings, and where are the biggest gaps (Food vs Service)?

✅ Does matching a consumer’s **personal cuisine preference** with a restaurant’s cuisine lead to higher ratings (Match vs NoMatch)?

## 📂 Dataset Description & Data Structure  

### 📌 Data Source  

- **Source**: Kaggle (Public Dataset – Restaurant Ratings in Mexico, 2012)
- **Format**: CSV
- **Size** :
  + **Tables (sheets)**: 5 tables
  + **Total rows**: ~1,871 rows across all tables
  + **Columns**: varies by table (2 → 14 columns)
 
### 📊 Data Structure & Relationships  

#### 1️⃣ Tables Used: 
The dataset consists of **5 main tables** used to build the Restaurant Ratings dashboard:

  - **Fact_Ratings** – Review-level ratings data (Overall / Food / Service) linked by Consumer_ID × Restaurant_ID.
  - **Dim_Restaurants** – Restaurant master data (city/state, price tier, facilities such as parking/area, etc.).
  - **Dim_Consumers** – Consumer profile data (age group, city/state, budget/behavior attributes).
  - **Bridge_RestaurantCuisines** – Maps each restaurant to one or more cuisines (many-to-many).
  - **Bridge_ConsumerPreferences** – Maps each consumer to one or more preferred cuisines (many-to-many).

#### 2️⃣ Table Schema & Data Snapshot  

<img width="1154" height="736" alt="image" src="https://github.com/user-attachments/assets/036acc6c-8306-4e0a-b52f-a6d41e5751df" />


