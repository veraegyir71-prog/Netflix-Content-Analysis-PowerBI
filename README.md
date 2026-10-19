# Netflix Content Overview & Global Insights Dashboard

## Project Overview
This project analyses **8,787 Netflix titles across 85 countries** to explore the relationship between content type, genre, country of origin, release year, year added to Netflix and audience ratings. The findings are presented in a 3-page interactive Power BI dashboard with written insights.

Completed as part of the Auspify internship task (October 2026).

## 📊 Dashboard Preview

**Page 1: Content Overview**
![Content Overview](screenshots/05_dashboard_content_overview.png)

**Page 2: Global Content Insights**
![Global Content Insights](screenshots/06_dashboard_global_content_insights.png)

**Page 3: Content Growth and Trend Analysis**
![Content Growth and Trend Analysis](screenshots/08_dashboard_growth_trends.png)

## 🎯 Objectives
- Analyse the composition of the Netflix catalogue (movies vs TV shows)
- Identify the most common genres
- Compare content volumes and formats across countries and regions
- Examine how content releases and Netflix additions have changed over time
- Track the share of TV content in new additions
- Present the findings as insights for stakeholders

## 🛠️ Tools Used
- Power BI Desktop
- Power Query (data cleaning and transformation)
- DAX (measures and calculated tables)
- Data Modelling (star-style relational model)
- Data Visualization
- Dashboard Design
- Exploratory Data Analysis

## 🔧 Process
1. **Data preparation (Power Query):** cleaned the raw titles file by splitting and trimming text fields, replacing unknown values and removing duplicates. See `power_query/`.
2. **Genre normalisation:** split the multi-value `listed_in` column into one row per show and genre, creating a `Genre` table linked by `show_id`.
3. **Data modelling:** connected the `Netflix Dataset`, `Genre` and `DimDate` tables, and built a custom `Region_Map` table mapping 85 countries to regions. See `data_model.md`.
4. **DAX measures:** created KPIs, country share, year-over-year growth and TV share. See `dax/measures.dax`.
5. **Dashboard design:** built three themed pages with slicers (type, rating, region, year), a map, drill-down charts and written insights.
6. **Validation:** documented data limitations (unknown countries and the incomplete 2021 year).

## Key Insights

### 1. The catalogue is movie-led
Movies make up **6,124 titles (69.69%)** and TV shows **2,663 titles (30.31%)**. The average movie runs **99.6 minutes**.

### 2. A small set of genres dominates
The top genres are International Movies (2,752), Dramas (2,424), Comedies (1,673) and International TV Shows (1,348). Documentaries (869) and Action & Adventure (859) follow.

### 3. The catalogue is concentrated in a few countries
The **United States (3,240 titles), India (1,056) and the United Kingdom (638)** account for **58.1%** of titles with a known country. The top 10 countries account for **78.0%**.

### 4. Each market has its own format
India is **92% movies**, while Pakistan (83%), South Korea (77%) and Japan (66%) are TV-show heavy. The US has 2,395 movies and 845 TV shows.

### 5. Asia is the second-largest region
Asia accounts for about 30% of titles, ahead of Europe. Most of its titles are movies (1,578 vs 936 TV shows), mainly because of India.

### 6. Global reach grew fast, then levelled off
The number of countries with content added rose from **14 in 2015 to 53 in 2017**, and has stayed between **57 and 63** since 2018.

### 7. Netflix additions peaked in 2019
Additions grew from 82 titles in 2015 to a peak of **2,014 in 2019**, then fell to 1,879 in 2020 and 1,498 in 2021. The 2016 to 2019 period (about 68% annual growth) accounts for **60%** of the whole catalogue.

### 8. The 2021 decline is a partial-year effect
The data ends on **25 September 2021**, so a full-year comparison is needed before reading 2021 as a real drop.

### 9. TV's share of new content is recovering
The TV share of additions fell from 41.08% in 2016 to 24.95% in 2018, then recovered to **33.71% in 2021**.

### 10. The catalogue is recent and arrives fresh
Release volume peaked in **2018 (1,144 titles)**. **70.6%** of titles were released in 2015 or later, and only 525 predate 2000. The median gap between release and Netflix addition is **1 year**, and 36.8% of titles were added in the year they were released.

## 💡 Key Takeaways
1. **The catalogue is movie-led:** about 70% movies and 30% TV shows.
2. **Content is concentrated:** the US, India and UK make up 58.1% of titles with a known country.
3. **Markets differ in format:** India leans heavily to movies, while Pakistan, South Korea and Japan lean to TV shows.
4. **Growth peaked in 2019:** 2,014 titles were added that year, and TV's share of additions is rising again.
5. **Opportunity:** with the US alone at 38.1% of titles, regional content in TV-heavy markets such as Pakistan and South Korea is where there is room to diversify.
6. **Limitations:** titles with unknown countries are excluded from country analysis, and 2021 is a partial year.

## Repository Structure
```
├── README.md
├── data_model.md
├── dax/               # DAX measures
├── power_query/       # Power Query (M) code
├── report/            # Power BI file (.pbix)
└── screenshots/       # dashboard, model and Power Query images
```

## Data Source
Netflix titles dataset (add link and licence here).

## 🎯 Conclusion
Overall, the analysis shows a Netflix catalogue that is movie-led, concentrated in a handful of countries, and heavily weighted towards recent releases. Growth in new additions peaked in 2019, while TV's share of new content is rising and market formats vary sharply by country.

The project demonstrates the use of Power BI, Power Query, DAX, data modelling, data visualization, KPI analysis and data storytelling to turn raw catalogue data into meaningful insights.

**Vera Egyir**
Data Analyst
