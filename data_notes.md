# Notes on data

**! TO BEAR IN MIND**

Data files have been "cut" to 2000 rows. This particularly affects the total available information we have for each variable. So far, we know that:

- For **RESTAURANTS**: if we want to go deeper with restaurants and their orderings, we need to restrict the RESTAURANT_ID to the one in the ORDER.csv table (for us, ORDER_DateTime.csv). 

- For **CUSTOMERS**: EACH time that we want to speak about customers' characteristics (=so, if we need to access the info in ORDER_DateTime.csv table), we need to FIND THE INTERSECTION of the CUSTOMER_ID between the CUSTOMER.csv table and the table of interest (ORDER.csv or ALLERGY_CUSTOMER.csv). However, if we want to relate only ALLERGY_CUSTOMER.csv and ORDER.csv (and we ARE NOT interested in any customers' characteristic, but just in absolute numbers -e.g., number of orderings x allergic customer-), then we need to use CUSTOMER_ID in ORDER_DateTime.csv as reference.

- For **ORDER ID**: there are 1999 ordering IDs (ID in ORDER table), but in the ORDER_ITEM table, there are only 733 different ORDER_IDs. Therefore, if we want to relate the ORDER_ID with ORDER_ITEM, we will need to filter the query at the first 733 ORDER_IDs.

