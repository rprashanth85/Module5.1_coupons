# Module5.1_coupons


# Link 
  https://github.com/rprashanth85/Module5.1_coupons.git


# Overview
The goal of this project is to use what you know about visualizations and probability distributions to distinguish between customers who accepted a driving coupon versus those that did not.


# Data
This data comes to us from the UCI Machine Learning repository and was collected via a survey on Amazon Mechanical Turk.


# Data Investigation 
  
  1.  Data Description:
      - Checking for mean, standard deviation, minimum, and maximum statistics on numerical columns to identify useful columns for data modeling.
  2.  isNull Check:
      -  Removing rows or columns with excessive null values as they are not useful for training a model.
  3.  Data Duplication:
      - Identifying genuine duplicates.
  4.  Data Merge:
      -  Exploring possibilities to merge columns or values within columns.
  5.  Heat Map:
      -  Analyzing correlations and relationships between variables to avoid redundancy and highlight significant correlations.
    

# Actions on Data Investigation

  1.  Column Drop:
      - 'car': Contains over 95% null values, hence not useful for the model.
      - 'direction_opp': Inverse of 'direction_same' column. These columns are boolean like; thus, one can be removed.
  2.  Replacing / Merging Column Values:
       - After dropping 'direction_opp', replaced 1 with “Same” and 0 with “Opposite”.
       - Merged “never” and “less1” values in any column value.
       - Replaced “below21” with 20 and “50plus” with 50 for 'age'.
  3.  Object to Numeric Conversion:
      - Converted age to a numeric field for faster filtering performance.
    

# Data Visualization

  1.  Libraries Used:
      - Plotly, Seaborn, Matplotlib, Pandas, IPython display.
  3.  Plots used for analysis.
      -  Subplots, Bar, Histogram and Pie Plots to compare drivers.
  3.  Display:
      -	Used display image function where Plotly visualizations were employed.


# Bar Chart Analysis and Hypothesis

  1.  Out of 12684 rows, only 2017 rows had bar coupons, around 15% of the total dataset.
  2.  Fn that 15% only 41% accepted the coupon.
  3.  Drivers visiting bars 3 or fewer times a month accepted the coupon more than those visiting more than 3 times, with a difference of around 100 drivers.
  4.  Little difference in coupon acceptance rate between drivers who frequent bars more than once a month and those over 25 years old (0.695 vs. 0.670 acceptance rates).
  5.  Moderate difference in acceptance rate between drivers who frequent bars more than once and have no child passengers and those not in farming, fishing, or forestry occupations (0.713 vs. 0.377 acceptance rates).
  6.  No significant acceptance rate difference between drivers who (go to bar more than once a month and passangera not kids and not Widowed) OR (go to bar more than once in a month and age under 30 ) OR (go to cheap restaurant more than 4 times a month and income less than 50K ) to all others. Acceptance rates are 0.605 and 0.543
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

