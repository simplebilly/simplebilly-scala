# ReorderProposalApi

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**applyReorderProposal**](ReorderProposalApi.md#applyReorderProposal) | **POST** /api/v1/reorder-proposals/apply | Convert a reorder proposal into a draft purchase order.
[**applyReorderProposalWithHttpInfo**](ReorderProposalApi.md#applyReorderProposalWithHttpInfo) | **POST** /api/v1/reorder-proposals/apply | Convert a reorder proposal into a draft purchase order.
[**getReorderProposal**](ReorderProposalApi.md#getReorderProposal) | **GET** /api/v1/reorder-proposals | 
[**getReorderProposalWithHttpInfo**](ReorderProposalApi.md#getReorderProposalWithHttpInfo) | **GET** /api/v1/reorder-proposals | 



## applyReorderProposal

> applyReorderProposal(applyReorderProposalRequest): ApiRequest[AnyType]

Convert a reorder proposal into a draft purchase order.

Returns the created purchase order id. Suggested line items are generated with the current reorder quantity per product.

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
    val apiInstance = ReorderProposalApi("https://demo.simplebilly.com")
    val configuredOnly: Boolean = true // Boolean | Only include products with a reorder point configured (`min_stock`).

    val warehouseId: String = warehouseId_example // String | Limit to a single warehouse id.
    
    val request = apiInstance.applyReorderProposal(configuredOnly, warehouseId)
    val response = apiInvoker.execute(request)

    response.onComplete {
        case Success(ApiResponse(code, content, headers)) =>
            System.out.println(s"Status code: $code}")
            System.out.println(s"Response headers: ${headers.mkString(", ")}")
            System.out.println(s"Response body: $content")
        
        case Failure(error @ ApiError(code, message, responseContent, cause, headers)) =>
            System.err.println("Exception when calling ReorderProposalApi#applyReorderProposal")
            System.err.println(s"Status code: $code}")
            System.err.println(s"Reason: $responseContent")
            System.err.println(s"Response headers: ${headers.mkString(", ")}")
            error.printStackTrace();

        case Failure(exception) => 
            System.err.println("Exception when calling ReorderProposalApi#applyReorderProposal")
            exception.printStackTrace();
    }
}
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **configuredOnly** | **Boolean**| Only include products with a reorder point configured (&#x60;min_stock&#x60;). | [optional]
 **warehouseId** | **String**| Limit to a single warehouse id. | [optional]

### Return type

ApiRequest[[**AnyType**](AnyType.md)]


### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Created |  -  |
| **400** | Bad request |  -  |
| **500** | Internal server error |  -  |


## getReorderProposal

> getReorderProposal(getReorderProposalRequest): ApiRequest[ReorderProposalResponse]



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
    val apiInstance = ReorderProposalApi("https://demo.simplebilly.com")
    val configuredOnly: Boolean = true // Boolean | Only include products with a reorder point configured (`min_stock`).

    val warehouseId: String = warehouseId_example // String | Limit to a single warehouse id.
    
    val request = apiInstance.getReorderProposal(configuredOnly, warehouseId)
    val response = apiInvoker.execute(request)

    response.onComplete {
        case Success(ApiResponse(code, content, headers)) =>
            System.out.println(s"Status code: $code}")
            System.out.println(s"Response headers: ${headers.mkString(", ")}")
            System.out.println(s"Response body: $content")
        
        case Failure(error @ ApiError(code, message, responseContent, cause, headers)) =>
            System.err.println("Exception when calling ReorderProposalApi#getReorderProposal")
            System.err.println(s"Status code: $code}")
            System.err.println(s"Reason: $responseContent")
            System.err.println(s"Response headers: ${headers.mkString(", ")}")
            error.printStackTrace();

        case Failure(exception) => 
            System.err.println("Exception when calling ReorderProposalApi#getReorderProposal")
            exception.printStackTrace();
    }
}
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **configuredOnly** | **Boolean**| Only include products with a reorder point configured (&#x60;min_stock&#x60;). | [optional]
 **warehouseId** | **String**| Limit to a single warehouse id. | [optional]

### Return type

ApiRequest[[**ReorderProposalResponse**](ReorderProposalResponse.md)]


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

