# Codebook for stress test analysis in the United States

**_S. Haque & S. Bechor_**

**_January 16, 2022_**

This document reports the codebook for the data used in the Stress Test Analysis of Loans to Corporations & Households in the United States. The dataset contains 16 indicators.

The collected data is in the form of time series and spans the period from 1994 Q4 to 2020 Q3. The number of observations is 104. The data is extracted from the sources Federal Reserve Economic data (FRED) and Federal Deposit Insurance Corporation (FDIC). The ID of the indicators are labeled according to the sources. The Description column defines each indicator and its source in square brackets [ ].

All indicators are recorded on a ratio scale, where the indicators are recorded as either percentage, US dollar value or index value. Note that three of the indicators (NPL in corporate sector, NPL in Household sector, Debt Ratio) are calculated by us and therefore described as “Authors’ calculation” in the Description. In addition, note that only the indicators that have a name in the Coding-column are the ones that are included in the analysis conducted in R.

### Bank-specific and Macroeconomic variables for the study
| | ID | Name  | Description | Measurement  | Frequency | Coding  |
| :---: | ------------- | ------------- | ------------- | ------------- | ------------- | ------------- |
| 1  | CPALTT01USM657N  | Inflation  | Consumer Price Index: Total All Items for the United States. [FRED, Economic Data] | Percent  | Quarterly | US_Inf  |
| 2  | FEDFUNDS  | Interest rate  | The federal funds rate is the interest rate at which depository institutions trade federal funds (balances held at Federal Reserve Banks) with each other overnight. [FRED, Economic Data] | Percent  | Quarterly | US_NomInt  |
| 3  | GDPC1  | Real GDP  | Real gross domestic product is the inflation adjusted value of the goods and services produced by labor and property located in the United States. [FRED, Economic Data] | USD  | Quarterly | US_GDP  |
| 4  | RBUSBIS  | Real exchange rate  | Real effective exchange rates are calculated as weighted averages of bilateral exchange rates adjusted by relative consumer prices. [FRED, Economic Data] | Index 2010=100  | Quarterly | US_RealEx  |
| 5  | UNRATE  | Unemployment rate  | The unemployment rate represents the number of unemployed as a percentage of the labor force. Labor force data are restricted to people 16 years of age and older, who currently reside in 1 of the 50 states or the District of Columbia, who do not reside in institutions (e.g., penal and mental facilities, homes for the aged), and who are not on active duty in the Armed Forces. [FRED, Economic Data] | Percent  | Quarterly | US_Unemp  |
| 6  | QUSCAMXDCA  | Total credit to nonfinancial sector  | The total credit volume. The "private non-financial sector" includes non-financial corporations (both private-owned and public-owned), households and non-profit institutions serving households as defined in the System of National Accounts 2008. Captures the outstanding amount of credit. [FRED, Economic Data] | USD  | Quarterly | |
| 7  | QUSHAMUSDA  | Total credit to household and NPISH  | Total Credit to Households and Non-Profit Institutions Serving Households, Adjusted for Breaks, for United States. [FRED, Economic Data] | USD  | Quarterly | |
| 8  | QUSNAMUSDA  | Total credit to corporate  | Total Credit to Non-Financial Sector, Adjusted for Breaks, for United States. [FRED, Economic Data] | USD  | Quarterly | |
| 9  | | NPL in corporate sector  | The fraction of corporate credit to the total credit volume have been combined with the insolvency rate (i.e. debt ratio). [Authors' calculation] | Percent  | Quarterly | US_NPL_Corp  |
| 10  | | NPL in Household sector  | The fraction of household credit to the total credit volume have been combined with the insolvency rate (i.e. debt ratio). [Authors' calculation] | Percent  | Quarterly | US_NPL_House  |
| 11  | | CAR  | Total capital to risk-weighted.  [FDIC, State Tables] | Percent  | Quarterly | US_CAR  |
| 12  | TLBACBW027SBOG  | Total Liabilities  | Total Liabilities, All Commercial Banks. [FRED, Economic Data] | USD  | Quarterly | |
| 13  | USROA  | ROA  | Return on Average Assets for all U.S. Banks. [FRED, Economic Data] | Percent  | Quarterly | US_ROA  |
| 14  | USROE  | ROE  | Return on Average Equity for all U.S. Banks. [FRED, Economic Data] | Percent  | Quarterly | US_ROE  |
| 15  | USTAST  | Total Assets  | Total Assets for Commercial Banks in United States. [FRED, Economic Data] | USD  | Quarterly | US_BankSize  |
| 16  | | Debt Ratio  | Total liabilities to total assets [Authors' calculation] | Percent  | Quarterly | US_DebtRatio  |
