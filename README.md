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

<img width="1359" height="789" alt="image" src="https://github.com/user-attachments/assets/a7ed21f4-92b1-49cc-8165-ccdb720c6624" />

<img width="1366" height="905" alt="image" src="https://github.com/user-attachments/assets/8a95847e-efa7-4b2f-89bf-ad4443132611" />




### 3️⃣ Ideate  

<img width="1367" height="911" alt="image" src="https://github.com/user-attachments/assets/bed30e0b-0354-4f40-b358-fbb4eeac003f" />

<img width="1362" height="725" alt="image" src="https://github.com/user-attachments/assets/fc254fb6-5ba9-46d4-b901-c6ead1deae8c" />



### 4️⃣ Prototype and review 

This part is in the dashboard


## 📊 Key Insights & Visualizations 

### 🔍 Dashboard Preview

### 1️⃣ Overview

<img width="1206" height="699" alt="image" src="https://github.com/user-attachments/assets/9544d953-3140-4461-af97-44b20361fc5e" />


## 📌 Key Findings

1. **Overall satisfaction is “moderate”, and Service is the main weakness**
   - Average ratings: **Avg Overall = 1.20**, **Avg Food = 1.22**, **Avg Service = 1.09**.
   - → The fastest lever to lift the overall experience is **Service quality/consistency**, not Food.

2. **Dataset coverage is solid (enough to compare cities/cuisines with confidence where volume is high)**
   - Dashboard covers **130 restaurants** and **138 consumers**.
   - Rating distribution totals **~1.16K ratings** (**Good 486 | OK 421 | Bad 254**).
   - → City/cuisine comparisons are most reliable in segments with **higher rating counts**.

3. **Most reviews are positive, but “Bad” is still a meaningful share**
   - Distribution: **Good (486) > OK (421) > Bad (254)**.
   - → Reducing “Bad” experiences is the **quickest path** to improve **Avg Overall**.

4. **Review volume is highly concentrated — San Luis Potosi drives the biggest impact**
   - **San Luis Potosi = 921 ratings** (largest volume) with **Avg Overall ~1.21**.
   - → Any improvement program in **SLP** will move the overall metric the most (**highest leverage city**).

5. **Clear city performance gap (Quality vs Volume)**
   - **Cuernavaca** shows the **highest quality** (**Avg Overall ~1.38**) with meaningful volume (~107).
   - **Ciudad Victoria** is the **lowest performer** (**Avg Overall ~0.93**) with moderate volume (~121).
   - → Use **Cuernavaca** as a benchmark and prioritize fixing experience issues in **Ciudad Victoria**.

6. **Cuisine mix is led by a few high-volume cuisines — improving them moves the needle**
   - Review share: **Mexican (~30%)**, **Bar (~18%)**, **Cafeteria (~13%)**, **Fast Food (~12%)**, **Seafood (~8%)** (+ **Other ~19%**).
   - → Focus service/experience improvements in **top-volume cuisines** (especially Mexican/Bar/Cafeteria) for the biggest overall lift.

7. **Young consumers contribute the largest share of ratings**
   - The **<25** age group contributes the biggest portion of reviews (dominant segment in the age chart).
   - → Prioritize experience fixes and communication that resonate with this segment, while still monitoring potential bias from uneven sample sizes.


### 2️⃣ Restaurant & Cuisine

<img width="1209" height="690" alt="image" src="https://github.com/user-attachments/assets/9044c4dc-feea-4d21-b0ce-dbdc0aafed77" />


### 📌 Key Findings: 

**1. Service is still the bottleneck (Food > Service), and it shows up even inside sub-segments**

- Overall on this page: **Avg Overall = 1.20**, **Avg Food = 1.22**, **Avg Service = 1.09**.

→ Any “quick win” uplift should prioritize **service consistency** (speed, accuracy, staff attitude), not only menu changes.

**2. Clear “Price → Quality” gradient — Low-price tier is where service breaks the most**

- **Medium/High** tiers rate higher than **Low** for both Food & Service
- In **Low** tier, **Service drops harder** than Food (service visibly lower than food).

→ For low-price restaurants, the fastest lift is **service playbook execution** (queue/wait-time control, greeting, order accuracy, recovery).

**3. Food–Service Gap tells you what to fix by cuisine (service-process vs food-quality problem)**

- Measure used: **FS Gap = Avg Food − Avg Service.**
- Negative gaps (**Service > Food**) indicate “service ok but food lags”: **Brewery/Seafood/American (~-0.03)**.

→ Food is acceptable, but service execution drags the experience” → prioritize **service process**.
→ “Service is ok, but food consistency/value perception needs work” → prioritize **food consistency & value clarity**.

**4. Cuisine portfolio: high-volume cuisines drive impact, but not always top quality**

- Volume vs Quality view shows high-volume cuisines (e.g., **Mexican / Bar / Cafeteria / Other**) clustering around **mid-level Avg Overall.**
- Some cuisines appear **higher quality but smaller scale** (more niche).

→ Strategy: **fix experience in high-volume cuisines first** (highest ROI per effort), then selectively scale “high-quality niche” concepts where city signals support it.

**5. Alcohol service correlates with a better satisfaction mix (more “Good”, less “Bad”)**

- **Wine & Beer / Full Bar** segments show higher Good share (~45–46%) and lower Bad (~20%) vs None (Good ~40%, Bad ~22%).
- Some cuisines appear **higher quality but smaller scale** (niche opportunities).

→ Strategy: **fix experience** in high-volume cuisines first, while selectively scaling “high-quality niche” cuisines in the right cities.

**6. City action priority is clearer when combining Volume + Avg Overall + Share-of-Total**

- City matrix highlights :
  +   **San Luis Potosi** dominates volume (**889 / 1043 cuisine-linked ratings**) with mid Avg Overall (~1.21) → **highest impact market.**
  +   **Cuernavaca** has the best quality (**Avg Overall ~1.47**) but smaller volume (59) → **benchmark city**.
  +   **Ciudad Victoria** is lowest quality (**~0.94**) with meaningful volume (83) → **recovery plan.**

→ Prioritize :  **SLP (impact)** → **Ciudad Victoria (fix)** → **Cuernavaca (benchmark & replicate)**..

#### 3️⃣ Personal Preference

<img width="1209" height="698" alt="image" src="https://github.com/user-attachments/assets/c016e7b5-6978-4f4e-9958-e5e7745fdcac" />


### 📌 Key Findings: 

**1. Preference Matching Does NOT Improve Ratings (Negative Uplift)**

- **Avg Overall (Match) = 1.11 vs Avg Overall (NoMatch) = 1.22 → Uplift = -0.12.**

→ Personalization based on cuisine preference is not a strong driver in this dataset.

**2. MatchShare Is Low → Limited Coverage for Personalization**

- **MatchShare = 18.86%** (only ~1/5 reviews are “matched”).

→ Even if match helped, its business impact would be limited unless match share increases.

**3. Rating Mix Shifts Slightly Worse Under “Match”**

- Rating structure chart shows the **Match group has a higher** **“bad” share** (red) and a lower “good” share than NoMatch.

→ Suggests “matching cuisine” alone doesn’t guarantee a better experience; execution matters more (service/quality).

**4. The Match vs NoMatch Gap Varies by Cuisine (Not Universal)**

- The cuisine comparison chart indicates some cuisines have **smaller gaps**, while others show **NoMatch outperforming Match** clearly.

→ Personalization should be **tested by cuisine**, not rolled out broadly.

**5. MatchShare Is Highly Skewed by City (Potential Bias)**

- City table highlights extremely high MatchShare in **Ciudad Victoria (~63.86%)** but **low Avg Overall (~0.94).**

→ City effect may be dominating: high match share can coexist with low satisfaction → underlying issues likely service/operations, not preference fit.

**6. San Luis Potosi Still Dominates Volume, So Match Impact Is Mostly There**

- Match share by city shows most reviews come from **San Luis Potosi**; improvements targeted there will move overall metrics most.

→ If running personalization pilots, start in **high-volume city** segments to get reliable results.

## 🔎 Final Conclusion & Recommendation

| Strategy | Insight | Recommendation |
|---|---|---|
| **1. Market Prioritization (City Strategy)** | - Satisfaction is **moderate** overall (**Avg Overall 1.20 \| Food 1.22 \| Service 1.09**) → **Service is the main constraint**.<br>- Review volume is **heavily concentrated in San Luis Potosi** (**~889 / 1,043** cuisine-linked ratings) → biggest “impact market”.<br>- Clear quality gap by city: **Cuernavaca** has the best quality (**Avg Overall ~1.47**) while **Ciudad Victoria** is the lowest (**~0.94**). | - **Fix Service-first in San Luis Potosi** to get the fastest overall uplift (largest volume).<br>- Use **Cuernavaca as a benchmark city** (replicate operating practices / service routines that drive higher ratings).<br>- Run a **recovery plan for Ciudad Victoria** (service audits + staff coaching) before any scale/expansion focus. |
| **2. Cuisine / Concept Portfolio Optimization** | - The **Food–Service Gap** clearly shows *what to fix* by cuisine: **Fast Food (+0.23), Mexican (+0.20), Chinese (+0.15)** → “Food is OK, service is dragging the experience”.<br>- Some cuisines are **service-led** (**Brewery/Seafood/American ~-0.03**) → likely “service OK, food/value perception needs work”.<br>- The **Volume vs Quality** view suggests a portfolio problem: high-volume cuisines contribute most impact but cluster around **mid-level quality**, while a few niches look higher quality but smaller scale. | - Build a **Cuisine Playbook by gap type**:<br>  **(A) Gap-positive cuisines (Food > Service):** prioritize **service execution** (speed, accuracy, queue management, staff attitude).<br>  **(B) Gap-negative cuisines (Service > Food):** prioritize **food consistency/value** (recipe standardization, freshness, portion consistency).<br>- Use “**High Volume × Low/Medium Quality**” cuisines as **first-wave improvement targets** (largest impact per effort).<br>- For “**High Quality × Low Volume**” niches: scale selectively only where city signals support it (avoid over-expanding without volume proof). |
| **3. Pricing & Positioning** | - **Medium/High** price tiers are rated higher than **Low** (Food & Service).<br>- In **Low** tier, **Service weakness** is most visible (service drops more than food). | - If prioritizing **mid-to-high positioning**, focus on the experience that customers “pay for” most: **Service consistency + atmosphere cues**.<br>  **Top 3 experience priorities:**<br>  1) **Service reliability** (greeting, wait-time control, order accuracy, problem resolution).<br>  2) **Comfort & ambiance basics** (cleanliness, noise/space comfort, staff presence).<br>  3) **Value clarity** (menu transparency, portion/value alignment, consistent quality).<br>- For **Low-price** restaurants: deploy a **Service Playbook** (speed, accuracy, staff training) to reduce “Bad” quickly and lift Avg Overall faster than menu changes. |
| **4. Experience Levers Beyond Menu (Alcohol Service)** | - Alcohol service correlates with a better satisfaction mix: **Wine & Beer / Full Bar** show higher **“Good” share (~45–46%)** vs **None (~40%)**, and lower “Bad”. | - Treat alcohol availability as a **premium experience signal** (not only product): improve **service flow**, staff attentiveness, and “occasion” feel.<br>- If adding alcohol is not feasible, mimic the “bar-like experience” through **service rituals** (recommendations, hospitality, smoother pacing). |
| **5. Measurement & Data Guardrails (Next Steps)** | - Cuisine-linked views show **1,043 ratings**, lower than the overall total (~1.1K) → some records are missing cuisine mapping → risk of biased conclusions.<br>- Some segments (city/cuisine/facility) may have low sample sizes → unstable averages. | - Always display **#Ratings** next to key visuals and apply **minimum sample thresholds** before concluding (e.g., cuisine/city ≥ N).<br>- Track success via a clear North Star: **increase Avg Overall + increase “Good” share + reduce “Bad” share**.<br>- If possible, enrich with **footfall/revenue/cost** to estimate ROI for pricing, facility, or service investments. |



