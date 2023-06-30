# Marketing Data Analysis for a Fintech Company

<b>About the Project:</b> As part of a graduation project, this project is about becoming a student consultant and solving a problem for a company. As a Marketing Data Analyst, I tracked the effectiveness of advertising campaigns and advertising creatives, evaluated their effectiveness, and provided strategies to provide air cover support for sales in order to better optimize advertising spending for a real-world fintech startup. I planned and carried out the project by holding weekly client meetings and internal meetings.


## Background and Objective of the Project

<b>* Company Goal</b>  
To optimize advertising expenditure more effectively, you need to track the effectiveness of advertising campaigns and ad materials and evaluate the impact of providing air cover support for sales. 

<b>* Customer’s Request</b>  
We would love to see a tool to help construct optimal campaign settings on LinkedIn Campaign Manager that maximize effectiveness. The ad fatigue trend and the quantified indicators play a big role.

<b>* Project Goals</b>  
The goal is to enhance advertising effectiveness by examining the currently available data. LinkedIn ad effectiveness analysis helps determine the best way to target customers and control the timing accurately. The following are important considerations:
* Making the right target decisions within the company at specific points in the sales cycle.
* Evaluating the performance of ad creatives over time

<b>* Details about the Project Goal</b>  
* Develop ETL and visualization solutions using Python or other open-source alternatives to provide insights as described above. 
* Create dashboards using Tableau or other visualization tools to allow non-technical users to gain insights from the data. 
* Analyze the results to propose marketing strategies and develop a Data Center for future use. 

<b>* Key Questions</b>  
* How does the target audience (TA) interact with the ad in each sales cycle 
* How well does the ad distribution perform over time 
* What are the signs showing advertisements reach ad fatigue 



## Project Approach


#### Approach method: Pyramid Hypothesis-based Analysis

#### Preferred Data or Analytics Methodology: CRISP-DM Methodology

<b>1. Business Understanding</b>  
* Unshield the complexity of LinkedIn API data  
  * Fragmented data points by LinkedIn policy and overlapping issues between creatives belonging to the same campaign  
* Find out important metrics for LinkedIn data  
  * Metrics that measure the performance (user reach, impression, clicks) 
  * Metrics that may appear as redundancy  
* Pieces of a recipe for the paid media engine  
  * XYZ action boost x % in performance metric
  * Quantify the ad performance/effectiveness of brand awareness/lead gen to a list of clear targeted audience  


<b>2. Data Understanding & Data Preparation</b>  
- LinkedIn API data and LinkedIn Campaign Manager (Primary)
- Google Analytics
- Hubspot  


<b>3. Data Preparation</b>  
+ Create a GitHub repository for version control  
+ Extract LinkedIn Ads data in Python
 + Explore data, and combine marketing goals to identify key features
 + Extract data using LinkedIn API to organize data source
+ Assist in building PostgreSQL database for analytics in Azure  


<b>4. Modeling</b>
      1) Select algorithms and generate a design 
         * Model parameters selection based on metrics from LinkedIn API data 
      2) Visualize descriptive analysis with Tableau dashboards 
      3) Perform A/B testing to determine creative deployment strategy 


<b>5. Evaluation</b>
- Evaluate the model’s prediction performance with test data 
- Evaluate the performance of Tableau dashboards 


<b>6. Deployment</b>
1) Deployment for technical groups (e.g. technical team) 
 * Upload ETL pipeline for data automation to GitHub repository 
 * Upload predictive machine learning model final codes to GitHub repository

2) Deployment for non-technical stakeholders (e.g Marketing team) 
 * Tableau visualization dashboards 
 * Written reports on future LinkedIn Ad strategy 

3) Keep records of unsolved problems and insights as guidance for the future analytics team 



## Products and Solutions


 ![image](https://github.com/itsIsabelle17/Business-Analytics-Practicum/assets/114459340/f833e74a-44c1-4d3f-8df7-457f6d3c8065)


### Data Pipeline and Database Construction

The data are generated from the LinkedIn Ads service, utilizing Python with LinkedIn Marketing Developer Platform, marketing APIs (Reporting & ROI), its access token, and LinkedIn Campaign Manager insights. With adCampaign Performance Analytics and adCreative Performance Analytics pipeline, we can access all ads performance metrics at ALL TIME, with their demographics data that is not included in the LinkedIn APIs directly.
* Ad Campaign Performance Analytics
* Ad Creative Performance Analytics
* Target Audience Setting Extraction

<img width="519" alt="image" src="https://github.com/itsIsabelle17/Business-Analytics-Practicum/assets/114459340/6f2b836b-b284-47ed-87f9-1c6b28bdc7bc">



### Ad Performance Tracking Center

#### Metrics for Evaluating Ad Performances
* Ad Quality: Cost per Click (CPC), Click Through Rate (CTR)
* Ad Fatigue: 7-Day Reach, 30-Day Reach
* Usually, a good ad quality has low CPC and high CTR. Marketers may compare the metrics with the past ad campaign analytics as well as the LinkedIn official stats benchmarks. According to LinkedIn, the average CTR is around 0.44% to 0.65%, and the average CPC is around $5.58. Based on the criteria representing CTR and CPC in the official LinkedIn statistical benchmarks, an overall analysis of the advertising campaign was conducted, dividing it into three tiers: 1) High CTR and low CPC, 2) High CTR and high CPC, low CTR and low CPC, 3) Low CTR and high CPC.


#### Detecting the Ad Fatigue
For detecting whether an ad campaign reaches its ad fatigue, marketers should look to 7- Day Reach and 30-Day Reach metrics. When a trend shows an inversion point and the trend becomes relatively flat, markets should consider either (1) adjusting the targeting criteria if the ad campaign runs at the early stage or (2) stopping the ad campaign if the ad campaign has run for a while. 
![image](https://github.com/itsIsabelle17/Business-Analytics-Practicum/assets/114459340/e89b1b1a-9166-4bb0-b4b3-e4f86a74f1b9) ![image](https://github.com/itsIsabelle17/Business-Analytics-Practicum/assets/114459340/5561b726-2d65-4e39-afaf-84fc1f8b4054)


#### Ad Campaign Performance
A Tableau dashboard was created to present an overview of the advertising campaign and compare it to the LinkedIn Advertising Benchmark. When evaluating the effectiveness of an advertising campaign, both ad quality and ad fatigue should be considered. This dashboard provides the number of Ad Campaigns used and Ad Cost, highlighted CPC (cost per click) and CTR (click-through rate), as well as Reach Metrics based on daily, 7-day, and 30-day data for each client. 
![image](https://github.com/itsIsabelle17/Business-Analytics-Practicum/assets/114459340/8f8e56d8-30d8-40c3-b227-e37d48a2c4b8)


#### Job Title Performance 
Once we identify the ad campaign performance, marketers still need to look into who was actually interacting with the ads and might need optimizations. The dashboard analyzes performance metrics (landing page clicks, CPC, CTR) for each position by extracting demographic data. It helps marketers know which Job Titles to target for each ad campaign. For example, by clicking on the job title recorded in the Job Title Performances dashboard, marketers may consider adding Senior Risk Manager, Vice President of Services, Risk Management Officer, Treasury Management Specialist, Risk Management Specialist...etc into the targeting criteria. Similar optimization analysis may also be done by the Job Title Performances and Company Performances dashboard.
![image](https://github.com/itsIsabelle17/Business-Analytics-Practicum/assets/114459340/06f99e22-24b8-481a-b548-b87384d3e2e6)


#### Roles in Sales Process & Ad Performance
After filtering out the top 200 benchmark ad creatives audiences, we tagged these audiences based on their titles and categorized* them as Decision-Maker, Do-er, Influencer, and Unidentified. The graphs show how different roles in the sales process respond to our ads in general.
* **Roles: 
* **  ● Decision-Maker: Ultimate decider, high-level manager (VP, CEO) 
* **  ● Influencer: Mid-level managers (head of department) 
* **  ● Do-er:Junior-level employees responsible for execution (Associate, Specialist) 
![image](https://github.com/itsIsabelle17/Business-Analytics-Practicum/assets/114459340/355f1f83-c27e-4f4e-854c-867e9a376e37)


#### Company Performance and Ad Creative Performance
The dashboard on adCreative shows a grand view of the financial industry-level performance metrics (impressions, CTR) filtered from the Top 200 audiences and its comparison on a single company level or the all industry level, with data mainly focusing on adCreative. The overall performance can be accessed on the bottom chart when selecting “All”. To standardize the data and avoid bias based on the number of employees of each company, we recommend reading the impression data first to have a sense of how a specific adCreative leaves impressions on the landing page by the target settings. The CTR for each company under specific adCreative would provide more accurate data than clicks with all target audiences to let you know the Ad quality. The industry-level analysis also helps you reduce the noise of other target industries' responses.
![image](https://github.com/itsIsabelle17/Business-Analytics-Practicum/assets/114459340/6ccdaff4-f523-4a7d-b817-db89e1d69a0d)

