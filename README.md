# Data Portfolio: Employee Payroll Dashboard

![Project-Main-Image](Assets/Payroll%20Dashboard%20Main%20Image.jpg)

## Objective
This report presents a comprehensive analysis of the company's 2024 payroll data. By examining compensation structures, departmental trends, and payment methods, we aim to identify opportunities to optimize payroll processes, improve compensation equity, and reduce operational costs.

## Executive Summary
This Employee Payroll Dashboard provides a robust analytical framework for understanding the company's 2024 payroll landscape. Our analysis reveals a **strong upward trend in total basic salary and net pay, with respective month-over-month growth. This consistent growth, particularly notable with an **18% basic salary increase in April and a 10% increase in February**, signals a healthy expansion of the workforce or adjustments in compensation structures. However, **deductions exhibited significant volatility, with a striking 62% increase in October and a 34% decrease in September**, warranting further investigation into their drivers, such as tax changes or new benefit enrollments.

Departmentally, **Marketing consistently accounts for the highest share of basic salary ($3.57M total), net pay ($3.81M total), and total employees (56)**, indicative of its substantial workforce or higher compensation scales. Conversely, the **IT department, while smaller in headcount (26), shows efficient resource allocation with proportionally lower basic salary (\$1.62M) and net pay (\$1.73M) expenditures**.

A critical finding in our payment method analysis is the **strategic shift in May towards incorporating Cash payments, which now represent 22.7% of total net pay**. This diversification from solely Bank Transfer and Mobile Money indicates an adaptation to employee preferences or a response to operational needs.

To optimize payroll management and enhance employee satisfaction, we recommend a **detailed audit of deduction variances to stabilize payroll outflow, potentially reducing deduction-related fluctuations by 15-20%**. Furthermore, implementing a **performance-based incentive program, particularly leveraging insights from top earners like Angela Phillips**, could drive overall productivity, potentially **boosting total net pay by an additional 3-5%** over the next fiscal year. By proactively managing deductions and strategically aligning compensation with performance, the company can enhance financial predictability and bolster employee engagement.

## Methodology
### Data Sources
The primary data source for this analysis is a payroll dataset for the year 2024, comprising 2,400 rows and 14 columns. Key columns include:

* PayrollID
* EmployeeID
* FullName
* Department: (Marketing, HR, Finance, Sales, IT).
* JobTitle
* PayDate
* EmploymentType (Internship, Part-time, Full-time).
* BasicSalary
* Allowances
* Deductions
* GrossPay
* NetPay
* PaymentMethod(Bank Transfer, Mobile Money, Cash).
* BankName

Each row in the dataset represents a payroll transaction for an individual.

![Data Source](Assets/Payroll%20Dashboard%20-%20Data%20Source.png)

### Tools Used
The following tools were utilized for data familiarization, analysis, and visualization:

* **Microsoft Excel** – Initial data familiarization, quick checks for data integrity.
* **Microsoft Power BI** – Data loading, transformation, DAX formula creation for custom measures, data aggregation, segmentation, and interactive dashboard development.

### Data Cleaning and Preparation
The dataset was loaded directly into Power BI. Key preparation steps included:

* **Data Type Conversion**: Used Power Query to ensure all columns were assigned appropriate data types (e.g., PayDate as Date, financial metrics as Currency, IDs as Whole Number, and categorical columns as Text).
* **Calendar Table Creation**: A dedicated calendar table was generated using DAX expressions to provide robust time intelligence capabilities. This table included Year, Month, Month Number, and Start of Month columns, with its Min and Max dates set to the Min and Max PayDate value of the salary dataset.

![DAX-Code](Assets/Payroll%20Dashboard%20-%20Calendar%20Table.png)

* **Relationship Management**: The newly created calendar table was linked to the main salary data table via the PayDate column (in the salary data) and the Date column (in the calendar table), establishing a one-to-many relationship for effective filtering and aggregation across time.

![Relational-Table](Assets/Payroll%20Dashboard%20-%20Relational%20Table.png)

* **Measures Table Initialization**: An empty table was created to house all calculated measures, ensuring a clean and organized Power BI data model.

### Data Exploration
Initial data exploration involved familiarizing with the structure and content of the payroll dataset in Excel. This included reviewing the range of PayDate values, understanding the distribution of EmploymentType and Department, and observing the magnitude of BasicSalary, Allowances, Deductions, and NetPay.

### Data Analysis Techniques
The following data analysis techniques were employed in Power BI:

* **Descriptive Analytics**: Created measures to calculate key performance indicators (KPIs) such as total basic salary, total allowances, total deductions, and total net pay. This provided a foundational understanding of the overall payroll expenditure for 2024.
* **Time Intelligence Analysis**: Utilized DAX measures to calculate month-over-month growth rates for basic salary, allowances, deductions, and net pay. This enabled the identification of trends, seasonal patterns, and significant fluctuations over the year.

![Basic-Salary-MoM-DAX](Assets/Payroll%20Dashboard%20-%20Basic%20Salary%20MoM.png)

![Allowances-MoM-DAX](Assets/Payroll%20Dashboard%20-%20Allowances%20MoM.png)

![Deductions-MoM-DAX](Assets/Payroll%20Dashboard%20-%20Deductions%20MoM.png)

![Net-Pay-MoM-DAX](Assets/Payroll%20Dashboard%20-%20Net%20SPay%20MoM.png)

* **Comparative Analysis**: Segmented financial metrics by Department to compare payroll costs and compensation structures across different organizational units and employee categories.
* **Top 5 Analysis**: Implemented a field parameter to dynamically identify and visualize the top 5 employees based on selected financial metrics (Basic Salary, Allowances, Deductions, Net Pay), facilitating targeted performance recognition.

![Top-5](Assets/Payroll%20Dashboard%20-%20Top%205%20Employees.png)

* **Forecasting**: Integrated Power BI's built-in forecasting capabilities on line charts to predict future trends for key payroll metrics, offering a forward-looking perspective for financial planning.

![KPI-Forecasting](Assets/Payroll%20Dashboard%20-%20KPI%20Forecasting.png)

## Future Considerations for Data Analysis
To further enhance the insights derived from this payroll dashboard, future analyses could explore:

* **Predictive Modeling**: Implement advanced analytics to forecast future payroll expenses more accurately, considering factors like projected hiring, salary hike increments, and changes in benefit plans. This could involve leveraging machine learning models to predict employee turnover and its impact on payroll.
* **Cost-Benefit Analysis of Allowances/Deductions**: Deep dive into the specific components of allowances and deductions to evaluate their impact on employee satisfaction and company costs. This could lead to optimizing benefits packages.
* **Correlation Analysis**: Investigate correlations between payroll metrics and other HR data points, such as employee performance ratings, tenure, or training hours, to identify relationships that could inform compensation strategies.
* **What-if Scenarios**: Develop interactive "what-if" scenarios within the dashboard to model the impact of various HR and compensation policy changes (e.g., a 5% salary increase, new bonus structures) on the overall payroll budget.

## Analysis of Payroll Performance
### Key Financial Metrics Overview
The total basic salary for 2024 stands at **\$12,833,314**, with total allowances at **\$1,618,928**, and total deductions at **\$736,063**, culminating in a total net pay of **\$13,716,179**. These figures represent the comprehensive financial outlay for employee compensation throughout the year.

![Total-KPIs](Assets/Payroll%20Dashboard%20-%20Overall.png)

### Monthly Trends and Growth Analysis

**Basic Salary Trends:**
Basic salary demonstrated a robust upward trajectory throughout 2024.
* **Strong Growth Phases**: Notable month-over-month (MoM) increases were observed in **February (+10%)**, **April (+18%)**, **June (+8%)**, **September (+4%)**, and **December (+7%)**. The **18% surge in April** is particularly significant, indicating a potential company-wide salary adjustment.

![April-MoM-1](Assets/Payroll%20Dashboard%20-%20April%20MoM%20Growth.png)

* **Plateau Periods**: Basic salary remained stable in March, May, July, August, and October, suggesting periods of consistent payroll without major adjustments.
* **Overall Annual Growth**: From January (\$802,141) to December (\$1,283,347), the total basic salary saw a significant **60% increase**, reflecting substantial growth in the company's compensation structure over the year.

![January-Basic-Salary](Assets/Payroll%20Dashboard%20-%20January%20Basic%20Salary.png)

![December-Basic-Salary](Assets/Payroll%20Dashboard%20-%20December%20Basic%20Salary.png)

**Allowances Trends:**
Allowances largely mirrored the basic salary growth, indicating a proportional increase with base compensation.
* **Consistent Increases**: Allowances also experienced a **10% increase in February**, an **18% increase in April**, an **8% increase in June**, a **4% increase in September**, and a **7% increase in December**. This synchronized growth suggests that allowances are often tied directly to basic salary or overall compensation policy.

![February-Allowances-MoM](Assets/Payroll%20Dashboard%20-%20February%20Allowances%20MoM%20Growth.png)

![April-Allowances-MoM](Assets/Payroll%20Dashboard%20-%20April%20Allowances%20MoM%20Growth.png)

* **Mirroring Plateaus**: Similar to basic salary, allowances also flattened out in March, May, July, August, and October.
* **Overall Annual Growth**: Total allowances grew from \$101,238 in January to \$161,907 in December, an impressive **60% increase** mirroring the basic salary's upward trend.

![January-Allowances](Assets/Payroll%20Dashboard%20-%20January%20Allowances.png)

![December-Allowances](Assets/Payroll%20Dashboard%20-%20December%20Allowances.png)

**Deductions Volatility:**
Deductions exhibited significant and often unpredictable month-over-month fluctuations.
* **Spikes and Drops**:
    * A remarkable **50% increase in February** (\$23,766 to \$35,650) suggests a new deduction type or a one-time adjustment.
 
* ![February-Deductions-MoM](Assets/Payroll%20Dashboard%20-%20February%20Deductions%20MoM%20Growth.png)

    * This was followed by a sharp **34% increase in March** (\$35,650 to \$47,639), indicating a further escalation or new persistent deductions.
 
* ![March-Deductions-MoM](Assets/Payroll%20Dashboard%20-%20March%20Deductions%20MoM%20Growth.png)

    * Another substantial **56% increase in June** (\$52,320 to \$81,626) and a **62% increase in October** (\$49,928 to \$80,895) stand out as major outliers, requiring granular investigation to identify the root causes, such as changes in tax withholding, benefits enrollment, or loan repayments.
 
* ![June-Deductions-MoM](Assets/Payroll%20Dashboard%20-%20June%20Deductions%20MoM%20Growth.png)

* ![October-Deductions-MoM](Assets/Payroll%20Dashboard%20-%20October%20Deductions%20MoM%20Growth.png)

* **Impact**: These volatile deduction patterns introduce unpredictability in net pay and warrant a deeper dive by the finance department to understand and potentially stabilize these outflows.

**Net Pay Trends:**
Net pay generally followed the positive trend of basic salary and allowances, albeit with some minor dips influenced by deduction spikes.
* **Consistent Growth**: Major MoM increases in net pay were observed in **February (+9%)**, **April (+19%)**, **June (+5%)**, **July (+2%)**, **September (+6%)**, and **December (+7%)**. The **19% increase in April** aligns with the basic salary surge, demonstrating the direct impact of compensation adjustments on take-home pay.
* **Minor Fluctuations**: Small decreases were noted in March (-1%), May (<1%), and August (-1%), primarily attributable to the corresponding increases in deductions during those periods.
* **Overall Annual Growth**: Net pay significantly increased from \$879,613 in January to \$1,357,215 in December, representing a **~54% annual growth**, reflecting the overall expansion of the company's payroll.

### Employee Distribution and Demographics
The company employs a total of **200 individuals**, with a diverse workforce distribution:
* **Internship**: 79 employees (39.5%)
* **Part-time**: 64 employees (32%)
* **Full-time**: 57 employees (28.5%)

This significant proportion of interns and part-time employees (collectively 71.5%) suggests a flexible workforce model, potentially optimized for project-based work.

![Employee-Numbers](Assets/Payroll%20Dashboard%20-%20Employee%20Numbers%20by%20Employment%20Type.png)

**Employee Count by Department and Employment Type:**
* **Marketing Department**: Exhibits a balanced distribution across employment types, with 20 Full-time, 20 Internship, and 20 Part-time employees, suggesting a robust and adaptable team structure.
* **HR Department**: Shows a healthy mix, with a notable presence of interns (17) and part-time employees (16) alongside full-time staff (14), possibly indicating a need for flexible support in administrative functions.
* **Finance Department**: Features a higher concentration of interns (19) compared to full-time (11) and part-time (11) roles, which might suggest a focus on talent development or project-based financial tasks.
* **Sales Department**: Has a lower number of full-time employees (5) but a significant number of interns (14) and part-time staff (11), reflecting a potentially commission-based or seasonal workforce model.
* **IT Department**: Has the smallest overall headcount, with a somewhat balanced distribution (7 Full-time, 9 Internship, 10 Part-time), indicating a more specialized and streamlined team.

![Employees-Numbers-By-Department-&-Employment-Type](Assets/Payroll%20Dashboard%20-%20Employee%20Numbers%20by%20Department.png)

### Departmental Payroll Analysis
* **Marketing Department**: Consistently leads in total basic salary (\$3,575,209) and net pay (\$3,810,816) for the year. This could be due to a larger headcount or higher average salaries within the Marketing function, potentially reflecting strategic investment in talent management.
* **HR Department**: Ranks second in total basic salary (\$3,116,481) and net pay (\$3,337,808), demonstrating a substantial investment in HR talent and operations.
* **IT Department**: Exhibits the lowest total basic salary (\$1,623,471) and net pay (\$1,725,555), suggesting a more streamlined team or potentially outsourced functions.

![KPIs-By-Department](Assets/Payroll%20Dashboard%20-%20KPIs%20By%20Department.png)

### Payment Method Distribution
* **Bank Transfer**: Dominates payment methods, accounting for **46.6% (\$6,393,292)** of total net pay.
* **Mobile Money**: Accounts for **30.7% (\$4,210,027)**, indicating its significant adoption.
* **Cash**: Introduced in May, quickly grew to represent **22.7% (\$3,112,860)** of total net pay by year-end, highlighting a strategic shift in payment disbursement. The transition from solely Bank Transfer and Mobile Money in earlier months to incorporating Cash in May and subsequent months suggests a strategic move to accommodate employee preferences or operational efficiencies. This rapid adoption indicates a need to monitor its associated administrative costs and security implications closely.

![Payment-Method-Legend](Assets/Payroll%20Dashboard%20-%20Payment%20Method%20By%20Employment%20Type%20Legend.png)

![Payment-Method-Breakdown](Assets/Payroll%20Dashboard%20-%20Payment%20Method%20By%20Breakdown.png)

**Monthly Net Pay by Payment Method Per Employment Type:**
The breakdown by payment method and employment type reveals interesting patterns:
* **Interns**: In the later half of the year (June-December), interns received a substantial portion of their net pay via Cash, particularly in December (\$218,067), suggesting a preference or operational necessity for this demographic.
* **Part-time Employees**: Consistently rely more on Bank Transfer and Mobile Money, with Cash payments being less prevalent for this group compared to interns, though still significant from June onwards.
* **Full-time Employees**: Exhibit a mixed payment preference, with a balanced distribution across Bank Transfer, Mobile Money, and Cash from June to December, indicating a diverse set of needs or accessibility.

![Net-Pay-Payment-Method-By-Employment-Type-(June---December)](Assets/Payroll%20Dashboard%20-%20Payment%20Method%20By%20Employment%20Type.png)

### Top 5 Employee Compensation Analysis
**Angela Phillips** consistently ranks as the top earner across basic salary, allowances, and net pay throughout the year, accumulating a total basic salary of **\$79,900**, allowances of **\$9,851**, and net pay of **\$88,052**. This consistent leadership positions her as a key contributor to the company and potentially a benchmark for compensation.

![Top-5-Employees-By-Net-Pay](Assets/Payroll%20Dashboard%20-%20Top%205%20Employees%20Net%20Pay.png)

**Amber Taylor** consistently features as the number 1 employee for deductions, with a total of **\$4,807**. This outlier status warrants a deeper investigation into the specific reasons for her higher deductions, which could range from high tax brackets, specific benefit enrollments, or perhaps loan repayments. Understanding this could provide insights into general employee financial behaviour or specific policy impacts.

![Top-5-Employees-By-Deductions](Assets/Payroll%20Dashboard%20-%20Top%205%20Employees%20Deductions.png)

## Recommendations
Based on the comprehensive analysis of the 2024 payroll data, the following strategic recommendations are proposed to optimize financial management, enhance employee satisfaction, and support strategic decision-making:

* **Investigate and Stabilize Deduction Volatility**: The erratic fluctuations in monthly deductions, particularly the **50% increase in February** and **56% increase in June**, present a significant area for financial review. A granular audit of these spikes is critical to identify underlying causes, such as changes in tax regulations, new benefit enrollments, or specific one-time deductions (e.g., loan repayments). By understanding and proactively managing these drivers, the company can achieve greater predictability in net pay outflows, potentially **reducing deduction-related month-over-month variances by 15-20%** and leading to more stable financial forecasting.

* **Optimize Payment Method Strategy**: The rapid adoption of Cash payments, now accounting for **22.7% of total net pay after its introduction in May**, indicates a strong employee preference or an effective operational adaptation. While offering flexibility, it's crucial to assess the administrative overhead and security implications associated with cash disbursements. Conduct a cost-benefit analysis of each payment method to identify the most efficient and secure channels. Exploring digital alternatives that offer similar convenience to mobile money while providing robust security could further **reduce administrative costs associated with physical cash handling by 5-8%**.

* **Strategic Workforce Planning by Department**: The significant variance in total basic salary and net pay across departments (e.g., Marketing's leading expenditure vs. IT's leaner structure) suggests diverse operational needs. Leverage these departmental insights to refine workforce planning. For departments with high payroll costs (e.g., Marketing, HR), consider optimizing headcount or reviewing compensation benchmarks. For departments with lower costs but potentially high impact (e.g., IT), evaluate opportunities for strategic investment in talent acquisition or upskilling to enhance capabilities, potentially **boosting IT department productivity and project delivery by 10%** with a targeted investment.

* **Leverage Top Earner Insights for Compensation Strategy**: The consistent presence of individuals like Angela Phillips among the top earners provides a valuable benchmark. Analyze the roles, responsibilities, and performance metrics of these top earners to inform overall compensation strategies. Consider implementing a performance-based incentive program that aligns with company objectives, potentially **increasing overall employee productivity and total net pay growth by an additional 3-5%** over the next fiscal year by recognizing and rewarding high performance. This could involve linking a portion of variable pay to key departmental or individual performance indicators.

* **Refine Forecasting Accuracy**: The current 2-month forecasting provides a baseline. To enhance financial foresight, incorporate additional variables into the forecasting model, such as projected hiring plans, anticipated salary adjustments, and historical seasonality of payroll expenses. This proactive approach can improve budgetary accuracy, potentially **reducing budget variances by 5-7%** and allowing for more agile financial resource allocation.

## Potential Impact of Recommendations
By implementing these recommendations, the company can anticipate the following positive outcomes:

* **Enhanced Financial Predictability**: Stabilizing deduction variances and refining forecasting accuracy will lead to more reliable financial planning and budgeting, enabling better resource allocation.
* **Improved Operational Efficiency**: Optimizing payment methods will streamline payroll processes, potentially reducing administrative costs and operational risks.
* **Strategic Workforce Optimization**: Departmental payroll insights will enable more informed decisions regarding headcount, compensation structures, and talent investment, leading to a more efficient and productive workforce.
* **Increased Employee Engagement and Retention**: A clear and fair compensation strategy, informed by top earner analysis and potentially incorporating performance-based incentives, can boost employee morale, satisfaction, and retention.

## Limitations and Future Considerations
While this payroll dashboard provides valuable insights, it's important to acknowledge certain limitations and areas for future development:

* **Data Granularity**: The current dataset provides a high-level overview of payroll components. Access to more granular data, such as specific deduction types (e.g., tax, insurance, loans) and allowance categories (e.g., housing, transport), would allow for a more detailed analysis of cost drivers and policy impacts.
* **Absence of Performance Data**: The current analysis does not incorporate employee performance metrics. Integrating performance data would enable a deeper understanding of the relationship between compensation and productivity, allowing for more impactful compensation strategy recommendations.
* **Causation vs. Correlation**: While trends and patterns have been identified, the analysis primarily focuses on correlation. Establishing causal relationships (e.g., why deductions spiked in certain months) would require additional data and in-depth qualitative analysis.
* **External Economic Factors**: The analysis does not account for external economic factors (e.g., inflation, economic downturns) that could influence salary adjustments or employee financial behaviour. Future analyses could integrate such external data for a more holistic view.

## Key Takeaways
This analysis provides crucial insights into the company's 2024 payroll landscape:

* **Consistent Payroll Growth**: The company experienced significant month-over-month growth in basic salary and net pay, indicating compensation adjustments.
* **Deduction Volatility is a Key Concern**: Unpredictable spikes in deductions warrant immediate investigation to ensure financial stability and transparency.
* **Diverse Workforce Model**: The high proportion of interns and part-time employees highlights a flexible staffing strategy.
* **Strategic Shift in Payment Methods**: The rapid adoption of cash payments in the latter half of the year signals a deliberate change in disbursement strategy.
* **Departmental Expenditure Varies Significantly**: Marketing & HR lead in payroll expenditure, while IT maintains a leaner cost structure.
* **Top Earners Provide Compensation Benchmarks**: Consistent top performers like Angela Phillips offer valuable insights for compensation review and incentive program design.

By leveraging these insights, the company can make data-driven decisions to optimize payroll management, foster financial health, and enhance employee satisfaction.
