# ListOpenItemsApi

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**listOpenItemsApi**](ListOpenItemsApi.md#listOpenItemsApi) | **GET** /api/v1/bookkeeping/open-items | 
[**listOpenItemsApiWithHttpInfo**](ListOpenItemsApi.md#listOpenItemsApiWithHttpInfo) | **GET** /api/v1/bookkeeping/open-items | 



## listOpenItemsApi

> listOpenItemsApi(listOpenItemsApiRequest): ApiRequest[Seq[OpenItem]]



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
    val apiInstance = ListOpenItemsApi("https://demo.simplebilly.com")
    val reminderLevel1Days: Long = 789 // Long | 

    val reminderLevel2Days: Long = 789 // Long | 

    val reminderLevel3Days: Long = 789 // Long | 

    val customerId: String = customerId_example // String | 
    
    val request = apiInstance.listOpenItemsApi(reminderLevel1Days, reminderLevel2Days, reminderLevel3Days, customerId)
    val response = apiInvoker.execute(request)

    response.onComplete {
        case Success(ApiResponse(code, content, headers)) =>
            System.out.println(s"Status code: $code}")
            System.out.println(s"Response headers: ${headers.mkString(", ")}")
            System.out.println(s"Response body: $content")
        
        case Failure(error @ ApiError(code, message, responseContent, cause, headers)) =>
            System.err.println("Exception when calling ListOpenItemsApi#listOpenItemsApi")
            System.err.println(s"Status code: $code}")
            System.err.println(s"Reason: $responseContent")
            System.err.println(s"Response headers: ${headers.mkString(", ")}")
            error.printStackTrace();

        case Failure(exception) => 
            System.err.println("Exception when calling ListOpenItemsApi#listOpenItemsApi")
            exception.printStackTrace();
    }
}
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **reminderLevel1Days** | **Long**|  | [optional]
 **reminderLevel2Days** | **Long**|  | [optional]
 **reminderLevel3Days** | **Long**|  | [optional]
 **customerId** | **String**|  | [optional]

### Return type

ApiRequest[[**Seq[OpenItem]**](OpenItem.md)]


### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | List of open invoices |  -  |
| **500** | Internal server error |  -  |

