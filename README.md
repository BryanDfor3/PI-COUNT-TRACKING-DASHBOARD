# PI Count Tracking Dashboard (2022-23)
![PI_Count_Tracking_Dashboard](https://github.com/user-attachments/assets/b21098f0-c0cf-4040-b8d0-c8e80d584a85)

(Note: The actual data used for the client engagement has been scrubbed and replaced with dummy data in the sceenshot above)

## Business Problem
To meet its compliance standards, an automotive manufacturer needed to perform quarterly physical inventory (PI) counts until its goal threshold was met (90% accuracy). These physical inventory counts required the manufacturing plant to have to temporarily shut down, and in the previous quarter, the manufacturer not only severely missed its target accuracy, but also had to use 9 days to complete the inventory count. This resulted in significant downtime for the factory that led to the underproduction of vehicles assembled.

In the subsequent quarter, the automotive manufacturer brought on consultants from PwC who provided support from both an operations and an analytics perspective. The focus of this use case is on the analytics side, where due to a lack of resources, the manufacturer did not have an easy way to understand how the physical inventory counts were going from both a progress standpoint and an accuracy standpoint. During the previous quarter, data would be manually extracted from SAP and then analyzed in Microsoft Excel to understand overall accuracy, what was left to be counted, and where counting support was needed.

## Methodology
1) Worked with client stakeholders (primarily inventory control, IT) to understand the material hierarchy (Plant / Shop / Physical Inventory Document / Bin / Product), counting procedure (counts / recounts / escalation counts) and SAP data generation for each count type, and "accurate count" logic
2) Secured access to client technologies and systems (virtual desktop, SAP / Tableau & Tableau Server prod and test environments / Alteryx / DBeaver / Amazon Redshift)
3) Leveraged SAP data from daily cycle counts to validate business logic
4) Worked with client IT team to develop a push of critical SAP tables to Amazon Redshift using Boomi scheduled jobs (due to inability to query SAP directly)
5) Developed data transformation workflow in Alteryx and data visualizations which adhered to the business logic established in step 1. SQL querys on Amazon Redshift were used as the method for data input, and Tableau sources (which would overwrite the data sources in the dashboards for each workflow run) were used as the output
6) Published Alteryx workflow to Alteryx Server and configured the workflow to run on a schedule, enabling near-real time dashboard views visible to the entire enterprise

## Skills
1) Data Extraction - SQL
2) Data Transformation - Alteryx
3) Data Visualization - Tableau / Tableau Server

## Results
Over the course of 12 months, the client was able to realize a 27% improvement in their inventory accuracy, and was eventually able to meet their accuracy target of 90%. Additionally, each PI count only spanned 2-3 days each, reducing the production downtime by over 67%, in part due to having the visibility offered by the Tableau dashboard.
