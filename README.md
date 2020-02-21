# Bank Loan Classifier

A bank wants to automate their loan approval process.  They have provided a semi-anonymized dataset containing 606 successful and 76 not successful loans along with their information and transactions. These loans are for existing clients. This could be used to pre-approve existing customers and market to them accordingly.

This analysis looks into a dataset from a Czech bank. The goal here is to produce a model that can predict whether client is high-risk for a bank loan.

Original with the data dictionary: [link](https://sorry.vse.cz/~berka/challenge/pkdd1999/berka.htm)

Overview of the results: [link](/Loan_Model_Slides.pdf)


## Prerequisites

All notebooks are written in Python 3. 

The libraries that are used in this notebook are listed under the `requirements.txt` file. One can simply issue to following command to insure the proper libraries are installed:

```bash
pip3 install -r requirements.txt
```

## Description of Analysis

All Ancillary tables were merged onto the loan data to be used as features. A Random Forest Model was used to classify good and bad loans. A SVM and Logisitic Regression Model were also created for comparison. Models were also created on just Small and Big Loans. Classifiers were then used to determine which of the remaining customer should be preapproved for loans. Shap Values were used to assess feature importance after modelling. 


## Figures

### Loan Analysis

![Amount Histogram](/png_files/Amount_Histogram.png)

![Loan Types](/png_files/Loan_Size_Type_Distribution.png)

![Money Remaining_1](/png_files/Loan_Remaining_To_Be_Paid.png)

![Money Remaining_2](/png_files/Loan_Remaining_To_Be_Paid_Small.png)


### Classifications

![Model Compare](/png_files/model_compare.png)

#### Shapely Values for RF model

![RF Shaply Values](/png_files/Shap_Values_RF_1.png)

#### Shapely Values for RF model (Small Loans Only < $100000)

![RF Shaply Values](/png_files/Shap_Values_RF_Small.png)

#### Shapely Values for RF model (Large Loans Only >$100000)

![RF Shaply Values](/png_files/Shap_Values_RF_Big.png)
