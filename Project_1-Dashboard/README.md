## Salary Dashboard with Excel
  
The data jobs salary dashboard was created to help job seekers investigate salaries for their desired jobs and ensure they are being adequately compensated.  

My final dashboard is in [Salary Dashboard](https://github.com/rosemaryobaro/Data_Analystics--Excel_Projects/blob/123c60c3a5bc13f0d477c2031db7dc6f0d781d49/Project_1-Dashboard/Salary%20Dashboard%20Project.xlsx) 

![Project_1-Dashboard/image/Salary_Dashboard-Excel_Project.png](https://github.com/rosemaryobaro/Data_Analystics--Excel_Projects/blob/3a47d12da1dcbe91938e3934bcfa66f5af5b99a9/Project_1-Dashboard/image/Salary_Dashboard-Excel_Project.png)

### Excel Skills Used  
The following Excel skills were used for analysis:

- **📉 Charts**
- **🧮 Formulas and Functions**
- **❎ Data Validation**

### Data Jobs Dataset

The dataset used for this project contains real-world data science job information from 2023. It includes detailed information on:

- **👨‍💼 Job titles**
- **💰 Salaries**
- **📍 Locations**
- **🛠️ Skills**

## Dashboard Build

### 1. 📉 Charts

#### 📊 Bar Chart- Data Science Job Salaries  

<img src="/Project_1-Dashboard/image/Job_Title_Chart.png" alt="Salary Dashboard Bar Chart1">

- **Excel Features:** Used bar chart feature (with formatted salary values) and optimized layout for clarity.
- **Design Choice:** Horizontal bar chart for visual comparison of median salaries.
- **Data Organization:** Sorted job titles by descending salary for improved readability.
- **Insights Gained:** This enables quick identification of salary trends, noting that Senior roles and Engineers are higher-paying than Analyst roles.

#### 🗺️ Map Chart- Country Median Salaries

![1_Salary_Dashboard_Chart2.png](/Project_1-Dashboard/image/Country_Map_Chart.png)

- **Excel Features:** Utilized Excel's map chart feature to plot median salaries globally.
- **Design Choice:** Color-coded map to visually differentiate salary levels across regions.
- **Data Representation:** Plotted median salary for each country with available data.
- **Visual Enhancement:** Improved readability and immediate understanding of geographic salary trends.
- **Insights Gained:** Enables quick grasp of global salary disparities and highlights high/low salary regions.

### 2. 🧮 Formulas and Functions

#### 💰 Median Salary by Job Titles

```
=MEDIAN(
IF(
    (jobs[job_title_short]=A2)*
    (jobs[job_country]=country)*
    (ISNUMBER(SEARCH(type,jobs[job_schedule_type])))*
    (jobs[salary_year_avg]<>0),
    jobs[salary_year_avg]
)
)
```

- **Multi-Criteria Filtering:** Checks job title, country, schedule type, and excludes blank salaries.
- **Array Formula:** Utilizes `MEDIAN()` function with nested `IF()` statement to analyze an array.
- **Tailored Insights:** Provides specific salary information for job titles, regions, and schedule types.
- **Formula Purpose:** This formula populates the table below, returning the median salary based on job title, country, and type specified.


![1_Salary_Dashboard_Screenshot1.png](https://github.com/rosemaryobaro/Data_Analystics--Excel_Projects/blob/3d174742be9af403f13decbc7ccb199aa0310ec8/Project_1-Dashboard/image/1_Salary_Dashboard_Screenshot1.png)  
*Background Table*  

<img src="/Project_1-Dashboard/image/Job_Title_Salary_Chart.png"  alt="Salary Dashboard Title">  

*Dashboard Implementation*

#### ⏰ Count of Job Schedule Type

```
=FILTER(J2#,(NOT(ISNUMBER(SEARCH("and",J2#))+ISNUMBER(SEARCH(",",J2#))))*(J2#<>0))
```

- **Unique List Generation:** This Excel formula below employs the `FILTER()` function to exclude entries containing "and" or commas, and omit zero values.
- **Formula Purpose:** This formula populates the table below, which gives us a list of unique job schedule types.

**Background Table8**  

![1_Salary_Dashboard_Type.png](/Project_1-Dashboard/image/Job_Type_Salary_Table.png)  

***📉 Dashboard Implementation:***  

<img src="/Project_1-Dashboard/image/Job_Type_Salary_Table.png" alt="Salary Dashboard Type">  

### 3. ❎ Data Validation

#### 🔍 Filtered List

- **Enhanced Data Validation:** Implementing the filtered list as a data validation rule under the `Job Title`, `Country`, and `Type` option in the Data tab ensures:
    - User input is restricted to predefined, validated schedule types
    - Incorrect or inconsistent entries are prevented
    - Overall usability of the dashboard is enhanced

<img src="/0_Resources/Images/1_Salary_Dashboard_Data_Validation.gif" width="425" height="400" alt="Salary Dashboard Data Validation">

## Conclusion

I created this dashboard to showcase insights into salary trends across various data-related job titles. Using the data provided, the dashboard allows users to make informed decisions about their career paths. Exploring the functionalities to understand how location and job type influence salaries. 
