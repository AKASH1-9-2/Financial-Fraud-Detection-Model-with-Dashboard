# Financial-Fraud-Detection-Model-with-Dashboard
**Project Title: Financial Fraud Detection Model with Dashboard**

**Objective:**
The goal of this project is to perform a detailed financial transaction analysis to detect potential fraudulent activities using a given dataset. This includes building interactive and insightful dashboards using Power BI for better monitoring and understanding of transaction patterns and fraud trends.

**Dataset Description:**
The dataset used contains records of financial transactions and has the following key columns:


**Column Name** |	**Description**
step	          |  Represents the time step of the transaction (in hours).
type            |	Type of transaction (PAYMENT, TRANSFER, CASH_OUT, CASH_IN, DEBIT).
amount          |  The amount of money transferred in the transaction.
nameOrig        |	 Customer ID of the originator (sender).
oldbalanceOrg   |  Initial balance of the originator before the transaction.
newbalanceOrig  |	 New balance of the originator after the transaction.
nameDest	      |  Customer ID of the recipient.
oldbalanceDest  |  Initial balance of the recipient before the transaction.
newbalanceDest  |	New balance of the recipient after the transaction.
isFraud	        |  1 if the transaction is fraudulent, 0 otherwise.
isFlaggedFraud  |	1 if the transaction is flagged as suspicious by the system, 0 otherwise.

**Dataset Observations:**

-Most transactions are of type PAYMENT.

-Significant fraud happens during TRANSFER and CASH_OUT transactions.

-isFraud cases are isolated and specific.

**Power BI Dashboard Description:**
The Power BI dashboard created includes the following visualizations:

1. Pie Chart (Sum of Amount by Type)
    -Displays the proportion of transaction types (PAYMENT, CASH_IN, TRANSFER, CASH_OUT, DEBIT).

    -PAYMENT dominates the transaction volume.

2. Bar Charts (Top Destinations by New Balance and Amount)
    -Shows the top recipient accounts (nameDest) based on:

    -Sum of newbalanceDest

    -Sum of amount

    -Helps to identify which accounts are receiving high-value transactions.

3. Line/Area Chart (Fraud Analysis by Type)
    -Shows the percentage of transactions that were fraudulent for each transaction type.

    -Major fraud is seen in TRANSFER and CASH_OUT types.

    -PAYMENT and CASH_IN types have almost 0% fraud.

4. Cards (KPI Metrics)
    -Total Number of Frauds Detected: 8K transactions.

    -Total Number of Flagged Frauds: 16 transactions.

    -Quick snapshot for monitoring.

5. Detailed Table (Transaction Summary)
   -Shows:

        -Step

        -Sum of old balance (origin)

        -Sum of new balance (origin)

        -Sum of transaction amount

        -Summarized by time step to understand how transactions evolve over time.

**Key Insights from the Dashboard:**
   -TRANSFER and CASH_OUT are the major fraudulent transaction types.

   -PAYMENT and CASH_IN transactions are relatively safe.

   -Very few transactions are actually flagged as suspicious by the system compared to actual frauds.

   -Monitoring certain destination accounts (high transaction volume) could help in detecting fraud early.

**Conclusion:**
This Power BI dashboard provides a clear view of transaction types, volume, fraud distribution, and risky destinations. It can be extremely helpful for financial institutions to focus their fraud detection efforts, monitor suspicious accounts, and take preventive measures.
