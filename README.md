# PoweBi-2024-job-analusis

### Dashboard Link : https://app.powerbi.com/groups/me/reports/384d017e-e935-44dc-9e7d-1626c1a36de1/ReportSection

## Problem Statement

This dashboard helps organizations understand their workforce better. It helps employers know if their employees are satisfied with their jobs and workplace conditions. Through various ratings, they can identify areas for improvement and enhance their employee satisfaction by addressing these specific concerns. The dashboard also provides insights into factors such as job satisfaction, turnover rates, and average work hours, allowing companies to take action on issues that may contribute to employee dissatisfaction or burnout.

Since the number of neutral/dissatisfied employees (almost 57%) is higher than the satisfied employees (around 43%), it is clear that employers need to focus on improving workplace conditions and overall employee engagement.

Additionally, with average work hours exceeding desired limits by about 15 minutes, companies should consider measures to optimize work-life balance and reduce unnecessary workload


### Steps followed 

- Step 1 : Load data into Power BI Desktop, dataset is a csv file.
- Step 2 : Open power query editor & in view tab under Data preview section, check "column distribution", "column quality" & "column profile" options.
- Step 3 : Also since by default, profile will be opened only for 1000 rows so you need to select "column profiling based on entire dataset".
- Step 4 : It was observed that in none of the columns errors & empty values were present except column named "charges".
- Step 5 : For calculating average salary, null values were not taken into account as only less than 1% values are null in this column(i.e column named "charges") 
- Step 6 : In the report view, under the view tab, theme was selected.
- Step 7 : Since the data contains various ratings, thus in order to represent ratings, a new visual was added using the three ellipses in the visualizations pane in report view. 
- Step 8 : Visual filters (Slicers) were added for four fields named "Id", "Job Type", "Location" & "Average salary".
- Step 9 : Two card visuals were added to the canvas, one representing average departure delay in minutes & other representing average arrival delay in minutes.
           Using visual level filter from the filters pane, basic filtering was used & null values were unselected for consideration into average calculation.
           
           Although, by default, while calculating average, blank values are ignored.
- Step 10 : A bar chart was also added to the report design area representing the number of satisfied & neutral/unsatisfied customers. While creating this visual, field named "Gender" was also added to the Legends bucket, thus number of customers are also seggregated according the gender. 
- Step 11 : Ratings Visual was used to represent different ratings mentioned below,

  (a) Country

  (b) Average Salary According to Job Titles
  
  (c) count on Syurvey Takers
  
  (d) Average Salary of Survey Takers
  
  (e) Life Salary
  
  (f) HappyWork/Life Blanace

  (g) Favotite Programming Language

  (h) Average Salary of Male and Female
  
In our dataset, Some parameters were assigned value 0, representing those parameters are not applicable for some customers.

All these values have been ignored while calculating average rating for each of the parameters mentioned above.

- Step 12 : In the report view, under the insert tab, two text boxes were added to the canvas, in one of them name of the airlines was mentioned & in the other one company's tagline was written.
- Step 13 : In the report view, under the insert tab, using shapes option from elements group a rectangle was inserted & similarly using image option company's logo was added to the report design area. 
- Step 14 : Calculated column was created in which, customers were grouped into various age groups.

for creating new column following DAX expression was written;
       
        AVerage salary = 
        
        ((Current Yearly Salary)+(Current Yearly Salary Max))/2
        
Snap of new calculated column ,

![Snap_1](https://github.com/user-attachments/assets/3cb61e39-3c53-4624-9de2-2a24f21352ec)

        
- Step 15 : New measure was created to find total count of customers.

Following DAX expression was written for the same,
        
        Count of Customers = COUNT(unique_id[ID])
        
A card visual was used to represent count of customers.

![Snap_Count](https://github.com/user-attachments/assets/0b7a389e-8c09-4eb4-b7a9-418d0ad23c57)

        
 - Step 16 : New measure was created to find  Average Age,
 
 Following DAX expression was written to find  Average Age,
 
         Averge Age = (Average(age))
 
 A card visual was used to represent this  Average Age.
 
 
 ![Snap_Percentage](https://github.com/user-attachments/assets/3b80cbe0-8ac8-43bc-9e0c-1377ab827294)


 
 - Step 18 : The report was then published to Power BI Service.
 

# Snapshot of Dashboard (Power BI Service)

![dashboard_snapo](https://github.com/user-attachments/assets/fda4553e-567f-432d-8f48-d66361d727f0)

 
 
