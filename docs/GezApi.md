# GezApi

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**gezApi**](GezApi.md#gezApi) | **GET** /api/v1/bookkeeping/gez | 
[**gezApiWithHttpInfo**](GezApi.md#gezApiWithHttpInfo) | **GET** /api/v1/bookkeeping/gez | 



## gezApi

> gezApi(gezApiRequest): ApiRequest[GezReport]



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
    val apiInstance = GezApi("https://demo.simplebilly.com")
    val jahr: Int = 56 // Int | 

    val betriebsstaetten: String = betriebsstaetten_example // String | Liste der Betriebsstätten als JSON, z.B. `[{\"name\":\"Filiale 1\",\"beschaefigte\":12}]`.

    val kfz: Long = 789 // Long | Gesamtzahl der betrieblich genutzten Kfz (falls keine Betriebsstätten angegeben sind).

    val hotelzimmer: Long = 789 // Long | Gesamtzahl der Hotel-/Gästezimmer und Ferienwohnungen.

    val beschaefigte: Long = 789 // Long | Gesamtzahl der Beschäftigten (verwendet nur, wenn `betriebsstaetten` fehlt; dann wird eine einzelne Betriebsstätte angenommen).
    
    val request = apiInstance.gezApi(jahr, betriebsstaetten, kfz, hotelzimmer, beschaefigte)
    val response = apiInvoker.execute(request)

    response.onComplete {
        case Success(ApiResponse(code, content, headers)) =>
            System.out.println(s"Status code: $code}")
            System.out.println(s"Response headers: ${headers.mkString(", ")}")
            System.out.println(s"Response body: $content")
        
        case Failure(error @ ApiError(code, message, responseContent, cause, headers)) =>
            System.err.println("Exception when calling GezApi#gezApi")
            System.err.println(s"Status code: $code}")
            System.err.println(s"Reason: $responseContent")
            System.err.println(s"Response headers: ${headers.mkString(", ")}")
            error.printStackTrace();

        case Failure(exception) => 
            System.err.println("Exception when calling GezApi#gezApi")
            exception.printStackTrace();
    }
}
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **jahr** | **Int**|  | [optional]
 **betriebsstaetten** | **String**| Liste der Betriebsstätten als JSON, z.B. &#x60;[{\&quot;name\&quot;:\&quot;Filiale 1\&quot;,\&quot;beschaefigte\&quot;:12}]&#x60;. | [optional]
 **kfz** | **Long**| Gesamtzahl der betrieblich genutzten Kfz (falls keine Betriebsstätten angegeben sind). | [optional]
 **hotelzimmer** | **Long**| Gesamtzahl der Hotel-/Gästezimmer und Ferienwohnungen. | [optional]
 **beschaefigte** | **Long**| Gesamtzahl der Beschäftigten (verwendet nur, wenn &#x60;betriebsstaetten&#x60; fehlt; dann wird eine einzelne Betriebsstätte angenommen). | [optional]

### Return type

ApiRequest[[**GezReport**](GezReport.md)]


### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Rundfunkbeitrag (GEZ) Berechnung nach § 5 RBStV |  -  |

