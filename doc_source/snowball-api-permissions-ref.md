--------

This guide is for the Snowball Edge\. If you are looking for documentation for the Snowball, see the [AWS Snowball User Guide](https://docs.aws.amazon.com/snowball/latest/ug/whatissnowball.html)\.

--------

# AWS Snowball API Permissions: Actions, Resources, and Conditions Reference<a name="snowball-api-permissions-ref"></a>

When you are setting up [Access Control in the AWS Cloud](authentication-and-access-control.md#access-control) and writing a permissions policy that you can attach to an IAM identity \(identity\-based policies\), you can use the following table as a reference\. The table following each AWS Snowball job management API operation and the corresponding actions for which you can grant permissions to perform the action\. It also includes for each API operation the AWS resource for which you can grant the permissions\. You specify the actions in the policy's `Action` field, and you specify the resource value in the policy's `Resource` field\. 

You can use AWS\-wide condition keys in your AWS Snowball policies to express conditions\. For a complete list of AWS\-wide keys, see [Available Keys](https://docs.aws.amazon.com/IAM/latest/UserGuide/reference_policies_elements.html#AvailableKeys) in the *IAM User Guide*\. 

**Note**  
To specify an action, use the `snowball:` prefix followed by the API operation name \(for example, `snowball:CreateJob`\)\.

If you see an expand arrow \(**↗**\) in the upper\-right corner of the table, you can open the table in a new window\. To close the window, choose the close button \(**X**\) in the lower\-right corner\.


**AWS Snowball Job Management API and Required Permissions for Actions**  

| Job Management API Actions | Required Permissions | 
| --- | --- | 
|   [CancelCluster](https://docs.aws.amazon.com/snowball/latest/api-reference/API_CancelCluster.html)   | snowball:CancelCluster | 
|   [CancelJob](https://docs.aws.amazon.com/snowball/latest/api-reference/API_CancelJob.html)  |  `snowball:CancelJob`  | 
|   [CreateAddress](https://docs.aws.amazon.com/snowball/latest/api-reference/API_CreateAddress.html)  | snowball:CreateAddress | 
|   [CreateCluster](https://docs.aws.amazon.com/snowball/latest/api-reference/API_CreateCluster.html)  | This action requires the following permissions: [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/snowball/latest/developer-guide/snowball-api-permissions-ref.html) | 
|   [CreateJob](https://docs.aws.amazon.com/snowball/latest/api-reference/API_CreateJob.html)  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/snowball/latest/developer-guide/snowball-api-permissions-ref.html) | 
|   [DescribeAddress](https://docs.aws.amazon.com/snowball/latest/api-reference/API_DescribeAddress.html)  | snowball:DescribeAddress | 
|   [DescribeAddresses](https://docs.aws.amazon.com/snowball/latest/api-reference/API_DescribeAddresses.html)  | snowball:DescribeAddresses | 
|   [DescribeCluster](https://docs.aws.amazon.com/snowball/latest/api-reference/API_DescribeCluster.html)  | snowball:DescribeCluster | 
|   [DescribeJob](https://docs.aws.amazon.com/snowball/latest/api-reference/API_DescribeJob.html)  | snowball:DescribeJob | 
|   [GetJobManifest](https://docs.aws.amazon.com/snowball/latest/api-reference/API_GetJobManifest.html)  | snowball:GetJobManifest | 
|   [GetJobUnlockCode](https://docs.aws.amazon.com/snowball/latest/api-reference/API_GetJobUnlockCode.html)  | snowball:GetJobUnlockCode | 
|   [GetSnowballUsage](https://docs.aws.amazon.com/snowball/latest/api-reference/API_GetSnowballUsage.html)  | snowball:GetSnowballUsage | 
|   [ListClusterJobs](https://docs.aws.amazon.com/snowball/latest/api-reference/API_ListClusterJobs.html)  | snowball:ListClusterJobs | 
|   [ListClusters](https://docs.aws.amazon.com/snowball/latest/api-reference/API_ListClusters.html)  | snowball:ListClusters | 
|   [ListJobs](https://docs.aws.amazon.com/snowball/latest/api-reference/API_ListJobs.html)  | snowball:ListJobs | 
|   [UpdateCluster](https://docs.aws.amazon.com/snowball/latest/api-reference/API_UpdateCluster.html)  | snowball:UpdateCluster | 
|   [UpdateJob](https://docs.aws.amazon.com/snowball/latest/api-reference/API_UpdateJob.html)  | snowball:UpdateJob | 