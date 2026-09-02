# CustomerCommunicationApi

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**createCommunication**](CustomerCommunicationApi.md#createCommunication) | **POST** /api/v1/communications | 
[**createCommunicationWithHttpInfo**](CustomerCommunicationApi.md#createCommunicationWithHttpInfo) | **POST** /api/v1/communications | 
[**customercommunicationRestore**](CustomerCommunicationApi.md#customercommunicationRestore) | **POST** /api/v1/communications/{communication_id}/restore | 
[**customercommunicationRestoreWithHttpInfo**](CustomerCommunicationApi.md#customercommunicationRestoreWithHttpInfo) | **POST** /api/v1/communications/{communication_id}/restore | 
[**deleteCommunication**](CustomerCommunicationApi.md#deleteCommunication) | **DELETE** /api/v1/communications/{communication_id} | 
[**deleteCommunicationWithHttpInfo**](CustomerCommunicationApi.md#deleteCommunicationWithHttpInfo) | **DELETE** /api/v1/communications/{communication_id} | 
[**getCommunication**](CustomerCommunicationApi.md#getCommunication) | **GET** /api/v1/communications/{communication_id} | 
[**getCommunicationWithHttpInfo**](CustomerCommunicationApi.md#getCommunicationWithHttpInfo) | **GET** /api/v1/communications/{communication_id} | 
[**getContactHistory**](CustomerCommunicationApi.md#getContactHistory) | **GET** /api/v1/contacts/{contact_id}/communications | 
[**getContactHistoryWithHttpInfo**](CustomerCommunicationApi.md#getContactHistoryWithHttpInfo) | **GET** /api/v1/contacts/{contact_id}/communications | 
[**listCommunications**](CustomerCommunicationApi.md#listCommunications) | **GET** /api/v1/communications/ | 
[**listCommunicationsWithHttpInfo**](CustomerCommunicationApi.md#listCommunicationsWithHttpInfo) | **GET** /api/v1/communications/ | 
[**updateCommunication**](CustomerCommunicationApi.md#updateCommunication) | **PUT** /api/v1/communications/{communication_id} | 
[**updateCommunicationWithHttpInfo**](CustomerCommunicationApi.md#updateCommunicationWithHttpInfo) | **PUT** /api/v1/communications/{communication_id} | 



## createCommunication

> createCommunication(createCommunicationRequest): ApiRequest[CustomerCommunication]



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
    val apiInstance = CustomerCommunicationApi("https://demo.simplebilly.com")
    val customerCommunicationCreate: CustomerCommunicationCreate =  // CustomerCommunicationCreate | 
    
    val request = apiInstance.createCommunication(customerCommunicationCreate)
    val response = apiInvoker.execute(request)

    response.onComplete {
        case Success(ApiResponse(code, content, headers)) =>
            System.out.println(s"Status code: $code}")
            System.out.println(s"Response headers: ${headers.mkString(", ")}")
            System.out.println(s"Response body: $content")
        
        case Failure(error @ ApiError(code, message, responseContent, cause, headers)) =>
            System.err.println("Exception when calling CustomerCommunicationApi#createCommunication")
            System.err.println(s"Status code: $code}")
            System.err.println(s"Reason: $responseContent")
            System.err.println(s"Response headers: ${headers.mkString(", ")}")
            error.printStackTrace();

        case Failure(exception) => 
            System.err.println("Exception when calling CustomerCommunicationApi#createCommunication")
            exception.printStackTrace();
    }
}
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **customerCommunicationCreate** | [**CustomerCommunicationCreate**](CustomerCommunicationCreate.md)|  |

### Return type

ApiRequest[[**CustomerCommunication**](CustomerCommunication.md)]


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


## customercommunicationRestore

> customercommunicationRestore(customercommunicationRestoreRequest): ApiRequest[CustomerCommunication]



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
    val apiInstance = CustomerCommunicationApi("https://demo.simplebilly.com")
    val communicationId: String = communicationId_example // String | 
    
    val request = apiInstance.customercommunicationRestore(communicationId)
    val response = apiInvoker.execute(request)

    response.onComplete {
        case Success(ApiResponse(code, content, headers)) =>
            System.out.println(s"Status code: $code}")
            System.out.println(s"Response headers: ${headers.mkString(", ")}")
            System.out.println(s"Response body: $content")
        
        case Failure(error @ ApiError(code, message, responseContent, cause, headers)) =>
            System.err.println("Exception when calling CustomerCommunicationApi#customercommunicationRestore")
            System.err.println(s"Status code: $code}")
            System.err.println(s"Reason: $responseContent")
            System.err.println(s"Response headers: ${headers.mkString(", ")}")
            error.printStackTrace();

        case Failure(exception) => 
            System.err.println("Exception when calling CustomerCommunicationApi#customercommunicationRestore")
            exception.printStackTrace();
    }
}
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **communicationId** | **String**|  |

### Return type

ApiRequest[[**CustomerCommunication**](CustomerCommunication.md)]


### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Restored |  -  |
| **404** | Not found |  -  |
| **500** | Internal server error |  -  |


## deleteCommunication

> deleteCommunication(deleteCommunicationRequest): ApiRequest[Unit]



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
    val apiInstance = CustomerCommunicationApi("https://demo.simplebilly.com")
    val communicationId: String = communicationId_example // String | 
    
    val request = apiInstance.deleteCommunication(communicationId)
    val response = apiInvoker.execute(request)

    response.onComplete {
        case Success(ApiResponse(code, content, headers)) =>
            System.out.println(s"Status code: $code}")
            System.out.println(s"Response headers: ${headers.mkString(", ")}")
        
        case Failure(error @ ApiError(code, message, responseContent, cause, headers)) =>
            System.err.println("Exception when calling CustomerCommunicationApi#deleteCommunication")
            System.err.println(s"Status code: $code}")
            System.err.println(s"Reason: $responseContent")
            System.err.println(s"Response headers: ${headers.mkString(", ")}")
            error.printStackTrace();

        case Failure(exception) => 
            System.err.println("Exception when calling CustomerCommunicationApi#deleteCommunication")
            exception.printStackTrace();
    }
}
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **communicationId** | **String**|  |

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


## getCommunication

> getCommunication(getCommunicationRequest): ApiRequest[CustomerCommunication]



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
    val apiInstance = CustomerCommunicationApi("https://demo.simplebilly.com")
    val communicationId: String = communicationId_example // String | 
    
    val request = apiInstance.getCommunication(communicationId)
    val response = apiInvoker.execute(request)

    response.onComplete {
        case Success(ApiResponse(code, content, headers)) =>
            System.out.println(s"Status code: $code}")
            System.out.println(s"Response headers: ${headers.mkString(", ")}")
            System.out.println(s"Response body: $content")
        
        case Failure(error @ ApiError(code, message, responseContent, cause, headers)) =>
            System.err.println("Exception when calling CustomerCommunicationApi#getCommunication")
            System.err.println(s"Status code: $code}")
            System.err.println(s"Reason: $responseContent")
            System.err.println(s"Response headers: ${headers.mkString(", ")}")
            error.printStackTrace();

        case Failure(exception) => 
            System.err.println("Exception when calling CustomerCommunicationApi#getCommunication")
            exception.printStackTrace();
    }
}
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **communicationId** | **String**|  |

### Return type

ApiRequest[[**CustomerCommunication**](CustomerCommunication.md)]


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


## getContactHistory

> getContactHistory(getContactHistoryRequest): ApiRequest[ContactHistoryResponse]



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
    val apiInstance = CustomerCommunicationApi("https://demo.simplebilly.com")
    val contactId: String = contactId_example // String | 
    
    val request = apiInstance.getContactHistory(contactId)
    val response = apiInvoker.execute(request)

    response.onComplete {
        case Success(ApiResponse(code, content, headers)) =>
            System.out.println(s"Status code: $code}")
            System.out.println(s"Response headers: ${headers.mkString(", ")}")
            System.out.println(s"Response body: $content")
        
        case Failure(error @ ApiError(code, message, responseContent, cause, headers)) =>
            System.err.println("Exception when calling CustomerCommunicationApi#getContactHistory")
            System.err.println(s"Status code: $code}")
            System.err.println(s"Reason: $responseContent")
            System.err.println(s"Response headers: ${headers.mkString(", ")}")
            error.printStackTrace();

        case Failure(exception) => 
            System.err.println("Exception when calling CustomerCommunicationApi#getContactHistory")
            exception.printStackTrace();
    }
}
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **contactId** | **String**|  |

### Return type

ApiRequest[[**ContactHistoryResponse**](ContactHistoryResponse.md)]


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


## listCommunications

> listCommunications(listCommunicationsRequest): ApiRequest[Seq[CustomerCommunication]]



### Example

```scala
// Import classes:
import 
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
    val apiInstance = CustomerCommunicationApi("https://demo.simplebilly.com")
    val page: Int = 56 // Int | 

    val pageSize: Int = 56 // Int | 

    val contactId: String = contactId_example // String | Filter history to a single contact.

    val channel: CommunicationChannel =  // CommunicationChannel | 

    val direction: CommunicationDirection =  // CommunicationDirection | 

    val from: LocalDate = 2013-10-20 // LocalDate | Only include communications after this ISO date (inclusive).

    val to: LocalDate = 2013-10-20 // LocalDate | Only include communications before this ISO date (inclusive).
    
    val request = apiInstance.listCommunications(page, pageSize, contactId, channel, direction, from, to)
    val response = apiInvoker.execute(request)

    response.onComplete {
        case Success(ApiResponse(code, content, headers)) =>
            System.out.println(s"Status code: $code}")
            System.out.println(s"Response headers: ${headers.mkString(", ")}")
            System.out.println(s"Response body: $content")
        
        case Failure(error @ ApiError(code, message, responseContent, cause, headers)) =>
            System.err.println("Exception when calling CustomerCommunicationApi#listCommunications")
            System.err.println(s"Status code: $code}")
            System.err.println(s"Reason: $responseContent")
            System.err.println(s"Response headers: ${headers.mkString(", ")}")
            error.printStackTrace();

        case Failure(exception) => 
            System.err.println("Exception when calling CustomerCommunicationApi#listCommunications")
            exception.printStackTrace();
    }
}
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **page** | **Int**|  | [optional]
 **pageSize** | **Int**|  | [optional]
 **contactId** | **String**| Filter history to a single contact. | [optional]
 **channel** | [**CommunicationChannel**](.md)|  | [optional] [enum: email, call, meeting, chat, note]
 **direction** | [**CommunicationDirection**](.md)|  | [optional] [enum: inbound, outbound]
 **from** | **LocalDate**| Only include communications after this ISO date (inclusive). | [optional]
 **to** | **LocalDate**| Only include communications before this ISO date (inclusive). | [optional]

### Return type

ApiRequest[[**Seq[CustomerCommunication]**](CustomerCommunication.md)]


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


## updateCommunication

> updateCommunication(updateCommunicationRequest): ApiRequest[CustomerCommunication]



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
    val apiInstance = CustomerCommunicationApi("https://demo.simplebilly.com")
    val communicationId: String = communicationId_example // String | 

    val customerCommunicationUpdate: CustomerCommunicationUpdate =  // CustomerCommunicationUpdate | 
    
    val request = apiInstance.updateCommunication(communicationId, customerCommunicationUpdate)
    val response = apiInvoker.execute(request)

    response.onComplete {
        case Success(ApiResponse(code, content, headers)) =>
            System.out.println(s"Status code: $code}")
            System.out.println(s"Response headers: ${headers.mkString(", ")}")
            System.out.println(s"Response body: $content")
        
        case Failure(error @ ApiError(code, message, responseContent, cause, headers)) =>
            System.err.println("Exception when calling CustomerCommunicationApi#updateCommunication")
            System.err.println(s"Status code: $code}")
            System.err.println(s"Reason: $responseContent")
            System.err.println(s"Response headers: ${headers.mkString(", ")}")
            error.printStackTrace();

        case Failure(exception) => 
            System.err.println("Exception when calling CustomerCommunicationApi#updateCommunication")
            exception.printStackTrace();
    }
}
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **communicationId** | **String**|  |
 **customerCommunicationUpdate** | [**CustomerCommunicationUpdate**](CustomerCommunicationUpdate.md)|  |

### Return type

ApiRequest[[**CustomerCommunication**](CustomerCommunication.md)]


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

