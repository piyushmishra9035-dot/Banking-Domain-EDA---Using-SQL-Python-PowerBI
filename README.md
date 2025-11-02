# 🏦 Banking Dashboard (Power BI Project)

## 📌 Problem Statement  
The main goal of this project is to develop a **basic understanding of risk analytics** in banking and financial services, and to understand **how data can be used to minimize financial risk** while lending to customers.

---

## 💡 Solution  
Using **Power BI’s latest data visualization tools**, interactive dashboards were created to help banks make **data-driven decisions** — such as determining whether an applicant is likely to repay a loan before approving it.  

These dashboards provide insights into **client profiles, deposits, loans, and engagement**, enabling efficient risk management and better decision-making.

---

## 📊 About the Dataset  
The dataset contains detailed information about:
- Banking Relationship  
- Client-Banking  
- Gender  
- Investment Advisor  
- Period  

All tables are interconnected through **primary and foreign keys**, forming a relational data model.

---

## 🧹 Data Cleaning & Transformation  

Performed in Power BI using Power Query and DAX:

1. **Engagement Timeframe** → Created a new column showing clients’ engagement duration with the bank.  
2. **Engagement Days** → Calculated number of days a client has been with the bank.
3.  Income Band → Created bins for Estimated Income:

< 100000 → Low

< 300000 → Mid

4. Processing Fees → Created based on fee structure:
IF('Clients - Banking'[Fee Structure] = "High", 0.05)

🧮 Key DAX Calculations
🔹 SUM
Bank Deposit = SUM('Clients - Banking'[Bank Deposits])

🔹 DISTINCTCOUNT
Total Clients = DISTINCTCOUNT('Clients - Banking'[Client ID])

🔹 SUMX
Total Fees = SUMX('Clients - Banking', [Total Loan] * 'Clients - Banking'[Processing Fees])

🔹 DATEDIFF
Engagement Days = DATEDIFF('Clients - Banking'[Joined Bank], TODAY(), DAY)

📊 Dashboards & Visualizations
🏠 Home Dashboard

Overview of all major KPIs

Filters for period, gender, and client type

💰 Loan Analysis Dashboard

Visual breakdown of loans by type, gender, and client category

Helps identify high-risk clients

💵 Deposit Analysis Dashboard

Deposits by account type and client demographics

Highlights investor groups with maximum deposits

📑 Summary Dashboard

Consolidated overview of all metrics

Helps stakeholders make quick data-driven decisions

🧠 Conclusion

With the help of Power BI dashboards, banks can:

Assess loan repayment risks before approval

Understand customer engagement trends

Track loans, deposits, and business lending effectively

Make smarter, faster, and data-backed decisions

🚀 Future Work

Add predictive models to estimate loan default probability

Integrate real-time banking APIs for live data updates

Compare public vs private banks for client strategy insights

Analyze nationality-wise loan trends for deeper understanding

🧰 Tools & Technologies

Power BI – Dashboard creation and data modeling

DAX – Data analysis expressions

Power Query – Data transformation

Excel / CSV – Raw data source

📷 Dashboard Preview
🏠 Home Dashboard

Overview of all major KPIs

Filters for period, gender, and client type

💰 Loan Analysis Dashboard

Visual breakdown of loans by type, gender, and client category

Helps identify high-risk clients

💵 Deposit Analysis Dashboard

Deposits by account type and client demographics

Highlights investor groups with maximum deposits

📑 Summary Dashboard

Consolidated overview of all metrics

Helps stakeholders make quick data-driven decisions

🧠 Conclusion

With the help of Power BI dashboards, banks can:

Assess loan repayment risks before approval

Understand customer engagement trends

Track loans, deposits, and business lending effectively

Make smarter, faster, and data-backed decisions

🚀 Future Work

Add predictive models to estimate loan default probability

Integrate real-time banking APIs for live data updates

Compare public vs private banks for client strategy insights

Analyze nationality-wise loan trends for deeper understanding

👤 Author

Piyush Kumar Mishra
🎯 Data Analyst | Power BI Developer | Excel Enthusiast



   ```DAX
   Engagement Days = DATEDIFF('Clients - Banking'[Joined Bank], TODAY(), DAY)
