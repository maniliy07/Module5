# Module5

### Required Assignment 5.1: Will the Customer Accept the Coupon?

https://github.com/maniliy07/Module5/blob/main/prompt.ipynb

**Context**

Imagine driving through town and a coupon is delivered to your cell phone for a restaurant near where you are driving. Would you accept that coupon and take a short detour to the restaurant? Would you accept the coupon but use it on a subsequent trip? Would you ignore the coupon entirely? What if the coupon was for a bar instead of a restaurant? What about a coffee house? Would you accept a bar coupon with a minor passenger in the car? What about if it was just you and your partner in the car? Would weather impact the rate of acceptance? What about the time of day?

Obviously, proximity to the business is a factor on whether the coupon is delivered to the driver or not, but what are the factors that determine whether a driver accepts the coupon once it is delivered to them? How would you determine whether a driver is likely to accept a coupon?

**Overview**

The goal of this project is to use what you know about visualizations and probability distributions to distinguish between customers who accepted a driving coupon versus those that did not.

**Data**

This data comes to us from the UCI Machine Learning repository and was collected via a survey on Amazon Mechanical Turk. The survey describes different driving scenarios including the destination, current time, weather, passenger, etc., and then ask the person whether he will accept the coupon if he is the driver. Answers that the user will drive there ‘right away’ or ‘later before the coupon expires’ are labeled as ‘Y = 1’ and answers ‘no, I do not want the coupon’ are labeled as ‘Y = 0’.  There are five different types of coupons -- less expensive restaurants (under \$20), coffee houses, carry out & take away, bar, and more expensive restaurants (\$20 - $50).

** Data Description **
Keep in mind that these values mentioned below are average values.

The attributes of this data set include:
1. User attributes
    -  Gender: male, female
    -  Age: below 21, 21 to 25, 26 to 30, etc.
    -  Marital Status: single, married partner, unmarried partner, or widowed
    -  Number of children: 0, 1, or more than 1
    -  Education: high school, bachelors degree, associates degree, or graduate degree
    -  Occupation: architecture & engineering, business & financial, etc.
    -  Annual income: less than \\$12500, \\$12500 - \\$24999, \\$25000 - \\$37499, etc.
    -  Number of times that he/she goes to a bar: 0, less than 1, 1 to 3, 4 to 8 or greater than 8
    -  Number of times that he/she buys takeaway food: 0, less than 1, 1 to 3, 4 to 8 or greater
    than 8
    -  Number of times that he/she goes to a coffee house: 0, less than 1, 1 to 3, 4 to 8 or
    greater than 8
    -  Number of times that he/she eats at a restaurant with average expense less than \\$20 per
    person: 0, less than 1, 1 to 3, 4 to 8 or greater than 8
    -  Number of times that he/she goes to a bar: 0, less than 1, 1 to 3, 4 to 8 or greater than 8
    

2. Contextual attributes
    - Driving destination: home, work, or no urgent destination
    - Location of user, coupon and destination: we provide a map to show the geographical
    location of the user, destination, and the venue, and we mark the distance between each
    two places with time of driving. The user can see whether the venue is in the same
    direction as the destination.
    - Weather: sunny, rainy, or snowy
    - Temperature: 30F, 55F, or 80F
    - Time: 10AM, 2PM, or 6PM
    - Passenger: alone, partner, kid(s), or friend(s)


3. Coupon attributes
    - time before it expires: 2 hours or one day
  
 **Based on the data analysis, several key hypotheses emerge regarding the characteristics of drivers who accept bar coupons:**

1. Behavioral Habit is the Primary Driver
The strongest predictor for accepting a bar coupon is the driver's existing habit. Drivers who visit bars more than three times a month accepted coupons at a rate of 76.88%, compared to only 37.06% for those who go less frequently.

**Hypothesis:** Bar coupons do not necessarily "create" new customers from non-bar-goers; instead, they are highly effective at incentivizing existing customers to visit again or perhaps choose a specific venue over another.

2. Social Context and Life Stage
Drivers without children in the car and those who are not widowed showed significantly higher acceptance rates. Furthermore, the combination of being a frequent bar-goer and being over the age of 25 (69.52%) or under the age of 30 (as part of the combined group) indicates a "socially active" demographic.

**Hypothesis:** The "Bar" coupon is viewed as a social/leisure tool. The presence of children acts as a logistical barrier to acceptance, while younger or socially active adults are more likely to view the coupon as an opportunity for a planned or spontaneous social outing.

3. The "Value-Seeking Socializer" Profile
The analysis showed that individuals who frequent cheap restaurants (more than 4 times a month) and have lower incomes (<$50k) also show a higher propensity to accept bar coupons.

**Hypothesis:** There is a specific segment of the population that is price-sensitive but socially active. These individuals are motivated by "value" and are more likely to utilize coupons to maintain their social lifestyle while staying within a budget.

4. Occupational and Demographic Stability
Drivers in professions like farming, fishing, or forestry were less likely to accept these coupons.

Hypothesis: Urban or office-based workers may have more access to bars or a social culture that revolves around "happy hours" compared to those in more rural or physically demanding manual labor occupations, making them a more receptive target for bar-related marketing.

**Summary Hypothesis**
The ideal candidate for a bar coupon is a regular bar-goer, likely between the ages of 21 and 35, who is currently driving without children and possesses a lifestyle that already incorporates frequent social dining (even at cheaper venues). Marketing efforts are most effective when targeting people based on their existing routines rather than trying to convert those who rarely visit such establishments.
