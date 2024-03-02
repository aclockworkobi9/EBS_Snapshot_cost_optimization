### "AWS Lambda Function for Cost Optimization through Unassociated Snapshot Deletion"

#### Overview
This repository contains a Lambda function tailored for cost optimization within AWS by automating the deletion of unassociated snapshots. The function, developed in Python, leverages the AWS SDK (boto3) for seamless integration with AWS services.

#### Functionality
1. **EC2 Instance Provisioning**: 
- Create an EC2 instance, it will automatically create default volume and it will be attached to this instance.
     
 ![MicrosoftTeams-image (2)](https://github.com/aclockworkobi9/EBS_Snapshot_cost_optimization/assets/146419037/aef9c1d7-f789-4c52-bcbb-197be32ae714)
 ![MicrosoftTeams-image (2 2)](https://github.com/aclockworkobi9/EBS_Snapshot_cost_optimization/assets/146419037/11423673-350d-4687-b36e-cbfad350658a)



2. **Snapshot Creation**:
- Now create a snapshot of this attached EBS volume.
  
 ![MicrosoftTeams-image (2 3)](https://github.com/aclockworkobi9/EBS_Snapshot_cost_optimization/assets/146419037/42fa4b34-e453-49c5-b37d-15a0ced31902)

3. **Lambda Function Setup**:

- Create the Lambda function with python, paste the Python code and click on deploy .

 ![MicrosoftTeams-image (2 4)](https://github.com/aclockworkobi9/EBS_Snapshot_cost_optimization/assets/146419037/0c28c8b8-9df4-4d1a-bbd9-26f3dd8eebc7)
 ![MicrosoftTeams-image (2 5)](https://github.com/aclockworkobi9/EBS_Snapshot_cost_optimization/assets/146419037/c8ad2260-bf22-48c6-b7ea-8181cb116bf6)


4. **Testing**:
- Now create test events for verification.
  
 ![MicrosoftTeams-image (3)](https://github.com/aclockworkobi9/EBS_Snapshot_cost_optimization/assets/146419037/436424d9-10b8-435f-93af-4b8f6ce6f649)



5. **Permissions:
- Any failures indicate potential Lambda permission issues. Address the permission gaps by establishing an inline policy granting essential permissions (describe volumes, instances, snapshots, delete snapshots). Ensure the policy attachment to the function's role.
  
 ![MicrosoftTeams-image (4)](https://github.com/aclockworkobi9/EBS_Snapshot_cost_optimization/assets/146419037/f6cad4fb-a774-4351-a809-2e2bfab3300b)
 ![MicrosoftTeams-image (5)](https://github.com/aclockworkobi9/EBS_Snapshot_cost_optimization/assets/146419037/b43ede8e-7757-4947-99c6-894ce75cc2e7)
 ![MicrosoftTeams-image (6)](https://github.com/aclockworkobi9/EBS_Snapshot_cost_optimization/assets/146419037/b1947b45-fa22-44bf-9ec8-e159c1d42c7f)
 ![MicrosoftTeams-image (7)](https://github.com/aclockworkobi9/EBS_Snapshot_cost_optimization/assets/146419037/38d339b0-9cbd-4736-a6e4-3c16c2c11f99)
 ![MicrosoftTeams-image (8)](https://github.com/aclockworkobi9/EBS_Snapshot_cost_optimization/assets/146419037/27e049a1-497e-4946-8d8f-f0d0824c4ed3)
 ![MicrosoftTeams-image (9)](https://github.com/aclockworkobi9/EBS_Snapshot_cost_optimization/assets/146419037/38fa6686-bd7f-4ec0-aa18-6c0a2973d4b5)
 ![MicrosoftTeams-image (10)](https://github.com/aclockworkobi9/EBS_Snapshot_cost_optimization/assets/146419037/fd8364c0-783c-4497-ae0e-bea2831a148c)

6. **Cost Optimization**:
- Now to test, delete instance, it will automatically remove associated volumes. Now trigger function, it will delete unassociated snapshots, minimizing costs by eliminating unnecessary expenses.
  
 <img width="538" alt="MicrosoftTeams-image (11)" src="https://github.com/aclockworkobi9/EBS_Snapshot_cost_optimization/assets/146419037/b9129679-8b52-4323-8edd-953ebec5520f">
 <img width="839" alt="MicrosoftTeams-image (12)" src="https://github.com/aclockworkobi9/EBS_Snapshot_cost_optimization/assets/146419037/4ddc0b69-bea6-4745-be4d-50d49a08ef40">
 <img width="998" alt="MicrosoftTeams-image (13)" src="https://github.com/aclockworkobi9/EBS_Snapshot_cost_optimization/assets/146419037/a57d0590-c27d-40d6-831c-b9eb9506fb7d">
 <img width="1322" alt="MicrosoftTeams-image (14)" src="https://github.com/aclockworkobi9/EBS_Snapshot_cost_optimization/assets/146419037/4f4dba45-c4a0-42d9-afdd-afc753020d4c">
 <img width="545" alt="MicrosoftTeams-image (15)" src="https://github.com/aclockworkobi9/EBS_Snapshot_cost_optimization/assets/146419037/e50559ba-7c19-4534-8d60-9cb7224d0370">




7. **Automation**:
- Support the scheduling through CloudWatch and Amazon EventBridge for hands-free execution.
     
 <img width="786" alt="MicrosoftTeams-image (16)" src="https://github.com/aclockworkobi9/EBS_Snapshot_cost_optimization/assets/146419037/d170bb0e-4ee7-4299-9fc0-c2702d325c38">


#### Usage
1. Clone the repository.
2. Paste the provided Python code into the Lambda function.
3. Deploy the Lambda function.
4. Verify execution by setting up a test event.
5. Ensure proper permissions by attaching the inline policy.
6. Re-test to confirm cost optimization, especially unassociated snapshot deletion.
7. Optionally, schedule the function for automated execution using CloudWatch or Amazon EventBridge.

#### Important
-Make sure you delete the lambda function and policies.
