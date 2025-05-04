COVID-19 Data Analysis Project
==============================

Overview
--------
This project provides a comprehensive SQL-based analysis of global COVID-19 data,
focusing on infections, deaths, and vaccination progress across countries and over time.
Using two main datasets - CovidDeaths and CovidVaccinations - the analysis explores key
pandemic metrics, calculates rates and percentages, and identifies trends to support
data-driven insights.

Check Out the Dashboard
-----------------------
I have created an interactive Tableau dashboard to visualize the findings of this project.
You can:
- View a snapshot of the dashboard in the included image file: [dashboard_image.png] (replace with your actual filename)
- Download and open the Tableau workbook (`.twb` or `.twbx`) in Tableau Desktop or Tableau Public to explore the dashboard interactively.

**To view the dashboard:**
1. Download the Tableau file from this repository.
2. Open it using Tableau Desktop or Tableau Public (free to download).
3. Explore the visualizations and insights.

Data Sources
------------
- CovidDeaths$: Contains daily records of COVID-19 cases, deaths, and population by country and date.
- CovidVaccinations$: Tracks daily vaccination numbers by country and date.

Key Analyses
------------
1. Data Exploration
   - Retrieve all records from the CovidDeaths table, ordered by date and location, to inspect the raw data and understand its structure.

2. Case and Death Trends
   - Analyze the progression of total cases, new cases, and total deaths over time for specific countries (e.g., United States).
   - Calculate the daily and cumulative death percentages using:
     Death Percentage = (total_deaths / total_cases) * 100

3. Infection Rates Relative to Population
   - Compute the percentage of the population infected in each country:
     Infection Percentage = (total_cases / population) * 100

4. Death Rates Relative to Population
   - Calculate the percentage of the population that died due to COVID-19 in each country:
     Death Rate = (total_deaths / population) * 100

5. Country-Level Summaries
   - Aggregate total deaths by country and create a view (total_deaths_by_country) for easy visualization and further analysis.
   - Summarize total deaths for specific countries (e.g., Egypt) to provide focused insights.

6. Vaccination Progress
   - Join CovidDeaths and CovidVaccinations tables to track vaccination rollout.
   - Calculate rolling totals of people vaccinated per country using SQL window functions.
   - Derive the percentage of the population vaccinated over time:
     Vaccinated Percentage = (rolling_people_vaccinated / population) * 100

7. Temporary Tables for Advanced Analysis
   - Create and populate a temporary table (#PercentPopulationVaccinated) to store and analyze vaccination progress by date, location, and continent.

Technical Highlights
--------------------
- SQL Window Functions: Used for calculating rolling sums (e.g., cumulative vaccinations).
- Data Type Handling: Explicit casting ensures accurate percentage calculations and avoids integer division errors.
- Views and Temporary Tables: Facilitate modular analysis and visualization.
- Order and Grouping: Queries are structured for clear chronological and geographical comparisons.

Insights & Use Cases
--------------------
- Track pandemic trends and compare the impact across countries and continents.
- Identify regions with the highest infection and death rates.
- Monitor vaccination progress and estimate herd immunity thresholds.
- Support data-driven decision-making for public health responses.

Conclusion
----------
This project demonstrates how SQL can transform raw COVID-19 data into actionable insights.
By leveraging advanced SQL techniques, it provides a robust framework for pandemic data analysis,
supporting research, policy, and public health planning.
