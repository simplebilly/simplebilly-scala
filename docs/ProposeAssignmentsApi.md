# ProposeAssignmentsApi

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**proposeAssignmentsApi**](ProposeAssignmentsApi.md#proposeAssignmentsApi) | **GET** /api/v1/bookkeeping/propose-assignments | 
[**proposeAssignmentsApiWithHttpInfo**](ProposeAssignmentsApi.md#proposeAssignmentsApiWithHttpInfo) | **GET** /api/v1/bookkeeping/propose-assignments | 



## proposeAssignmentsApi

> proposeAssignmentsApi(proposeAssignmentsApiRequest): ApiRequest[Seq[ProposedAssignment]]



### Example

```scala
// Import classes:
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
    val apiInstance = ProposeAssignmentsApi("https://demo.simplebilly.com")
    val minConfidence: Double = 1.2 // Double | 

    val customerId: String = customerId_example // String | 
    
    val request = apiInstance.proposeAssignmentsApi(minConfidence, customerId)
    val response = apiInvoker.execute(request)

    response.onComplete {
        case Success(ApiResponse(code, content, headers)) =>
            System.out.println(s"Status code: $code}")
            System.out.println(s"Response headers: ${headers.mkString(", ")}")
            System.out.println(s"Response body: $content")
        
        case Failure(error @ ApiError(code, message, responseContent, cause, headers)) =>
            System.err.println("Exception when calling ProposeAssignmentsApi#proposeAssignmentsApi")
            System.err.println(s"Status code: $code}")
            System.err.println(s"Reason: $responseContent")
            System.err.println(s"Response headers: ${headers.mkString(", ")}")
            error.printStackTrace();

        case Failure(exception) => 
            System.err.println("Exception when calling ProposeAssignmentsApi#proposeAssignmentsApi")
            exception.printStackTrace();
    }
}
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **minConfidence** | **Double**|  | [optional]
 **customerId** | **String**|  | [optional]

### Return type

ApiRequest[[**Seq[ProposedAssignment]**](ProposedAssignment.md)]


### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Proposed payment to invoice assignments |  -  |
| **500** | Internal server error |  -  |

