# pandas-challenge
UCB Data Analytics Week 4 Challenge

**District Summary**

Perform the necessary calculations and then create a high-level snapshot of the district's key metrics in a DataFrame.
Include the following:
- Total number of unique schools
- Total students
- Total budget
- Avg. Math Score
- Avg. Reading Score
- % passing math (percentage of students who passed math)
- % passing reading (percentage of students who passed reading)
- % overall passing (percentage of students who passed math AND reading)

**School Summary**

Perform the necessary calculations and then create a DataFrame that summarizes key metrics about each school.
Include the following:
- School name
- School type
- Total students
- Total school budget
- Per school budget
- Avg. Math Score
- Avg. Reading Score
- % passing math (percentage of students who passed math)
- % passing reading (percentage of students who passed reading)
- % overall passing (percentage of students who passed math AND reading)

**Highest-Performing Schools (by % Overall Passing)**

Sort the schools by "% Overall Passing" in descending order and display the top 5 rows.
Save the results in a DataFrame called "top_schools"

**Lowest-Performing Schools (by % Overall Passing)**

Sort the schools by "% Overall Passing" in ascending order and display the top 5 rows.
Save the results in a DataFrame called "bottom_schools"

**Math Scores by Grade**

Perform the necessary calculations to create a DataFrame that lists the average math score for students of each grade level (9th, 10th, 11th, 12th) at each school.

**Reading Scores by Grade**
Create a DataFrame that lists the average reading score for students of each grade level (9th, 10th, 11th, 12th) at each school.

**Scores by School Spending**
Create a table that breaks down school performance based on average spending ranges (per student).
Use the code provided below to create four bins with reasonable cutoff values to group school spending.

    spending_bins = [0, 585, 630, 645, 680]
    labels = ["<$585", "$585-630", "$630-645", "$645-680"]

Use pd.cut to categorize spending based on the bins.
Use the following code to then calculate mean scores per spending range.

    spending_math_scores = school_spending_df.groupby(["Spending Ranges (Per Student)"]).mean()["Average Math Score"]
    spending_reading_scores = school_spending_df.groupby(["Spending Ranges (Per Student)"]).mean()["Average Reading Score"]
    spending_passing_math = school_spending_df.groupby(["Spending Ranges (Per Student)"]).mean()["% Passing Math"]
    spending_passing_reading = school_spending_df.groupby(["Spending Ranges (Per Student)"]).mean()["% Passing Reading"]
    overall_passing_spending = school_spending_df.groupby(["Spending Ranges (Per Student)"]).mean()["% Overall Passing"]

Use the scores above to create a DataFrame called spending_summary.
Include the following metrics in the table:
- Average math score
- Average reading score
- % passing math (the percentage of students who passed math)
- % passing reading (the percentage of students who passed reading)
- % overall passing (the percentage of students who passed math AND reading)

**Scores by School Size**
Use the following code to bin the per_school_summary.

    size_bins = [0, 1000, 2000, 5000]
    labels = ["Small (<1000)", "Medium (1000-2000)", "Large (2000-5000)"]

Use pd.cut on the "Total Students" column of the per_school_summary DataFrame.
Create a DataFrame called size_summary that breaks down school performance based on school size (small, medium, or large).

**Scores by School Type**
Use the per_school_summary DataFrame from the previous step to create a new DataFrame called type_summary.
This new DataFrame should show school performance based on the "School Type".

**Written Report**
To receive all points, the written report presents a cohesive written analysis that:
- Summarizes the analysis
- Draws two correct conclusions or comparisons from the calculations
