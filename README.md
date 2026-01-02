# Banking-Domain-Data-Analytics-Project
Develop a basic understanding of risk analytics in banking and financial services, and understand how data is used to minimize the risk of losing money while lending to customers.

This dataset basically contains information about bank details, various client details, which consists of multiple tables that are interlinked with each other through keys like primary key and foreign key.

The various tables are Banking Relationship, Client-Banking, Gender, Investment Advisor, and Period.


**EDA Insights Report: Customer Financial Correlations**

1. Analysis of Strong Banking Correlations

In my analysis of the correlation heatmap, I observed exceptionally high positive correlations between Bank Deposits, Checking Accounts ($0.84$), and Saving Accounts ($0.75$).

Hypothesis: I suspect that "Bank Deposits" is an aggregate variable representing the sum of liquid assets. Since Checking and Saving accounts likely make up the bulk of this total, they naturally move in tandem with it.

Implication: To avoid multicollinearity in my future predictive modeling, I will likely exclude the "Bank Deposits" variable and instead use the distinct Checking and Savings features, as they provide more granular information without the redundancy.

2. Income vs. Accumulated Wealth

I found that Estimated Income is not a strong predictor of a customer's actual assets. The correlation between Income and Bank Deposits is relatively weak ($0.26$).

Insight: This suggests that high earners in my dataset are not necessarily high savers. I should be careful not to use Income as a proxy for wealth; a customer may have high cash flow but low retained assets.

3. The "Entrepreneurial" Borrower

I identified a moderate correlation ($0.42$) between Bank Loans and Business Lending.

Insight: This indicates a distinct segment of customers who rely on credit for both personal and business needs. I can potentially cluster these users into a specific "Entrepreneurial Borrower" segment for targeted lending offers.

4. Independence of Retirement Savings

I noticed that Superannuation Savings behaves independently of day-to-day banking variables. Its correlation with Checking Accounts is quite low ($0.20$).

Insight: A customer's long-term retirement planning does not seem to reflect their short-term liquidity. I cannot reliably predict a customer's retirement balance based solely on their daily transaction accounts.
