# FristenApi

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**fristenApi**](FristenApi.md#fristenApi) | **GET** /api/v1/bookkeeping/fristen | 
[**fristenApiWithHttpInfo**](FristenApi.md#fristenApiWithHttpInfo) | **GET** /api/v1/bookkeeping/fristen | 



## fristenApi

> fristenApi(fristenApiRequest): ApiRequest[FristenErgebnis]



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
    val apiInstance = FristenApi("https://demo.simplebilly.com")
    val bundesland: String = bundesland_example // String | 

    val voranmeldungsrhythmus: String = voranmeldungsrhythmus_example // String | 

    val dauerfristverlaengerung: Boolean = true // Boolean | 

    val estAktiv: Boolean = true // Boolean | 

    val gewstAktiv: Boolean = true // Boolean | 

    val monate: Int = 56 // Int | 
    
    val request = apiInstance.fristenApi(bundesland, voranmeldungsrhythmus, dauerfristverlaengerung, estAktiv, gewstAktiv, monate)
    val response = apiInvoker.execute(request)

    response.onComplete {
        case Success(ApiResponse(code, content, headers)) =>
            System.out.println(s"Status code: $code}")
            System.out.println(s"Response headers: ${headers.mkString(", ")}")
            System.out.println(s"Response body: $content")
        
        case Failure(error @ ApiError(code, message, responseContent, cause, headers)) =>
            System.err.println("Exception when calling FristenApi#fristenApi")
            System.err.println(s"Status code: $code}")
            System.err.println(s"Reason: $responseContent")
            System.err.println(s"Response headers: ${headers.mkString(", ")}")
            error.printStackTrace();

        case Failure(exception) => 
            System.err.println("Exception when calling FristenApi#fristenApi")
            exception.printStackTrace();
    }
}
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **bundesland** | **String**|  | [optional]
 **voranmeldungsrhythmus** | **String**|  | [optional]
 **dauerfristverlaengerung** | **Boolean**|  | [optional]
 **estAktiv** | **Boolean**|  | [optional]
 **gewstAktiv** | **Boolean**|  | [optional]
 **monate** | **Int**|  | [optional]

### Return type

ApiRequest[[**FristenErgebnis**](FristenErgebnis.md)]


### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Steuerliche Fristen |  -  |

