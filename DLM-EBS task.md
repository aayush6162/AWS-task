# Document outlining the steps involved in configuring Data Lifecycle Manager for Elastic Block Store (EBS) on AWS.

### Overview:

You can use Amazon Data Lifecycle Manager to automate the creation, retention, and deletion of EBS
snapshots and EBS-backed AMIs. When you automate snapshot, it helps you to:

-   To protect valuable data or a regular backup schedules.
-   To create standardized AMls that can be refreshed at regular intervals.
-   To retain backups as requirement.
-   To reduce storage costs by deleting outdated backups.
-   The most important is creating disaster recovery backup policies data isolated accounts.
<img width="685" alt="screenshot_download" src="https://github.com/aayush6162/AWS-task/assets/137821023/4bc27b04-a432-4f1b-884d-c177ec3f5c48">


This Structure is AWS Data Lifecycle Manager for Elastic Block Store (EBS)
-   Now i completed the documentation outlining the steps involved in configuring Data Lifecycle Manager for Elastic Block Store (EBS) on AWS.

Lab steps:-
-	Go to the EC2 instance and create the instance.
![image](https://github.com/aayush6162/AWS-task/assets/137821023/1f62bb47-a92a-48dd-a77b-199d9702b052)

-	Than move to the Lifecycle Manager.
![image](https://github.com/aayush6162/AWS-task/assets/137821023/132359e1-a5e5-4644-bd1f-4489fe0ad0b3)


![image](https://github.com/aayush6162/AWS-task/assets/137821023/83ef295e-bb92-4e46-8112-09920b23c53a)




-	Select the policy type- EBS snapshot policy than click on next.
![image](https://github.com/aayush6162/AWS-task/assets/137821023/75023c92-10bf-4acf-ab3e-3bb0fc9bb972)



-	Now select to EBS snapshot policy and create new lifecycle policy.
- In the (Policy name) enter a name for your policy.
- In the (Description) enter a description for your policy (optional).
- Under (Target resources) select "Amazon EBS".
![image](https://github.com/aayush6162/AWS-task/assets/137821023/f2e00a1a-c50a-40a6-aa06-a5277da5cf08)




Policy select Enabled click to next 
![image](https://github.com/aayush6162/AWS-task/assets/137821023/ced3d79a-03ff-48cf-892d-f1bdbd154a24)


-	Give the name of schedule and select the frequency of automatic EBS snapshots.
Schedule name: Daily-backup
Frequency: every 1 Hour ,Daily
Retention type: Count
Keep snapshots: 1
![image](https://github.com/aayush6162/AWS-task/assets/137821023/126ff4a3-4ac2-4c3f-94d1-3110c484923f)




-	Now review the Policy and click on create policy.
![image](https://github.com/aayush6162/AWS-task/assets/137821023/6fc1feef-544b-418a-b80e-052bdbd8d791)

 


-	Now Snapshots will be automatically created for the EBS volumes Name : DLM-EBS based on the scheduled defined in the EBS snapshot policy. 
-	For this lab, you will have to wait for one hour after creating the Snapshot policy.
![image](https://github.com/aayush6162/AWS-task/assets/137821023/b2095ebf-3341-43db-9121-b7ed0fd01783)



-	Data lifecycle manager policy details:-

![image](https://github.com/aayush6162/AWS-task/assets/137821023/ab01cce0-f60f-4ea8-aa37-32caaa587c4a)





