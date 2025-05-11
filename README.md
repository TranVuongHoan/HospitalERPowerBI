# Hospital ER Performance Analysis Project

## Description
This project analyzes emergency department operations data to optimize patient flow, improve service quality, and enhance resource allocation. The dataset includes 9,216 patient visits with metrics on wait times, department referrals, satisfaction scores, and demographic factors.

**Data Source**: Hospital EHR System (Anonymized)

## Objectives
The primary goals of this analysis are to:

1. **Assess Operational Efficiency**
   - Identify peak demand periods and wait time patterns
   - Evaluate department referral workflows

2. **Improve Patient Experience**  
   - Analyze satisfaction score drivers
   - Identify demographic-specific service gaps

3. **Optimize Resource Allocation**
   - Correlate staffing levels with performance metrics
   - Identify high-value process improvements

4. **Technical Skill Development**
   - Enhance data cleaning capabilities with complex patient records
   - Master time-series analysis techniques
   - Build interactive healthcare dashboards

## Project Phases

### 1. Data Preparation
- **Data Examination**: 
  - Reviewed 11 raw data fields including timestamps, demographics, and clinical outcomes
  - Identified inconsistencies in department naming conventions

- **Data Transformation**:
  - Standardized time formats (HH:MM → minutes)
  - Categorized continuous variables (age groups, wait time buckets)
  - Handled missing satisfaction scores (7.5% of records)

### 2. Data Modeling
- **Schema Structure**:
  - Implemented star schema with fact_visits central table
  - Created dimensions for time, patients, and departments

## 3. Data Analysis

### Key Focus Areas:

#### Patient Flow Analysis
- Identified 44% YTD volume increase  
- Detected 18% higher Monday arrivals  

#### Operational Performance
- Average wait time: 35.26 minutes (+1% YTD)  
- Gastroenterology shows longest waits (37 mins)  

#### Experience Quality
- Overall satisfaction: 5.47/10  
- Strong negative correlation (r=-0.62) between wait times and satisfaction  

#### Demographic Insights
- Seniors (65+) report highest satisfaction (5.9)  
- Young adults (18-24) report lowest (4.8)  

---

## 4. Report Creation

### Interactive Dashboard Features:
- Real-time patient volume monitoring  
- Department performance benchmarking  
- Satisfaction score predictors analysis  

**Access the Dashboard**: [Hospital ER Dashboard](#)  

### Key Visualizations:
- Heatmaps of hourly/weekly demand  
- Wait time distribution curves  
- Satisfaction vs. wait time scatter plots  

---

## Actionable Insights

### Immediate Actions:
- Implement fast-track for 25% lowest-acuity cases  
- Adjust staffing to cover 2PM-8PM peak  

### Strategic Initiatives:
- Digital wait time notification system  
- Targeted communication training  

### Data Quality Improvements:
- Standardize department naming  
- Enhance age documentation  
