#### *Personal Project: December 2023*

<p align="center">
<img src="https://github.com/jvenncpe/2023.12_Case_Study_Analyzing_Customer_Churn_in_Power_BI/blob/main/Case%20Study%20Analyzing%20Customer%20Churn%20in%20Power%20BI.gif"/>
</p>

# Case Study: Analyzing Customer Churn in Power BI

For subscription-based businesses, mitigating customer churn stands as a paramount objective.

In this Power BI case study, our focus centers on scrutinizing a dataset from Databel, a telecom company, to comprehensively assess their churn rates. However, this study transcends mere numerical analysis; its core objective is to discern the reasons behind customer departures and strategize means to retain them.

Our goal isn't just to measure churn, but to understand its root causes. This deep dive will pave the way for targeted interventions, personalized experiences, and ultimately, happier, more loyal customers.


## Dataset Context

<p align="center">
<img src="https://github.com/jvenncpe/2023.12_Case_Study_Analyzing_Customer_Churn_in_Power_BI/assets/35190918/679c2c0b-986a-46bc-b27e-ae270b221645")/>
</p>

This dataset holds info on customers, like IDs, if they've churned (stopped using), account duration, call details, international usage, service plans, charges, demographics, and reasons for leaving. 

<p align="center">
<img src="https://github.com/jvenncpe/2023.12_Case_Study_Analyzing_Customer_Churn_in_Power_BI/assets/35190918/3092de67-ca76-47e2-82c0-765b9dab89a1")/>
</p>

---
## Methodology and Implementation 

- Loading and Transforming .csv to Power BI:
  - This step involves bringing in the data from a .csv file into Power BI, where we clean it up, organize it, and prepare it for analysis such as checking distinct values and format of each columns that are need for the analysis. Also, columns that are not needed were dropped to facilitate better response time at later queries.

<p align="center">
<img src="https://github.com/jvenncpe/2023.12_Case_Study_Analyzing_Customer_Churn_in_Power_BI/assets/35190918/e088b4ac-5474-4c49-8ac0-d36b13630e3e"/>
</p>

- DAX Modeling (FACT and DIMENSION tables) and Verfication of Relationships:

  - DAX Modeling is where we apply calculations and organize our data into FACT and DIMENSION tables. These tables form the backbone of our analysis, allowing us to make sense of complex relationships within the data. The fact tables are the measureable events in the data such as customer interactions and charges per customer ID. Meanwhile, the dimension tables store description attributes gender, location and type of account does the customer have. The goal is to establish and simplify the complex relationship of the columns to have a better understanding for data analysis.

<p align="center"><br><img src="https://github.com/jvenncpe/2023.12_Case_Study_Analyzing_Customer_Churn_in_Power_BI/assets/35190918/94a4005d-2620-4aa9-8ea9-d288f078fd40"/></p>

  - Afterwards, we are going to verify the relationship properties of each tables that were created as shown below:

<p align="center"><br><img src="https://github.com/jvenncpe/2023.12_Case_Study_Analyzing_Customer_Churn_in_Power_BI/assets/35190918/bc291a78-ee27-4e31-a015-e5191b2e31bc"/></p>


- Implementation of Measures:
  - Measures are like calculated fields that provide valuable insights. Here, we're creating metrics such as churn count (how many customers left), subscriber count (total users), and churn rates (percentage of customers leaving) across different segments.

<table align="center">
  <tr>
    <td width="33%" align="center">Measures (.shape)</td>
    <td width="33%" align="center">Formula Syntax</td>
    <td width="33%" align="center">Description (Remarks)</td>
  </tr>
  <tr>
    <td width="33%" align="center">Churn Count</td>
    <td width="33%" align="center"><p align="center"> <img src="https://github.com/jvenncpe/2023.12_Case_Study_Analyzing_Customer_Churn_in_Power_BI/assets/35190918/ea766066-adf4-416f-ba98-09c22cb31c38)"/></p></td>
    <td width="33%" align="center">Churned users means that the user unsubscribed with the services.</td>
    
  </tr>

  <tr>
    <td width="33%" align="center">User Count</td>
    <td width="33%" align="center"><p align="center"> <img src="https://github.com/jvenncpe/2023.12_Case_Study_Analyzing_Customer_Churn_in_Power_BI/assets/35190918/fe1210de-87cc-417a-a9ab-672168baaa3d"/></p></td>
    <td width="33%" align="center">User count is the number of overall customers (churned and unchurned). </td>
  </tr>

  <tr>
    <td width="33%" align="center">Churn Rate</td>
    <td width="33%" align="center"><p align="center"> <img src="https://github.com/jvenncpe/2023.12_Case_Study_Analyzing_Customer_Churn_in_Power_BI/assets/35190918/2fa66c96-c8ac-4f9d-8e8a-79c6d9c67117"/></p></td>
    <td width="33%" align="center">Churned users are computed using COUNTROWS and nested FILTER function where Churn Code is "NO", means that the user unsubscribed with the services.</td>
  </tr>
</table>

  - After making the measures, we nested them inside a folder to have them organized and easier access along with the fact and dimension tables we made as shown below in the data panel:
<p align="center"> <img src="https://github.com/jvenncpe/2023.12_Case_Study_Analyzing_Customer_Churn_in_Power_BI/assets/35190918/6dffa515-24f8-4d5e-afee-dda2500d2994"/></p>

- Tables and Visualizations:
  - This step involves creating different visual representations of the data using tables, graphs, and highlight cards. These visuals make it easier to understand and draw key insights from the information.

    - Tables & Visualizations:
        I haphazardly made initial visual presentation to have basic insights from the dataset in whihch helped me organize in making my low-fidelity design.

<p align="center"><br></p>
> Churn Demographics
<p align="center"> <img src="https://github.com/jvenncpe/2023.12_Case_Study_Analyzing_Customer_Churn_in_Power_BI/assets/35190918/a786f7c9-56ba-4b50-91cf-2b0fae41b450"/><br></p>

<p align="center"><br></p>
> Groups and Categories
<p align="center"> <img src="https://github.com/jvenncpe/2023.12_Case_Study_Analyzing_Customer_Churn_in_Power_BI/assets/35190918/f6e6c863-182a-42d9-a13c-e6eafb63945f"/><br></p>

<p align="center"><br></p>
> Contract Type
<p align="center"> <img src="https://github.com/jvenncpe/2023.12_Case_Study_Analyzing_Customer_Churn_in_Power_BI/assets/35190918/d54f9e69-d375-407b-ac3b-2fbfc7c96ca2"/><br></p>

<p align="center"><br></p>
> Age Groups
<p align="center"> <img src="https://github.com/jvenncpe/2023.12_Case_Study_Analyzing_Customer_Churn_in_Power_BI/assets/35190918/15988a7d-638b-4c75-ada1-20a3b66c6216"/><br></p>


<p align="center"><br></p>
<p align="center"><br></p>
- Low Fidelity Design:
  - Initially, I wanted to make a low fidelity design. However, since there are no board members or immediate supervisors that will have to check my design --- I opted to just make the backdrop and directly worked on Power BI visualization reporting.

<p align="center"><br></p>
  > I used powerpoint to make a backdrop and saved is as .svg to have the backdrop be properly scaled once used in Power BI dashboad.
<p align="center"> <img src="https://github.com/jvenncpe/2023.12_Case_Study_Analyzing_Customer_Churn_in_Power_BI/assets/35190918/60726403-6991-4c70-b30a-25ad5854ad9f"/><br></p>

<p align="center"><br></p>
  >The vertical panel line will serve as the hold of navigation options, and yellow line will be a connector for a fly-out panel for a dynamic visual transmission since I planned to have at least three (3) set of reports to be integrated in my dashboard as shown below:
<p align="center"> <img src="https://github.com/jvenncpe/2023.12_Case_Study_Analyzing_Customer_Churn_in_Power_BI/assets/35190918/31b7c34f-9b3b-41b9-95e8-4c4cdae002a7"/><br></p>

<p align="center"><br></p>
<p align="center"><br></p>
- Page Navigations Using Buttons and Bookmarks:
  - Implement buttons and bookmarks for seamless navigation between report pages, creating buttons and bookmarks that allow users to move seamlessly between different sections for a smoother experience.
<p align="center"><br></p>
<p align="center"> <img src="https://github.com/jvenncpe/2023.12_Case_Study_Analyzing_Customer_Churn_in_Power_BI/assets/35190918/67e6cf39-760d-4209-9c70-b9c08366e982"/><br></p>

<p align="center"><br></p>
<p align="center"><br></p>
- Breakdown of Visual Formulas:
  - The most tricky part (for me) in the visualization are the call-out cards or values in which I wanted to display the top churning categories and such for each segment the I wanted to visualize. In order to organize my thouhghts first, I created visual tables that will serve as holder for each report page with nested folders that are holding the formulas that I will be needing to have a dynamic title, subtitle and call-out values in my call-out cards as show below:

<p align="center"><br></p>
> Call-Out Cards
<p> 
    <img src="https://github.com/jvenncpe/2023.12_Case_Study_Analyzing_Customer_Churn_in_Power_BI/assets/35190918/034746b3-8490-492b-bcb8-88353573f2d7"/>&nbsp;
    <img src="https://github.com/jvenncpe/2023.12_Case_Study_Analyzing_Customer_Churn_in_Power_BI/assets/35190918/f0c31ef4-2020-4f46-8e56-219bb6c22b3b"/>&nbsp;
</p>

<p align="center"><br></p>
> Visual Table Holders
<p align="center"> <img src="https://github.com/jvenncpe/2023.12_Case_Study_Analyzing_Customer_Churn_in_Power_BI/assets/35190918/933313cf-0c37-4af4-867d-391eb8a7f4f3"/><br></p>

<p align="center"><br></p>
> DAX Formulas used in Dynamic Title, Subtitles and Call-out Values
<dl>
  <dt><p>Title</p></dd>
  <dd><p align="center"> <img src="https://github.com/jvenncpe/2023.12_Case_Study_Analyzing_Customer_Churn_in_Power_BI/assets/35190918/1445975b-cf31-44b8-be9c-a61fc9c84e73"/><br></p></dd>

  <dt><p>Subtitle</p></dd><dt>
  <dd><p align="center"> <img src="https://github.com/jvenncpe/2023.12_Case_Study_Analyzing_Customer_Churn_in_Power_BI/assets/35190918/e8b3f896-7dc0-44cf-8477-21f3fb2dab2e"/><br></p></dd>

  <dt><p>Call-out Value</p></dt>
  <dd>
    <p align="center"> <img src="https://github.com/jvenncpe/2023.12_Case_Study_Analyzing_Customer_Churn_in_Power_BI/assets/35190918/6f5046f8-532f-44b4-9cfb-2fca77225447"/><br></p>
    <p align="center"> <img src="https://github.com/jvenncpe/2023.12_Case_Study_Analyzing_Customer_Churn_in_Power_BI/assets/35190918/c660c64f-def1-4b99-8ec8-ddf20f39900c"/><br><br></p>
  </dd>
</dl>

- Wrapping Up Interactions among Slicers and Dynamic Visuals:
  - I explored the slicers to dynamically filter and interact with visuals for advanced exploration. This is to filter the needed visuals that are supposedly not be affected by the slicers ensuring that all the different elements within the report—like slicers (interactive filters) and dynamic visuals—work together harmoniously, allowing users to interact and explore the data effortlessly as shown below:

<p align="center"> <img src="https://github.com/jvenncpe/2023.12_Case_Study_Analyzing_Customer_Churn_in_Power_BI/assets/35190918/97ab1138-de60-47e7-9059-65709ce8adc0"/><br></p>


## Results and Discussion

Dashboard Summary:
- Pareto Chart were added in the visualization to determine and identify critical key figures to be worked out by the company to prevent churning as shown below:

<dl>
  <dt><p>Age Bin</p></dd>
  <dd><p align="center"> <img src="https://github.com/jvenncpe/2023.12_Case_Study_Analyzing_Customer_Churn_in_Power_BI/assets/35190918/b2815754-eb5b-4c7c-b97c-7058945ace18"/><br></p></dd>

  <dt><p>Churn Category</p></dd><dt>
  <dd><p align="center"> <img src="https://github.com/jvenncpe/2023.12_Case_Study_Analyzing_Customer_Churn_in_Power_BI/assets/35190918/08a72b55-edd5-496c-9f10-9c186adc969c"/><br></p></dd>

  <dt><p>Churn Reason</p></dt>
  <dd>
    <p align="center"> <img src="https://github.com/jvenncpe/2023.12_Case_Study_Analyzing_Customer_Churn_in_Power_BI/assets/35190918/e4342b7b-3089-4fe9-8e3c-3d2c35efba5a"/><br></p>
  </dd>
</dl>

- Overall, the top contributors of the churn rate are as follows:
    <p align="center"> <img src="https://github.com/jvenncpe/2023.12_Case_Study_Analyzing_Customer_Churn_in_Power_BI/assets/35190918/f95bcfa5-4747-450c-b72b-d4793c88021e"/><br></p>

Demographic Breakdown:
- In terms of demographic breakdown, the "age bin:85" has the highest churn rate accross age groups. However, this does not mean that it is the most needed attention accross the age bins. Instead, the top contributor is from the "age bin: 25" that has top churning age as shown below:

<dl>
  <dt><p>At Age Bin: 85, Churn Rate is as high as 52%.</p>
      <p align="center"> <img src="https://github.com/jvenncpe/2023.12_Case_Study_Analyzing_Customer_Churn_in_Power_BI/assets/35190918/566e07da-0866-4037-8faa-f3637e90ce3c"/><br></p></dt>

  <dt><p>However, the Top Churning Age is 29 wherein belongs to Age Bin: 25. This churning age bin contributes 0.84% out of 26.86% of the overall churn rate.</p>
      <p align="center"> <img src="https://github.com/jvenncpe/2023.12_Case_Study_Analyzing_Customer_Churn_in_Power_BI/assets/35190918/31747eff-d07e-433c-af19-fc23c1b4e1ef"/><br></p></dt>

  <dt><p>Meanwhile, the Churning Age Bin: 85 only contributes 0.19% out of 26.86% of the overall churn rate.</p>
      <p align="center"> <img src="https://github.com/jvenncpe/2023.12_Case_Study_Analyzing_Customer_Churn_in_Power_BI/assets/35190918/dcc7a1df-09fa-4340-a4ee-345908b1f500"/><br></p></dt>
</dl>

Account Breakdown:
- In terms of account breakdown, the "Accumulated Service Calls: 4 & 5" has the highest churn rate over the segment. However, this does not mean that it is the most needed attention. Just like the age bin, the top contributor is from the segement "Accumulated Service Calls: 0" as shown below:

<dl>
  <dt><p>"Accumulated Service Calls: 4 & 5", Churn Rate is as high as 100%.</p>
      <p align="center"> <img src="https://github.com/jvenncpe/2023.12_Case_Study_Analyzing_Customer_Churn_in_Power_BI/assets/35190918/e9e0e3af-c810-47c5-87fa-b7c6dcd1e324"/><br></p></dt>

  <dt><p>However, the Top Churning is from "Accumulated Service Calls: 0" wherein contributes 5.40% out of 26.86% of the overall churn rate.</p>
      <p align="center"> <img src="https://github.com/jvenncpe/2023.12_Case_Study_Analyzing_Customer_Churn_in_Power_BI/assets/35190918/b0509275-bcae-465e-b8a1-defbcdbf4eb8"/><br></p></dt>


  <dt><p>Meanwhile, the Churning Rate from "Accumulated Service Calls: 4 & 5" only contributes 4.37% and 4.32%, respectively out of 26.86% of the overall churn rate.</p>
      <p align="center"> <img src="https://github.com/jvenncpe/2023.12_Case_Study_Analyzing_Customer_Churn_in_Power_BI/assets/35190918/58d1c878-3bba-49ae-891c-2c72b89a5e27"/><br></p>
      <p align="center"> <img src="https://github.com/jvenncpe/2023.12_Case_Study_Analyzing_Customer_Churn_in_Power_BI/assets/35190918/ed7716e9-3f3d-4c80-99e5-2caa3ca50870"/><br></p>
</dt>
</dl>


## Summary, Conclusion & Recommendations:
---

### *In summary, this project encapsulates a thorough and detailed data analysis aimed at understanding and curbing customer churn in various business settings. Our analysis revealed the key finding stipulated above, paving the way for targeted interventions. By implementing the recommendations, it has the potential to mitigate churning of customers, ultimately leading to increased customer loyalty and brand success.*

<p align="center">
<img src="https://github.com/jvenncpe/2023.12_Case_Study_Analyzing_Customer_Churn_in_Power_BI/blob/main/Case%20Study%20Analyzing%20Customer%20Churn%20in%20Power%20BI.gif"/>
</p>


### *Further research could explore for time-series (if the dataset is available, since in this dataset it's not available) related insights to deepen our understanding of churn behavior and its multifaceted drivers.*

# Thank you!
