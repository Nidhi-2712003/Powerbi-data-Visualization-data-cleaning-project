# Club Members Analysis Dashboard – Power BI

A comprehensive **data cleaning and visualization project** showcasing end-to-end business intelligence skills using **Power Query** for ETL transformations and **Power BI** for interactive dashboard development.

---

## Project Overview

This project demonstrates professional data analytics capabilities through the complete BI workflow:
- **Data Extraction**: Importing raw club membership data from Excel
- **Data Transformation**: Advanced cleaning and standardization using Power Query M language
- **Data Loading**: Structured data modeling in Power BI
- **Data Visualization**: Interactive dashboard design with actionable business insights

**Dataset**: Club Member Information (Mock Data)  
**Tools Used**: Power Query Editor, Power BI Desktop, Excel

(Note - This project uses a publicly available dataset originally published by [iweld](https://github.com/iweld/data_cleaning). All SQL cleaning logic and documentation were developed independently.)

---

## Business Objective

Analyze club membership data to discover:
- **Demographic trends** (age groups, marital status)
- **Geographic distribution** patterns across states
- **Membership growth** metrics over time
- **Professional profiles** of club members

These insights enable data-driven strategies for member engagement, targeted marketing campaigns, and club expansion decisions.

---

## Technical Implementation

### Phase 1: Data Cleaning & Transformation (Power Query)

Implemented comprehensive data quality processes using Power Query M language:

#### **1. Data Import & Initial Setup**
- Loaded raw CSV data with proper encoding
- Promoted headers and established column structure
- Set initial data types for validation

#### **2. Column Standardization**
- **Renamed columns** for consistency and clarity
- **Capitalized each word** in text fields (Full_name, Job_title, Marital_status)
- **Trimmed whitespace** to eliminate leading/trailing spaces
- **Removed special characters** from address and name fields

#### **3. Data Quality Improvements**
- **Removed duplicate records** based on Email (primary key)
- **Handled null values**: Replaced empty strings with proper NULL values
- **Sorted data** by Email for organized processing

#### **4. Address Data Parsing**
- **Split full_address column** by delimiter (",") into component parts
- Extracted **Street**, **City**, **State**, and **Zip** into separate columns
- Removed intermediate transformation columns for clean final output

#### **5. Date Standardization & Cleaning**
- **Created custom date parsing logic** to handle multiple formats:
  - Standalone 4-digit years (e.g., "1995")
  - MM/DD/YYYY format
  - MM-DD-YYYY format
  - Years in 1900s automatically converted to 2000s (e.g., 1995 → 2095)
- Built conditional logic to extract month, day, and year components
- Converted cleaned date strings to proper **Date data type**

#### **6. Age Data Transformation**
- **Added custom Age column** with conditional logic:
  - Extracted numeric values from text
  - Handled 2-digit ages (prepended "0" for formatting)
  - Validated age ranges and converted to **whole number type**

#### **7. Phone Number Formatting**
- **Cleaned phone data** by extracting numeric digits only
- Applied consistent **10-digit format** with proper spacing
- Created formatted phone number column: `(XXX) XXX-XXXX`

#### **8. Final Data Structure**
- Reordered columns logically: Demographics → Contact Info → Location
- Removed temporary transformation columns
- Validated all data types before loading

**All transformation steps documented in**: (`/Power query/Applied_Steps`)

**Cleaned data file available at**: [`/Power query/Club_member_info_Project.xlsx`](./Power%20query/Club_member_info_Project.xlsx)

---

### Phase 2: Data Modeling (Power BI)

- Imported cleaned dataset into Power BI Desktop
- Verified column data types and relationships
- Prepared data model for visualization layer


---

### Phase 3: Dashboard Development

#### **Key Performance Indicators (KPIs)**
- **Total Members** card
- **Membership Growth Rate** (Year-over-Year)
- **Average Member Age**

#### **Visual Components**

1. **Membership Trend Line Chart**
   - Tracks new member enrollments over time
   - Identifies growth patterns and seasonal trends

2. **Geographic Distribution Map**
   - Visualizes member concentration by State
   - Helps identify top markets for expansion

3. **Demographic Breakdown**
   - **Pie Chart**: Marital Status distribution
   - **Bar Chart**: Age group segmentation
   - Reveals target audience characteristics

4. **Professional Profile Analysis**
   - **Matrix/Table**: Top 10 Job Titles by member count
   - Shows club's professional membership base

5. **Interactive Filters (Slicers)**
   - State selector
   - Marital Status filter
   - Job Title filter
   - Age Group filter
   - Enables dynamic, user-driven exploration

#### **Design Principles Applied**
- Clean, professional layout with consistent spacing
- Brand-aligned color palette (blues and grays)
- Clear visual hierarchy and data-ink ratio optimization
- Descriptive titles and tooltips for user guidance
- Mobile-responsive design considerations

---

![Screenshot Name](https://github.com/user-attachments/assets/ffb20002-0afc-4019-9e35-4ca18200e144)


---

## Key Insights & Business Value

### Sample Findings (Based on Mock Data)

- **Primary Age Group**: 25-34 years old represent the largest member segment
- **Marital Status**: 60% single members suggest opportunities for young professional engagement programs
- **Geographic Concentration**: California, Texas, and New York show highest membership density
- **Professional Composition**: Analysts, Managers, and Developers are top 3 job roles
- **Growth Trajectory**: 20% YoY membership increase indicates successful retention and recruitment

### Business Applications

**Marketing Strategy**: Target campaigns toward young professionals in top 3 states  
**Program Development**: Create networking events aligned with member demographics  
**Expansion Planning**: Prioritize new locations in underrepresented high-potential markets  
**Resource Allocation**: Staff and fund initiatives based on member concentration patterns

---

## Repository Structure

```
Powerbi-data-Visualization-data-cleaning-project/
│
├── Power query/
│   ├── Applied_Steps                          # Complete Power Query M code with all transformation steps
│   └── Club_member_info_Project.xlsx          # Power Query cleaned data file
│
├── Club_Members_Power_BI_Visulatiization.pbix  # Power BI Dashboard file
│
└── README.md                                   # Project documentation (this file)
```

---

## Skills Demonstrated

### Technical Skills
- **Power Query M Language**: Complex data transformations and conditional logic
- **ETL Processes**: Extract, Transform, Load best practices
- **Data Cleaning**: Handling nulls, duplicates, inconsistent formats
- **Data Modeling**: Proper data types and structure
- **Power BI Development**: Interactive dashboard design
- **Data Visualization**: Chart selection and design principles
- **Business Intelligence**: Translating data into actionable insights

### Analytical Skills
- Identifying business requirements and KPIs
- Demographic and geographic trend analysis
- Data quality assessment and remediation
- Insight generation and storytelling with data

---

## About

**Created by**: Nidhi  
**Purpose**: Portfolio project demonstrating Business Analytics and Power BI skills  
**Status**: Complete (Open to enhancements)

---

## Contact & Feedback

Interested in discussing this project or collaborating? Feel free to reach out!

- **GitHub**: [@Nidhi-2712003](https://github.com/Nidhi-2712003)
- **LinkedIn**: [Connect with me](https://www.linkedin.com/in/d-nidhi-sree-998a6037a/)
- **Email**: domarajunidhi@gmail.com

---

> © 2025 Nidhi Sree. This project is for educational and professional portfolio purposes. All examples use mock or publicly available data.
