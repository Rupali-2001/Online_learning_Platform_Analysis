# 📊 Online Course Platform Analysis - Power BI Dashboard

This Power BI project analyzes user engagement, course performance, ratings, and certification outcomes on an online course platform.

## 🔍 Project Objective

To visualize and monitor key metrics for an online learning platform. This dashboard supports data-driven decision-making by providing insights into user activity, course performance, feedback trends, and certification outcomes.


## 📂  Dashboard Links
 - <a href="https://github.com/Rupali-2001/Online_learning_Platform_Analysis/blob/main/User%20Overview.jpg">User Overview</a>
 - <a href="https://github.com/Rupali-2001/Online_learning_Platform_Analysis/blob/main/Course%20Performance.jpg">Course Performance</a>
 - <a href="https://github.com/Rupali-2001/Online_learning_Platform_Analysis/blob/main/Engagement_analysis.jpg">Engagement Analysis</a>
 - <a href="https://github.com/Rupali-2001/Online_learning_Platform_Analysis/blob/main/Rating%20%26%20Feedback.jpg">Rating & Feedback</a>



## 📁 Dataset: Download Dataset
- <a href="https://github.com/Rupali-2001/Online_learning_Platform_Analysis/blob/main/OnlineLearningPlatform.csv">Dataset</a>
## 📊 Power BI Dashboard (PBIX): View Dashboard File
- <a href="https://github.com/Rupali-2001/Online_learning_Platform_Analysis/blob/main/online_learning_dashboard.pbix">Analysis Dashboard</a>


### 1️⃣ User Overview
- **KPIs**: Total Users, New Users This Month, Average Tenure, Active Users (30 Days)
- **Visuals**:
  - User distribution by age group, gender, country
  - Enrollment trends by month and category

### 2️⃣ Course Performance
- **KPIs**: Total Enrollments, Average Completion Rate, Top-Performing Category
- **Visuals**:
  - Completion funnel
  - Course category breakdown
  - Completion rate heatmap

### 3️⃣ Engagement Analysis
- **KPIs**: Avg. Time Spent per User,  % High-Engagement Users
- **Visuals**:
  - Time trend analysis
  - Session distribution
  - Engagement segmentation

### 4️⃣ Ratings & Feedback
- **KPIs**: Overall Avg. Rating, % of 5-Star Ratings, Courses with Rating < 3, Response Rate
- **Visuals**:
  - Ratings over time
  - Category-wise rating breakdown
  - Low-rated courses list

## 📊 Sample KPIs (DAX Measures)

```DAX
Total Users = DISTINCTCOUNT('Users'[User ID])

New Users This Month = 
CALCULATE(
    DISTINCTCOUNT('Users'[User ID]),
    FILTER('Users', 'Users'[Enrollment Date] >= EOMONTH(TODAY(), -1) + 1)
)

Avg. Completion Rate = 
DIVIDE([Total Completions], [Total Enrollments])

Overall Avg. Rating = 
AVERAGEX('Ratings', 'Ratings'[Rating])

## ⚠️ Challenges Faced

During the development of the **Online Course Platform Analysis** Power BI dashboard, several challenges were encountered and addressed:

1. **Data Cleaning & Transformation**
   - Inconsistent formats in date and categorical fields required substantial preprocessing.
   - Time spent data had to be normalized (converted from minutes to hours) for accurate analysis.

2. **Complex DAX Calculations**
   - KPIs such as *Churn Rate*, *Avg. Time Spent per User*, and *Engagement Metrics* needed advanced DAX logic using `CALCULATE`, `FILTER`, `SUMX`, and `DIVIDE`.
   - Troubleshooting data type mismatches and logical errors in DAX measures took significant effort.

3. **User Segmentation**
   - Implementing dynamic logic for *New Users This Month* and *Active Users (30 Days)* required advanced time intelligence functions like `TODAY()`, `EOMONTH()`, and relative date filtering.

4. **Page Navigation Design**
   - Creating seamless navigation between dashboard pages using buttons and bookmarks was initially confusing and required a clear mapping strategy.
   - Ensuring navigation worked consistently across different report views took testing and refinement.

5. **Visual Design & Layout**
   - Organizing multiple KPIs and charts per page without cluttering the interface required careful layout planning.
   - Maintaining a visually engaging, brand-consistent design across pages was key for presentation quality.

6. **Data Modeling**
   - Ensuring correct relationships between multiple tables (Users, Courses, Sessions, Ratings) was essential for accurate cross-filtering and aggregation.

## ✅ Conclusion

The **Online Course Platform Analysis** dashboard provides a robust, interactive environment for analyzing key metrics such as:

- User acquisition, retention, and churn trends
- Course engagement and completion patterns
- Learner feedback and course ratings
- Certification performance and final scores

Through thoughtful visualizations, navigation, and filtering, the dashboard empowers stakeholders to:

- Make data-driven decisions to improve course content
- Identify user behavior trends to enhance engagement
- Monitor course quality and user satisfaction over time

This project also significantly improved my skills in Power BI, including:
- Designing multi-page dashboards
- Writing and optimizing DAX measures
- Creating intuitive navigation and filters
- Modeling relational datasets effectively

The end result is a powerful analytical tool for ongoing performance monitoring and strategic planning in any online learning environment.
