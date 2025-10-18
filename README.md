# Maji-ndogo-water-project-powerBI
A Power BI dashboard project analyzing water access and distribution in the Maji Ndogo region. This project transforms raw data into actionable insights, visualizing key metrics like water availability, usage trends, and infrastructure gaps. Built to support data-driven decision-making for sustainable water management.
# Dashboards included
This project features two distinct Power BI dashboards:

1. Maji Ndogo Stakeholder's Dashboard (For Decision-Makers)
<img width="1189" height="741" alt="maji ndogo" src="https://github.com/user-attachments/assets/e5deebd3-5ff7-4a78-8be2-0c00e9b4a41c" />
This dashboard is tailored for key decision-makers, such as President Aziza Naledi and provincial leaders, providing them with critical data to understand the overall status of water access, identify challenges, and make informed financial and operational decisions.

Purpose: To empower national and provincial leaders with accurate, actionable data regarding water access challenges, upgrade requirements, and financial expenditures, facilitating strategic planning and resource allocation.

Data Sources: This dashboard primarily leverages the Md_water_services_data.xlsx dataset, which includes comprehensive information on water sources, visits, infrastructure costs, and project progress.

Key Features / Visuals:

Overall Water Access Status: Summarizes population-related water access on national and provincial levels, distinguishing between rural and urban areas.
Water Access Challenges: Communicates the number of affected people and the types of challenges, potentially hiding less critical sources like tap_in_homes for strategic focus.
Upgrade Costs & Allocation: Displays national and provincial budget requirements for upgrades, breaking down costs by province, rural/urban split, and improvement type.
High-Impact Summaries: Includes prominent cards showing total cost of upgrades, current percentage of basic water access, and projected improvement percentages.
Interactive Controls: Features province selectors (slicers) and potentially rural/urban filters to allow decision-makers to focus on relevant data.
Dynamic Financial Views (Bookmarks): Utilizes bookmarks and buttons to toggle between detailed budget tables/visuals per province and per improvement type, optimizing dashboard space.
Provincial-Specific Pages: Designed with the ability to drill down or navigate to dedicated pages for each province, providing localized insights relevant to provincial leaders (e.g., breakdown of budget by town, rural/urban spending, improvements, and relevant provincial data like queues, gender composition, and crime).
Key Insights:

Strategic Resource Allocation: Helps leaders understand where funds are most needed (by province, urban/rural, improvement type) to maximize impact on water access.
Impact Assessment: Connects financial investment to tangible improvements in basic water access, allowing for measurement of project success.
Targeted Interventions: Identifies specific water source challenges and affected populations, guiding targeted interventions.
Accountability: Provides a clear overview of financial commitments and their corresponding outputs.
# 2 Maji Ndogo Public Dashboard (For Public Project Monitoring)
![the mcq 4 powerbi_page-0002](https://github.com/user-attachments/assets/cdb77a84-2f3d-49db-8ed0-8fdbc0ca0307)
This dashboard focuses on the financial oversight and progress tracking of water improvement projects across Maji Ndogo. It aims to provide transparency to the general public and stakeholders on budgeted vs. actual costs and project completion status.

Purpose: To provide a public-facing overview of the financial health and progress of water infrastructure improvement projects, enabling citizens and external stakeholders to monitor spending against budget and track project completion rates over time and by various categories.

Data Sources: The dashboard is built upon the Md_water_services_data(public).xlsx dataset, specifically utilizing the following tables (or imported CSVs from it):

project_progress.csv: Core project details, completion dates, budgeted and actual costs, and project status.
infrastructure_cost.csv: Standard and rural-adjusted unit costs for different improvement types.
location.csv: Geographic information for towns and regions.
vendors.csv: Details about the vendors involved in projects.
Key Features / Visuals:

Cumulative Budget & Cost Line Chart: Tracks the running total of budgeted and actual costs over time, allowing for easy comparison of financial performance.
Key Performance Indicator (KPI) Cards:
Cumulative Budget: Total allocated budget for completed projects ($128,450).
Cumulative Cost: Total actual expenditure on completed projects ($131,914.91).
Difference: Variance between budgeted and actual costs (reveals if over or under budget).
Total Projects in Backlog: Count of projects awaiting completion.
Number of Completed Projects: Count of successfully finished projects.
Project Status Bar Chart: Visualizes the distribution of projects between "Backlog" and "Complete" statuses.
Projects by Town/Location Chart: Shows the number of projects implemented in different towns/regions.
Projects by Improvement Type Chart: Categorizes projects by the type of water infrastructure improvement (e.g., "Drill well", "Install pump").
Projects by Vendor Chart: Displays the number of projects each vendor is associated with.
Interactive Slicers: Date range slicer and Town slicer for dynamic filtering and drilling down into specific periods or locations.
Key Insights:

Budget vs. Actual Spend: Provides clear visibility into whether projects are adhering to their allocated budgets or incurring overspends.
Project Progress Monitoring: Allows tracking of projects from backlog to completion, aiding in operational oversight.
Geographic Distribution: Identifies areas with high project activity or specific needs.
Resource Allocation: Insights into which types of improvements are prioritized and which vendors are most active.
Data Model Highlights:

Dedicated Date Table: A best practice implemented for robust time intelligence calculations, connected to project_progress via date_of_completion.
Calculated Columns:
budgeted_improvement_cost: Dynamically calculates project-specific budgeted costs, accounting for rural adjustments.
Rural_adjusted_cost (in infrastructure_cost table): Adjusts unit costs for rural projects (e.g., unit_cost_USD * 1.5).
Aggregated_improvements: A DAX column to consolidate similar improvement types for clearer visualization (e.g., "Install 1-8 taps" into "Install public tap(s)*")
Average_queue_time (in water_source table): Calculates average queue time per source for basic access classification.
Basic_water_access (in water_source table): Classifies each water source as 'Basic Access' or 'Below Basic Access' based on UN requirements and specific criteria (e.g., clean wells, queue times for shared taps, taps in homes).
DAX Measures: Custom measures for cumulative sums (cumulative_budget, cumulative_cost), basic water access percentage, and project counts (Total projects in backlog, Number of completed projects), and cost difference (Difference).
 
