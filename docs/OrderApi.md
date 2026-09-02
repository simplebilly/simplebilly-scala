# OrderApi

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**addOrderTags**](OrderApi.md#addOrderTags) | **POST** /api/v1/orders/{order_id}/tags | 
[**addOrderTagsWithHttpInfo**](OrderApi.md#addOrderTagsWithHttpInfo) | **POST** /api/v1/orders/{order_id}/tags | 
[**findOrderByExternalRef**](OrderApi.md#findOrderByExternalRef) | **GET** /api/v1/orders/by-ext-ref/{ext_ref} | 
[**findOrderByExternalRefWithHttpInfo**](OrderApi.md#findOrderByExternalRefWithHttpInfo) | **GET** /api/v1/orders/by-ext-ref/{ext_ref} | 
[**getOrder**](OrderApi.md#getOrder) | **GET** /api/v1/order/{order_number} | 
[**getOrderWithHttpInfo**](OrderApi.md#getOrderWithHttpInfo) | **GET** /api/v1/order/{order_number} | 
[**getOrders**](OrderApi.md#getOrders) | **GET** /api/v1/orders | 
[**getOrdersWithHttpInfo**](OrderApi.md#getOrdersWithHttpInfo) | **GET** /api/v1/orders | 
[**patchOrder**](OrderApi.md#patchOrder) | **PATCH** /api/v1/orders/{order_id} | 
[**patchOrderWithHttpInfo**](OrderApi.md#patchOrderWithHttpInfo) | **PATCH** /api/v1/orders/{order_id} | 
[**replaceOrderTags**](OrderApi.md#replaceOrderTags) | **PUT** /api/v1/orders/{order_id}/tags | 
[**replaceOrderTagsWithHttpInfo**](OrderApi.md#replaceOrderTagsWithHttpInfo) | **PUT** /api/v1/orders/{order_id}/tags | 
[**updateOrderState**](OrderApi.md#updateOrderState) | **PUT** /api/v1/orders/{order_id}/state | 
[**updateOrderStateWithHttpInfo**](OrderApi.md#updateOrderStateWithHttpInfo) | **PUT** /api/v1/orders/{order_id}/state | 



## addOrderTags

> addOrderTags(addOrderTagsRequest): ApiRequest[Order]



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
    val apiInstance = OrderApi("https://demo.simplebilly.com")
    val orderId: String = orderId_example // String | 

    val orderTagsRequest: OrderTagsRequest =  // OrderTagsRequest | 
    
    val request = apiInstance.addOrderTags(orderId, orderTagsRequest)
    val response = apiInvoker.execute(request)

    response.onComplete {
        case Success(ApiResponse(code, content, headers)) =>
            System.out.println(s"Status code: $code}")
            System.out.println(s"Response headers: ${headers.mkString(", ")}")
            System.out.println(s"Response body: $content")
        
        case Failure(error @ ApiError(code, message, responseContent, cause, headers)) =>
            System.err.println("Exception when calling OrderApi#addOrderTags")
            System.err.println(s"Status code: $code}")
            System.err.println(s"Reason: $responseContent")
            System.err.println(s"Response headers: ${headers.mkString(", ")}")
            error.printStackTrace();

        case Failure(exception) => 
            System.err.println("Exception when calling OrderApi#addOrderTags")
            exception.printStackTrace();
    }
}
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **orderId** | **String**|  |
 **orderTagsRequest** | [**OrderTagsRequest**](OrderTagsRequest.md)|  |

### Return type

ApiRequest[[**Order**](Order.md)]


### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Tags added |  -  |
| **404** | Order not found |  -  |
| **500** | Internal server error |  -  |


## findOrderByExternalRef

> findOrderByExternalRef(findOrderByExternalRefRequest): ApiRequest[Order]



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
    val apiInstance = OrderApi("https://demo.simplebilly.com")
    val extRef: String = extRef_example // String | 
    
    val request = apiInstance.findOrderByExternalRef(extRef)
    val response = apiInvoker.execute(request)

    response.onComplete {
        case Success(ApiResponse(code, content, headers)) =>
            System.out.println(s"Status code: $code}")
            System.out.println(s"Response headers: ${headers.mkString(", ")}")
            System.out.println(s"Response body: $content")
        
        case Failure(error @ ApiError(code, message, responseContent, cause, headers)) =>
            System.err.println("Exception when calling OrderApi#findOrderByExternalRef")
            System.err.println(s"Status code: $code}")
            System.err.println(s"Reason: $responseContent")
            System.err.println(s"Response headers: ${headers.mkString(", ")}")
            error.printStackTrace();

        case Failure(exception) => 
            System.err.println("Exception when calling OrderApi#findOrderByExternalRef")
            exception.printStackTrace();
    }
}
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **extRef** | **String**|  |

### Return type

ApiRequest[[**Order**](Order.md)]


### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Order found |  -  |
| **404** | Order not found |  -  |
| **500** | Internal server error |  -  |


## getOrder

> getOrder(getOrderRequest): ApiRequest[Order]



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
    val apiInstance = OrderApi("https://demo.simplebilly.com")
    val orderNumber: String = orderNumber_example // String | 
    
    val request = apiInstance.getOrder(orderNumber)
    val response = apiInvoker.execute(request)

    response.onComplete {
        case Success(ApiResponse(code, content, headers)) =>
            System.out.println(s"Status code: $code}")
            System.out.println(s"Response headers: ${headers.mkString(", ")}")
            System.out.println(s"Response body: $content")
        
        case Failure(error @ ApiError(code, message, responseContent, cause, headers)) =>
            System.err.println("Exception when calling OrderApi#getOrder")
            System.err.println(s"Status code: $code}")
            System.err.println(s"Reason: $responseContent")
            System.err.println(s"Response headers: ${headers.mkString(", ")}")
            error.printStackTrace();

        case Failure(exception) => 
            System.err.println("Exception when calling OrderApi#getOrder")
            exception.printStackTrace();
    }
}
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **orderNumber** | **String**|  |

### Return type

ApiRequest[[**Order**](Order.md)]


### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Order found |  -  |
| **400** | Bad Request |  -  |
| **404** | Order not found |  -  |
| **500** | Internal Server Error |  -  |


## getOrders

> getOrders(getOrdersRequest): ApiRequest[Seq[Order]]



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
    val apiInstance = OrderApi("https://demo.simplebilly.com")
    val page: Int = 1 // Int | 

    val pageSize: Int = 56 // Int | 

    val search: String = search_example // String | 

    val includeDeleted: Boolean = true // Boolean | Soft-delete entities: set true to include rows with `deleted_at` set.
    
    val request = apiInstance.getOrders(page, pageSize, search, includeDeleted)
    val response = apiInvoker.execute(request)

    response.onComplete {
        case Success(ApiResponse(code, content, headers)) =>
            System.out.println(s"Status code: $code}")
            System.out.println(s"Response headers: ${headers.mkString(", ")}")
            System.out.println(s"Response body: $content")
        
        case Failure(error @ ApiError(code, message, responseContent, cause, headers)) =>
            System.err.println("Exception when calling OrderApi#getOrders")
            System.err.println(s"Status code: $code}")
            System.err.println(s"Reason: $responseContent")
            System.err.println(s"Response headers: ${headers.mkString(", ")}")
            error.printStackTrace();

        case Failure(exception) => 
            System.err.println("Exception when calling OrderApi#getOrders")
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

ApiRequest[[**Seq[Order]**](Order.md)]


### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Orders found |  -  |
| **400** | Bad Request |  -  |
| **404** | No orders found |  -  |
| **500** | Internal Server Error |  -  |


## patchOrder

> patchOrder(patchOrderRequest): ApiRequest[Order]



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
    val apiInstance = OrderApi("https://demo.simplebilly.com")
    val orderId: String = orderId_example // String | 

    val body: AnyType =  // AnyType | 
    
    val request = apiInstance.patchOrder(orderId, body)
    val response = apiInvoker.execute(request)

    response.onComplete {
        case Success(ApiResponse(code, content, headers)) =>
            System.out.println(s"Status code: $code}")
            System.out.println(s"Response headers: ${headers.mkString(", ")}")
            System.out.println(s"Response body: $content")
        
        case Failure(error @ ApiError(code, message, responseContent, cause, headers)) =>
            System.err.println("Exception when calling OrderApi#patchOrder")
            System.err.println(s"Status code: $code}")
            System.err.println(s"Reason: $responseContent")
            System.err.println(s"Response headers: ${headers.mkString(", ")}")
            error.printStackTrace();

        case Failure(exception) => 
            System.err.println("Exception when calling OrderApi#patchOrder")
            exception.printStackTrace();
    }
}
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **orderId** | **String**|  |
 **body** | **AnyType**|  |

### Return type

ApiRequest[[**Order**](Order.md)]


### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Order updated |  -  |
| **400** | Bad request |  -  |
| **404** | Order not found |  -  |
| **500** | Internal server error |  -  |


## replaceOrderTags

> replaceOrderTags(replaceOrderTagsRequest): ApiRequest[Order]



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
    val apiInstance = OrderApi("https://demo.simplebilly.com")
    val orderId: String = orderId_example // String | 

    val orderTagsRequest: OrderTagsRequest =  // OrderTagsRequest | 
    
    val request = apiInstance.replaceOrderTags(orderId, orderTagsRequest)
    val response = apiInvoker.execute(request)

    response.onComplete {
        case Success(ApiResponse(code, content, headers)) =>
            System.out.println(s"Status code: $code}")
            System.out.println(s"Response headers: ${headers.mkString(", ")}")
            System.out.println(s"Response body: $content")
        
        case Failure(error @ ApiError(code, message, responseContent, cause, headers)) =>
            System.err.println("Exception when calling OrderApi#replaceOrderTags")
            System.err.println(s"Status code: $code}")
            System.err.println(s"Reason: $responseContent")
            System.err.println(s"Response headers: ${headers.mkString(", ")}")
            error.printStackTrace();

        case Failure(exception) => 
            System.err.println("Exception when calling OrderApi#replaceOrderTags")
            exception.printStackTrace();
    }
}
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **orderId** | **String**|  |
 **orderTagsRequest** | [**OrderTagsRequest**](OrderTagsRequest.md)|  |

### Return type

ApiRequest[[**Order**](Order.md)]


### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Tags replaced |  -  |
| **404** | Order not found |  -  |
| **500** | Internal server error |  -  |


## updateOrderState

> updateOrderState(updateOrderStateRequest): ApiRequest[Order]



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
    val apiInstance = OrderApi("https://demo.simplebilly.com")
    val orderId: String = orderId_example // String | 

    val orderStateUpdate: OrderStateUpdate =  // OrderStateUpdate | 
    
    val request = apiInstance.updateOrderState(orderId, orderStateUpdate)
    val response = apiInvoker.execute(request)

    response.onComplete {
        case Success(ApiResponse(code, content, headers)) =>
            System.out.println(s"Status code: $code}")
            System.out.println(s"Response headers: ${headers.mkString(", ")}")
            System.out.println(s"Response body: $content")
        
        case Failure(error @ ApiError(code, message, responseContent, cause, headers)) =>
            System.err.println("Exception when calling OrderApi#updateOrderState")
            System.err.println(s"Status code: $code}")
            System.err.println(s"Reason: $responseContent")
            System.err.println(s"Response headers: ${headers.mkString(", ")}")
            error.printStackTrace();

        case Failure(exception) => 
            System.err.println("Exception when calling OrderApi#updateOrderState")
            exception.printStackTrace();
    }
}
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **orderId** | **String**|  |
 **orderStateUpdate** | [**OrderStateUpdate**](OrderStateUpdate.md)|  |

### Return type

ApiRequest[[**Order**](Order.md)]


### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Order state updated |  -  |
| **400** | Bad request |  -  |
| **404** | Order not found |  -  |
| **500** | Internal server error |  -  |

