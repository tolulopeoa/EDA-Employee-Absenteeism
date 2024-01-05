# Exploratory Data Analysis on Employee Absenteeism using Pandas, Matplotlib and Seaborn

## Business Case Study
>This dataset was put together using absenteeism records from a courier company in Brazil from July 2007 to July 2010.
>
## The Business Task
>In this exercise, I will use exploratory data analysis to determine the likely cause of `Employee Absenteeism` at the company during working hours.
>
## What is Absenteeism?
> `Absenteeism` at work refers to the habitual or intentional absence of an employee from their workplace, where the absence is often unscheduled and unplanned. It is a measure of the frequency and duration of employees being away from work when they are scheduled to be present.
> 
## Purpose of the EDA
>In this exercise, I will analyze patterns of `Absenteeism`, such as the most common reasons for absence, the distribution of absenteeism durations, and any potential correlations with other features in the dataset.
>
>I will explore questions like:
>
>* What are the most common reasons for employee absenteeism?
>* How does the season or month affect absenteeism?
>* Are there patterns in absenteeism based on certain demographics or characteristics?
>
## Findings
>1. What are the most common reasons for employee absenteeism?
>
![Top reasons](https://github.com/tolulopeoa/EDA-Employee-Absenteeism/assets/102050942/98de7505-43b2-4bf8-bb4c-43b418a17664)
<br>
>The primary reason is attributed to `'Diseases of the musculoskeletal system and connective tissue'`, which leads with
the highest absenteeism time of `842 hours`, followed by 'Injury, poisoning, and certain other consequences of external causes' with 729 hours and 'Medical Consultation' ranking third at 725 hours.
>
>Dispatch riders often face challenges such as prolonged periods of riding, exposure to vibrations, navigating through traffic, and handling packages, which collectively increase the risk of musculoskeletal strains and injuries.
>
<br>

>2. How does the season or month affect absenteeism?
![Time variables](https://github.com/tolulopeoa/EDA-Employee-Absenteeism/assets/102050942/6214dd81-d4c0-45da-98be-42e5fb70914f)

<br>

>The Seasons represents; Summer (1), Autumn (2), Winter (3), and Spring (4). It is evident that `‘Winter’ `records the highest absenteeism time among employees. This could be attributed to various factors, including weather conditions, potential health issues associated with winter, or increased workload during the winter season.
>
>Month of absence is from January (1) to December (12). The month with the highest absenteeism time is
`‘March’`, closely followed by `‘July’`. Conversely, `‘January’` has the lowest absenteeism time. This could be related to a fresh start in the new year, with employees generally being more present and engaged.
>
>Days are represented as Monday (2) to Friday (6). `‘Monday’` stands out as the day with the highest absenteeism time. This could be attributed to the "Monday blues" phenomenon, where employees might experience higher stress levels or challenges returning to work after the weekend.
>

>3.  What is the correlation between various employee demographics/characteristics and absenteeism time?

![Correlation](https://github.com/tolulopeoa/EDA-Employee-Absenteeism/assets/102050942/ae347f54-28f5-44db-8513-6efbf9f20b1f)

>The `weak correlations` suggests that age, body mass index, and other work and lifestyle factors have minimal impact on absenteeism.


## Conclusion
>Diseases of the musculoskeletal system and connective tissue contributes significantly to the highest absenteeism hours. The nature of their work also `involves repetitive motions, exposure to external elements, and the potential for accident`s, contributing to health issues related to the musculoskeletal system and injuries.
>
>The seasonal analysis identifies winter as the peak season for absenteeism, potentially influenced by the physically demanding nature of a courier job. The weak correlations suggests that age, body mass index, and other work and lifestyle factors have minimal impact on absenteeism
>
## Recommendation
>To address this, the company might consider implementing measures to enhance employee well-being, such as
`ergonomic improvements, health and safety programs, or periodic health check-ups`.
>
>Additionally, providing adequate support and resources for employees in such physically demanding roles could contribute to a healthier and more productive work environment with less absenteeism time.

<br>
<br>
<br>

## Employee Absenteeism Exploration using SQL
>I performed an equivalent SQL query on the datasets with the objective of merging datasets, applying transformations, extracting only the relevant columns, and addressing specific questions.
>

>Viewing the contents of all the three tables.
>

![Absenteeism_at_work table](https://github.com/tolulopeoa/EDA-Employee-Absenteeism/assets/102050942/2066be92-201d-423f-8b02-98f330e49ae6)
<br>
![compensation table](https://github.com/tolulopeoa/EDA-Employee-Absenteeism/assets/102050942/5e605650-c98c-406b-9427-96763bbf120b)
<br>
![Reasons table](https://github.com/tolulopeoa/EDA-Employee-Absenteeism/assets/102050942/87d236ee-baa0-42c2-87bb-7667ee632cfe)
<br>
<br>


>Changing the column name 'Work_Load_Average/day_' in Absenteeism_at_work table.
>
![work_load_average_per_day](https://github.com/tolulopeoa/EDA-Employee-Absenteeism/assets/102050942/135fab9e-992f-45fd-acbf-459f2cdc32de)
<br>

>Joining all three tables
>![Untitled 5](https://github.com/tolulopeoa/EDA-Employee-Absenteeism/assets/102050942/8259d7c3-d6ab-4257-a618-f0f3a03fbff6)
<br>

>Finding the healthiest employees that will be given bonuses
>
![Employees qualified for bonuses](https://github.com/tolulopeoa/EDA-Employee-Absenteeism/assets/102050942/84f81593-e798-4057-8f16-14ffea69e997)

>Combining these conditions ensures that only employees who do not drink socially, do not smoke socially, have a BMI less than 25, and have absenteeism time less than the average are included in the result set. These employees are considered the "healthiest" based on the provided criteria and are eligible for a bonus.
>
<br>

>What is the compensation rate increase for non-smokers?
![Non-Smokers compensation](https://github.com/tolulopeoa/EDA-Employee-Absenteeism/assets/102050942/86855e95-bdd9-476f-a6bc-3b112bc536f8)
>
>This query essentially provides the count of employees who do not smoke socially. This information could be relevant because the company is considering a compensation rate increase specifically for non-smokers.
>>
<br>

>Optimize the query by joining all three tables, adding new columns and selecting only relevant fields for analysis.
>
![Optimization](https://github.com/tolulopeoa/EDA-Employee-Absenteeism/assets/102050942/b6e9c5c4-53b1-41ab-bbd8-3db5cd087df7)
![Optimization](https://github.com/tolulopeoa/EDA-Employee-Absenteeism/assets/102050942/4e31a68e-13dd-4a7d-9caa-fc78f46a6410)
>
>The result is a dataset that includes data on the absenteeism, compensation, and reasons for absence, with additional columns providing categorized information about BMI, season, day of the week, and month. This can facilitate easier analysis and interpretation of the data.
>







