# BatchDetectEntitiesItemResult<a name="API_BatchDetectEntitiesItemResult"></a>

The result of calling the [BatchDetectKeyPhrases](API_BatchDetectKeyPhrases.md) operation\. The operation returns one object for each document that is successfully processed by the operation\.

## Contents<a name="API_BatchDetectEntitiesItemResult_Contents"></a>

 **Entities**   
One or more [Entity](API_Entity.md) objects, one for each entity detected in the document\.  
Type: Array of [Entity](API_Entity.md) objects  
Required: No

 **Index**   
The zero\-based index of the document in the input list\.  
Type: Integer  
Required: No

## See Also<a name="API_BatchDetectEntitiesItemResult_SeeAlso"></a>

For more information about using this API in one of the language\-specific AWS SDKs, see the following:

+  [AWS SDK for C\+\+](http://docs.aws.amazon.com/goto/SdkForCpp/comprehend-2017-11-27/BatchDetectEntitiesItemResult) 

+  [AWS SDK for Go](http://docs.aws.amazon.com/goto/SdkForGoV1/comprehend-2017-11-27/BatchDetectEntitiesItemResult) 

+  [AWS SDK for Java](http://docs.aws.amazon.com/goto/SdkForJava/comprehend-2017-11-27/BatchDetectEntitiesItemResult) 

+  [AWS SDK for Ruby V2](http://docs.aws.amazon.com/goto/SdkForRubyV2/comprehend-2017-11-27/BatchDetectEntitiesItemResult) 