# Employee Data Analysis

## Project Overview
This project involves cleaning, analyzing and storing employee data 
using Python and MySQL. The raw data contained multiple errors, 
inconsistencies and missing values which were cleaned and normalized 
into 3 database tables.

## Dataset
- **Source:** Raw Employee Dataset
- **Size:** 515 employees
- **Columns:** Employee ID, Name, Department, Hire Date, 
Salary, Performance Rating, Email, Location

## Tools Used
- **Python (Jupyter Notebook)** — Data cleaning and transformation
- **MySQL Workbench** — Database creation and management
- **phpMyAdmin** — Online database hosting and verification

## Data Cleaning Steps (Python)
- Removed empty columns
- Fixed name formatting (double spaces, wrong casing)
- Standardized 29 department variations into 7 clean departments
- Standardized 20 location variations into 5 clean cities
- Cleaned salary column (removed $ and commas, handled outliers)
- Generated missing emails from employee names
- Fixed hire date format to YYYY-MM-DD
- Filled missing values appropriately
- Removed 20 duplicate employee IDs

## Database Structure (MySQL)
Three normalized tables created:

### Department Table
| dept_id | department |
|---|---|
| 1 | HR |
| 2 | Sales |
| 3 | Engineering |
| 4 | IT |
| 5 | Finance |
| 6 | Operations |
| 7 | Marketing |

### Location Table
| location_id | location |
|---|---|
| 1 | Chicago |
| 2 | New York |
| 3 | San Francisco |
| 4 | Boston |
| 5 | Austin |

### Employee Table
| Column | Type |
|---|---|
| employee_id | INT (Primary Key) |
| name | VARCHAR(100) |
| dept_id | INT (Foreign Key) |
| hire_date | DATE |
| salary | DECIMAL(10,2) |
| performance_rating | INT |
| email | VARCHAR(100) |
| location_id | INT (Foreign Key) |

## Key Findings
- 495 unique employees across 7 departments
- Engineering had the highest average salary
- Data had significant quality issues including 29 department 
name variations and 20 location variations

## Files
- `employee.csv` — Original dirty dataset
- `Employee Data Cleaned.ipynb` — Jupyter Notebook with full cleaning
- `department_table.csv` — Cleaned department data
- `location_table.csv` — Cleaned location data
- `employee_table_final.csv` — Cleaned employee data
- `employee_db.sql` — Full MySQL database script

