# ReportsApi

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**bilanzReportApi**](ReportsApi.md#bilanzReportApi) | **GET** /api/v1/bookkeeping/reports/bilanz | Bilanz (Balance Sheet)
[**bilanzReportApiWithHttpInfo**](ReportsApi.md#bilanzReportApiWithHttpInfo) | **GET** /api/v1/bookkeeping/reports/bilanz | Bilanz (Balance Sheet)
[**guvReportApi**](ReportsApi.md#guvReportApi) | **GET** /api/v1/bookkeeping/reports/guv | Gewinn- und Verlustrechnung (P&amp;L statement)
[**guvReportApiWithHttpInfo**](ReportsApi.md#guvReportApiWithHttpInfo) | **GET** /api/v1/bookkeeping/reports/guv | Gewinn- und Verlustrechnung (P&amp;L statement)
[**kontenansichtReportApi**](ReportsApi.md#kontenansichtReportApi) | **GET** /api/v1/bookkeeping/reports/kontenansicht | Kontenansicht (Account Overview)
[**kontenansichtReportApiWithHttpInfo**](ReportsApi.md#kontenansichtReportApiWithHttpInfo) | **GET** /api/v1/bookkeeping/reports/kontenansicht | Kontenansicht (Account Overview)
[**umsatzsteuerReportApi**](ReportsApi.md#umsatzsteuerReportApi) | **GET** /api/v1/bookkeeping/reports/umsatzsteuer | Umsatzsteuer-Voranmeldung (VAT report)
[**umsatzsteuerReportApiWithHttpInfo**](ReportsApi.md#umsatzsteuerReportApiWithHttpInfo) | **GET** /api/v1/bookkeeping/reports/umsatzsteuer | Umsatzsteuer-Voranmeldung (VAT report)



## bilanzReportApi

> bilanzReportApi(bilanzReportApiRequest): ApiRequest[BilanzReport]

Bilanz (Balance Sheet)

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
    val apiInstance = ReportsApi("https://demo.simplebilly.com")
    val year: Int = 56 // Int | 

    val month: Int = 56 // Int | 

    val dateFrom: String = dateFrom_example // String | 

    val dateTo: String = dateTo_example // String | 

    val page: Int = 56 // Int | 

    val pageSize: Int = 56 // Int | 
    
    val request = apiInstance.bilanzReportApi(year, month, dateFrom, dateTo, page, pageSize)
    val response = apiInvoker.execute(request)

    response.onComplete {
        case Success(ApiResponse(code, content, headers)) =>
            System.out.println(s"Status code: $code}")
            System.out.println(s"Response headers: ${headers.mkString(", ")}")
            System.out.println(s"Response body: $content")
        
        case Failure(error @ ApiError(code, message, responseContent, cause, headers)) =>
            System.err.println("Exception when calling ReportsApi#bilanzReportApi")
            System.err.println(s"Status code: $code}")
            System.err.println(s"Reason: $responseContent")
            System.err.println(s"Response headers: ${headers.mkString(", ")}")
            error.printStackTrace();

        case Failure(exception) => 
            System.err.println("Exception when calling ReportsApi#bilanzReportApi")
            exception.printStackTrace();
    }
}
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **year** | **Int**|  | [optional]
 **month** | **Int**|  | [optional]
 **dateFrom** | **String**|  | [optional]
 **dateTo** | **String**|  | [optional]
 **page** | **Int**|  | [optional]
 **pageSize** | **Int**|  | [optional]

### Return type

ApiRequest[[**BilanzReport**](BilanzReport.md)]


### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Balance sheet |  -  |


## guvReportApi

> guvReportApi(guvReportApiRequest): ApiRequest[GuVReport]

Gewinn- und Verlustrechnung (P&amp;L statement)

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
    val apiInstance = ReportsApi("https://demo.simplebilly.com")
    val year: Int = 56 // Int | 

    val month: Int = 56 // Int | 

    val dateFrom: String = dateFrom_example // String | 

    val dateTo: String = dateTo_example // String | 

    val page: Int = 56 // Int | 

    val pageSize: Int = 56 // Int | 
    
    val request = apiInstance.guvReportApi(year, month, dateFrom, dateTo, page, pageSize)
    val response = apiInvoker.execute(request)

    response.onComplete {
        case Success(ApiResponse(code, content, headers)) =>
            System.out.println(s"Status code: $code}")
            System.out.println(s"Response headers: ${headers.mkString(", ")}")
            System.out.println(s"Response body: $content")
        
        case Failure(error @ ApiError(code, message, responseContent, cause, headers)) =>
            System.err.println("Exception when calling ReportsApi#guvReportApi")
            System.err.println(s"Status code: $code}")
            System.err.println(s"Reason: $responseContent")
            System.err.println(s"Response headers: ${headers.mkString(", ")}")
            error.printStackTrace();

        case Failure(exception) => 
            System.err.println("Exception when calling ReportsApi#guvReportApi")
            exception.printStackTrace();
    }
}
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **year** | **Int**|  | [optional]
 **month** | **Int**|  | [optional]
 **dateFrom** | **String**|  | [optional]
 **dateTo** | **String**|  | [optional]
 **page** | **Int**|  | [optional]
 **pageSize** | **Int**|  | [optional]

### Return type

ApiRequest[[**GuVReport**](GuVReport.md)]


### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | GuV report |  -  |


## kontenansichtReportApi

> kontenansichtReportApi(kontenansichtReportApiRequest): ApiRequest[KontoReport]

Kontenansicht (Account Overview)

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
    val apiInstance = ReportsApi("https://demo.simplebilly.com")
    val year: Int = 56 // Int | 

    val month: Int = 56 // Int | 

    val dateFrom: String = dateFrom_example // String | 

    val dateTo: String = dateTo_example // String | 

    val page: Int = 56 // Int | 

    val pageSize: Int = 56 // Int | 
    
    val request = apiInstance.kontenansichtReportApi(year, month, dateFrom, dateTo, page, pageSize)
    val response = apiInvoker.execute(request)

    response.onComplete {
        case Success(ApiResponse(code, content, headers)) =>
            System.out.println(s"Status code: $code}")
            System.out.println(s"Response headers: ${headers.mkString(", ")}")
            System.out.println(s"Response body: $content")
        
        case Failure(error @ ApiError(code, message, responseContent, cause, headers)) =>
            System.err.println("Exception when calling ReportsApi#kontenansichtReportApi")
            System.err.println(s"Status code: $code}")
            System.err.println(s"Reason: $responseContent")
            System.err.println(s"Response headers: ${headers.mkString(", ")}")
            error.printStackTrace();

        case Failure(exception) => 
            System.err.println("Exception when calling ReportsApi#kontenansichtReportApi")
            exception.printStackTrace();
    }
}
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **year** | **Int**|  | [optional]
 **month** | **Int**|  | [optional]
 **dateFrom** | **String**|  | [optional]
 **dateTo** | **String**|  | [optional]
 **page** | **Int**|  | [optional]
 **pageSize** | **Int**|  | [optional]

### Return type

ApiRequest[[**KontoReport**](KontoReport.md)]


### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Account overview |  -  |


## umsatzsteuerReportApi

> umsatzsteuerReportApi(umsatzsteuerReportApiRequest): ApiRequest[UmsatzsteuerReport]

Umsatzsteuer-Voranmeldung (VAT report)

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
    val apiInstance = ReportsApi("https://demo.simplebilly.com")
    val year: Int = 56 // Int | 

    val month: Int = 56 // Int | 

    val dateFrom: String = dateFrom_example // String | 

    val dateTo: String = dateTo_example // String | 

    val page: Int = 56 // Int | 

    val pageSize: Int = 56 // Int | 
    
    val request = apiInstance.umsatzsteuerReportApi(year, month, dateFrom, dateTo, page, pageSize)
    val response = apiInvoker.execute(request)

    response.onComplete {
        case Success(ApiResponse(code, content, headers)) =>
            System.out.println(s"Status code: $code}")
            System.out.println(s"Response headers: ${headers.mkString(", ")}")
            System.out.println(s"Response body: $content")
        
        case Failure(error @ ApiError(code, message, responseContent, cause, headers)) =>
            System.err.println("Exception when calling ReportsApi#umsatzsteuerReportApi")
            System.err.println(s"Status code: $code}")
            System.err.println(s"Reason: $responseContent")
            System.err.println(s"Response headers: ${headers.mkString(", ")}")
            error.printStackTrace();

        case Failure(exception) => 
            System.err.println("Exception when calling ReportsApi#umsatzsteuerReportApi")
            exception.printStackTrace();
    }
}
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **year** | **Int**|  | [optional]
 **month** | **Int**|  | [optional]
 **dateFrom** | **String**|  | [optional]
 **dateTo** | **String**|  | [optional]
 **page** | **Int**|  | [optional]
 **pageSize** | **Int**|  | [optional]

### Return type

ApiRequest[[**UmsatzsteuerReport**](UmsatzsteuerReport.md)]


### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | VAT report |  -  |

