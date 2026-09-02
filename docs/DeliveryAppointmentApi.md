# DeliveryAppointmentApi

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**createDeliveryAppointment**](DeliveryAppointmentApi.md#createDeliveryAppointment) | **POST** /api/v1/delivery-appointments | 
[**createDeliveryAppointmentWithHttpInfo**](DeliveryAppointmentApi.md#createDeliveryAppointmentWithHttpInfo) | **POST** /api/v1/delivery-appointments | 
[**deleteDeliveryAppointment**](DeliveryAppointmentApi.md#deleteDeliveryAppointment) | **DELETE** /api/v1/delivery-appointments/{appointment_id} | 
[**deleteDeliveryAppointmentWithHttpInfo**](DeliveryAppointmentApi.md#deleteDeliveryAppointmentWithHttpInfo) | **DELETE** /api/v1/delivery-appointments/{appointment_id} | 
[**getDeliveryAppointment**](DeliveryAppointmentApi.md#getDeliveryAppointment) | **GET** /api/v1/delivery-appointments/{appointment_id} | 
[**getDeliveryAppointmentWithHttpInfo**](DeliveryAppointmentApi.md#getDeliveryAppointmentWithHttpInfo) | **GET** /api/v1/delivery-appointments/{appointment_id} | 
[**getPublicDeliveryAppointmentStatus**](DeliveryAppointmentApi.md#getPublicDeliveryAppointmentStatus) | **GET** /api/v1/public/delivery-appointments/status | Supplier/carrier checks appointment status (public, no auth). The appointment is only revealed when email AND token match.
[**getPublicDeliveryAppointmentStatusWithHttpInfo**](DeliveryAppointmentApi.md#getPublicDeliveryAppointmentStatusWithHttpInfo) | **GET** /api/v1/public/delivery-appointments/status | Supplier/carrier checks appointment status (public, no auth). The appointment is only revealed when email AND token match.
[**listDeliveryAppointments**](DeliveryAppointmentApi.md#listDeliveryAppointments) | **GET** /api/v1/delivery-appointments | 
[**listDeliveryAppointmentsWithHttpInfo**](DeliveryAppointmentApi.md#listDeliveryAppointmentsWithHttpInfo) | **GET** /api/v1/delivery-appointments | 
[**requestPublicDeliveryAppointment**](DeliveryAppointmentApi.md#requestPublicDeliveryAppointment) | **POST** /api/v1/public/delivery-appointments/request | Supplier/carrier requests an inbound delivery slot (public, no auth). The tenant is derived from the warehouse found by &#x60;code&#x60; — never from the request.
[**requestPublicDeliveryAppointmentWithHttpInfo**](DeliveryAppointmentApi.md#requestPublicDeliveryAppointmentWithHttpInfo) | **POST** /api/v1/public/delivery-appointments/request | Supplier/carrier requests an inbound delivery slot (public, no auth). The tenant is derived from the warehouse found by &#x60;code&#x60; — never from the request.
[**updateDeliveryAppointment**](DeliveryAppointmentApi.md#updateDeliveryAppointment) | **PUT** /api/v1/delivery-appointments/{appointment_id} | 
[**updateDeliveryAppointmentWithHttpInfo**](DeliveryAppointmentApi.md#updateDeliveryAppointmentWithHttpInfo) | **PUT** /api/v1/delivery-appointments/{appointment_id} | 
[**updateDeliveryAppointmentStatus**](DeliveryAppointmentApi.md#updateDeliveryAppointmentStatus) | **PUT** /api/v1/delivery-appointments/{appointment_id}/status | 
[**updateDeliveryAppointmentStatusWithHttpInfo**](DeliveryAppointmentApi.md#updateDeliveryAppointmentStatusWithHttpInfo) | **PUT** /api/v1/delivery-appointments/{appointment_id}/status | 



## createDeliveryAppointment

> createDeliveryAppointment(createDeliveryAppointmentRequest): ApiRequest[DeliveryAppointment]



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
    val apiInstance = DeliveryAppointmentApi("https://demo.simplebilly.com")
    val deliveryAppointmentCreate: DeliveryAppointmentCreate =  // DeliveryAppointmentCreate | 
    
    val request = apiInstance.createDeliveryAppointment(deliveryAppointmentCreate)
    val response = apiInvoker.execute(request)

    response.onComplete {
        case Success(ApiResponse(code, content, headers)) =>
            System.out.println(s"Status code: $code}")
            System.out.println(s"Response headers: ${headers.mkString(", ")}")
            System.out.println(s"Response body: $content")
        
        case Failure(error @ ApiError(code, message, responseContent, cause, headers)) =>
            System.err.println("Exception when calling DeliveryAppointmentApi#createDeliveryAppointment")
            System.err.println(s"Status code: $code}")
            System.err.println(s"Reason: $responseContent")
            System.err.println(s"Response headers: ${headers.mkString(", ")}")
            error.printStackTrace();

        case Failure(exception) => 
            System.err.println("Exception when calling DeliveryAppointmentApi#createDeliveryAppointment")
            exception.printStackTrace();
    }
}
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **deliveryAppointmentCreate** | [**DeliveryAppointmentCreate**](DeliveryAppointmentCreate.md)|  |

### Return type

ApiRequest[[**DeliveryAppointment**](DeliveryAppointment.md)]


### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Created |  -  |
| **400** | Bad request |  -  |
| **500** | Internal server error |  -  |


## deleteDeliveryAppointment

> deleteDeliveryAppointment(deleteDeliveryAppointmentRequest): ApiRequest[Unit]



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
    val apiInstance = DeliveryAppointmentApi("https://demo.simplebilly.com")
    val appointmentId: String = appointmentId_example // String | 
    
    val request = apiInstance.deleteDeliveryAppointment(appointmentId)
    val response = apiInvoker.execute(request)

    response.onComplete {
        case Success(ApiResponse(code, content, headers)) =>
            System.out.println(s"Status code: $code}")
            System.out.println(s"Response headers: ${headers.mkString(", ")}")
        
        case Failure(error @ ApiError(code, message, responseContent, cause, headers)) =>
            System.err.println("Exception when calling DeliveryAppointmentApi#deleteDeliveryAppointment")
            System.err.println(s"Status code: $code}")
            System.err.println(s"Reason: $responseContent")
            System.err.println(s"Response headers: ${headers.mkString(", ")}")
            error.printStackTrace();

        case Failure(exception) => 
            System.err.println("Exception when calling DeliveryAppointmentApi#deleteDeliveryAppointment")
            exception.printStackTrace();
    }
}
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **appointmentId** | **String**|  |

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
| **204** | No Content |  -  |
| **404** | Not found |  -  |
| **500** | Internal server error |  -  |


## getDeliveryAppointment

> getDeliveryAppointment(getDeliveryAppointmentRequest): ApiRequest[DeliveryAppointment]



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
    val apiInstance = DeliveryAppointmentApi("https://demo.simplebilly.com")
    val appointmentId: String = appointmentId_example // String | 
    
    val request = apiInstance.getDeliveryAppointment(appointmentId)
    val response = apiInvoker.execute(request)

    response.onComplete {
        case Success(ApiResponse(code, content, headers)) =>
            System.out.println(s"Status code: $code}")
            System.out.println(s"Response headers: ${headers.mkString(", ")}")
            System.out.println(s"Response body: $content")
        
        case Failure(error @ ApiError(code, message, responseContent, cause, headers)) =>
            System.err.println("Exception when calling DeliveryAppointmentApi#getDeliveryAppointment")
            System.err.println(s"Status code: $code}")
            System.err.println(s"Reason: $responseContent")
            System.err.println(s"Response headers: ${headers.mkString(", ")}")
            error.printStackTrace();

        case Failure(exception) => 
            System.err.println("Exception when calling DeliveryAppointmentApi#getDeliveryAppointment")
            exception.printStackTrace();
    }
}
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **appointmentId** | **String**|  |

### Return type

ApiRequest[[**DeliveryAppointment**](DeliveryAppointment.md)]


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


## getPublicDeliveryAppointmentStatus

> getPublicDeliveryAppointmentStatus(getPublicDeliveryAppointmentStatusRequest): ApiRequest[PublicDeliveryAppointmentStatusResponse]

Supplier/carrier checks appointment status (public, no auth). The appointment is only revealed when email AND token match.

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
    val apiInstance = DeliveryAppointmentApi("https://demo.simplebilly.com")
    val appointmentId: String = appointmentId_example // String | 

    val email: String = email_example // String | 

    val token: String = token_example // String | 
    
    val request = apiInstance.getPublicDeliveryAppointmentStatus(appointmentId, email, token)
    val response = apiInvoker.execute(request)

    response.onComplete {
        case Success(ApiResponse(code, content, headers)) =>
            System.out.println(s"Status code: $code}")
            System.out.println(s"Response headers: ${headers.mkString(", ")}")
            System.out.println(s"Response body: $content")
        
        case Failure(error @ ApiError(code, message, responseContent, cause, headers)) =>
            System.err.println("Exception when calling DeliveryAppointmentApi#getPublicDeliveryAppointmentStatus")
            System.err.println(s"Status code: $code}")
            System.err.println(s"Reason: $responseContent")
            System.err.println(s"Response headers: ${headers.mkString(", ")}")
            error.printStackTrace();

        case Failure(exception) => 
            System.err.println("Exception when calling DeliveryAppointmentApi#getPublicDeliveryAppointmentStatus")
            exception.printStackTrace();
    }
}
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **appointmentId** | **String**|  |
 **email** | **String**|  |
 **token** | **String**|  |

### Return type

ApiRequest[[**PublicDeliveryAppointmentStatusResponse**](PublicDeliveryAppointmentStatusResponse.md)]


### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Appointment status |  -  |
| **404** | Appointment not found or credentials mismatch |  -  |
| **500** | Internal server error |  -  |


## listDeliveryAppointments

> listDeliveryAppointments(listDeliveryAppointmentsRequest): ApiRequest[Seq[DeliveryAppointment]]



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
    val apiInstance = DeliveryAppointmentApi("https://demo.simplebilly.com")
    val page: Int = 56 // Int | 

    val pageSize: Int = 56 // Int | 

    val status: String = status_example // String | 

    val warehouseId: String = warehouseId_example // String | 

    val from: LocalDate = 2013-10-20 // LocalDate | 

    val to: LocalDate = 2013-10-20 // LocalDate | 
    
    val request = apiInstance.listDeliveryAppointments(page, pageSize, status, warehouseId, from, to)
    val response = apiInvoker.execute(request)

    response.onComplete {
        case Success(ApiResponse(code, content, headers)) =>
            System.out.println(s"Status code: $code}")
            System.out.println(s"Response headers: ${headers.mkString(", ")}")
            System.out.println(s"Response body: $content")
        
        case Failure(error @ ApiError(code, message, responseContent, cause, headers)) =>
            System.err.println("Exception when calling DeliveryAppointmentApi#listDeliveryAppointments")
            System.err.println(s"Status code: $code}")
            System.err.println(s"Reason: $responseContent")
            System.err.println(s"Response headers: ${headers.mkString(", ")}")
            error.printStackTrace();

        case Failure(exception) => 
            System.err.println("Exception when calling DeliveryAppointmentApi#listDeliveryAppointments")
            exception.printStackTrace();
    }
}
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **page** | **Int**|  | [optional]
 **pageSize** | **Int**|  | [optional]
 **status** | **String**|  | [optional]
 **warehouseId** | **String**|  | [optional]
 **from** | **LocalDate**|  | [optional]
 **to** | **LocalDate**|  | [optional]

### Return type

ApiRequest[[**Seq[DeliveryAppointment]**](DeliveryAppointment.md)]


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


## requestPublicDeliveryAppointment

> requestPublicDeliveryAppointment(requestPublicDeliveryAppointmentRequest): ApiRequest[PublicDeliveryAppointmentResponse]

Supplier/carrier requests an inbound delivery slot (public, no auth). The tenant is derived from the warehouse found by &#x60;code&#x60; — never from the request.

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
    val apiInstance = DeliveryAppointmentApi("https://demo.simplebilly.com")
    val publicDeliveryAppointmentRequest: PublicDeliveryAppointmentRequest =  // PublicDeliveryAppointmentRequest | 
    
    val request = apiInstance.requestPublicDeliveryAppointment(publicDeliveryAppointmentRequest)
    val response = apiInvoker.execute(request)

    response.onComplete {
        case Success(ApiResponse(code, content, headers)) =>
            System.out.println(s"Status code: $code}")
            System.out.println(s"Response headers: ${headers.mkString(", ")}")
            System.out.println(s"Response body: $content")
        
        case Failure(error @ ApiError(code, message, responseContent, cause, headers)) =>
            System.err.println("Exception when calling DeliveryAppointmentApi#requestPublicDeliveryAppointment")
            System.err.println(s"Status code: $code}")
            System.err.println(s"Reason: $responseContent")
            System.err.println(s"Response headers: ${headers.mkString(", ")}")
            error.printStackTrace();

        case Failure(exception) => 
            System.err.println("Exception when calling DeliveryAppointmentApi#requestPublicDeliveryAppointment")
            exception.printStackTrace();
    }
}
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **publicDeliveryAppointmentRequest** | [**PublicDeliveryAppointmentRequest**](PublicDeliveryAppointmentRequest.md)|  |

### Return type

ApiRequest[[**PublicDeliveryAppointmentResponse**](PublicDeliveryAppointmentResponse.md)]


### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Appointment requested |  -  |
| **404** | Warehouse not found |  -  |
| **500** | Internal server error |  -  |


## updateDeliveryAppointment

> updateDeliveryAppointment(updateDeliveryAppointmentRequest): ApiRequest[DeliveryAppointment]



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
    val apiInstance = DeliveryAppointmentApi("https://demo.simplebilly.com")
    val appointmentId: String = appointmentId_example // String | 

    val body: AnyType =  // AnyType | 
    
    val request = apiInstance.updateDeliveryAppointment(appointmentId, body)
    val response = apiInvoker.execute(request)

    response.onComplete {
        case Success(ApiResponse(code, content, headers)) =>
            System.out.println(s"Status code: $code}")
            System.out.println(s"Response headers: ${headers.mkString(", ")}")
            System.out.println(s"Response body: $content")
        
        case Failure(error @ ApiError(code, message, responseContent, cause, headers)) =>
            System.err.println("Exception when calling DeliveryAppointmentApi#updateDeliveryAppointment")
            System.err.println(s"Status code: $code}")
            System.err.println(s"Reason: $responseContent")
            System.err.println(s"Response headers: ${headers.mkString(", ")}")
            error.printStackTrace();

        case Failure(exception) => 
            System.err.println("Exception when calling DeliveryAppointmentApi#updateDeliveryAppointment")
            exception.printStackTrace();
    }
}
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **appointmentId** | **String**|  |
 **body** | **AnyType**|  |

### Return type

ApiRequest[[**DeliveryAppointment**](DeliveryAppointment.md)]


### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |
| **400** | Bad request |  -  |
| **404** | Not found |  -  |
| **500** | Internal server error |  -  |


## updateDeliveryAppointmentStatus

> updateDeliveryAppointmentStatus(updateDeliveryAppointmentStatusRequest): ApiRequest[DeliveryAppointment]



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
    val apiInstance = DeliveryAppointmentApi("https://demo.simplebilly.com")
    val appointmentId: String = appointmentId_example // String | 

    val appointmentStatusUpdate: AppointmentStatusUpdate =  // AppointmentStatusUpdate | 
    
    val request = apiInstance.updateDeliveryAppointmentStatus(appointmentId, appointmentStatusUpdate)
    val response = apiInvoker.execute(request)

    response.onComplete {
        case Success(ApiResponse(code, content, headers)) =>
            System.out.println(s"Status code: $code}")
            System.out.println(s"Response headers: ${headers.mkString(", ")}")
            System.out.println(s"Response body: $content")
        
        case Failure(error @ ApiError(code, message, responseContent, cause, headers)) =>
            System.err.println("Exception when calling DeliveryAppointmentApi#updateDeliveryAppointmentStatus")
            System.err.println(s"Status code: $code}")
            System.err.println(s"Reason: $responseContent")
            System.err.println(s"Response headers: ${headers.mkString(", ")}")
            error.printStackTrace();

        case Failure(exception) => 
            System.err.println("Exception when calling DeliveryAppointmentApi#updateDeliveryAppointmentStatus")
            exception.printStackTrace();
    }
}
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **appointmentId** | **String**|  |
 **appointmentStatusUpdate** | [**AppointmentStatusUpdate**](AppointmentStatusUpdate.md)|  |

### Return type

ApiRequest[[**DeliveryAppointment**](DeliveryAppointment.md)]


### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |
| **400** | Bad request / invalid transition |  -  |
| **404** | Not found |  -  |
| **500** | Internal server error |  -  |

