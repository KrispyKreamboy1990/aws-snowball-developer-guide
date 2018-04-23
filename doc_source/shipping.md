--------

This guide is for the Snowball Edge \(100 TB of storage space\)\. If you are looking for documentation for the Snowball, see the [AWS Snowball User Guide](http://docs.aws.amazon.com/snowball/latest/ug/whatissnowball.html)\.

--------

# Shipping Considerations for AWS Snowball<a name="shipping"></a>

Following, you can find information about how shipping is handled for an AWS Snowball Edge appliance, and a list that shows each AWS Region that is supported\. The shipping rate you choose for a job apply to both sending and receiving the AWS Snowball Edge appliance or AWS Snowball Edge appliances used for that job\. For information on shipping charges, see [AWS Snowball Edge Pricing](http://aws.amazon.com/snowball-edge/pricing)\.

**Topics**
+ [Preparing an AWS Snowball Edge for Shipping](#appliance-shipping)
+ [Region\-Based Shipping Restrictions](#shipwithinregion)
+ [Shipping an AWS Snowball Edge](mailing-storage.md)

When you create a job, you specify a shipping address and shipping speed\. This shipping speed doesn’t indicate how soon you can expect to receive the AWS Snowball Edge appliance from the day you created the job\. It only shows the time that the appliance is in transit between AWS and your shipping address\. That time doesn’t include any time for processing, which depends on factors including job type \(exports take longer than imports, typically\) and job size \(cluster jobs take longer than individual jobs, typically\)\. Also, carriers generally only pick up outgoing AWS Snowball Edge appliances once a day\. Thus, processing before shipping can take a day or more\.

**Note**  
Snowball Edge devices can only be used to import or export data within the AWS Region where the devices were ordered\.

## Preparing an AWS Snowball Edge for Shipping<a name="appliance-shipping"></a>

The following explains how to prepare a Snowball appliance and ship it back to AWS\.

**To prepare an AWS Snowball Edge appliance for shipping**

1. Make sure that you've finished transferring all the data for this job to or from the AWS Snowball Edge appliance\.

1. Press the power button above the LCD display\. It takes about 20 seconds for the appliance to power off\.
**Note**  
If you've powered off and unplugged the AWS Snowball Edge appliance, and your shipping label doesn't appear after about a minute on the E Ink display on top of the appliance, contact [AWS Support](https://aws.amazon.com/premiumsupport/)\.

1. Disconnect and stow the power cable the AWS Snowball Edge appliance was sent with in the cable nook on top of the appliance\.

1. Close the three doors on the back, the top, and the front of the AWS Snowball Edge appliance, pressing in on each one at a time until you hear and feel them click\.

You don't need to pack the AWS Snowball Edge appliance in a container, because it is its own physically rugged shipping container\. The E Ink display on the top of the AWS Snowball Edge appliance changes to your return shipping label when the AWS Snowball Edge appliance is turned off\.

## Region\-Based Shipping Restrictions<a name="shipwithinregion"></a>

Before you create a job, you should sign in to the console from the AWS Region that your Amazon S3 or Amazon Glacier data is housed in\. A few shipping restrictions apply, as follows:
+ For data transfers in US regions, we don't ship AWS Snowball Edge appliances outside of the United States\.
+ We don't ship AWS Snowball Edge appliances between non\-US regions—for example, from EU \(Ireland\) to EU \(Frankfurt\), or from Asia Pacific \(Mumbai\) to Asia Pacific \(Sydney\)\.
+ For data transfers in Asia Pacific \(Sydney\), we only ship AWS Snowball Edge appliances within Australia\.
+ For data transfers in the EU regions, we only ship AWS Snowball Edge appliances to the EU member countries listed following: Austria, Belgium, Bulgaria, Croatia, Republic of Cyprus, Czech Republic, Denmark, Estonia, Finland, France, Germany, Greece, Hungary, Ireland, Latvia, Lithuania, Luxembourg, Malta, Netherlands, Poland, Portugal, Romania, Slovakia, Slovenia, Spain, Sweden, and the UK\.
+ For data transfers in the Asia Pacific \(Singapore\) region, we only ship s to Singapore\.

**Note**  
AWS doesn't ship AWS Snowball Edge appliances to post office boxes\.