--------

This guide is for the Snowball Edge \(100 TB of storage space\)\. If you are looking for documentation for the Snowball, see the [AWS Snowball User Guide](http://docs.aws.amazon.com/snowball/latest/ug/whatissnowball.html)\.

--------

# AWS Snowball Edge Limits<a name="limits"></a>

Following, you can find information about limitations on using the AWS Snowball Edge appliance\.

**Important**  
When you transfer data into Amazon Simple Storage Service using a Snowball Edge, keep in mind that individual Amazon S3 objects can range in size from a minimum of 0 bytes to a maximum of 5 terabytes \(TB\)\.

## Regional Limitations for AWS Snowball<a name="region-limits"></a>

The AWS Snowball service has two device types, the standard Snowball and the Snowball Edge\. The following table highlights which of these devices are available in which regions\. 

**Note**  
The guide you're reading now is for the Snowball Edge, which has 100 TB of storage space\. If you are looking for documentation for the Snowball, see the [AWS Snowball User Guide](http://docs.aws.amazon.com/snowball/latest/ug/whatissnowball.html)\.


****  

| Region | Snowball Availability | Snowball Edge Availability | 
| --- | --- | --- | 
| US East \(Ohio\) | 50 TB and 80 TB | 100 TB | 
| US East \(N\. Virginia\) | 50 TB and 80 TB | 100 TB | 
| US West \(N\. California\) | 50 TB and 80 TB | 100 TB | 
| US West \(Oregon\) | 50 TB and 80 TB | 100 TB | 
| Canada \(Central\) | 80 TB only | 100 TB | 
| Asia Pacific \(Mumbai\) | 80 TB only | Not available | 
| Asia Pacific \(Sydney\) | 80 TB only | 100 TB | 
| Asia Pacific \(Tokyo\) | 80 TB only | 100 TB | 
| EU \(Frankfurt\) | 80 TB only | 100 TB | 
| EU \(Ireland\) | 80 TB only | 100 TB | 
| EU \(London\) | 80 TB only | 100 TB | 
| South America \(São Paulo\) | 80 TB only | 100 TB | 

## Limitations on AWS Snowball Edge Jobs<a name="job-limits"></a>

The following limitations exist for creating AWS Snowball Edge appliance jobs:

+ For security purposes, jobs must be completed within 120 days of the AWS Snowball Edge appliance being prepared\. If you need to keep one or more devices for longer than 120 days, contact AWS Support\.

+ Currently, AWS Snowball Edge appliance doesn't support server\-side encryption with AWS Key Management Service–managed keys \(SSE\-KMS\) or server\-side encryption with customer\-provided keys \(SSE\-C\)\. AWS Snowball Edge appliance does support server\-side encryption with Amazon S3–managed encryption keys \(SSE\-S3\)\. For more information on SSE\-S3, see [Protecting Data Using Server\-Side Encryption with Amazon S3\-Managed Encryption Keys \(SSE\-S3\)](http://docs.aws.amazon.com/AmazonS3/latest/dev/UsingServerSideEncryption.html) in the *Amazon Simple Storage Service Developer Guide\.*

+ If you're using AWS Snowball Edge appliance to import data, and you need to transfer more data than will fit on a single AWS Snowball Edge appliance, create additional jobs\. Each export job can use multiple AWS Snowball Edge appliances\.

+ The default service limit for the number of AWS Snowball Edge appliances you can have at one time is 1\. If you want to increase your service limit or create a cluster job, contact [AWS Support](https://aws.amazon.com/premiumsupport/)\.

+ Metadata for objects transferred to an appliance is not persisted, unless it's transferred with the file interface\. The only metadata that remains the same is `filename` and `filesize`\. All other metadata is set as in the following example: `-rw-rw-r-- 1 root root [filesize] Dec 31 1969 [path/filename]`

## Limitations on Transferring On\-Premises Data with an AWS Snowball Edge Appliance<a name="transfer-limits"></a>

The following limitations exist for transferring data to or from a AWS Snowball Edge appliance on\-premises:

+ Files must be in a static state while being written\. Files that are modified while they are being transferred will not be imported into Amazon S3\.

+ Jumbo frames are not supported—that is, Ethernet frames with more than 1500 bytes of payload\.

+ When selecting what data to export, keep in mind that objects with trailing slashes in their names \(`/` or `\`\) will not be transferred\. Before exporting any objects with trailing slashes, update their names to remove the slash\.

+ When using the Amazon S3 Adapter for Snowball with the AWS CLI to transfer data, note that the `--recursive` option for the `cp` command is only supported for uploading data to an AWS Snowball Edge appliance, not for downloading data from a AWS Snowball Edge appliance\.

## Limitations for Lambda Powered by AWS Greengrass<a name="function-limits"></a>

If you allocate the minimum recommendation of 128 MB of memory for each of your functions, you can have up to seven Lambda functions in a single job\. This limitation occurs because the physical nature of the Snowball Edge limits the amount of memory available for running Lambda functions on the device\. 

## Limitations on Shipping an AWS Snowball Edge<a name="shipping-limits"></a>

The following limitations exist for shipping a AWS Snowball Edge appliance:

+ AWS will not ship a AWS Snowball Edge appliance to a post office box\.

+ AWS will not ship a AWS Snowball Edge appliance between non\-US regions—for example, from EU \(Ireland\) to EU \(Frankfurt\), or to Asia Pacific \(Sydney\)\.

+ Moving a AWS Snowball Edge appliance to an address other than the one specified when the job was created is not allowed and is a violation of the AWS Service Terms\.

For more information on shipping, see [Shipping Considerations for AWS Snowball](shipping.md)\.

## Limitations on Processing Your Returned AWS Snowball Edge for Import<a name="return-limits"></a>

To import your data into AWS, the appliance must meet the following requirements:

+ The AWS Snowball Edge appliance must not be compromised\. Except for opening the three doors on the front, back, and top, or to add and replace the optional air filter, don't open the AWS Snowball Edge appliance for any reason\.

+ The appliance must not be physically damaged\. You can prevent damage by closing the three doors on the AWS Snowball Edge appliance until the latches make an audible clicking sound\.

+ The AWS Snowball Edge appliance's E Ink display must be visible, and must show the return label that was automatically generated when you finished transferring your data onto the AWS Snowball Edge appliance\.

**Note**  
All AWS Snowball Edge appliances returned that do not meet these requirements are erased without work performed on them\.