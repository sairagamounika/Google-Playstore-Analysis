# 📱 Google Playstore App Analysis  
**Exploring trends in app ratings, installs, categories, and monetization models**

![Language](https://img.shields.io/badge/Language-R-blue)
![Visualization](https://img.shields.io/badge/Visualization-ggplot2%2C%20networkD3-orange)
![Dataset](https://img.shields.io/badge/Dataset-Kaggle%20Playstore%20Apps-green)
![Status](https://img.shields.io/badge/Status-Completed-success)

---

## 🎯 Objective
The goal of this project was to analyze a comprehensive dataset of **Google Playstore apps** to uncover trends and relationships across categories, content ratings, installs, and pricing models.  
By visualizing key variables, the project aimed to answer:
- What app categories dominate the Playstore?
- How do ratings and installs influence success?
- Are free apps more popular than paid ones?
- How does content rating distribution vary across app types?

---

## 🧠 Dataset Overview
- **Source:** [Kaggle – Google Playstore Apps Dataset](https://www.kaggle.com)  
- **Records:** ~1,048,573  
- **Variables:** 21  
- **Key Attributes:**  
  - App Name, Category, Subcategory  
  - Rating, Rating Count  
  - Installs (Min/Max/Average)  
  - Free or Paid  
  - Price, Size, Currency  
  - Content Rating (Everyone, Teen, etc.)  
  - Android Version, Release & Update Dates  
  - In-App Purchases, Ad Support, Editor’s Choice  

---

## ⚙️ Methodology

### 🔹 Data Cleaning & Preparation
- Removed irrelevant columns (e.g., developer info, privacy policy links).  
- Handled missing ratings and installs by imputing with zeros and filtering invalid rows.  
- Converted categorical variables to factors and numeric fields to numeric type.  
- Created new **Category** variable by grouping subcategories (e.g., merging all game genres into “Games”).  
- Generated new features:
  - `Average_Installs` = (Minimum + Maximum Installs)/2  
  - `Size_in_MB` – standardized using a custom R function.  

### 🔹 Exploratory Data Analysis
Performed EDA using **tidyverse** and **ggplot2**, focusing on:
- Ratings distribution across categories.  
- Free vs Paid app proportions.  
- Content ratings by category (mosaic plot).  
- Install patterns over time.  
- Relationship between release year, update frequency, and installs.

### 🔹 Visualization Techniques
- **Mosaic Plot:** Content rating distribution across categories.  
- **Violin Plot:** Rating spread across app categories.  
- **Sankey Diagram:** Average installs by category and pricing model (Free/Paid).  
- **Dual-Line Chart:** Average installs by year of release vs. last update.  
- **Trend Line (Smoothed):** Ratings trend over time (2010 – 2021).  

---

## 📊 Key Insights
1. **User Preference:**  
   Free apps dominate the Playstore, receiving significantly higher installs than paid ones.

2. **Category Popularity:**  
   - *Games*, *Entertainment & Media*, and *Productivity & Tools* are the top three categories by installs.  
   - Educational and art-related apps maintain high user satisfaction despite lower volume.  

3. **Content Ratings:**  
   - “Everyone” category leads across most app types.  
   - “Games” and “Social & Dating” have more mature-rated apps, reflecting diverse audiences.  

4. **Ratings & Quality:**  
   - Most apps cluster between ratings 4–5, showing general user satisfaction.  
   - Productivity apps maintain consistent ratings; social and gaming apps show greater variability.  

5. **Temporal Trends:**  
   - Average ratings declined slightly over time.  
   - Newer or frequently updated apps attract higher installs, showing that **recency and maintenance** impact success.

---

## 🧩 Tools & Libraries
- **Language:** R  
- **Libraries:** `tidyverse`, `ggplot2`, `ggmosaic`, `networkD3`, `viridis`, `lubridate`, `scales`  
- **Techniques:** EDA, Data Cleaning, Feature Engineering, Visualization Design, Time-Series Analysis  

---

## 🏁 Conclusion
- Free apps dominate the market, though monetization opportunities remain in niche paid segments.  
- Regular updates and high-quality experiences sustain user retention and installs.  
- Category- and audience-specific targeting (e.g., mature vs general apps) helps developers optimize performance.  
- Future work: build an **interactive dashboard (R Shiny)** integrating category filters and visualization widgets.

