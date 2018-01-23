--------

This guide is for the Snowball Edge \(100 TB of storage space\)\. If you are looking for documentation for the Snowball, see the [AWS Snowball User Guide](http://docs.aws.amazon.com/snowball/latest/ug/whatissnowball.html)\.

--------

# Best Practices for the AWS Snowball Edge Appliance<a name="BestPractices"></a>

To help get the maximum benefit from and satisfaction with AWS Snowball Edge appliance, we recommend that you follow these practices:

**Security**

+ If you notice anything that looks suspicious about the AWS Snowball Edge appliance, don't connect it to your internal network\. Instead, contact [AWS Support](https://aws.amazon.com/premiumsupport/), and a new AWS Snowball Edge appliance will be shipped to you\.

+ We recommend that you don't save a copy of the unlock code in the same location in the workstation as the manifest for that job\. Saving these separately helps prevent unauthorized parties from gaining access to the AWS Snowball Edge appliance\. For example, you can save a copy of the manifest to your local server, and email the code to a user that will unlock the appliance\. This approach limits access to the AWS Snowball Edge appliance to individuals who have access to files saved on the server and also that user's email address\.

+ The credentials displayed when you run the Snowball client command `snowballEdge credentials` are a pair of keys: an access key and a secret key\. These keys are only associated with the job and the local resources on the appliance\. They don't map to your AWS account or any other AWS account\. If you try to use these keys to access services and resources in the AWS Cloud, they fail, because they work only for the local resources associated with your job\.

**Network**

+ We recommend that you only use one method of reading and writing data to a local bucket on an AWS Snowball Edge appliance at a time\. Using both the file interface and the Amazon S3 Adapter for Snowball on the same bucket at the same time can result in read/write conflicts\.

+ To prevent corrupting your data, don't disconnect an AWS Snowball Edge appliance or change its network settings while transferring data\.

+ Files should be in a static state while being written to the appliance\. Files that are modified while they are being written can result in read/write conflicts\.

+ For more information about improving performance of your AWS Snowball Edge appliance, see [Performance](#performance)\.

**Resource Management**

+ The 10 free days for performing your on\-premises data transfer start the day after the AWS Snowball Edge appliance arrives at your data center\.

+ The **Job created** status is the only status in which you can cancel a job\. When a job changes to a different status, it can’t be canceled\. This functionality is also true for clusters\.

+ For import jobs, don't delete your local copies of the transferred data until the import into Amazon Simple Storage Service \(Amazon S3\) is successful at the end of the process and you can verify the results of the data transfer\.

## Performance<a name="performance"></a>

Following, you can find information about AWS Snowball Edge appliance performance\. Here, we discuss performance in general terms, because on\-premises environments each have a different way of doing things—different network technologies, different hardware, different operating systems, different procedures, and so on\.

The following table outlines how your network's transfer rate impacts how long it takes to fill a Snowball Edge with data\. Transferring smaller files will reduce your transfer speed due to decreased overhead\. If you have many small files, we recommend that you zip them up into larger archives before transferring them onto a Snowball\.


| Rate \(MB/s\) | 82 TB Transfer Time | 
| --- | --- | 
| 800 | 1\.22 days | 
| 450 | 2\.11 days | 
| 400 | 2\.37 days | 
| 300 | 3\.16 days | 
| 277 | 3\.42 days | 
| 200 | 4\.75 days | 
| 100 | 9\.49 days | 
| 60 | 15\.53 days | 
| 30 | 31\.06 days | 
| 10 | 85\.42 days | 

To provide meaningful guidance about performance, the following sections describe how to determine when to use AWS Snowball Edge appliance and how to get the most out of the service\.

### Performance Recommendations<a name="perf-recommendations"></a>

The following recommendations are highly suggested, as they will have the largest impact in improving the performance of your data transfer\.

+ We recommend that you have no more than 500,000 files or directories within each directory\.

+ We recommend that all files transferred to a Snowball be no smaller than 1 MB in size\.

+ If you have many files smaller than 1 MB in size each, we recommend that you zip them up into larger archives before transferring them onto a Snowball\.

### Speeding up Data Transfer<a name="transferspeed"></a>

One of the major ways you can improve the performance of an AWS Snowball Edge appliance is to speed up the transfer of data going to and from an appliance\. In general, you can improve the transfer speed from your data source to the appliance in the following ways, ordered from largest to smallest positive impact on performance:

1. **Perform multiple write operations at one time** – You can perform multiple write operations at one time\. You can do this by running each command from multiple terminal windows on a computer with a network connection to a single AWS Snowball Edge appliance\.

1. **Write from multiple computers** – A single AWS Snowball Edge appliance can be connected to many computers on a network\. Each computer can connect to any of the three network interfaces at once\.

1. **Transfer large files or batch small files together** – Each copy operation has some overhead because of encryption\. To speed the process up, batch files together in a single archive\. 

1. **Don't perform other operations on files during transfer** – Renaming files during transfer, changing their metadata, or writing data to the files during a copy operation has a negative impact on transfer performance\. We recommend that your files remain in a static state while you transfer them\. 

1. **Reducing local network use** – Because the AWS Snowball Edge appliance communicates across your local network, reducing or otherwise eliminating other local network traffic between the AWS Snowball Edge appliance, the switch it's connected to, and the computer that hosts your data source can result in an improvement of data transfer speeds\.

1. **Eliminating unnecessary hops** – If you set up your AWS Snowball Edge appliance, your data source, and the computer running the terminal connection between them so that they're the only machines communicating across a single switch, it can result in an improvement of data transfer speeds\.