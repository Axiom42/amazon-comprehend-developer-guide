# Detecting the Dominant Language<a name="get-started-api-dominant-language"></a>

To determine the dominant language used in text, use the Amazon Comprehend [DetectDominantLanguage](API_DetectDominantLanguage.md) operation\. To detect the dominant language in up to 25 documents in a batch, use the [BatchDetectDominantLanguage](API_BatchDetectDominantLanguage.md) operation\. For more information, see [Using the Batch APIs](get-started-batch.md)\.


+ [Detecting the Dominant Language Using the AWS Command Line Interface](#get-started-api-dominant-language-cli)
+ [Detecting the Dominant Language Using the AWS SDK for Java](#get-started-api-dominant-language-java)
+ [Detecting the Dominant Language Using the AWS SDK for Python \(Boto\)](#get-started-api-dominant-language-python)

## Detecting the Dominant Language Using the AWS Command Line Interface<a name="get-started-api-dominant-language-cli"></a>

The following example demonstrates using the `DetectDominantLanguage` operation with the AWS CLI\.

The example is formatted for Unix, Linux, and macOS\. For Windows, replace the backslash \(\\\) Unix continuation character at the end of each line with a caret \(^\)\.

```
aws comprehend detect-dominant-language \
    --region region \
    --text "It is raining today in Seattle."
```

Amazon Comprehend responds with the following:

```
{
    "Languages": [
        {
            "LanguageCode": "en",
            "Score": 0.9793661236763
        }
    ]
}
```

## Detecting the Dominant Language Using the AWS SDK for Java<a name="get-started-api-dominant-language-java"></a>

The following example uses the `DetectDominantLanguage` operation with Java\.

```
import com.amazonaws.auth.AWSStaticCredentialsProvider;
import com.amazonaws.auth.BasicAWSCredentials;
import com.amazonaws.services.comprehend.AmazonComprehend;
import com.amazonaws.services.comprehend.AmazonComprehendClientBuilder;
import com.amazonaws.services.comprehend.model.DetectDominantLanguageRequest;
import com.amazonaws.services.comprehend.model.DetectDominantLanguageResult;

public class App 
{
    public static void main( String[] args )
    {

        String text = "It is raining today in Seattle";

        BasicAWSCredentials awsCreds = new BasicAWSCredentials("access key ID", "secret access key");

        AmazonComprehend comprehendClient = 
            AmazonComprehendClientBuilder.standard()
                                         .withCredentials(new AWSStaticCredentialsProvider(awsCreds))
                                         .withRegion("region")
                                         .build();
                                         
        // Call detectDominantLanguage API
        System.out.println("Calling DetectDominantLanguage");
        DetectDominantLanguageRequest detectDominantLanguageRequest = new DetectDominantLanguageRequest().withText(text);
        DetectDominantLanguageResult detectDominantLanguageResult = comprehendClient.detectDominantLanguage(detectDominantLanguageRequest);
        detectDominantLanguageResult.getLanguages().forEach(System.out::println);
        System.out.println("Calling DetectDominantLanguage\n");
        System.out.println( "Done" );
    }
}
```

## Detecting the Dominant Language Using the AWS SDK for Python \(Boto\)<a name="get-started-api-dominant-language-python"></a>

The following example demonstrates using the `DetectDominantLanguage` operation with Python\.

```
import boto3
import json

comprehend = boto3.client(service_name='comprehend', region_name='region')
text = "It is raining today in Seattle"

print('Calling DetectDominantLanguage')
print(json.dumps(comprehend.detect_dominant_language(Text = text), sort_keys=True, indent=4))
print("End of DetectDominantLanguage\n")
```