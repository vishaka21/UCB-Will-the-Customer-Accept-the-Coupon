# Will the customer accept the coupon?
### Problem Statement
Will a customer accept the coupon?

Consider a marketing campaign where drivers are sent coupons to their cell phone for a nearby dining establishment.
We will answer the question of what factors impact whether a customer accepts the coupon.

Jupyter notebook used for this analysis is located here: 

### Approach
This analysis is broken into two segments:
1. A guided prompt, where I will answer specific questions about the data
2. An independent investigation based on a coupon type that I find interesting. I have chosen this based on the results of my exploratory analysis

Note that the Results, Recommendations, and Next Steps in this report come from the 2nd part of the assignment--the independent investigation.

Using my work from step 1 as motivation, I selected the coupon category "Carry out and Take away" for further investigation (note that I will sometimes refer to this coupon category as "Takeout").
My reasoning was that drivers, by the nature of the fact that they are outside of the home and driving, would more likely accept more conveninet coupons. I believed this applied not only to attributes that implied convenience (like less distance from driver), but also the coupon category itself, because Takeout is a convenient way of dining. Also, a typical Takeout has parking or a drive-through of some sort, wich aligns with the activity of driving.

So building on this theme, I focused my exploratory data analysis on the attributes that I deemd to be related to convenience:
* Destination
* Passanger
* Weather
* Distance
* Direction

### Results
#### Overall
I did confirm my suspicion that the Takeout acceptance rate was the highest of all coupon categories, at 73.8%



#### Focused Attribute Investigation
Looking at the attributes I deemed to be related to convenience, they were mostly positively correlated to acceptance rate, but there was some mixed results as well.

__Destination__
When drivers were headed home or no urgent place, their acceptance rate was high, at 79% and 76% respectively, as opposed to work, which was 66%

__Passanger__
Friend(s) was the only value of passanger that exceeds the average acceptance rate for Takeaway, and Kid(s) was the lowest.
If "Friend(s)" or "Alone" can be associated with more freedom and less urgency than Kid(s) or Partner, then these results would suppor the theme.
However, we are speculating a bit here. It would be good follow-up to see how Passanger correlates to other relevant attributes.

__Weather__
Acceptance rate was clearly worse than average when the weather was poor. In fact it was 76.4% when the weather was Sunny.
Drivers definitely do not want to drive in poor weather.



__Distance__
Here's where my predisposition really begins to be challenged (along with direction). There is no consistency with acceptance rate as related to distance!
When the Takeout restaurant is GE15 minutes away, the acceptance rate is lower than average. However, when it is GE25 minutes away, the rate is higher!


__Direction__
In a major surprise, when the Takeout restaurant was in the direction the driver was headed, the acceptance rate was __lower__.

#### Other attributes
After finding some inconsistency with my targeted approach, I did review the acceptance rate by other attributes so that I could understand comprehensively what factors impact acceptance rate.
* Temperature: Higher acceptance rate when temperature is lower
* Time of day: Acceptance rate is higher in the late afternoon and evening than in the early morning.
* Age: No consistent pattern here
* Marital Status: Widowed had the highest acceptance rate, followed by Single. Divorced or living with a partner were all below the average acceptance rate of the coupon group
* Has children: No correlation
* Income: There seems to be an inverse relationship here. Lower incomes have higher acceptance rates than higher incomes.
* Education: Again, education is inversely correlated with acceptance rate. Meaning, acceptance rates were higher with lower levels of education attainment. It's not strictly increasing, but the general trend does exist, with the lowest level ("Some High School") having the highest acceptance rate, and the highest level ("Graduate degree") having the lowest acceptance rate.

#### Summary of findings
In this analysis, we determined that the coupon type with the highest acceptance rate was Carry out & Take Away, at 73.8%.

I surmised that this was due to the convenient nature of takeaways, relative to the fact that the consumer was already driving in their car.

There seems to be some evidence to support this, given that acceptance rate is much higher when
* the consumer is driving Home or Nowhere Urgent
* weather is good for driving (not hazardous)
* the driver is with Friend(s), the assumption being that if they are with friends then they are exercising free time and are not in a hurry

On the flip side, I would have expected that same direction and short distances to the Takeaway location would be very heavily correlated with higher acceptance rate, but the results were ambiguous!

### Recommendation
Takeout restaurants should target their coupons during days with nice weather, in the second half of the day.
They should also target individuals with lower incomes and lower levels of educational attainment.

### Next Steps
The analysis of direction and distance really deserves further investigation. I think statistical analysis, and not just exploratory data analysis, is needed to uncover the relationship of these variables with acceptance rate. This makes for a good future project.

There were a few other attributes that I reviewed high-level, but for which I did not perform a deep dive, like income and education. These were not part of my in-depth review because they were not related to my central task at hand, yielded interesting findings regarding their relation to acceptance rate, and merit a deeper dive. These would be good follow-ups if I wanted a comprehensive data exploration.
