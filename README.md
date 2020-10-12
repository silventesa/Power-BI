# _FOOD ON THE GO_ DATASET

This dataset belongs to a **food on the go platform** providing online meal deliveroo services. 

The datasets contain information about 3 big and interrelated blocks, namely the **restaurants** delivering food, the **orderings** and the **customers**.

We are asked to get interesting insights from the data that can be informative to clients, which can be either the restaurant holders, the customers or the platform holders.


## For whom?

- [ ] Restaurants
- [ ] Customers
- [ ] Food on the go platform


## What?

## Actions?

___

## Brainstorming

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
