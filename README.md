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

## 🧠 Design Thinking Process 

### 1️⃣ Empathize  

<img width="1365" height="904" alt="image" src="https://github.com/user-attachments/assets/356a1b3a-d8a3-4e18-99b1-6651e7d7629d" />

<img width="1363" height="898" alt="image" src="https://github.com/user-attachments/assets/12042df3-73cb-4c60-8274-a735a67fb2fc" />


### 2️⃣ Define point of view 

<img width="1368" height="912" alt="image" src="https://github.com/user-attachments/assets/d578e601-d013-45bd-95e9-0206dd38cef2" />

<img width="1370" height="912" alt="image" src="https://github.com/user-attachments/assets/166438ee-c998-4aff-b723-df2df0c1ede0" />


### 3️⃣ Ideate  

<img width="1373" height="905" alt="image" src="https://github.com/user-attachments/assets/ab6c7b5a-816c-41a8-aa93-bd9d97b6e5fd" />

<img width="1370" height="906" alt="image" src="https://github.com/user-attachments/assets/fabff289-b21e-4ebd-b0be-61fd614727ad" />


### 4️⃣ Prototype and review 

This part is in the dashboard


## 📊 Key Insights & Visualizations 

### 🔍 Dashboard Preview

### 1️⃣ Overview

<img width="1202" height="696" alt="image" src="https://github.com/user-attachments/assets/842facec-d13b-497b-9d8f-d016e891cd9e" />

### 📌 Key Findings: 

**1. Overall Satisfaction Is “Okay”, Service Lags Behind**
   
- Avg ratings are moderate **(Avg Overall 1.20 | Avg Food 1.22 | Avg Service 1.09)**.
  
→ The biggest improvement lever is **service quality**, not food.

**2. Most Reviews Are Positive, but “Bad” Still Makes Up a Meaningful Share**

- Rating distribution by label: **Good (486)** > **OK (421)** > **Bad (254)** (total ~1.1K reviews).

→ Focus on **reducing bad experiences** to lift the overall average faster.

**3. Review Volume Is Concentrated — San Luis Potosi Dominates the Dataset**

- **San Luis Potosi = 921 ratings** (largest volume) with Avg Overall ~1.21.

→ Any initiative in SLP will have the **highest impact** on overall results.

**4. Clear City Performance Gap (Quality vs Volume)**

- **Cuernavaca** has higher quality (Avg Overall **~1.38**) with moderate volume (**~107**), while **Ciudad Victoria** is lower (Avg Overall **~0.93**, **~121** ratings).

→ Prioritize **Cuernavaca** as a quality benchmark and investigate/repair **Ciudad Victoria**.

**5. Mexican Cuisine Leads Review Share**

- Cuisine share is led by **Mexican (238 | ~30%)**, followed by **Bar (140 | ~18%)** and **Cafeteria (102 | ~13%).**

→ Improving experience in top cuisines will move the needle the most.

**6. Young Consumers Drive Most Ratings**

- The **<25** age group contributes the largest share of reviews (dominant segment on the chart).

→ Target experience improvements and messaging toward this primary reviewer group (but still monitor bias vs other age groups).


### 2️⃣ Restaurant & Cuisine

<img width="1207" height="691" alt="image" src="https://github.com/user-attachments/assets/c8981a14-0045-4db0-b7cf-e96af9036be3" />

### 📌 Key Findings: 

**1 Higher Price Tiers Receive Better Ratings (Especially Service)**

- **Medium/High** segments score higher than **Low** (Food & Service).

→ Suggests customers perceive better value/experience when restaurants are positioned above low-price.

**2. Low Price Has the Biggest Service Weakness**

- In **Low** tier, **Service (~0.92)** is notably below Food (~1.13).

→ The fastest uplift lever for low-price restaurants is **service consistency** (speed, staff attitude, order accuracy).

**3. Food–Service Gap Highlights Where Experience Is Unbalanced**

- Biggest positive gaps (Food > Service): **Fast Food (+0.23)**, **Mexican (+0.20)**, **Chinese (+0.15)**.

→ These cuisines likely need **service process improvements** more than menu changes.

- Negative gaps (Service > Food): **Brewery/Seafood/American (~-0.03)**.

→ These cuisines may have good service but should **upgrade food quality** to lift overall.

**4. Volume vs Quality Trade-off by Cuisine**

- High-volume cuisines (e.g., **Mexican/Bar/Cafeteria**) drive most reviews but cluster around **mid-level quality**.
- Some cuisines **show higher quality but smaller scale** (more niche).

→ Use this to guide **selective expansion**: scale “high-quality niche” in the right cities, while fixing experience in “high-volume mid-quality”.

**5. Facilities (Area × Parking) Show Signals but Need Sample-Size Guardrails**

- Certain combinations look better/worse, but results can be skewed by low counts (some facility types have few ratings).

→ Recommend showing #Ratings or setting a minimum sample threshold before concluding.

**6. Top Restaurants Are Skewed by Coverage of Cuisine Data**

- The table total is **1043 ratings**, lower than overall 1.1K → indicates cuisine-linked analysis excludes records without cuisine mapping.

→ Important caveat: top lists by cuisine may not represent the full dataset.

#### 3️⃣ Personal Preference

<img width="1204" height="697" alt="image" src="https://github.com/user-attachments/assets/1cd0cfad-9d63-414d-85ad-f263bfd7b5ea" />

### 📌 Key Findings: 

**1. Preference Matching Does NOT Improve Ratings (Negative Uplift)**

- **Avg Overall (Match) = 1.11 vs Avg Overall (NoMatch) = 1.22 → Uplift = -0.12.**

→ Personalization based on cuisine preference is not a strong driver in this dataset.


