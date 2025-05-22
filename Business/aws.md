### **How to Access CloudWatch Logs**

#### **Step 1: Log in to AWS**

- Go to [https://console.aws.amazon.com/](https://console.aws.amazon.com/)
    
- Sign in with your sepio AWS account credentials.
    

#### **Step 2: Navigate to CloudWatch**

- From the AWS Console home, either:
    
    - Search for “CloudWatch” in the search bar at the top, or
        
    - Click on **Services** > **CloudWatch** under the “Management & Governance” section.
        
![[Pasted image 20250424123538.png]]

#### **Step 3: Access Log Groups**

- In the CloudWatch console:
    
    - On the left sidebar, click **Logs** > **Log groups**.
        
    - You’ll see a list of all the log groups in the account. Search for USABMX
        
        ![[Pasted image 20250424123701.png]]
	- Depending on the application you might want to search in one of these
	  ![[Pasted image 20250424123824.png]]
	  

#### **Step 4: View Logs**

- Click on a log group to open it.
    
- Inside, you'll see **log streams**—each strally represents a container which ran a specific version of the software at that point in time
    
- Click a log stream to view the log events.
    

#### **Step 5: Filter and Search Logs (Optional)**

- Use the **Search** bar to filter log entries by keywords, timestamps, or patterns.
    
- You can also use **Insights** for more advanced queries.
    

---

### **Tips**

- If you are monitoring ECS, it might be easier to go to the ECS service and tail live logs 