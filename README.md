# Project: Indeed Data Jobs Market Analysis (2019)

## Project Purpose
The purpose of this project is to analyze the US job market for Data Jobs to answer the following questions.
The scope of this project is limited to top 10 US Tech(IT) cities.

## Tools & Modules Used
**Python3 | Pandas | Plotly | API Requests | Beautiful Soup | RegEx**

![think_data](images/plot1.png)


## Analysis/Questions Addressed
*   Job count section:
    1.  Which US cities—out of the "tech hubs"—has more data jobs?
    2.  City-wise, which companies are posting more data jobs?
    3.  Which companies (combined for all 10 cities) are posting relatively higher number of data jobs?
    4.  What is the number of data jobs getting posted for various job titles like data analyst, data scientist, data engineer, BI, AI, Machine Learning etc.? Are there more jobs for one  job title over the other? Which job title has been posted the most and which has been posted the least?

*   Salary section:
    1.  What is the salary range for data job wages? How does it change based on the city?
    2.  Is there a correlation between data job salary and company rating?
    3.  Is there a correlation between data job salary and minimum experience required?
    4.  Where does the data wages stand in comparison to city/state median wages?
    5.  How well are the data wages doing in comparison to the apartment rent based on the city?
    6.  How well are the data wages doing in comparison to the median house prices based on the city?

*   Crime section:
    1.  What is the ratio of number of data jobs posted and per capita crime rate based on the city?

## Project Scope
* Job Titles in Scope of the Project:
All Titles with the word 'Data' (includes data analyst, scientist, engineer etc.), Business Intelligence/BI, Artificial Intelligence/AI, Machine Learning, Tableau, Power BI, Statistician/Statistical.

* Cities in Scope of the Project - Following cities and 25 miles around them:
Austin-TX, San Francisco-CA, Raleigh-NC, Denver-CO, Seattle-WA, Atlanta-GA, Boston-MA, New York City-NY, Washington-D.C., Columbus-OH

## Data Sources
*   Jobs data csv created using Indeed API (in data_collection module)
*   Salary, rating, experience csv files created using web scraping (in data collection module)
*   Zillow - csv files for House Prices
*   BLS - csv for City and State Median Salary (All Occupation) data
*   Data.World (using FBI data 2015) - csv for Crime data
*   Apartment List (Rentonomics) - csv for Apartment Rents data

## Analysis Results
*   **Top 10 US Tech Cities vs Number of data jobs posted in the last quarter or 2019:** Based off of daily samples for 120 days (based of pubdates), I was we were able to find the total number of jobs posted by each one of the 10 "tech hubs" in the US for all data-related jobs (e.g. data scientist, BI analyst, data engineer, etc.). This was simply extracted by using Indeed's API and getting the value_counts() of these jobs (q or queries) in these cities (l or locations). It is pretty clear to see that most of the growth in the last 4 months is happening in cities like DC (metro area), NYC and San Francisco.
*   **Citywise Top 50 Companies vs Number of Data Jobs Posted:** By continuing the analysis of our data jobs dataframe, we're now looking at the aggregate of total number of data jobs for the top 50 companies, grouped by cities to determine which companies are hiring like mad in the past 4 months across all these tech hubs. Unsurprisingly, names such as Deloitte, Accenture, Dell appear in most. Amazon has the lead in Seattle, Dell in Austin, and so on.
*   **Top 20 Companies that posted highest number of data-related jobs in the last quarter of 2019:** This graph is rather a continuation of the previous one, but instead of looking at the top 50 companies by number of jobs and grouping by city, we're now looking at the top 20 with the highest number of data jobs to determine—across all tech hubs—which are the ones that have the most job openings in the past 120 days. We were shocked to discover the Ho-Chunk is the company that has posted the most (based on DC), followed by Amazon (Seattle) and Compass (NYC).
*   **City-Based: Job Title vs Number of Jobs Posted in the last quarter of 2019:** There are more openings for Data Analyst and Data Engineer positions as compared to other Data Job Titles. Data Science positions are next in row. AI and Statistic jobs are relatively less in number.
*   **Annual Data Job Salaries:** This visualization represents the salary range based on the city. For most cities among this data, the max salaries or outliers, are significantly further away from the median than the minimum salaries. A feature of both visualizations is the median salary of a data job in San Francisco is higher. However, this is probably because of the higher living costs in the city themselves.
*   **Annual Median Wages Comparison - Data Job Wages vs City Wages vs State Wages:** In most cities, Data Jobs have higher median salaries than the respecitve city and state’s median salary for all job types. The outlier in the dataset is Seattle, this may be explained by the limited availiblity of salary data publically.
*   **Company Annual Max Data Job Salary vs Company Rating:** There does not appear to be a strong linear correlation between company’s rating and the salaries their employees are paid. Most companies fall within a rating range of 3.5-4.5/5. Consistent salary data was difficult to obtain via scraping the Indeed job posts, the resulting data required additional cleaning which may skew the results. Some information that was not gathered for this exercise but may help to explain these ratings would be total compensation (insurance, stock options, etc.).
*   **Maximum Data Job Salary vs Minimum Experience Required for the Job:** There does not appear to be a strong linear correlation between maximum salary and minimum experience requirement for the job. Most of the max salaries fall within an experience requirement of 1 to 5 years. Consistent experience data was difficult to obtain via scraping the Indeed job posts, the resulting data required additional cleaning which may skew the results.
*   **Monthly Minimum Median Data Job Wages vs Apartment Average Rent:** The city with the highest median salaries for data science jobs, San Francisco, also has the most expensive apartment costs of all the cities in the dataset. The relationship of high salary/high rent is not present for other large cities in the dataset. For example, Atlanta has a large metropolitan population but has low rental cost relative to median salary.
*   **Annual Minimum Median Data Job Wages vs Median House Price:** This figure illustrates a similar trend that was seen in the median rent vs median salary information. Cities that have higher median salaries have a more expensive real estate market. San Francisco has the highest home prices as well as highest median salary of all the cities in the dataset.
*   **Number of Data Jobs vs Per Capita City Crime Rate:** One of the more interesting observations from the graph is the amount of violent crime compared to data jobs. There is almost twice as much crime as there is data jobs listed in Atlanta. Conversely, the city with the lowest crime rate in proportion to the highest job count is New York City. The two most prevalent crimes other than violent crimes within the cities is aggravated assault and robbery.

## Conclusion
The job market for Data Jobs is quite promising based on the last quarter of Indeed data for 2019. Big as well as small - all sorts of companies have many data related jobs posted. Salaries for Data Jobs are quite good as well as compared to the city and state median salaries for all occupations.

As there is always a scope for improvement, we would want to explore historical data for data jobs market (if availabe) and use advanced RegEx for web scraping.
