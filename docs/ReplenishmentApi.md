# ReplenishmentApi

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**applyReplenishments**](ReplenishmentApi.md#applyReplenishments) | **POST** /api/v1/replenishments/apply | Create one draft stock transfer per (source → target) pair carrying all suggested product lines for that pair.
[**applyReplenishmentsWithHttpInfo**](ReplenishmentApi.md#applyReplenishmentsWithHttpInfo) | **POST** /api/v1/replenishments/apply | Create one draft stock transfer per (source → target) pair carrying all suggested product lines for that pair.
[**getReplenishments**](ReplenishmentApi.md#getReplenishments) | **GET** /api/v1/replenishments | 
[**getReplenishmentsWithHttpInfo**](ReplenishmentApi.md#getReplenishmentsWithHttpInfo) | **GET** /api/v1/replenishments | 



## applyReplenishments

> applyReplenishments(applyReplenishmentsRequest): ApiRequest[AnyType]

Create one draft stock transfer per (source → target) pair carrying all suggested product lines for that pair.

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
    val apiInstance = ReplenishmentApi("https://demo.simplebilly.com")
    val targetWarehouseId: String = targetWarehouseId_example // String | Warehouse to be replenished. Defaults to the tenant's default warehouse.

    val sourceWarehouseId: String = sourceWarehouseId_example // String | Restrict source warehouses to this id.
    
    val request = apiInstance.applyReplenishments(targetWarehouseId, sourceWarehouseId)
    val response = apiInvoker.execute(request)

    response.onComplete {
        case Success(ApiResponse(code, content, headers)) =>
            System.out.println(s"Status code: $code}")
            System.out.println(s"Response headers: ${headers.mkString(", ")}")
            System.out.println(s"Response body: $content")
        
        case Failure(error @ ApiError(code, message, responseContent, cause, headers)) =>
            System.err.println("Exception when calling ReplenishmentApi#applyReplenishments")
            System.err.println(s"Status code: $code}")
            System.err.println(s"Reason: $responseContent")
            System.err.println(s"Response headers: ${headers.mkString(", ")}")
            error.printStackTrace();

        case Failure(exception) => 
            System.err.println("Exception when calling ReplenishmentApi#applyReplenishments")
            exception.printStackTrace();
    }
}
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **targetWarehouseId** | **String**| Warehouse to be replenished. Defaults to the tenant&#39;s default warehouse. | [optional]
 **sourceWarehouseId** | **String**| Restrict source warehouses to this id. | [optional]

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


## getReplenishments

> getReplenishments(getReplenishmentsRequest): ApiRequest[ReplenishmentResponse]



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
    val apiInstance = ReplenishmentApi("https://demo.simplebilly.com")
    val targetWarehouseId: String = targetWarehouseId_example // String | Warehouse to be replenished. Defaults to the tenant's default warehouse.

    val sourceWarehouseId: String = sourceWarehouseId_example // String | Restrict source warehouses to this id.
    
    val request = apiInstance.getReplenishments(targetWarehouseId, sourceWarehouseId)
    val response = apiInvoker.execute(request)

    response.onComplete {
        case Success(ApiResponse(code, content, headers)) =>
            System.out.println(s"Status code: $code}")
            System.out.println(s"Response headers: ${headers.mkString(", ")}")
            System.out.println(s"Response body: $content")
        
        case Failure(error @ ApiError(code, message, responseContent, cause, headers)) =>
            System.err.println("Exception when calling ReplenishmentApi#getReplenishments")
            System.err.println(s"Status code: $code}")
            System.err.println(s"Reason: $responseContent")
            System.err.println(s"Response headers: ${headers.mkString(", ")}")
            error.printStackTrace();

        case Failure(exception) => 
            System.err.println("Exception when calling ReplenishmentApi#getReplenishments")
            exception.printStackTrace();
    }
}
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **targetWarehouseId** | **String**| Warehouse to be replenished. Defaults to the tenant&#39;s default warehouse. | [optional]
 **sourceWarehouseId** | **String**| Restrict source warehouses to this id. | [optional]

### Return type

ApiRequest[[**ReplenishmentResponse**](ReplenishmentResponse.md)]


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

