
## Customer Risk Intelligence Dashboard

## DASHBOARD LINK 

https://app.powerbi.com/links/jGt1RqxW_k?ctid=03cb5f0c-1f82-4993-9621-36330f6309ec&pbi_source=linkShare&bookmarkGuid=c9abdc8a-cd7e-4d5f-9ec9-78b79979bddb

## Problem Stament 

Financial institutions and digital service platforms face increasing challenges in managing customer churn, fraud incidents, and device-level risk. With rising transaction volumes and complex user behaviors, it becomes difficult to identify which customers are at risk of leaving, which channels are most vulnerable to fraud, and which devices exhibit suspicious activity.

The organization lacked a unified analytical system that could:

Track customer churn patterns and payment failures.

Identify fraud hotspots across channels, cities, and time periods.

Detect high-risk devices based on FraudRiskScore and transaction anomalies.

Consolidate key risk indicators into a single, actionable dashboard for decision-makers.

Due to fragmented data and limited visibility into behavioral risk, stakeholders were unable to proactively prevent losses, reduce churn, or optimize fraud-mitigation strategies.
## Steps Followed :

Step 1:
    The dataset for Customer, Fraud, Transactions, and Device Risk was created using Generative AI tools (ChatGPT & Gemini).
    These tools helped generate structured CSV-style synthetic data for analysis.

Step 2: 
    Imported the AI-generated dataset into SQL database.

    Created tables for Customer, Fraud, Device Risk, and Transactions.

    Inserted the generated data into respective SQL tables.

Step 3: 
    Performed SQL-based data cleaning:

        Removed duplicates

        Standardized date/time formats

        Converted numeric fields to correct data types

        Filled or ignored missing values where appropriate

        Ensured referential consistency across CustomerID, DeviceID, and Channel fields

Step 4: 
     Exported the cleaned SQL tables into CSV files for Power BI.
(Alternatively, SQL Server connection could be used — based on availability.)

Step 5:     
    Loaded the cleaned CSV files into Power BI Desktop using Get Data → Text/CSV.

Step 6:
    Opened Power Query Editor and turned on:

        Column quality
 
        Column distribution

        Column profile
    Also enabled “Column profiling based on entire dataset” for accurate validation.

Step 7:
    Further refined data in Power Query:

        Standardized column names

        Removed unnecessary columns

        Converted incorrect data types

    Ensured null values (<1%) in risk/payment fields do not affect calculations

Step 8:
    Built a structured data model using relationships between:

        Customer Table

        Fraud Table

        Device Risk Table

        Transactions Table
Relationships were created using CustomerID, DeviceID, Channel, etc.

Step 9:
    Created DAX Measures for key KPIs such as:

        Churn Rate

        Total Fraud Cases

        Fraud Loss Amount

        High-Risk Devices

        Average FraudRiskScore

        Payment Success & Failure Metrics

        Monthly Trends

Step 10: 
    Designed the dashboard using appropriate visuals:

        KPI Cards

        Line charts, bar charts, donut charts

        Geo/location visuals (if needed)

        Risk score distribution charts

        Device-level analytics (DeviceID vs RiskScore)

Step 11: 
    Added Slicers/Visual Filters for interactive analysis:

        Month

        Channel

        City

        Risk Category

        Device ID

Step 12: 
    Organized report into three dashboard pages:

        Customer Churn & Payment Insights

        Fraud Cases & Loss Insights

        Device Risk & FraudScore Analysis

Step 13: 
    Enhanced the report visually:

        Applied theme

        Added headers, section labels, and descriptions

        Enabled tooltips & drill-downs

        Applied conditional formatting for high-risk segments

Step 14: 
    Exported the final dashboard snapshots and prepared documentation for GitHub.
    
## Dashboard Snapshot

Customer Churn & Payment Insights:
![Dashboard Snapshots](https://github.com/user-attachments/assets/b4739d20-0a06-494a-8d67-beb90f2680ce)

Fraud Cases & Loss Insights :
![Dashboard Snapshot](https://github.com/user-attachments/assets/280947ab-9034-4306-8f52-e37f4d91394e)

Device Risk & FraudScore Analysis:
![Dashboard Snapshot](https://github.com/user-attachments/assets/77653010-09c3-43c5-b370-e8b89d984364)

## Insights 

[1] Customer Overview & Churn Insights

        The dashboard shows a total customer base with clear segmentation of Active vs Churned customers.

        Churn Rate indicates a measurable percentage of customers leaving the organization, driven largely by payment failures, low tenure, and higher risk scores.

        Tenured customers show lower churn probability, whereas newer customers are more likely to churn. 

        Customers with higher failed payment counts displayed a higher churn percentage, indicating a strong correlation between payment behaviour and customer retention.

        Inference:
→       Churn is primarily driven by payment issues and low engagement (low tenure).

[2] Payment Behaviour & Transaction Insights

        Successful payments significantly outweigh failed payments, but failed transactions cluster around high-risk customer segments.

        Customers with frequent missed payments contribute heavily to higher churn and higher risk scores.

        Monthly payment trends show visible fluctuations, suggesting periods of operational stress or customer behaviour changes.

        Inference:
→         Tracking payment failures is essential to preventing customer churn and reducing financial risk.

[3] Fraud Cases & Loss Insights

        The total number of fraud cases and the fraud loss amount highlight major operational risk.

        ATM and Online transactions show a higher frequency of fraud cases compared to other channels.

        Some cities contribute disproportionately to fraud cases, indicating location-based fraud hotspots.

        Monthly fraud trends show spikes that can help in forecasting fraud events or improving monitoring.

        Inference:
→           Fraud risk is unevenly distributed across channels and locations, requiring channel-specific security measures.

[4] FraudRiskScore Analysis

         The average FraudRiskScore indicates moderate overall risk, but a small segment of customers/devices fall into high-risk categories.

            High-risk customers also show:

            Higher missed payments

            Higher churn probabilities

            More fraudulent transactions

        Inference:
→           FraudRiskScore is a strong indicator of both churn and fraud vulnerability.

[5] Device-Level Insights

        A large number of unique devices are used by customers, but only a small percentage are marked as high-risk.

       High-risk devices correspond to:

             Higher FraudRiskScore

              Higher fraud loss amounts

             More suspicious transaction patterns

             Devices with repeated alerts contribute significantly to monthly fraud spikes.

        Inference:
→           Device fingerprinting helps isolate fraud origins and track recurring malicious behaviour.

[6] Channel-Level Insights

        Channels such as Online, App, and ATM have the highest fraud loss exposure.

        POS transactions show lower fraud intensity but higher transaction volume.

        Channel-wise segmentation helps identify where stronger security layers are needed.

        Inference:
→           Channel-level fraud monitoring is critical for prioritizing security measures.

[7] Monthly Trends

        Monthly churn, fraud cases, and fraud loss show clear seasonal and behavioural patterns.

        Peaks in fraud loss often occur during the same months as spikes in high-risk device activity.

        Inference:
→           Monthly trend correlations help predict future risk and prepare preventive strategies

## Conclusion
The Customer Risk Intelligence Dashboard provides a unified and data-driven view of customer behaviour, fraud activity, and device-level risk patterns. By integrating churn indicators, payment behaviour, fraud cases, and FraudRiskScore insights, the dashboard helps stakeholders identify high-risk customers, detect suspicious transactions, and understand the operational factors contributing to financial losses.

The analysis clearly shows that payment failures, low customer tenure, and high FraudRiskScores are major drivers of churn, while fraud incidents are concentrated in specific channels and locations. Device-level tracking further strengthens the ability to pinpoint recurring high-risk activities and potential fraud origins.

By enabling real-time monitoring and interactive exploration through slicers and dynamic visuals, this dashboard empowers decision-makers to:

Reduce customer churn through targeted interventions

Strengthen fraud prevention strategies

Prioritize high-risk channels and locations

Improve the organization’s overall risk management framework

Overall, the dashboard transforms raw synthetic data into actionable intelligence, offering a scalable foundation for future enhancements such as predictive churn modelling, anomaly detection, and automated fraud alerts.
