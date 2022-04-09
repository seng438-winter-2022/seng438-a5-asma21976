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

The 8 simulations are ran first, using the E, F as covariates:
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



*TALK ABT LAPLACE TESTING RESULTS*
# Assessment Using Reliability Demonstration Chart 

![8](/media/RDC_colours.PNG)  
*Figure 8: Reliability Demo Chart*

![9](/media/RDC_Preview.PNG)  
*Figure 9: Preview of Reliability Demo Chart*


In terms of the charts, we chose the following parameters:
* Discrimination Ratio: 2
* Developer's Risk: 0.0001
* User's Risk: 0.150
We chose these numbers to match the RDC Preview to the predfined parameters in the R-Demo-Chart.

In RDC testing, we can see that the system passes. This is under the assumption of a base failure intensity objective of 406 failures / 1000 events. However, since the system barely is in the acceptance range, the develops may elect to continue to test the system. Nonetheless, based on the parameters, the system passes and is ground for it to be pushed into release or the next phase of development.


![10](/media/RDC_colours_doubleMTTF.PNG)  
*Figure 10: Reliability Demo Chart with Double MTTF*

![11](/media/RDC_colours_halfMTTF.PNG)  
*Figure 11: Reliability Demo Chart with Half MTTF*

When halfing the number of events, effectively halfing the MTTF, we can see that the system is well into the acceptance region. This means the system is reliabily accepted. When doubling the MTTF, the system is rejected. In this scenairo, the developers either need to scrap the project or continue development of the system to get within reliability specifications. Usually this is done by testing specfic components of the system to see its failure rate. The developers can then build redundancy into the system if the component is prone to failure by its nature or just engineer a better solution.


# Comparison of Results
The SUT seems to be reliable in the sense that both the Relaibiltiy Growth Testing and the Relaibility Demo Chart gave the same results. The overall system remains reliable and all the failure data is used.

In RDC, we can see that the system is borderline in the acceptance range. Thus, it would be up to the client and developers to further test the system or just leave it as is for release. In RGT, there model is model comparision data on top of the many visuals provided. Using this in conjunction with RDC may be able to provide this extra perspective that the develops and clients need.

# Discussion on Similarity and Differences of the Two Techniques

RDC and RGT are different in that they prioritze different data in order to calculate the reliability of the SUT. For example, in RDC will use MTTF alongside risk of the parties involved to suggest the course of action for reliability of the SUT. Additionally, the RDC provides limited options as to how to view the data. This is because in order to do RDC, the raw data can be inputted into the excel sheet and an RDC graph will appear. However, for RDT the data needs to be prepared and formatted. This pays off because the resulting output is more informative and can be displayed in multiple different formats.

The two techniques are similar, first and foremost, in that that they assess the reliability of the SUT. Although the data needed to be modified, RDC and RDT can generally use the same failure data. 

# How the team work/effort was divided and managed
We have divided the workload between the four members into pairs of two, each tackling part 1 and part 2. 
In the report, the respective pairs will write their own reports and findings in the lab report.
After everyone reports their findings, we can decide and compare the results and conclude our findings.

# Difficulties encountered, challenges overcome, and lessons learned
The major difficulty we had found is using the softwares/tools provided for the lab. The instructions at a lot of times were unclear to our group and major assumptions were needed to continue on. The major challenges were definitely getting familiar with the tools that were provided, and manipulating the RDC data to retrieve the desired graphs.
The group has gotten more comfortable and familiar with the tools (SRTAT & RDC), but more guidance and hands on experience would be preffered.

# Comments/feedback on the lab itself
