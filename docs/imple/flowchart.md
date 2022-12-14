<!--**
 @file
 @copyright FHNW Switzerland 2022, FHNW
 @authors JongGwan An [kman3212@gmail.com]
-->

<h2>Flow Chart</h2>
Figure 12 shows the flow chart of Indicator as how to provide GEIGER score for threat of SMEs. The indicator checks the master node of LDS using GEIGER API to synchronize GEIGER toolbox (Step. 1). The current user and device UUID require access to necessary nodes to calculate (Step. 2). Setup the listener to get a notification of data events using LDS API (Step. 3) and then Preparing the threat data to use on the GEIGER algorithm (Step. 4). Before starting to calculate the GEIGER score, check the existing GEIGER score nodes in LDS for creation or update (Step. 5). These works as upper are initial work on GEIGER Indicator workflow. Now, to calculate GEIGER score as a threat for SMEs, the indicator waits for the metric nodes (“data:metric”) on LDS and uses a listener and checks if it exists (Step. 6).  Finally, The GEIGER score nodes store to LDS and then check the existence of the enterprise nodes for calculation of GEIGER MSE nodes (Step. 7). 

![flow-chart](https://user-images.githubusercontent.com/15152117/184823588-91acc0ba-d5bb-4d68-b120-2acdc6aa049e.png)
