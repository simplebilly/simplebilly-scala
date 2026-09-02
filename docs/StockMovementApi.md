# StockMovementApi

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**getStockMovement**](StockMovementApi.md#getStockMovement) | **GET** /api/v1/stock-movements/{movement_id} | 
[**getStockMovementWithHttpInfo**](StockMovementApi.md#getStockMovementWithHttpInfo) | **GET** /api/v1/stock-movements/{movement_id} | 
[**listStockMovements**](StockMovementApi.md#listStockMovements) | **GET** /api/v1/stock-movements/ | 
[**listStockMovementsWithHttpInfo**](StockMovementApi.md#listStockMovementsWithHttpInfo) | **GET** /api/v1/stock-movements/ | 



## getStockMovement

> getStockMovement(getStockMovementRequest): ApiRequest[StockMovement]



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
    val apiInstance = StockMovementApi("https://demo.simplebilly.com")
    val movementId: String = movementId_example // String | 
    
    val request = apiInstance.getStockMovement(movementId)
    val response = apiInvoker.execute(request)

    response.onComplete {
        case Success(ApiResponse(code, content, headers)) =>
            System.out.println(s"Status code: $code}")
            System.out.println(s"Response headers: ${headers.mkString(", ")}")
            System.out.println(s"Response body: $content")
        
        case Failure(error @ ApiError(code, message, responseContent, cause, headers)) =>
            System.err.println("Exception when calling StockMovementApi#getStockMovement")
            System.err.println(s"Status code: $code}")
            System.err.println(s"Reason: $responseContent")
            System.err.println(s"Response headers: ${headers.mkString(", ")}")
            error.printStackTrace();

        case Failure(exception) => 
            System.err.println("Exception when calling StockMovementApi#getStockMovement")
            exception.printStackTrace();
    }
}
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **movementId** | **String**|  |

### Return type

ApiRequest[[**StockMovement**](StockMovement.md)]


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


## listStockMovements

> listStockMovements(listStockMovementsRequest): ApiRequest[Seq[StockMovement]]



### Example

```scala
// Import classes:
import 
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
    val apiInstance = StockMovementApi("https://demo.simplebilly.com")
    val page: Int = 56 // Int | 

    val pageSize: Int = 56 // Int | 

    val productId: UUID = 38400000-8cf0-11bd-b23e-10b96e4ef00d // UUID | 

    val warehouseId: String = warehouseId_example // String | 

    val movementType: String = movementType_example // String | 

    val from: LocalDate = 2013-10-20 // LocalDate | Only movements on or after this date (inclusive).

    val to: LocalDate = 2013-10-20 // LocalDate | Only movements on or before this date (inclusive).
    
    val request = apiInstance.listStockMovements(page, pageSize, productId, warehouseId, movementType, from, to)
    val response = apiInvoker.execute(request)

    response.onComplete {
        case Success(ApiResponse(code, content, headers)) =>
            System.out.println(s"Status code: $code}")
            System.out.println(s"Response headers: ${headers.mkString(", ")}")
            System.out.println(s"Response body: $content")
        
        case Failure(error @ ApiError(code, message, responseContent, cause, headers)) =>
            System.err.println("Exception when calling StockMovementApi#listStockMovements")
            System.err.println(s"Status code: $code}")
            System.err.println(s"Reason: $responseContent")
            System.err.println(s"Response headers: ${headers.mkString(", ")}")
            error.printStackTrace();

        case Failure(exception) => 
            System.err.println("Exception when calling StockMovementApi#listStockMovements")
            exception.printStackTrace();
    }
}
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **page** | **Int**|  | [optional]
 **pageSize** | **Int**|  | [optional]
 **productId** | **UUID**|  | [optional]
 **warehouseId** | **String**|  | [optional]
 **movementType** | **String**|  | [optional]
 **from** | **LocalDate**| Only movements on or after this date (inclusive). | [optional]
 **to** | **LocalDate**| Only movements on or before this date (inclusive). | [optional]

### Return type

ApiRequest[[**Seq[StockMovement]**](StockMovement.md)]


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

