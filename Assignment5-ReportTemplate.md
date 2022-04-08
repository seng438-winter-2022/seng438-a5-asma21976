**SENG 438- Software Testing, Reliability, and Quality**

**Lab. Report \#5 – Software Reliability Assessment**

| Group \#:       |   |
|-----------------|---|
| Student Names:  |   |
| Asma Hashmi     |30093995|
| Hesham Elkaliouby|  30089907   |
| Tom Altankhuyag  |  30100861   |

# Introduction
The purpose of this assignment is to give us hands-on experience on assessing the reliability of a hypothetical system given all the failure data gathered from the integration testing. We are required to install a reliability growth assessment tool, such as CASRE or STRAT, and create plots of failure rate and reliability of SUT. 
After completing this lab, we gained an understanding of what reliability growth testing is. We are also able to measure failure rate, MTTF and reliability of the SUT through analyzing the test data. Lastly, we became familiar with the features and usages of a reliability growth testing too.

# Assessment Using Reliability Growth Testing 
Our team used C-FRAT for this section, as STRAT does not work for mac users. The failure data was imported first. The imported data includes, IFRSB, IFRGSB, S, GM, DW2, DW3, NB2, and TL. The software generated a Total Cumulative Failure vs Time interval graph:

![1](/media/1.jpg)
*Figure 1: Failure VS. Time Interval*

The 8 simulations are run first, using the E, F as covariates:
![2](/media/2.jpg)
*Figure 2: RGT Models for Covariate Failure Data*

This is the model comparison data:
![3](/media/3.jpg)
*Figure 3: Model Comparison Data*

For this graph, we compared several models to see which was closely followed the pattern of failures on the different time intervals. When going through the models, we noticed that IFRGSB is the top model and GM is the second best. This models were shifted from S, GM, TL on AIC, BIC, SSE, and PSSE. 
![4](/media/4.jpg)
*Figure 4: Best-Fit RGT Models*

C-STRAT allows us to view models and data in different formats. Here we see a bar graph for the failure intensity(x-axis) VS time(y-axis).  
![5](/media/5.jpg)
*Figure 5: Failure Intensity Graph*

![6](/media/6.jpg)
*Figure 6: RGT Models on Failure Intensity Graph*

![7](/media/7.jpg)
*Figure 7: Isolated Best-Fit RGT Models*

# Assessment Using Reliability Demonstration Chart 

# 

# Comparison of Results

# Discussion on Similarity and Differences of the Two Techniques

# How the team work/effort was divided and managed

# 

# Difficulties encountered, challenges overcome, and lessons learned

# Comments/feedback on the lab itself
