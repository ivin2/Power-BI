# HR Analytics - Dashboard



## Problem Statement

The HR managers may better understand their employees with the use of this dashboard. It helps the airlines determine whether or not their employees are working, what amenities to offer based on employee needs, and whether or not there is wage inequality. They identify their areas for improvement through various analyses, enabling them to provide their employees facilities or training. They will be able to track employee records with its assistance.



Given that there are about five times as many female workers as male workers (around 45%), there should be greater resources available for hygienic conditions, safety, and security, as well as wellness initiatives.
Furthermore, given that some employees have leave balances greater than 20 days, it indicates that they may be overworked and should be encouraged to take a break.




### Steps followed 

- Step 1 : Load data into Power BI Desktop, dataset is a csv file.
- Step 2 : Open power query editor & in view tab under Data preview section, check "column salary", "column age" & "column leave balance".
-Step 3 : Changed the data type to currency from text for column "salary", text to whole number for column "age" and "leave balance".
- Step 4 : It was observed that in none of the columns had errors or empty values were present.
- Step 5 : We created two more columns for age bins and initials for colummn "Name". 

![power_query_changes](https://github.com/user-attachments/assets/913c4342-a3ea-43f7-9c42-6a5381aa9c58)

- Step 6 : We had to make a background for the report in the report view, filling it with a gradient colour before exporting the PowerPoint slide.
- Step 7 : We created various measures like avg. salary, cummulative headcounts, headcount, avg. leave balance and so on. Following are the measures :-

  Avg. Salary = AVERAGE(Staff[Salary])

  Average Leave Balance = AVERAGE(Staff[Leave Balance])

  Headcount = COUNTROWS(Staff)
  
  Cummulative Headcount = 
    VAR currentdate = LASTDATE(Staff[Date of Join])
    RETURN
    CALCULATE([Headcount],ALL(Staff[Date of Join]),Staff[Date of Join]<= currentdate)

LB over 20 = CALCULATE([Headcount], Staff[Leave Balance]>20)
    

- Step 8 : We had to make a separate table for educational qualification, giving each one a unique ID, in order to generate a scatter plot to see whether there is any relationship between salary and qualification.
![Scatter_plot](https://github.com/user-attachments/assets/fa11d34f-712c-409c-8d48-ff17793cc3af)

- Step 9 : Created four card visuals which gives headcounts of the staff, avgerage salary, average leave balance and no. of employee who has leave balance over 20 days.
![screenshot_card](https://github.com/user-attachments/assets/d5de1249-1635-4811-9d80-e522bff428e3)


- Step 10 : A bar chart  and pie chart was added to the report design area representing the number of employees at different position which also act as an filterfor the report.

![Bar_graph](https://github.com/user-attachments/assets/4135f30f-a99d-4fa0-bd4f-0a62754fb2c3)

- Step 11 : To better comprehend the age ranges of the employees, we built a funnel chart.
- Step 12 : We also added a line grapgh to understand no. of people we employed each year. It required a measure which tells cummulative headcount. Here is the snapshot of the measure


- Step 13 : In order to get employee details, we created an extra report in the report view. We first created a slicer for initials so that HR could filter based on them. We also kept the same bar graph from the initial report in case HR needed information specific to the job title. 

![Slicer](https://github.com/user-attachments/assets/3cac5b46-5446-4aea-92f3-fded6f944b72)

- Step 14 : Two tables were made by us. If job title or initials are used as filters, one shows the top three earners' details. The employee's name, job title, gender, date of hire, remaining leave balance, educational background, and compensation are all listed in the second table.

        
- Step 15 : Additionally, we produced a chart that illustrates the major factors influencing an employee's pay and demonstrates the significance of the job title in determining pay.

![Key_influencers](https://github.com/user-attachments/assets/974c34f0-6e27-4135-a421-e945500804cc)
        
 - Step 16 : We created two text boxes in every report that list the names of the dashboard and the report.

 - Step 17 : The "overview" and "Staff details" buttons that we recently added will allow you to switch between the two reports.

 
 # Report Snapshot (Power BI DESKTOP)

 
![Dashboard_Overview](https://github.com/user-attachments/assets/727725ec-e1fc-4c77-be12-3eb434c9c33a)

![Dashboard_Staff_details](https://github.com/user-attachments/assets/101bc783-3c33-4452-b933-79d71290ac48)

# Insights

A two page report was created on Power BI Desktop 

Following inferences can be drawn from the dashboard;

### [1] Young staff

Total number of staff = 161

Approximately 140 individuals, or 87.5% of the entire population, are between the ages of 20 and 35, indicating that our population is youthful and industrious. 
It implies that, with the right motivation, we may accomplish large goals quickly.

           
### [2] Most of our staff are females
Male employees make up 45% of our workforce, while female employees make up 55%. This indicates to us that the organisation values gender diversity and inclusivity. 

When it comes to gender equity, the organisation may be seen more favourably, which can draw top talent and devoted clients.

It should be mentioned that the organisation has to improve hygienic conditions, safety policies, and professional development opportunities.

  
  ### [3] Salary VS Qualification VS Job title 
  
  We may conclude that job title has a greater influence on compensation after examining the scatter plot and important influencers. There are workers that earn great salaries despite possessing only a diploma. The three highest-paying job categories are research scientist, marketing manager, and product manager.
  According to the key influencer chart, the average salary of a product manager increases by $31,750, while that of a research scientist increases by $25,730 and that of a marketing manager by $20,580.

 ### [4] Qualification
 
 The top three earners in the company hold master's degrees, thus a higher qualification can help a person advance in their career more quickly and receive more rewards.
 
 ### [5] Recruiting 

We were able to identify the organization's HR recruiting module with the use of line graphs. It is evident that, starting in 2018, they will continue to hire about 30 workers annually through 2022. We hired about twenty workers in 2023.

Additionally, there appears to be a small increase from October to December, suggesting that this is when they hire the majority of their staff.



         
