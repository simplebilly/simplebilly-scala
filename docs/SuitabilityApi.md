# SuitabilityApi

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**shippingSuitabilityApi**](SuitabilityApi.md#shippingSuitabilityApi) | **POST** /api/v1/shipping/suitability | 
[**shippingSuitabilityApiWithHttpInfo**](SuitabilityApi.md#shippingSuitabilityApiWithHttpInfo) | **POST** /api/v1/shipping/suitability | 



## shippingSuitabilityApi

> shippingSuitabilityApi(shippingSuitabilityApiRequest): ApiRequest[SuitabilityResult]



### Example

```scala
// Import classes:
import 
import 
import 
import org.openapitools.client.core._
import org.openapitools.client.core.CollectionFormats._
import org.openapitools.client.core.ApiKeyLocations._

import akka.actor.ActorSystem
import scala.concurrent.Future
import scala.util.{Failure, Success}

object Example extends App {
    
    implicit val system: ActorSystem = ActorSystem()
    import system.dispatcher
    
    // Configure HTTP bearer authorization: bearer_token
    implicit val bearer_token: BearerToken = BearerToken("BEARER TOKEN")

    val apiInvoker = ApiInvoker()
    val apiInstance = SuitabilityApi("https://demo.simplebilly.com")
    val suitabilityRequest: SuitabilityRequest =  // SuitabilityRequest | 
    
    val request = apiInstance.shippingSuitabilityApi(suitabilityRequest)
    val response = apiInvoker.execute(request)

    response.onComplete {
        case Success(ApiResponse(code, content, headers)) =>
            System.out.println(s"Status code: $code}")
            System.out.println(s"Response headers: ${headers.mkString(", ")}")
            System.out.println(s"Response body: $content")
        
        case Failure(error @ ApiError(code, message, responseContent, cause, headers)) =>
            System.err.println("Exception when calling SuitabilityApi#shippingSuitabilityApi")
            System.err.println(s"Status code: $code}")
            System.err.println(s"Reason: $responseContent")
            System.err.println(s"Response headers: ${headers.mkString(", ")}")
            error.printStackTrace();

        case Failure(exception) => 
            System.err.println("Exception when calling SuitabilityApi#shippingSuitabilityApi")
            exception.printStackTrace();
    }
}
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **suitabilityRequest** | [**SuitabilityRequest**](SuitabilityRequest.md)|  |

### Return type

ApiRequest[[**SuitabilityResult**](SuitabilityResult.md)]


### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Shipping suitability results |  -  |
| **400** | Bad request |  -  |
| **500** | Internal server error |  -  |

