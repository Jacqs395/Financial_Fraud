# Financial_Fraud

Which insights did you gain from your EDA? 

How did you determine which columns to drop or keep? If your EDA informed this process, explain which insights you used to determine which columns were not needed. 
    In my initial EDA, I decided to drop "step", "nameOrig" and "nameDest". As I was performing EDA on various columns, I decided that I was not really interested in the "step" data. Analyzing "isFraud" clearly showed that most fraudulent activities were occuring in two specific transaction types: transfers and cash_out. The timeframe of when the fraud occurred was not important to me. I was also not interested in the name of the origin account, or the name of the destination account. What mattered most was the type of transactions where fraud was prevalent, and also the amount. 