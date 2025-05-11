# Data Modelling Analysis for Hospital ER System

## Star Schema Structure

The hospital ER data model follows a star schema structure optimized for analytical queries, with fact tables containing measurable events and dimension tables providing descriptive context.

### Fact Table
**fact_visits**
- `visit_id` (PK): Unique identifier for each patient visit  
- `patient_id` (FK): Links to dim_patient dimension  
- `date_key` (FK): Links to dim_date dimension  
- `time_key` (FK): Links to dim_time dimension  
- `department_id` (FK): Links to dim_department  
- `wait_time_minutes`: Quantitative measure  
- `has_referral`: Boolean flag  
- `admin_flag`: Boolean administrative status  

### Dimension Tables

**dim_patient**
- `patient_id` (PK): Unique patient identifier  
- `first_initial`: Patient's first initial  
- `last_name`: Patient surname  
- `gender`: M/F classification  
- `race`: Ethnic identification  
- `age_group`: Categorical age bucket (pediatric/adult/senior)  

**dim_time**
- `time_key` (PK): Unique time identifier  
- `hour`: Hour of visit (24h format)  
- `minute`: Minute of visit  
- `time_period`: Morning/Afternoon/Evening/Night  

**dim_date**  
- `date_key` (PK): Surrogate date key  
- `full_date`: Actual datetime  
- `day_of_week`: Monday-Sunday  
- `is_weekend`: Boolean flag  
- `month_name`: Full month name  
- `quarter`: Calendar quarter  

**dim_department**
- `department_id` (PK): Unique department identifier  
- `department_name`: General Practice/Orthopedics/etc.  
- `is_specialty`: Boolean flag for specialty departments  

## Data Loading Strategy

**Dimension Tables First**:
   - Load static reference data (departments, time slots)  
   - Process patient demographics with deduplication  

## Entity-Relationship Diagram
