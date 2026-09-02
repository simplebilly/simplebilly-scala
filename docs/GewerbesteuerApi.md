# GewerbesteuerApi

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**gewerbesteuerApi**](GewerbesteuerApi.md#gewerbesteuerApi) | **GET** /api/v1/bookkeeping/gewerbesteuer | 
[**gewerbesteuerApiWithHttpInfo**](GewerbesteuerApi.md#gewerbesteuerApiWithHttpInfo) | **GET** /api/v1/bookkeeping/gewerbesteuer | 



## gewerbesteuerApi

> gewerbesteuerApi(gewerbesteuerApiRequest): ApiRequest[GewerbesteuerErgebnis]



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
    val apiInstance = GewerbesteuerApi("https://demo.simplebilly.com")
    val year: Int = 56 // Int | 

    val hebesatz: String = hebesatz_example // String | 

    val gewerbeertrag: String = gewerbeertrag_example // String | 

    val country: String = country_example // String | 

    val gemeindeschluessel: String = gemeindeschluessel_example // String | 
    
    val request = apiInstance.gewerbesteuerApi(year, hebesatz, gewerbeertrag, country, gemeindeschluessel)
    val response = apiInvoker.execute(request)

    response.onComplete {
        case Success(ApiResponse(code, content, headers)) =>
            System.out.println(s"Status code: $code}")
            System.out.println(s"Response headers: ${headers.mkString(", ")}")
            System.out.println(s"Response body: $content")
        
        case Failure(error @ ApiError(code, message, responseContent, cause, headers)) =>
            System.err.println("Exception when calling GewerbesteuerApi#gewerbesteuerApi")
            System.err.println(s"Status code: $code}")
            System.err.println(s"Reason: $responseContent")
            System.err.println(s"Response headers: ${headers.mkString(", ")}")
            error.printStackTrace();

        case Failure(exception) => 
            System.err.println("Exception when calling GewerbesteuerApi#gewerbesteuerApi")
            exception.printStackTrace();
    }
}
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **year** | **Int**|  |
 **hebesatz** | **String**|  | [optional]
 **gewerbeertrag** | **String**|  | [optional]
 **country** | **String**|  | [optional]
 **gemeindeschluessel** | **String**|  | [optional]

### Return type

ApiRequest[[**GewerbesteuerErgebnis**](GewerbesteuerErgebnis.md)]


### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Gewerbesteuer / Trade Tax Ergebnis |  -  |

