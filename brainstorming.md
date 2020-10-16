# Brainstormings

## LAST MINUTE


**! TO BEAR IN MIND**

Data files have been "cut" to 2000 rows. This particularly affects the total available information we have for each variable. So far, we know that:

- For **RESTAURANTS**: if we want to go deeper with restaurants and their orderings, we need to restrict the RESTAURANT_ID to the one in the ORDER.csv table (for us, ORDER_DateTime.csv). 

- For **CUSTOMERS**: EACH time that we want to speak about customers' characteristics (=so, if we need to access the info in ORDER_DateTime.csv table), we need to FIND THE INTERSECTION of the CUSTOMER_ID between the CUSTOMER.csv table and the table of interest (ORDER.csv or ALLERGY_CUSTOMER.csv). However, if we want to relate only ALLERGY_CUSTOMER.csv and ORDER.csv (and we ARE NOT interested in any customers' characteristic, but just in absolute numbers -e.g., number of orderings x allergic customer-), then we need to use CUSTOMER_ID in ORDER_DateTime.csv as reference.

- For **ORDER ID**: there are 1999 ordering IDs (ID in ORDER table), but in the ORDER_ITEM table, there are only 733 different ORDER_IDs. Therefore, if we want to relate the ORDER_ID with ORDER_ITEM, we will need to filter the query at the first 733 ORDER_IDs.

___

Given the data about orderings provides information for just two months (April and May 2017), a narrower question that is in line with a narrow period of time seems to be more appropriate. 

#### Exploring the effects of opening hours

Example of a question to restaurants: _How many orderings are you missing because of your opening hours?_

##### STEP 1

_The pick of orderings happened on (day of the week) between (hour) and (hour) and costumered spent a mean of (amount) per order (for April and May 2017)_

To fill the sentence, we need first to identify:

1. _Which are the days (Mo-Sun) with highest amount of orderings?_ **Works on it: Opap's**

2. _At which time slot **more orderings** are made?_ ORDER table: ID, Creation Date **Works on it: Orhan**

    2.1. _How many items are ordered in this time slot?_ Number of items per order. Get mean and std.
  
    2.2. _What is the total price of orderings made at this time slot?_ Total price of ordering. Get mean and std.

Questions from 1 to 2 can be analysed from a **top-down approach**, so we'll have data for:
- global/ general
- cities
- if relevant, streets.

**Result of STEP 1: gold time slot for global and city perspective.**

##### STEP 2

Now that we have the information about the best moment for orderings, we could go further into Restaurant and Customers characteristics. 

**Customers**

- Characterise curstomers in this gold time slot: age, gender, (language?), allergies (quantity and severity). Works on it: **Opap's**

**Restaurants**

- Characterise restaurants: items that are more ordered and price. Works on it: **Orhan**
___

## Day 2_First brainstorming

* Client: Platform holders. 
	What would be the main targets they would be interested in?
	- Adds in cities
	- Adds to customers
		- gender
		- language : dutch & english
		- allergies 

* Top-down approach: from more general (dashboard) to more specific (pages)
	Filters:	
		- cities
		- gender
		- creation date: check the oldest
		- price 
		- opening hours
		- allergy
			* allergy type
			* allergy severity

* Possible big topics:
	- CUSTOMER LOYALTY
	- BETTER BUSINESS EXPANSION (geographical part matters)
		* Should the platform target more restaurants in one city than in others?
		* What are the best customers?
	- BETTER SERIVCE TO CLIENTS (here, restaurants)
		* Should you higher/lower your price?
		* Should you add more allergy-dree dishes (taking into account the number of allergies in your city/street?)

Opap's brainstorming

- Display calendar with customer birthdays: take benefit of it for adds --> FUTURE ACTIONS MADE BY THE COMPANY
- Growth of number of customers and restaurants throughout time --> GROWTH OF THE COMPANY
- For restaurants: % of orderings they are missing because of their opening hours
	* Do your customers order outside when you're closed?
	* Price: is it price a barrier for customers to order other items? Are restaurants too cheap? Too expensive?
- Insights on the most ordered dish in each restaurant
- Number of orderings x customer
- Number of items x ordering x customer

Orhan's brainstorming

- Which streets have the highest customer/restaurant counts?

___

## Day1_Draft: example of questions

### TABLES

#### T1: RESTAURANTS

#### T2: ORDER

##### Getting know restaurants

1. _Insights on the ordering rates by city_
2. _Insights on the ordering rates by opening-hours_


##### Getting know customers
1. _Number of ordering per customers_
   
    - Relationship between customers and ordering items (e.g., do those that consume the most share similar tastes?)
    

2. _Identifying the dreamed customers_

What is better (= more economically wortwhile), a customer with more commands but less items or viceversa?
    
- **Top10**: Which and how are the best customers? How many are there? Fix a threshold (percentile?)
        - Gender
        - City
        - Age
        - Language (?)
    
- **Customers loyalty**: Among best customers, how is their relationship with restaurants? Do they often repeat in the same restaurant or do they prefer variety? 
        * If they prefer repeating, do they always order the same?
        * If they do NOT repeat in the same restaurant, do they stay in the same city though?

   
#### T3: ORDER TABLES

1. _Freak idea_

- Check for restaurants or order table names containing "vege" or "vegg" (vegetarian, veggie, etc.) and relate it with customer profiles.

#### T4: ORDER ITEMS


#### T5: CUSTOMER

#### T6: CUSTOMER ALLERGIES

1. Gradient of allergies and number of orderings
    - Do customers with allergies order less than customers with allergies? (allergies vs. non-allergies)
    - Do customers with less allergies order more than customers with more allergies? (+/- num of allergies)
    - Do customers with less SEVERE allergies order more than customers with more severe allergies? (+/- severity of allergies)
    
    1.2. Do age or gender play a role in this relationships? 
    - Here it would be important to control for the effect of age; for example, younger people could be more prone to online deliveroos than older people. 
