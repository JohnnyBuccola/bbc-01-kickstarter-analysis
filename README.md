# Kickstarting with Excel

## Overview of Project

### Purpose

To determine whether there is an optimal Kickstarter launch date and goal amount for theater campaigns that will lead to a successful outcome. This is done by filtering, charting, and analyzing raw Kickstarter data imported into Excel.

## Analysis and Challenges

### Analysis of Outcomes Based on Launch Date

<img src="Resources/Theater_Outcomes_vs_Launch.png" alt="Chart: Outcomes Based on Launch Date" height = "400"/>

One of our goals was to determine whether there was an ideal month of the year for a campaign to launch. The possible outcomes for a kickstarter (Successful, Failed, Cancelled) were counted up for each month of the calendar year across all years where data was available (2009-2017) by using an Excel PivotChart, filtered by the "Theater" category. Because dates were retrieved in a Unix format, they had to be converted to a standardized `DD/MM/YYYY` format to be able to extract the month.  This would have been a challenge if it weren't for Excel's nifty conversion tool.  The resulting line plot can be seen above.

### Analysis of Outcomes Based on Goals

<img src="Resources/Outcomes_vs_Goals.png" alt="Chart: Outcomes Based on Goal Amounts" height = "400"/>

Because Kickstarters will only be funded if the goal is met, it's important that a reasonable goal is set.  Depending on the _category_ of product being funded, what is considered "reasonable" might vary.  The data was filtered on Kickstarters of category "Play", and a series was created for each outcome (Successful, failed, and Cancelled). Finally, each outcome was grouped by a discrete range of goal amounts, in $5000 increments.  This resulting chart above allows us to clearly count which $5000 ranges would be the most likely to result in a successful outcome for a play.

### Challenges and Difficulties Encountered

## Results

- What are two conclusions you can draw about the Outcomes based on Launch Date?
    1. Theater campaigns launched in the late Spring / early Summer have historically been more successful when compared to other months.
    2. The number of failed outcomes do not vary significantly by launch date. 

- What can you conclude about the Outcomes based on Goals?

    Kickstarters with goals of up to $5000 were roughly 75% likely to succeed. Over 700 campaigns in this category were launched in the $0 - $4999 range, so the sample is statistically significant.  While the chart seems to indicate a high success rate around $35,000-$49,999, closer investigation shows that only a total of 9 campaigns exist in that range - which is not a large enough sample to be conclusive.

- What are some limitations of this dataset?

    - The amount of data is relatively small, especially when trying to create statistical predictions for theater / play kickstarters only.
    - The data is outdated - only entries through 2017 are included.
    - There are not many kickstarters with goals above $15,000, especially in the relevant theater / play category.
    - The actual quality of the kickstarter campaign is difficult to gauge using only the `blurb`.  Because kickstarters are free to create it would help to have an evaluation of a "good" or "complete" campaign, like a rating or a number of views.

- What are some other possible tables and/or graphs that we could create?

    - The outcomes by duration (subtract the deadline date by launched on date) for theater categories
    - Outcomes by Launch Date for the entire data set
    - Word cloud using the descriptions of successful blubs (not sure if Excel can do this)
    - Display the total number of projects (for example by using a separate bar chart series) on the Outcomes Based on Goals to help eliminate invalid statitstical sets.