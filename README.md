# Module5.1_coupons


# Link 
  https://github.com/rprashanth85/Module5.1_coupons.git


# Overview
The goal of this project is to use what you know about visualizations and probability distributions to distinguish between customers who accepted a driving coupon versus those that did not.


# Data
This data comes to us from the UCI Machine Learning repository and was collected via a survey on Amazon Mechanical Turk.


# Data Investigation 
  
  1.  Data Describe
      - checking for Mean, STD, Min and Max Statistics on numerical columns. Helpful to remove columns that are not useful for data modeling.
  2.  isNull Check
      -  More null rows/coulmns cannot be useful for training a model. Those rows or columns can be removed.
  3.  Data Duplication
      - To see if duplication is genuine.
  4.  Data Merge,
      -  To see if we can merge columns or values in columns.
  5.  Heat Map,
      -  To see correlation and relationship between variable. Helpful to avoid high redundancy. Also gives high and low correlation between variable.
    

# Actions on Data Investigation

  1.  Column Drop
      - 'car' : This column has more than 95% of the data as null. This will not provide any useful data for the model.
      - 'direction_opp' : This is inverse of 'direct_same' column. Also these 2 columns are like boolean value. Meaning, value 1 in 'direction_opp' would be 0 in 'direction_same'. Checked there are no NaN or Null values.
  2.  Replacing / Merging Column Values
       - After dropping 'direction_opp' column. Replaced 1 with value "Same" and 0 with value "Opposite".
       - In any column value "never" and "less 1" are same. Merged them with a common value.
       - For Age: replaced "below21" value as 20 and "50plus" as 50.
  3.  Object to Numeric
      - Converted Age to Numeric field.
      - Faster to filter performance.
    

# Data Visualization

  1.  Libraries used for analysis, investigation and Visualization
      - Plotly, Seaborn and Matplotlib, Pandas, IPython display.
  3.  Plots used for analysis.
      -  Subplots, Bar, Histogram and Pie Plots to compare drivers.
  3.  Used display image function in places where Plotly visualizations are used.


# Bar Chart Analysis and Hypothesis

  1.  Out of 12684 rows only 2017 rows had Bar Coupons. This is around 15% percent of the total data set.
  2.  On that 15% only 41% accepted the coupon.
  3.  Drivers who go to bar 3 or less times has accepted the coupon more than those went to bar more than 3 times in a month. The diffrence is around 100 drivers between the two category.
  4.  There is no much difference in coupon acceptance rate between the drivers who go to bar more than once a month and over the age of 25 to all others. Acceptance rates are 0.695 and 0.670 respectively.
  5.  And there is a mediocre difference between the acceptance rate of drivers who go to bar more than once and has no passanger as kids and also does occupation other than Farming, fishing or Forestry to all others. Acceptance rates are 0.713 and 0.377
  6.  Also there is no significant acceptance rate difference between drivers who (go to bar more than once a month and passangera not kids and not Widowed) OR (go to bar more than once in a month and age under 30 ) OR (go to cheap restaurant more than 4 times a month and income less than 50K ) to all others. Acceptance rates are 0.605 and 0.543
  7.  The analysis reveals that certain demographic and behavioral factors influence the acceptance of bar coupons, but the differences are not always substantial. Therefore, a nuanced marketing strategy that considers a combination of factors, such as age, social activity, family responsibilities, and occupation, might be more effective in increasing the acceptance rates of bar coupons. Further detailed analysis and segmentation could help in identifying more specific target groups and tailoring marketing efforts accordingly.


# Independent Investigation, Analysis and Hypothesis

Used a bar chart to explore what other coupon groups I can try to determine the characteristics of passengers (drivers) who accept the coupons. Based on the analysis Coffee House has a good data set

  1. **Age and Coupon Acceptance**
	  - Hypothesis: Drivers within the age range of 20-30 are the most likely to accept coffee house coupons, followed by drivers aged 30-35 and those above 50.
	  - Rationale: Younger drivers may have a higher propensity for social activities like visiting coffee houses, while older drivers might have different motivations, such as leisure time or established routines that include coffee consumption.

  2. **Travel Direction and Coupon Acceptance**
	  - Hypothesis: Drivers who are traveling in the opposite direction from their destination are more likely to accept coffee house coupons.
	  - Rationale: Drivers going in the opposite direction may have more flexibility in their travel plans, making them more open to detours such as stopping for coffee.

  3. **Time of Day and Coupon Acceptance**
	  - Hypothesis: Coffee house coupons are more likely to be accepted in the evening around 6 PM and the next most popular time is in the morning around 7 AM.
	  - Rationale: Evening coffee consumption might be linked to socializing after work or evening activities, while morning coffee is a common routine for starting the day.

  4. **Coupon Expiry and Usage**
	  - Hypothesis: Coffee house coupons with a 1-day expiry are 25% more likely to be used compared to those with a 2-hour expiry.
	  - Rationale: Longer expiry times provide more flexibility and convenience, leading to higher acceptance rates.


# Next Steps for Analysis

1. **Detailed Analysis of Travel Direction and Coupon Usage Time**
	- Objective: Understand how the direction of travel and the time of day influence coupon acceptance.
	- Action: Create cross-tabulations and visualizations to examine the relationship between travel direction, time of day, and coupon acceptance rates.
    
2. **Age and Occupation Analysis within a Specific Range**
	- Objective: Determine if certain occupations are more likely to accept coffee house coupons within the age range of 20-35.
	- Action: Filter the dataset to include only drivers aged 20-35 and create visualizations to compare coupon acceptance rates across different occupations.

