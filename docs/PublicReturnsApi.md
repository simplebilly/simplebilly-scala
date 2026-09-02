# PublicReturnsApi

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**getPublicReturnStatus**](PublicReturnsApi.md#getPublicReturnStatus) | **GET** /api/v1/public/returns/status | Customer checks the status of a return (public, no auth). The return is only revealed when its linked order&#39;s email matches.
[**getPublicReturnStatusWithHttpInfo**](PublicReturnsApi.md#getPublicReturnStatusWithHttpInfo) | **GET** /api/v1/public/returns/status | Customer checks the status of a return (public, no auth). The return is only revealed when its linked order&#39;s email matches.
[**listPublicReturns**](PublicReturnsApi.md#listPublicReturns) | **GET** /api/v1/public/returns/list | List all returns for an order (public, no auth).
[**listPublicReturnsWithHttpInfo**](PublicReturnsApi.md#listPublicReturnsWithHttpInfo) | **GET** /api/v1/public/returns/list | List all returns for an order (public, no auth).
[**requestPublicReturn**](PublicReturnsApi.md#requestPublicReturn) | **POST** /api/v1/public/returns/request | Customer requests a return for an order (public, no auth).
[**requestPublicReturnWithHttpInfo**](PublicReturnsApi.md#requestPublicReturnWithHttpInfo) | **POST** /api/v1/public/returns/request | Customer requests a return for an order (public, no auth).



## getPublicReturnStatus

> getPublicReturnStatus(getPublicReturnStatusRequest): ApiRequest[PublicReturnStatusResponse]

Customer checks the status of a return (public, no auth). The return is only revealed when its linked order&#39;s email matches.

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
    val apiInstance = PublicReturnsApi("https://demo.simplebilly.com")
    val email: String = email_example // String | 

    val returnNumber: String = returnNumber_example // String | Either return_number or return_order_id must be provided.

    val returnOrderId: String = returnOrderId_example // String | 

    val orderNumber: String = orderNumber_example // String | 
    
    val request = apiInstance.getPublicReturnStatus(email, returnNumber, returnOrderId, orderNumber)
    val response = apiInvoker.execute(request)

    response.onComplete {
        case Success(ApiResponse(code, content, headers)) =>
            System.out.println(s"Status code: $code}")
            System.out.println(s"Response headers: ${headers.mkString(", ")}")
            System.out.println(s"Response body: $content")
        
        case Failure(error @ ApiError(code, message, responseContent, cause, headers)) =>
            System.err.println("Exception when calling PublicReturnsApi#getPublicReturnStatus")
            System.err.println(s"Status code: $code}")
            System.err.println(s"Reason: $responseContent")
            System.err.println(s"Response headers: ${headers.mkString(", ")}")
            error.printStackTrace();

        case Failure(exception) => 
            System.err.println("Exception when calling PublicReturnsApi#getPublicReturnStatus")
            exception.printStackTrace();
    }
}
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **email** | **String**|  |
 **returnNumber** | **String**| Either return_number or return_order_id must be provided. | [optional]
 **returnOrderId** | **String**|  | [optional]
 **orderNumber** | **String**|  | [optional]

### Return type

ApiRequest[[**PublicReturnStatusResponse**](PublicReturnStatusResponse.md)]


### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Return status |  -  |
| **400** | Bad request (missing return identifier) |  -  |
| **404** | Return not found or email mismatch |  -  |
| **500** | Internal server error |  -  |


## listPublicReturns

> listPublicReturns(listPublicReturnsRequest): ApiRequest[Seq[PublicReturnStatusResponse]]

List all returns for an order (public, no auth).

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
    val apiInstance = PublicReturnsApi("https://demo.simplebilly.com")
    val orderNumber: String = orderNumber_example // String | 

    val email: String = email_example // String | 
    
    val request = apiInstance.listPublicReturns(orderNumber, email)
    val response = apiInvoker.execute(request)

    response.onComplete {
        case Success(ApiResponse(code, content, headers)) =>
            System.out.println(s"Status code: $code}")
            System.out.println(s"Response headers: ${headers.mkString(", ")}")
            System.out.println(s"Response body: $content")
        
        case Failure(error @ ApiError(code, message, responseContent, cause, headers)) =>
            System.err.println("Exception when calling PublicReturnsApi#listPublicReturns")
            System.err.println(s"Status code: $code}")
            System.err.println(s"Reason: $responseContent")
            System.err.println(s"Response headers: ${headers.mkString(", ")}")
            error.printStackTrace();

        case Failure(exception) => 
            System.err.println("Exception when calling PublicReturnsApi#listPublicReturns")
            exception.printStackTrace();
    }
}
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **orderNumber** | **String**|  |
 **email** | **String**|  |

### Return type

ApiRequest[[**Seq[PublicReturnStatusResponse]**](PublicReturnStatusResponse.md)]


### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Returns for the order |  -  |
| **404** | Order not found or email mismatch |  -  |
| **500** | Internal server error |  -  |


## requestPublicReturn

> requestPublicReturn(requestPublicReturnRequest): ApiRequest[PublicReturnResponse]

Customer requests a return for an order (public, no auth).

### Example

```scala
// Import classes:
import 
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
    val apiInstance = PublicReturnsApi("https://demo.simplebilly.com")
    val publicReturnRequest: PublicReturnRequest =  // PublicReturnRequest | 
    
    val request = apiInstance.requestPublicReturn(publicReturnRequest)
    val response = apiInvoker.execute(request)

    response.onComplete {
        case Success(ApiResponse(code, content, headers)) =>
            System.out.println(s"Status code: $code}")
            System.out.println(s"Response headers: ${headers.mkString(", ")}")
            System.out.println(s"Response body: $content")
        
        case Failure(error @ ApiError(code, message, responseContent, cause, headers)) =>
            System.err.println("Exception when calling PublicReturnsApi#requestPublicReturn")
            System.err.println(s"Status code: $code}")
            System.err.println(s"Reason: $responseContent")
            System.err.println(s"Response headers: ${headers.mkString(", ")}")
            error.printStackTrace();

        case Failure(exception) => 
            System.err.println("Exception when calling PublicReturnsApi#requestPublicReturn")
            exception.printStackTrace();
    }
}
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **publicReturnRequest** | [**PublicReturnRequest**](PublicReturnRequest.md)|  |

### Return type

ApiRequest[[**PublicReturnResponse**](PublicReturnResponse.md)]


### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Return requested |  -  |
| **400** | Bad request (item not in order / quantity too high) |  -  |
| **404** | Order not found or email mismatch |  -  |
| **500** | Internal server error |  -  |

