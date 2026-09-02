# DownPaymentInvoiceApi

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**downloadDownPaymentInvoicePdf**](DownPaymentInvoiceApi.md#downloadDownPaymentInvoicePdf) | **GET** /api/v1/down-payment-invoices/{id}/pdf | 
[**downloadDownPaymentInvoicePdfWithHttpInfo**](DownPaymentInvoiceApi.md#downloadDownPaymentInvoicePdfWithHttpInfo) | **GET** /api/v1/down-payment-invoices/{id}/pdf | 
[**getDownPaymentInvoice**](DownPaymentInvoiceApi.md#getDownPaymentInvoice) | **GET** /api/v1/down-payment-invoices/{id} | 
[**getDownPaymentInvoiceWithHttpInfo**](DownPaymentInvoiceApi.md#getDownPaymentInvoiceWithHttpInfo) | **GET** /api/v1/down-payment-invoices/{id} | 
[**listDownPaymentInvoices**](DownPaymentInvoiceApi.md#listDownPaymentInvoices) | **GET** /api/v1/down-payment-invoices/ | 
[**listDownPaymentInvoicesWithHttpInfo**](DownPaymentInvoiceApi.md#listDownPaymentInvoicesWithHttpInfo) | **GET** /api/v1/down-payment-invoices/ | 



## downloadDownPaymentInvoicePdf

> downloadDownPaymentInvoicePdf(downloadDownPaymentInvoicePdfRequest): ApiRequest[Unit]



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
    val apiInstance = DownPaymentInvoiceApi("https://demo.simplebilly.com")
    val id: String = id_example // String | 
    
    val request = apiInstance.downloadDownPaymentInvoicePdf(id)
    val response = apiInvoker.execute(request)

    response.onComplete {
        case Success(ApiResponse(code, content, headers)) =>
            System.out.println(s"Status code: $code}")
            System.out.println(s"Response headers: ${headers.mkString(", ")}")
        
        case Failure(error @ ApiError(code, message, responseContent, cause, headers)) =>
            System.err.println("Exception when calling DownPaymentInvoiceApi#downloadDownPaymentInvoicePdf")
            System.err.println(s"Status code: $code}")
            System.err.println(s"Reason: $responseContent")
            System.err.println(s"Response headers: ${headers.mkString(", ")}")
            error.printStackTrace();

        case Failure(exception) => 
            System.err.println("Exception when calling DownPaymentInvoiceApi#downloadDownPaymentInvoicePdf")
            exception.printStackTrace();
    }
}
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **String**|  |

### Return type


ApiRequest[Unit] (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | PDF placeholder |  -  |
| **500** | Internal server error |  -  |


## getDownPaymentInvoice

> getDownPaymentInvoice(getDownPaymentInvoiceRequest): ApiRequest[DownPaymentInvoice]



### Example

```scala
// Import classes:
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
    val apiInstance = DownPaymentInvoiceApi("https://demo.simplebilly.com")
    val id: String = id_example // String | 
    
    val request = apiInstance.getDownPaymentInvoice(id)
    val response = apiInvoker.execute(request)

    response.onComplete {
        case Success(ApiResponse(code, content, headers)) =>
            System.out.println(s"Status code: $code}")
            System.out.println(s"Response headers: ${headers.mkString(", ")}")
            System.out.println(s"Response body: $content")
        
        case Failure(error @ ApiError(code, message, responseContent, cause, headers)) =>
            System.err.println("Exception when calling DownPaymentInvoiceApi#getDownPaymentInvoice")
            System.err.println(s"Status code: $code}")
            System.err.println(s"Reason: $responseContent")
            System.err.println(s"Response headers: ${headers.mkString(", ")}")
            error.printStackTrace();

        case Failure(exception) => 
            System.err.println("Exception when calling DownPaymentInvoiceApi#getDownPaymentInvoice")
            exception.printStackTrace();
    }
}
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **String**|  |

### Return type

ApiRequest[[**DownPaymentInvoice**](DownPaymentInvoice.md)]


### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |
| **404** | Not found |  -  |
| **500** | Internal server error |  -  |


## listDownPaymentInvoices

> listDownPaymentInvoices(listDownPaymentInvoicesRequest): ApiRequest[Seq[DownPaymentInvoice]]



### Example

```scala
// Import classes:
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
    val apiInstance = DownPaymentInvoiceApi("https://demo.simplebilly.com")
    val page: Int = 1 // Int | 

    val pageSize: Int = 56 // Int | 

    val search: String = search_example // String | 

    val includeDeleted: Boolean = true // Boolean | Soft-delete entities: set true to include rows with `deleted_at` set.
    
    val request = apiInstance.listDownPaymentInvoices(page, pageSize, search, includeDeleted)
    val response = apiInvoker.execute(request)

    response.onComplete {
        case Success(ApiResponse(code, content, headers)) =>
            System.out.println(s"Status code: $code}")
            System.out.println(s"Response headers: ${headers.mkString(", ")}")
            System.out.println(s"Response body: $content")
        
        case Failure(error @ ApiError(code, message, responseContent, cause, headers)) =>
            System.err.println("Exception when calling DownPaymentInvoiceApi#listDownPaymentInvoices")
            System.err.println(s"Status code: $code}")
            System.err.println(s"Reason: $responseContent")
            System.err.println(s"Response headers: ${headers.mkString(", ")}")
            error.printStackTrace();

        case Failure(exception) => 
            System.err.println("Exception when calling DownPaymentInvoiceApi#listDownPaymentInvoices")
            exception.printStackTrace();
    }
}
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **page** | **Int**|  | [optional]
 **pageSize** | **Int**|  | [optional]
 **search** | **String**|  | [optional]
 **includeDeleted** | **Boolean**| Soft-delete entities: set true to include rows with &#x60;deleted_at&#x60; set. | [optional]

### Return type

ApiRequest[[**Seq[DownPaymentInvoice]**](DownPaymentInvoice.md)]


### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |
| **500** | Internal server error |  -  |

