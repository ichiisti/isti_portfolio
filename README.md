# **[Project 1: Gained and Lost Costumers ](https://github.com/ichiisti/gl)**

*Objective:*

To monitor business performance, systematically analyze customer dynamics by calculating yearly gains and losses, tracking B2C churn rate, evaluating net changes in B2B customer base, and monitoring key competitors in both B2C and B2B markets.


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

# **[Project 3: Estimated Gross Margin Calculation ](https://github.com/ichiisti/pgm)**

*Objectives:*

1. Estimated acqusisiton cost allocation on customer / hourly level for short / middle termn, by using allocation keys
2. Monthly cost calculation on costumer level based on hourly data. 
3. Gross margin calculation on costumer level based on income, acqusition cost and fixed cost. 
4. Gross margin simulation for three scenarios
5. Calculate quantity deviation ( gained, lost and existing costumers)
6. Contracted quantites for short and middle term

*Calculation frequency:* Calculation is done on quarterly basis for B2B ( business to business) and B2C ( business to costumers)\
*Data source:* excel / flat files / database.

*Data processing:*
1. Import: upload / get data from data sources
2. Database : in the database the informations are organized on 3 levels:\
          1. level 1 - interface tables / raw data. Bulk load data with minimal validations. Data validation is done with the help of stored procedures and errors are inserted into "vf" ( verification ) table type.\
          2. level 2 - intermediat calculation / aggregate data  are inserted into "calc" table type.\
          3. level 3 - final dates are organized into "md" table type (dimension and fact table used for creating data models in BI )
3. Data processing : data processing is done using T-SQL procedures. During data processing messages are inserted into log table.

# **[Project 4: EtL process for flat files ](https://github.com/ichiisti/EtL_process)**

*Objectives:*

1. Retrieve all the required data from source files and load into database.

*Calculation frequency:* Calculation is done on monthly basis for B2C ( business to consumer) and B2B ( business to business) consumers.\
*Data source:* flat files.

*Data processing:*
1. Extract: get all the necessary information from source files.
2. Transform : "lite" transformation stage.\
3. Load : the newly prepared data is loaded into the database.

