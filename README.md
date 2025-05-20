# EX - 4 Auditing Cloud Activity Using AWS CloudTrail

## Aim
To enable and analyze AWS CloudTrail logs to audit user and resource activities in a cloud environment.

## Requirements

- AWS Console access  
- AWS CloudTrail service enabled  
- An S3 bucket (to store logs)  
- IAM permissions to view CloudTrail logs  

## Procedure

### **Step 1: Enable CloudTrail**

1. Navigate to **CloudTrail** in the AWS Console  
2. Click **Trails** > **Create trail**
3. Configure the trail:
    - **Name:** `CloudAuditTrail`
    - **Apply trail to all regions:** 
    - **Log events:**
        - **Management events:** Read & Write
        - **Data events:** 
            - S3 
            - Lambda (optional)
    - **S3 bucket:** Create or select one for log storage
    - (Optional) Enable **CloudWatch Logs integration**

### **Step 2: Review Event History**

1. Go to **CloudTrail > Event history**
2. Use filters to refine search:
    - **Username** (IAM user or role)
    - **Event name** (e.g., `CreateBucket`, `TerminateInstances`)
    - **Date/Time**
    - **Resource type** (e.g., `S3`, `EC2`)

### **Step 3: Download or Export Logs**

- Click **Download CSV** to export logs  
- Analyze logs using **Excel**, **Google Sheets**, or other tools for reporting and auditing

## Output

![444500791-8953eee6-bb40-43d0-81c6-88da6444b349](https://github.com/user-attachments/assets/b2139336-89fa-4821-9278-bdd32d5d27b1)

## Result
All AWS user activities, including volume creation, deletion, and permission changes, were successfully audited using CloudTrail.

