# User Engagement Analytics

## Project Overview

This project analyzes website user engagement data to understand how users interact with a website and how engagement differs across device types.

The project was developed as part of a data analytics exercise focused on debugging, data validation, time calculations, and visualization. The original user engagement code was producing impossible results, including bounce rates above 100% and negative session times. The analysis identifies these issues, corrects the calculations, validates the data, and produces meaningful engagement insights.

The dataset contains 1,500 website sessions with information about users, devices, page views, session duration, visit dates, browsers, traffic sources, and conversions.

---

## Objectives

The main objectives of this project are to:

- Identify errors in the original engagement metrics code.
- Validate the quality and consistency of the dataset.
- Correct the calculation of bounce rate.
- Calculate average session duration correctly.
- Calculate average pages per session.
- Compare engagement metrics across device types.
- Create visualizations to communicate the results.
- Generate actionable insights from user engagement data.

---

## Dataset

The project uses the **Saudi Website Visitors & Registered Users** dataset.

The dataset contains 1,500 records and 16 variables, including:

| Column | Description |
|---|---|
| `user_id` | Unique identifier for the user |
| `is_registered` | Whether the user is registered |
| `visit_datetime` | Date and time of the visit |
| `session_id` | Unique identifier for the session |
| `device_type` | Device used to access the website |
| `browser` | Browser used by the visitor |
| `referrer` | Source that referred the visitor |
| `page_views` | Number of pages viewed |
| `session_duration_sec` | Session duration in seconds |
| `country` | Visitor's country |
| `city` | Visitor's city |
| `signup_date` | User registration date |
| `user_type` | Type of website user |
| `conversion` | Whether the visitor converted |
| `pages_visited` | Pages visited during the session |
| `utm_source` | Marketing source |

---

## Technologies Used

The project was developed using:

- Python
- Jupyter Notebook
- Pandas
- NumPy
- Matplotlib

---

## Data Validation

Several validation checks were performed before calculating the engagement metrics.

These included:

- Checking the dataset dimensions.
- Checking for missing values.
- Checking for duplicate records.
- Checking for negative page views.
- Checking for negative session durations.
- Checking the number of unique sessions.
- Checking available device types.
- Validating the date/time column.

The `visit_datetime` column was converted to a proper datetime format using:

```python
pd.to_datetime(logs_df['visit_datetime'], errors='coerce')
