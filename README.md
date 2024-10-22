# DPDzero Data Analyst Assignment




---



This assignment is designed to give you a flavor of the kind of data analysis a typical data analyst does at DPDzero. Data analysts here leverage **Jupyter notebooks** heavily, and you are expected to use the **same tool** to complete this task.

Please note that this is an **open-ended** assignment.

## Dataset

DPDzero is a data-driven organization where most decisions are based on data analyst recommendations. Below is a typical anonymized dataset that a data analyst may work with:

[Data_Analyst_Assignment_Dataset.csv](https://prod-files-secure.s3.us-west-2.amazonaws.com/0fb337c8-6186-4010-911c-38ba2e525070/7e55b4b1-5878-4d1c-9dce-75419c39c4c5/Data_Analyst_Assignment_Dataset.csv)

The dataset contains loan data for various borrowers in a loan portfolio.

### Column Descriptions:

| **Column Name**     | **Description**                                                                                                                                                                                                                                                                                                                                                                                                       |
| ------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Amount Pending**   | EMI amount pending.                                                                                                                                                                                                                                                                                                                                                                                                   |
| **State**            | The borrower’s state.                                                                                                                                                                                                                                                                                                                                                                                                 |
| **Tenure**           | Total tenure of the borrower (i.e., the total tenure of the loan).                                                                                                                                                                                                                                                                                                                                                    |
| **Interest Rate**    | Interest rate of the loan.                                                                                                                                                                                                                                                                                                                                                                                             |
| **City**             | The borrower’s city.                                                                                                                                                                                                                                                                                                                                                                                                  |
| **Bounce String**    | Explains customer’s bounce behavior since the disbursal of the loan: <br> - S or H: No bounce in that month. <br> - B or L: Bounce in that month. <br> - FEMI: First EMI, no known behavior. <br> The last character represents the last month, and the first character represents the first month on the book (e.g., "SSB" means the customer has been on the book for 4 months and bounced in the last month). |
| **Disbursed Amount** | The total disbursed amount of the loan.                                                                                                                                                                                                                                                                                                                                                                               |
| **Loan Number**      | The unique identifier for the loan.                                                                                                                                                                                                                                                                                                                                                                                   |

---

## Deriving Values from Raw Data

At DPDzero, data analysts enhance the raw dataset by deriving new insights. As part of this assignment, calculate the following:

### Risk Label Calculation:

| **Risk Category**  | **Description**                                                                                                                                                          |
| ------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| **Unknown Risk**   | New customers.                                                                                                                                                            |
| **Low Risk**       | Customers who have not bounced in the last 6 months.                                                                                                                      |
| **Medium Risk**    | Customers who have bounced a maximum of twice in the last 6 months, but not in the last month.                                                                            |
| **High Risk**      | All other customers.                                                                                                                                                      |

### Tenure Labeling:

| **Tenure Stage**  | **Description**                                                 |
| ----------------- | --------------------------------------------------------------- |
| **Early Tenure**  | Customers who have been on the book for 3 months.               |
| **Late Tenure**   | Customers who are 3 months away from closing their loan.        |
| **Mid Tenure**    | All other customers.                                            |

### Borrower Segmentation by Ticket Size:

Distribute the data into 3 cohorts based on ticket size, ensuring that the sum of the pending amount in each cohort is approximately equal. Apply the following labels:

1. **Low Ticket Size**
2. **Medium Ticket Size**
3. **High Ticket Size**

At the end of this exercise, you should have more borrowers in the low ticket size category, while the sum of the amount pending should be approximately equal across all cohorts.

---

## Channel Spend Recommendations

DPDzero employs different channels to communicate with borrowers to encourage timely repayment. You are allowed to use the following resources:

### Communication Channels:

1. **WhatsApp Bot**: Cost: ₹5 per borrower.
2. **Voice Bot**: Cost: ₹10 per borrower.
3. **Human Calling**: Cost: ₹50 per borrower (use sparingly).

### Channel Efficiency:

- **WhatsApp Bot** works well for:
  1. Customers with excellent repayment behavior.
  2. Customers with first EMIs.
  3. Customers with low EMIs.

- **Voice Bot** works well when:
  1. The customer knows Hindi or English:
     - Metropolitan areas have a higher probability of English speakers.
     - Borrowers with low interest rates are also typically English speakers.
     - Some states have a higher prevalence of Hindi-speaking borrowers.
  2. The customer has low bounce behavior.
  3. The customer has low or medium-sized EMIs.

- **Human Calling** can be used in all scenarios but is the costliest option and should be used only when absolutely necessary.

---


   - Any other interesting insights derived from the data.




---

