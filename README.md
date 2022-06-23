# **[Project 1: Gained and Lost Costumers ](https://github.com/ichiisti/gl)**

*Objectives:*

1. Calculation / aggregation of yearly quantity for gained and lost customers.
2. Tracking churn rate for B2C customers.
3. Highlight net/gained/lost quantity for B2B customers.
4. Tracking main competitors for B2C and B2B customers.

*Calculation frequency:* 
Calculation is done on monthly basis for B2C ( business to consumer) and B2B ( business to business) consumers.

*Data source:* 
excel files

*Data processing:*
1. Import: data sources are uploaded to database using the ETL script.
2. Database : in the database the informations are organized on 3 levels\
          1. level 1 - interface tables / raw data\
          2. level 2 - calculation / aggregate data\
          3. level 3 - data set table for analysis
3. Data processing : for B2C costumers yearly quantities are calculated taking into account the county and historical data, for B2B clients the volumes are calculated taking into account historical data. Data processing is done using the T-SQL procedures. During data processing messages are inserted into log table.

# **[Project 2: Realised Gross Margin Calculation ](https://github.com/ichiisti/rgm_v1)**

*Objectives:*
1. Acqusisiton cost allocation on customer / hourly level, by using allocation keys. 
2. Monthly cost calculation on costumer level based on hourly data. 
3. Gross margin calculation on costumer level based on income, acqusition cost and fixed cost. 

*Calculation frequency:* Calculation is done on monthly basis for B2B ( business to business) consumers. 
*Data source:* excel / flat files / database.

*Data processing:*
1. Import: upload / get data from data sources
2. Database : in the database the informations are organized on 3 levels\
          1. level 1 - interface tables/raw data. Bulk load data with minimal validations. Data validation is done with the help of stored procedures and errors are inserted into "vf" ( verification ) table type.\
          2. level 2 - intermediat calculation/aggregate data  are inserted into "calc" table type.\
          3. level 3 - final dates are organized into "md" table type (dimension and fact table used for creating data models in BI )
3. Data processing : data processing is done using T-SQL procedures. During data processing messages are inserted into log table.
