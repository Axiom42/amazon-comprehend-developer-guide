# DescribeTopicsDetectionJob<a name="API_DescribeTopicsDetectionJob"></a>

Gets the properties associated with a topic detection job\. Use this operation to get the status of a detection job\.

## Request Syntax<a name="API_DescribeTopicsDetectionJob_RequestSyntax"></a>

```
{
   "JobId": "string"
}
```

## Request Parameters<a name="API_DescribeTopicsDetectionJob_RequestParameters"></a>

For information about the parameters that are common to all actions, see Common Parameters\.

The request accepts the following data in JSON format\.

 ** JobId **   
The identifier assigned by the user to the detection job\.  
Type: String  
Length Constraints: Minimum length of 1\. Maximum length of 32\.  
Required: Yes

## Response Syntax<a name="API_DescribeTopicsDetectionJob_ResponseSyntax"></a>

```
{
   "TopicsDetectionJobProperties": { 
      "EndTime": number,
      "InputDataConfig": { 
         "InputFormat": "string",
         "S3Uri": "string"
      },
      "JobId": "string",
      "JobName": "string",
      "JobStatus": "string",
      "Message": "string",
      "NumberOfTopics": number,
      "OutputDataConfig": { 
         "S3Uri": "string"
      },
      "SubmitTime": number
   }
}
```

## Response Elements<a name="API_DescribeTopicsDetectionJob_ResponseElements"></a>

If the action is successful, the service sends back an HTTP 200 response\.

The following data is returned in JSON format by the service\.

 ** TopicsDetectionJobProperties **   
The list of properties for the requested job\.  
Type: [TopicsDetectionJobProperties](API_TopicsDetectionJobProperties.md) object

## Errors<a name="API_DescribeTopicsDetectionJob_Errors"></a>

For information about the errors that are common to all actions, see [Common Errors](CommonErrors.md)\.

 **InternalServerException**   
An internal server error occurred\. Retry your request\.  
HTTP Status Code: 500

 **InvalidRequestException**   
The request is invalid\.  
HTTP Status Code: 400

 **JobNotFoundException**   
The specified job was not found\. Check the job ID and try again\.  
HTTP Status Code: 400

 **TooManyRequestsException**   
The number of requests exceeds the limit\. Resubmit your request later\.  
HTTP Status Code: 400

## See Also<a name="API_DescribeTopicsDetectionJob_SeeAlso"></a>

For more information about using this API in one of the language\-specific AWS SDKs, see the following:

+  [AWS Command Line Interface](http://docs.aws.amazon.com/goto/aws-cli/comprehend-2017-11-27/DescribeTopicsDetectionJob) 

+  [AWS SDK for \.NET](http://docs.aws.amazon.com/goto/DotNetSDKV3/comprehend-2017-11-27/DescribeTopicsDetectionJob) 

+  [AWS SDK for C\+\+](http://docs.aws.amazon.com/goto/SdkForCpp/comprehend-2017-11-27/DescribeTopicsDetectionJob) 

+  [AWS SDK for Go](http://docs.aws.amazon.com/goto/SdkForGoV1/comprehend-2017-11-27/DescribeTopicsDetectionJob) 

+  [AWS SDK for Java](http://docs.aws.amazon.com/goto/SdkForJava/comprehend-2017-11-27/DescribeTopicsDetectionJob) 

+  [AWS SDK for JavaScript](http://docs.aws.amazon.com/goto/AWSJavaScriptSDK/comprehend-2017-11-27/DescribeTopicsDetectionJob) 

+  [AWS SDK for PHP V3](http://docs.aws.amazon.com/goto/SdkForPHPV3/comprehend-2017-11-27/DescribeTopicsDetectionJob) 

+  [AWS SDK for Python](http://docs.aws.amazon.com/goto/boto3/comprehend-2017-11-27/DescribeTopicsDetectionJob) 

+  [AWS SDK for Ruby V2](http://docs.aws.amazon.com/goto/SdkForRubyV2/comprehend-2017-11-27/DescribeTopicsDetectionJob) 