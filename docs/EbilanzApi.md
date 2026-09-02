# EbilanzApi

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**ebilanzReportApi**](EbilanzApi.md#ebilanzReportApi) | **GET** /api/v1/bookkeeping/ebilanz | 
[**ebilanzReportApiWithHttpInfo**](EbilanzApi.md#ebilanzReportApiWithHttpInfo) | **GET** /api/v1/bookkeeping/ebilanz | 
[**ebilanzXbrlExportApi**](EbilanzApi.md#ebilanzXbrlExportApi) | **GET** /api/v1/bookkeeping/ebilanz/xbrl | 
[**ebilanzXbrlExportApiWithHttpInfo**](EbilanzApi.md#ebilanzXbrlExportApiWithHttpInfo) | **GET** /api/v1/bookkeeping/ebilanz/xbrl | 



## ebilanzReportApi

> ebilanzReportApi(ebilanzReportApiRequest): ApiRequest[EBilanzReport]



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
    val apiInstance = EbilanzApi("https://demo.simplebilly.com")
    val year: Int = 56 // Int | 

    val dateFrom: String = dateFrom_example // String | 

    val dateTo: String = dateTo_example // String | 
    
    val request = apiInstance.ebilanzReportApi(year, dateFrom, dateTo)
    val response = apiInvoker.execute(request)

    response.onComplete {
        case Success(ApiResponse(code, content, headers)) =>
            System.out.println(s"Status code: $code}")
            System.out.println(s"Response headers: ${headers.mkString(", ")}")
            System.out.println(s"Response body: $content")
        
        case Failure(error @ ApiError(code, message, responseContent, cause, headers)) =>
            System.err.println("Exception when calling EbilanzApi#ebilanzReportApi")
            System.err.println(s"Status code: $code}")
            System.err.println(s"Reason: $responseContent")
            System.err.println(s"Response headers: ${headers.mkString(", ")}")
            error.printStackTrace();

        case Failure(exception) => 
            System.err.println("Exception when calling EbilanzApi#ebilanzReportApi")
            exception.printStackTrace();
    }
}
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **year** | **Int**|  | [optional]
 **dateFrom** | **String**|  | [optional]
 **dateTo** | **String**|  | [optional]

### Return type

ApiRequest[[**EBilanzReport**](EBilanzReport.md)]


### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | E-Bilanz report |  -  |


## ebilanzXbrlExportApi

> ebilanzXbrlExportApi(ebilanzXbrlExportApiRequest): ApiRequest[Unit]



### Example

```scala
// Import classes:
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
    val apiInstance = EbilanzApi("https://demo.simplebilly.com")
    val year: Int = 56 // Int | 

    val dateFrom: String = dateFrom_example // String | 

    val dateTo: String = dateTo_example // String | 
    
    val request = apiInstance.ebilanzXbrlExportApi(year, dateFrom, dateTo)
    val response = apiInvoker.execute(request)

    response.onComplete {
        case Success(ApiResponse(code, content, headers)) =>
            System.out.println(s"Status code: $code}")
            System.out.println(s"Response headers: ${headers.mkString(", ")}")
        
        case Failure(error @ ApiError(code, message, responseContent, cause, headers)) =>
            System.err.println("Exception when calling EbilanzApi#ebilanzXbrlExportApi")
            System.err.println(s"Status code: $code}")
            System.err.println(s"Reason: $responseContent")
            System.err.println(s"Response headers: ${headers.mkString(", ")}")
            error.printStackTrace();

        case Failure(exception) => 
            System.err.println("Exception when calling EbilanzApi#ebilanzXbrlExportApi")
            exception.printStackTrace();
    }
}
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **year** | **Int**|  | [optional]
 **dateFrom** | **String**|  | [optional]
 **dateTo** | **String**|  | [optional]

### Return type


ApiRequest[Unit] (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/xml

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | XBRL XML content |  -  |

