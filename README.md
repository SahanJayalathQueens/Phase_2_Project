#**introduction:** 

I am representing The Walt Disney company and they are looking to venture more into the horror franchise. With the TMDB database we want to generate provable statistics that not olny prove horror movies are successful, and how we would make sucessful horror movies. We want to also prove that horror movies can be sucessful with small budgets but still yield returns enough to make future investment. 

![The_nightmare_before_christmas_poster](https://github.com/user-attachments/assets/6dcfcdfc-6e64-4ddc-8805-9d42361c1b4c)
![1_q68GLFmiuXTgbMqDg_OhzQ](https://github.com/user-attachments/assets/586cfd84-80f7-467f-ab01-6c76b2e84989)

#**Overview:**
With the TMDB database, I found over 30,000 entries with plenty of metrics to test our data with. We used the initial filters where we decided to look at movies from 1996 to the present day because these movies tend to have more realistic budgets that we can get concrete trends from. 

![Initial DataFrame](Images/init_df.png)

Since we're specifically looking at horror it just made sense to break up this large data frame into 

- Average Budget to Revenue Analysis, including information on ROI
- Average popularity of all of the directors (within the United States)
- Average voter score of all of the directors (with over 100 votes and movies released in the United States)

# **Business Understanding:**
Now that we have cleaned and made usable data from our 3 data frames, we need mainly prove two things:

1\) Is there any correlation between movies using small budgets and yielding large returns?
2\)  Are there any directors that appear in all three of these graphs?

# **Data Understanding and Analysis:**

So first things first, we need to find if there is indeed a relationship between movies with low budgets that yield high revenues. So lets use some linear regression testing and display our findings with a scatter plot: 
**Testing our hypothesis**
<br> ![Lin_reg](https://github.com/user-attachments/assets/88710bc0-36dd-4cf8-8095-f9fe49999379)</br>

After looking at this it's clear that there is some sort of positive correlation between directors who use small budgets but still yield high returns as we see a lot of our values lie above the regression line. we also see a lot of values clustered below the budget of 20 million dollars and yet still trend upward. 

**So let's move ahead with grouping our findings with directors!**
Earlier the data frame that cared about revenue, budget, and ROI statistics was drastically cut due to some of the related data being either NaN values or valued at zero implying that it simply wasnt available in our data frame. So we ended up going from : 
<br>![og_rev_df](https://github.com/user-attachments/assets/3ba28d9d-f78a-40a4-a17a-9d07ffbb6c09)</br>
**To**
<br>![nu_rev_df](https://github.com/user-attachments/assets/cc39f978-7c1a-4c0d-b441-8578eb2248b2)</br>

so lets focus on the directors left with usable data and translating them into graphs :
<br>![ROI_dir](https://github.com/user-attachments/assets/9eacd800-416b-472c-872b-2526668a65ab)</br>


<br>![vote_dir](https://github.com/user-attachments/assets/cfb8116c-cfb9-4c11-b669-b9bb6613b426)</br>


<br>![Pop_dir](https://github.com/user-attachments/assets/bd589d78-d6e6-4e51-a14f-4baa89fe6e7e)</br>

# **Results:** 

So with all of our relevant data visualized, we can see a decent portion of the directors in the graph who care about ROI don't match up with the other two, and that's most likely because most if not all of the values that cared either budget or revenue got dropped from our sorted dataframes. So when it comes to choosing what director we move forward with we should draw on information from ratings. 

# **Conclusions:**

When looking at both graphs that care about voter and popular reception we see there are directors that defintely land in both of those sets of data. When we Measure out our data we see can arrive at two distinct directors that stand out : 
<br>![Conclusion](https://github.com/user-attachments/assets/08ad1783-53e5-4253-9d6a-7e02fe9ba1dc)</br>
