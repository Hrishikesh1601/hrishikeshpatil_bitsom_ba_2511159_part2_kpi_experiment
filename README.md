# hrishikeshpatil_bitsom_ba_2511159_part2_kpi_experiment

Business Context
A subscription-based digital product company ran a new onboarding and activation campaign aimed at improving user conversion and early engagement. Users were randomly split into two groups: a Control group (existing onboarding experience) and a Treatment group (new onboarding experience). The goal of this project was to decide whether the new experience should be rolled out to everyone based on solid experiment results and business metrics.
Business Problem Statement
The company needs to decide if the new onboarding campaign should replace the current one. This decision affects product, marketing, customer success, and leadership teams. The main objective is to increase Paid Conversion Rate without negatively impacting customer experience, revenue quality, or operational costs. We needed clear statistical evidence and careful guardrail checks before making a recommendation.
Dataset Description
The dataset contains user-level data from the A/B experiment.
After cleaning:
Initial records: 1,408
Duplicates removed: 8
Final records used: 1,400
Control group: 690 users
Treatment group: 710 users
Key fields include Experiment Group, Landing Page Visit, Trial Started, Onboarding Completed, Paid Conversion, Revenue (30 days), Refund Request, Support Tickets, Engagement Score, Days to Convert, Region, Device Type, Traffic Source, and Plan Type.
Data Cleaning Summary
We performed the following checks and fixes:
Removed 8 duplicate User IDs
Noted missing values: Device Type (18), Traffic Source (24), Engagement Score (14)
Days to Convert missing for 1,328 records (expected, since non-converted users don’t have a conversion date)
Verified balanced experiment group split
Checked for revenue outliers
Confirmed Support Tickets were properly treated as count data
North Star Metric
Paid Conversion Rate
We selected Paid Conversion Rate as the North Star Metric because it directly reflects business growth — showing the percentage of users who become paying customers.
Supporting metrics we tracked:
Landing Page Visit Rate
Trial Start Rate
Onboarding Completion Rate
Average Revenue Per User
Engagement Score
We also monitored guardrail metrics because pushing only for higher conversions could increase refunds or support load.
KPI Tree Summary
North Star Metric: Paid Conversion Rate
Primary Drivers:
Acquisition
Landing Page Visit Rate
Traffic Source Quality
Activation
Trial Start Rate
Onboarding Completion Rate
Monetization
Average Revenue Per User
Revenue per Converted User
Guardrail Metrics:
Refund Rate
Support Ticket Rate
Average Days to Convert
Experiment Analysis Summary
Metric
Control
Treatment
User Count
690
710
Landing Page Visit Rate
63.62%
72.39%
Trial Start Rate
25.07%
29.01%
Onboarding Completion Rate
15.65%
21.13%
Paid Conversion Rate
3.19%
7.04%
Average Revenue Per User
51.97
54.25
Revenue per Converted User
1630.10
770.41
Refund Rate
0.00%
0.42%
Support Ticket Rate
14.78%
24.79%
Average Engagement Score
57.03
62.94
Average Days to Convert
8.86
6.40
Hypothesis Test Summary
We ran a one-tailed Two-Proportion Z-Test on Paid Conversion Rate.
Null Hypothesis (H₀): No significant difference between groups.
Alternative Hypothesis (H₁): Treatment group has a higher Paid Conversion Rate.
Significance Level (α): 0.05
Test Statistic (Z): 3.264
P-value: 0.00055
Since the p-value is well below 0.05, we reject the null hypothesis. The improvement in Paid Conversion Rate is statistically significant.
Guardrail Metrics Considered
While the new experience delivered strong gains, we watched several guardrails:
Refund Rate increased slightly (0.00% → 0.42%).
Support Ticket Rate increased noticeably (14.78% → 24.79%), suggesting higher customer support demand.
Average Days to Convert improved (users converted faster).
Revenue per Converted User dropped significantly (₹1630.10 → ₹770.41), meaning each paying customer brought in less revenue on average.
Final Recommendation
Recommendation: Launch the new onboarding only for selected high-performing segments while closely monitoring guardrail metrics.
The Treatment group showed a clear, statistically significant lift in Paid Conversion Rate, better engagement, and faster conversions. However, the rise in support tickets and drop in revenue per converted user mean a full rollout right now carries risks. A phased approach with continued optimization is the safer path.
Assumptions and Limitations
Missing values in optional fields were kept where they didn’t affect core analysis.
Days to Convert only applies to users who actually converted.
Segment analysis may be slightly impacted by missing Device Type and Traffic Source data.
Results are based on the current experiment period and dataset.
Repository Contents
Dataset
Experiment Analysis Workbook
Hypothesis Test Notes
KPI Tree
Experiment Summary Workbook
Recommendation Memo
Screenshots
README
Screenshots Included
summary_metrics.png
hypothesis_test_output.png
kpi_tree_preview.png
