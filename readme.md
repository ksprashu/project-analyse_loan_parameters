# Loan Data Exploration
## by Prashanth Subrahmanyam


## Dataset

The loan data set provided by prosper contains data for upwards of 110K loans, with 81 variables about each loan such as loan amount, interest rate, loan status, borrower income and so on. Some of these variables are applicable for loans originated before 2009, whereas some other variables are relevant for loans originated post July 2009.

Also it can be seeing that about 50% of the loans are in closed state. 

As there are 81 variables about a given loan, it might not be possible to analyse every one of these variables and hence it makes sense to pose a few questions to determine which might be the variables of interest and filter out the rest.

The question we selected to answer was what determines the interest rate (APR) provided? 

Before proceeding we tried to remove data that seemed of bad quality (missing data / NaNs) without reducing the overall dataset size. Some of the data could still be analyzed while some of the columsn had NaNs, so this was left as is. Some variables like monthly income were rounded off into integers for better analysis. Credit Score which was a range was averaged and used for simplifying analysis. Categorical data that was sequential, like Credit Ratings and Quarters, was converted into types so that the visualizations would show them in the right order.

Finally the data was saved to a file so that it could be reused without wranging.


## Summary of Findings

The BorrowerAPR was generally normally distributed. A clear distribution was observed without having to do any sort of transformations. What was unusual in this distribution was that there was a rather large peak at about 0.36 that was standing out within this otherwise normal distribution.

Most of the other distributions were right skewed. The distributions of Employment Status duration, Debt to Income ratio, and Loan Original Amounts were better visualized when a log transformation was done of the data. None of the other data needed any sort of transformation to analyse. The range of Average Credit Score, Monthly Income, and Debt to Income ratio was limited so as to cover 95% of the population. The entire range of data caused the distributions to be too skewed to meaninfully analyze. Distribution of Credit Ratings and Home Owner status was definitely surprising to me and was much different from what I had initially expected.

There were some very obvious trends that BorrowerAPR reflected. As expected the BorrowerAPR was inversely correlated to increasing Credit Scores or Credit Ratings. BorrowerAPR also seemed to be correlated to the Loan Original Amount and as the Loan amounts got larger, the APR showed a reducing trend. APR vs Income was showing some sort of a trend, so it might be worthwhile plotting it in relation to other variables.

Borrowers who who have higher incomes, seem to have a higher appetite for credit and these individuals show an increasing trend in the number of Credit Lines they have as well as they tend to take larger Loan Amounts as loans. 

Some very obvious relations we see are high incomes relate to taking bigger loans - this would be due to the capacity to pay off bigger loans. We see high credit ratngs related to higher loans - this might be in part to higher loans being offered to more credit worthy individuals. Part time employees have the lowest of all incomes, lowest amounts of loans taken, as well as lowest number of credit lines which makes a lot of sense, however they are on an average credit worthy. Tne relation of homeowners with credit ratings is very interesting as well seeing that higher credit ratings is more strongly correlated with being a homeowner.

Employment status and LoanOriginationYear shows some interesting relationships. Some Employment statuses were only active in certain year and not in other years. This probably shows that some data is not tidy. The lack of any relationship of certain data fields was very interesting. Being a homeowner had no impact on anything. I expected more credit lines to have a negative impact on risk, but this was negated by high monthly incomes. Loan amounts taken show a relationship to the year in which it was taken, generally showing an increasing trend. Lower credit ratings either don't get larger credit lines, or can't afford it. Higher credit ratings don't seem to need larger credit lines, if at all.


## Key Insights for Presentation

- The overwhelming relation of APR was to Credit Ratings. 
- A second factor was to the Year in which the loan was taken. 
- To much lesser effect, the APR was related to the monetary figures of loan amount. 
- APR was suprisingly not related to Employment Status, or being a Home Owner.


## Resources
- [Pandas] (https://pandas.pydata.org)
- [Matplotlib] (https://matplotlib.org/)
- [Seaborn] (https://seaborn.pydata.org/index.html)
- [Udacity] (https://in.udacity.com/course/data-analyst-nanodegree--nd002)
- [Stackoverflow] (https://stackoverflow.com/)
- [Prosper] (https://www.prosper.com)
