# KonzernApi

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**konzernExportApi**](KonzernApi.md#konzernExportApi) | **GET** /api/v1/bookkeeping/konzern/status/export | 
[**konzernExportApiWithHttpInfo**](KonzernApi.md#konzernExportApiWithHttpInfo) | **GET** /api/v1/bookkeeping/konzern/status/export | 
[**konzernStatusApi**](KonzernApi.md#konzernStatusApi) | **GET** /api/v1/bookkeeping/konzern/status | 
[**konzernStatusApiWithHttpInfo**](KonzernApi.md#konzernStatusApiWithHttpInfo) | **GET** /api/v1/bookkeeping/konzern/status | 



## konzernExportApi

> konzernExportApi(konzernExportApiRequest): ApiRequest[KonzernExportResponse]



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
    val apiInstance = KonzernApi("https://demo.simplebilly.com")
    val year: Int = 56 // Int | 
    
    val request = apiInstance.konzernExportApi(year)
    val response = apiInvoker.execute(request)

    response.onComplete {
        case Success(ApiResponse(code, content, headers)) =>
            System.out.println(s"Status code: $code}")
            System.out.println(s"Response headers: ${headers.mkString(", ")}")
            System.out.println(s"Response body: $content")
        
        case Failure(error @ ApiError(code, message, responseContent, cause, headers)) =>
            System.err.println("Exception when calling KonzernApi#konzernExportApi")
            System.err.println(s"Status code: $code}")
            System.err.println(s"Reason: $responseContent")
            System.err.println(s"Response headers: ${headers.mkString(", ")}")
            error.printStackTrace();

        case Failure(exception) => 
            System.err.println("Exception when calling KonzernApi#konzernExportApi")
            exception.printStackTrace();
    }
}
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **year** | **Int**|  |

### Return type

ApiRequest[[**KonzernExportResponse**](KonzernExportResponse.md)]


### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Konzern-Beteiligungen mit Kontrollstatus als CSV (BOM, Semikolon) |  -  |


## konzernStatusApi

> konzernStatusApi(konzernStatusApiRequest): ApiRequest[KonzernStatus]



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
    val apiInstance = KonzernApi("https://demo.simplebilly.com")
    val year: Int = 56 // Int | 
    
    val request = apiInstance.konzernStatusApi(year)
    val response = apiInvoker.execute(request)

    response.onComplete {
        case Success(ApiResponse(code, content, headers)) =>
            System.out.println(s"Status code: $code}")
            System.out.println(s"Response headers: ${headers.mkString(", ")}")
            System.out.println(s"Response body: $content")
        
        case Failure(error @ ApiError(code, message, responseContent, cause, headers)) =>
            System.err.println("Exception when calling KonzernApi#konzernStatusApi")
            System.err.println(s"Status code: $code}")
            System.err.println(s"Reason: $responseContent")
            System.err.println(s"Response headers: ${headers.mkString(", ")}")
            error.printStackTrace();

        case Failure(exception) => 
            System.err.println("Exception when calling KonzernApi#konzernStatusApi")
            exception.printStackTrace();
    }
}
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **year** | **Int**|  |

### Return type

ApiRequest[[**KonzernStatus**](KonzernStatus.md)]


### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Konzern-Status (§§ 290, 291, 293 HGB) |  -  |

