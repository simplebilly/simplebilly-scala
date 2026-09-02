# DatevApi

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**datevExportApi**](DatevApi.md#datevExportApi) | **GET** /api/v1/bookkeeping/datev/export | Export bookkeeping data as DATEV CSV
[**datevExportApiWithHttpInfo**](DatevApi.md#datevExportApiWithHttpInfo) | **GET** /api/v1/bookkeeping/datev/export | Export bookkeeping data as DATEV CSV
[**datevPreviewApi**](DatevApi.md#datevPreviewApi) | **GET** /api/v1/bookkeeping/datev/preview | Exported_datev_bookings: returns formed bookings for review
[**datevPreviewApiWithHttpInfo**](DatevApi.md#datevPreviewApiWithHttpInfo) | **GET** /api/v1/bookkeeping/datev/preview | Exported_datev_bookings: returns formed bookings for review



## datevExportApi

> datevExportApi(datevExportApiRequest): ApiRequest[DatevExportResponse]

Export bookkeeping data as DATEV CSV

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
    val apiInstance = DatevApi("https://demo.simplebilly.com")
    val accountSchema: String = accountSchema_example // String | 

    val dateFrom: String = dateFrom_example // String | 

    val dateTo: String = dateTo_example // String | 

    val page: Int = 56 // Int | 

    val pageSize: Int = 56 // Int | 
    
    val request = apiInstance.datevExportApi(accountSchema, dateFrom, dateTo, page, pageSize)
    val response = apiInvoker.execute(request)

    response.onComplete {
        case Success(ApiResponse(code, content, headers)) =>
            System.out.println(s"Status code: $code}")
            System.out.println(s"Response headers: ${headers.mkString(", ")}")
            System.out.println(s"Response body: $content")
        
        case Failure(error @ ApiError(code, message, responseContent, cause, headers)) =>
            System.err.println("Exception when calling DatevApi#datevExportApi")
            System.err.println(s"Status code: $code}")
            System.err.println(s"Reason: $responseContent")
            System.err.println(s"Response headers: ${headers.mkString(", ")}")
            error.printStackTrace();

        case Failure(exception) => 
            System.err.println("Exception when calling DatevApi#datevExportApi")
            exception.printStackTrace();
    }
}
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **accountSchema** | **String**|  | [optional]
 **dateFrom** | **String**|  | [optional]
 **dateTo** | **String**|  | [optional]
 **page** | **Int**|  | [optional]
 **pageSize** | **Int**|  | [optional]

### Return type

ApiRequest[[**DatevExportResponse**](DatevExportResponse.md)]


### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | DATEV CSV export |  -  |


## datevPreviewApi

> datevPreviewApi(datevPreviewApiRequest): ApiRequest[Seq[DatevBookingPreview]]

Exported_datev_bookings: returns formed bookings for review

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
    val apiInstance = DatevApi("https://demo.simplebilly.com")
    val accountSchema: String = accountSchema_example // String | 

    val dateFrom: String = dateFrom_example // String | 

    val dateTo: String = dateTo_example // String | 

    val page: Int = 56 // Int | 

    val pageSize: Int = 56 // Int | 
    
    val request = apiInstance.datevPreviewApi(accountSchema, dateFrom, dateTo, page, pageSize)
    val response = apiInvoker.execute(request)

    response.onComplete {
        case Success(ApiResponse(code, content, headers)) =>
            System.out.println(s"Status code: $code}")
            System.out.println(s"Response headers: ${headers.mkString(", ")}")
            System.out.println(s"Response body: $content")
        
        case Failure(error @ ApiError(code, message, responseContent, cause, headers)) =>
            System.err.println("Exception when calling DatevApi#datevPreviewApi")
            System.err.println(s"Status code: $code}")
            System.err.println(s"Reason: $responseContent")
            System.err.println(s"Response headers: ${headers.mkString(", ")}")
            error.printStackTrace();

        case Failure(exception) => 
            System.err.println("Exception when calling DatevApi#datevPreviewApi")
            exception.printStackTrace();
    }
}
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **accountSchema** | **String**|  | [optional]
 **dateFrom** | **String**|  | [optional]
 **dateTo** | **String**|  | [optional]
 **page** | **Int**|  | [optional]
 **pageSize** | **Int**|  | [optional]

### Return type

ApiRequest[[**Seq[DatevBookingPreview]**](DatevBookingPreview.md)]


### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | DATEV booking preview |  -  |

