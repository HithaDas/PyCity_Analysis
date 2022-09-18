# PyBer_Analysis
Student data Analysis using Pandas

# Overview of Project

Maria is the chief data scientist for a city school district. Maria is responsible for analyzing information from a variety of sources and in a variety of formats. In this role, she is tasked with preparing all standardized test data for analysis, reporting, and presentation to provide insights about performance trends and patterns.
These insights are used to inform discussions and strategic decisions at the school and district level. This will help Maria analyze data on student funding and student's standardized test scores.
The analysis consits of the following deliverables -

Deliverable 1: Collect the student data into a DataFrame.

Deliverable 2: Prepare a cleaned version of the DataFrame.

Deliverable 3: Summarize key pieces of the data.

Deliverable 4: Drill down into the data to analyze specific subsets.

Deliverable 5: Compare and contrast the data through grouping and aggregation functions.

Deliverable 6: A written analysis of your results (README.md).

Data resources - csv file, jupyter notebook and pandas.

# Collecting Data 

1. Data from "new_full_student_data.csv" file is imported into DatafRame "student_df" using pandas function -"read_csv" and the "os module".
2. Confirming the Pandas has correctly imported data using the "head" function.
![Screen Shot 2022-09-17 at 11 51 14 PM](https://user-images.githubusercontent.com/110873947/190887849-0e59f76c-219d-4969-83f7-106a7cadfeba.png)

# Preparing the Data 

1. In the student DataFrame, check for rows that have NaN (or missing) values, and remove those rows, as the following image shows:
![Screen Shot 2022-09-17 at 11 52 24 PM](https://user-images.githubusercontent.com/110873947/190887884-9272680c-e80d-47b3-9ec0-218130d4a517.png)
<img width="171" alt="Screen Shot 2022-09-17 at 11 53 53 PM" src="https://user-images.githubusercontent.com/110873947/190887919-def1bfd5-2877-41df-bb56-fc7a2a0b49e6.png">

2. Next step in the student DataFrame is to check for duplicate rows, and remove them.
<img width="378" alt="Screen Shot 2022-09-17 at 11 55 37 PM" src="https://user-images.githubusercontent.com/110873947/190887967-45ab09a9-d3e6-4dc2-b3e3-ecf7ad0d089e.png"

3. Next is to check for data types of the columns by using the dtypes property, as the following image shows:
<img width="231" alt="Screen Shot 2022-09-17 at 11 56 39 PM" src="https://user-images.githubusercontent.com/110873947/190888006-e9b4daba-84a0-4241-8882-dbe5a6e84e93.png">

4. Now in the grade column, remove the "th" suffix from every value by using str and replace. Then convert grade to the int type as the following image shows:
<img width="570" alt="Screen Shot 2022-09-18 at 12 00 28 AM" src="https://user-images.githubusercontent.com/110873947/190888098-ddf4f4fa-6263-4afc-b6d7-29f8938b6c8e.png">

# Summarizing the Data

1. Generate the summary statistics for each DataFrame by using the describe function.
<img width="511" alt="Screen Shot 2022-09-18 at 12 03 25 AM" src="https://user-images.githubusercontent.com/110873947/190888154-fc76d9d5-7067-459a-bd6a-046c45ec196a.png">

2. Display the mean math score using the mean function.
<img width="470" alt="Screen Shot 2022-09-18 at 12 03 50 AM" src="https://user-images.githubusercontent.com/110873947/190888164-d4332bc3-2568-4f2d-8fad-f169be794999.png">

3. Store the minimum reading score as min_reading_score.
<img width="513" alt="Screen Shot 2022-09-18 at 12 04 12 AM" src="https://user-images.githubusercontent.com/110873947/190888177-77becce3-e126-4a7f-b843-6635f9659557.png">

# Data Analysis

1. Use loc to display the grade column.
<img width="379" alt="Screen Shot 2022-09-18 at 12 06 41 AM" src="https://user-images.githubusercontent.com/110873947/190888259-d8109811-c568-4d16-8519-4fa11cd3011d.png">

2. Use iloc to display the first 3 rows and columns 3, 4, and 5.
<img width="574" alt="Screen Shot 2022-09-18 at 12 07 02 AM" src="https://user-images.githubusercontent.com/110873947/190888272-c015d301-0fa7-43bc-ae61-59d5229dc359.png">

3. Show the rows for grade nine using loc.
<img width="474" alt="Screen Shot 2022-09-18 at 12 07 25 AM" src="https://user-images.githubusercontent.com/110873947/190888285-6b1b175b-74bb-48e1-9244-858087e0f367.png">

4. Store the row with the minimum overall reading score as min_reading_row using loc and the min_reading_score found in Deliverable 3.
<img width="753" alt="Screen Shot 2022-09-18 at 12 07 42 AM" src="https://user-images.githubusercontent.com/110873947/190888298-92c2e544-c8a0-42ab-9fbd-f135ab45210f.png">

5. Find the reading scores for the school "Dixon High SChool" and grade "10th" from the output of step three using loc with multiple conditional statements.
<img width="273" alt="Screen Shot 2022-09-18 at 12 08 47 AM" src="https://user-images.githubusercontent.com/110873947/190888328-f7e5f13f-fbc7-479d-bb7a-0be65e286b95.png">

6. Using conditional statements and loc or iloc, find the mean reading score for all students in grades 11 and 12 combined.
<img width="802" alt="Screen Shot 2022-09-18 at 12 09 14 AM" src="https://user-images.githubusercontent.com/110873947/190888344-c252772d-c1ee-42c0-9fc3-2e60fdff9a93.png">

# Data Comparison between Public and Charter Schools
Comparing public vs charter schools for budget, size, and scores. For this compariosn with our data following steps are taken -

1. Using the groupby and mean functions, look at the average reading and math scores per school type.
<img width="263" alt="Screen Shot 2022-09-18 at 12 11 08 AM" src="https://user-images.githubusercontent.com/110873947/190888400-11ccd85f-0075-4fe3-ac67-bb7d394880b4.png">

2. Using the groupby and count functions, find the total number of students at each school.
<img width="287" alt="Screen Shot 2022-09-18 at 12 11 39 AM" src="https://user-images.githubusercontent.com/110873947/190888416-5fe03de6-4394-4d6d-b042-e8a80778b4c0.png">

3. Using the groupby and mean functions, find the average budget per grade for each school type.
<img width="204" alt="Screen Shot 2022-09-18 at 12 12 00 AM" src="https://user-images.githubusercontent.com/110873947/190888424-3cc1fa60-c223-4268-9069-5ab689a75767.png">
<img width="236" alt="Screen Shot 2022-09-18 at 12 12 23 AM" src="https://user-images.githubusercontent.com/110873947/190888442-9ac7ce28-c031-477d-b49b-efd67d3e55f7.png">

# Challenges and Difficulties Encountered
None

# Results

reading_score had 1968 rows with null data whereas null data in  math_score was 982.

1836 rows with duplicate values.

Minimum reading score is a student in Dixon High school named -Mathew Thomas with 10.5 score.

Average budget for Public school is higher than Chartered schools.

Highest number of students are in "Montgomery High School" and least are in "Chang High SChool".

Average math score in charter schools are higher in Grades -9th, 10th and 11th whereas Grade 12th in Public SChool has higher average.


