# Security best practices<a name="security-best-practices"></a>



**Topics**

CodePipeline provides a number of security features to consider as you develop and implement your own security policies\. The following best practices are general guidelines and don’t represent a complete security solution\. Because these best practices might not be appropriate or sufficient for your environment, treat them as helpful considerations rather than prescriptions\.

You use encryption and authentication for the source repositories that connect to your pipelines\. These are the CodePipeline best practices for security:
+ If you create a pipeline that uses an S3 source bucket, configure server\-side encryption for artifacts stored in Amazon S3 for CodePipeline by managing AWS KMS keys, as described in [Configure server\-side encryption for artifacts stored in Amazon S3 for CodePipeline](S3-artifact-encryption.md)\.
+ If you are using the Jenkins action provider, when you use a Jenkins build provider for your pipeline’s build or test action, install Jenkins on an EC2 instance and configure a separate EC2 instance profile\. Make sure that the instance profile grants Jenkins only the AWS permissions required to perform tasks for your project, such as retrieving files from Amazon S3\. To learn how to create the role for your Jenkins instance profile, see the steps in [Create an IAM role to use for Jenkins integration](tutorials-four-stage-pipeline.md#tutorials-four-stage-pipeline-prerequisites-jenkins-iam-role)\.