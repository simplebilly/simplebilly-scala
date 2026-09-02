# KycRecordApi

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**createKycRecord**](KycRecordApi.md#createKycRecord) | **POST** /api/v1/kyc-records | 
[**createKycRecordWithHttpInfo**](KycRecordApi.md#createKycRecordWithHttpInfo) | **POST** /api/v1/kyc-records | 
[**deleteKycRecord**](KycRecordApi.md#deleteKycRecord) | **DELETE** /api/v1/kyc-records/{id} | 
[**deleteKycRecordWithHttpInfo**](KycRecordApi.md#deleteKycRecordWithHttpInfo) | **DELETE** /api/v1/kyc-records/{id} | 
[**getKycRecord**](KycRecordApi.md#getKycRecord) | **GET** /api/v1/kyc-records/{id} | 
[**getKycRecordWithHttpInfo**](KycRecordApi.md#getKycRecordWithHttpInfo) | **GET** /api/v1/kyc-records/{id} | 
[**getKycRecords**](KycRecordApi.md#getKycRecords) | **GET** /api/v1/kyc-records/ | 
[**getKycRecordsWithHttpInfo**](KycRecordApi.md#getKycRecordsWithHttpInfo) | **GET** /api/v1/kyc-records/ | 
[**updateKycRecord**](KycRecordApi.md#updateKycRecord) | **PUT** /api/v1/kyc-records/{id} | 
[**updateKycRecordWithHttpInfo**](KycRecordApi.md#updateKycRecordWithHttpInfo) | **PUT** /api/v1/kyc-records/{id} | 



## createKycRecord

> createKycRecord(createKycRecordRequest): ApiRequest[KycRecord]



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
    val apiInstance = KycRecordApi("https://demo.simplebilly.com")
    val kycRecordCreate: KycRecordCreate =  // KycRecordCreate | 
    
    val request = apiInstance.createKycRecord(kycRecordCreate)
    val response = apiInvoker.execute(request)

    response.onComplete {
        case Success(ApiResponse(code, content, headers)) =>
            System.out.println(s"Status code: $code}")
            System.out.println(s"Response headers: ${headers.mkString(", ")}")
            System.out.println(s"Response body: $content")
        
        case Failure(error @ ApiError(code, message, responseContent, cause, headers)) =>
            System.err.println("Exception when calling KycRecordApi#createKycRecord")
            System.err.println(s"Status code: $code}")
            System.err.println(s"Reason: $responseContent")
            System.err.println(s"Response headers: ${headers.mkString(", ")}")
            error.printStackTrace();

        case Failure(exception) => 
            System.err.println("Exception when calling KycRecordApi#createKycRecord")
            exception.printStackTrace();
    }
}
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **kycRecordCreate** | [**KycRecordCreate**](KycRecordCreate.md)|  |

### Return type

ApiRequest[[**KycRecord**](KycRecord.md)]


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


## deleteKycRecord

> deleteKycRecord(deleteKycRecordRequest): ApiRequest[Unit]



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
    val apiInstance = KycRecordApi("https://demo.simplebilly.com")
    val id: UUID = 38400000-8cf0-11bd-b23e-10b96e4ef00d // UUID | 
    
    val request = apiInstance.deleteKycRecord(id)
    val response = apiInvoker.execute(request)

    response.onComplete {
        case Success(ApiResponse(code, content, headers)) =>
            System.out.println(s"Status code: $code}")
            System.out.println(s"Response headers: ${headers.mkString(", ")}")
        
        case Failure(error @ ApiError(code, message, responseContent, cause, headers)) =>
            System.err.println("Exception when calling KycRecordApi#deleteKycRecord")
            System.err.println(s"Status code: $code}")
            System.err.println(s"Reason: $responseContent")
            System.err.println(s"Response headers: ${headers.mkString(", ")}")
            error.printStackTrace();

        case Failure(exception) => 
            System.err.println("Exception when calling KycRecordApi#deleteKycRecord")
            exception.printStackTrace();
    }
}
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **UUID**|  |

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


## getKycRecord

> getKycRecord(getKycRecordRequest): ApiRequest[KycRecord]



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
    val apiInstance = KycRecordApi("https://demo.simplebilly.com")
    val id: UUID = 38400000-8cf0-11bd-b23e-10b96e4ef00d // UUID | 
    
    val request = apiInstance.getKycRecord(id)
    val response = apiInvoker.execute(request)

    response.onComplete {
        case Success(ApiResponse(code, content, headers)) =>
            System.out.println(s"Status code: $code}")
            System.out.println(s"Response headers: ${headers.mkString(", ")}")
            System.out.println(s"Response body: $content")
        
        case Failure(error @ ApiError(code, message, responseContent, cause, headers)) =>
            System.err.println("Exception when calling KycRecordApi#getKycRecord")
            System.err.println(s"Status code: $code}")
            System.err.println(s"Reason: $responseContent")
            System.err.println(s"Response headers: ${headers.mkString(", ")}")
            error.printStackTrace();

        case Failure(exception) => 
            System.err.println("Exception when calling KycRecordApi#getKycRecord")
            exception.printStackTrace();
    }
}
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **UUID**|  |

### Return type

ApiRequest[[**KycRecord**](KycRecord.md)]


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


## getKycRecords

> getKycRecords(getKycRecordsRequest): ApiRequest[Seq[KycRecord]]



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
    val apiInstance = KycRecordApi("https://demo.simplebilly.com")
    val page: Int = 1 // Int | 

    val pageSize: Int = 56 // Int | 

    val search: String = search_example // String | 

    val includeDeleted: Boolean = true // Boolean | Soft-delete entities: set true to include rows with `deleted_at` set.
    
    val request = apiInstance.getKycRecords(page, pageSize, search, includeDeleted)
    val response = apiInvoker.execute(request)

    response.onComplete {
        case Success(ApiResponse(code, content, headers)) =>
            System.out.println(s"Status code: $code}")
            System.out.println(s"Response headers: ${headers.mkString(", ")}")
            System.out.println(s"Response body: $content")
        
        case Failure(error @ ApiError(code, message, responseContent, cause, headers)) =>
            System.err.println("Exception when calling KycRecordApi#getKycRecords")
            System.err.println(s"Status code: $code}")
            System.err.println(s"Reason: $responseContent")
            System.err.println(s"Response headers: ${headers.mkString(", ")}")
            error.printStackTrace();

        case Failure(exception) => 
            System.err.println("Exception when calling KycRecordApi#getKycRecords")
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

ApiRequest[[**Seq[KycRecord]**](KycRecord.md)]


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


## updateKycRecord

> updateKycRecord(updateKycRecordRequest): ApiRequest[KycRecord]



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
    val apiInstance = KycRecordApi("https://demo.simplebilly.com")
    val id: UUID = 38400000-8cf0-11bd-b23e-10b96e4ef00d // UUID | 

    val kycRecordUpdate: KycRecordUpdate =  // KycRecordUpdate | 
    
    val request = apiInstance.updateKycRecord(id, kycRecordUpdate)
    val response = apiInvoker.execute(request)

    response.onComplete {
        case Success(ApiResponse(code, content, headers)) =>
            System.out.println(s"Status code: $code}")
            System.out.println(s"Response headers: ${headers.mkString(", ")}")
            System.out.println(s"Response body: $content")
        
        case Failure(error @ ApiError(code, message, responseContent, cause, headers)) =>
            System.err.println("Exception when calling KycRecordApi#updateKycRecord")
            System.err.println(s"Status code: $code}")
            System.err.println(s"Reason: $responseContent")
            System.err.println(s"Response headers: ${headers.mkString(", ")}")
            error.printStackTrace();

        case Failure(exception) => 
            System.err.println("Exception when calling KycRecordApi#updateKycRecord")
            exception.printStackTrace();
    }
}
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **UUID**|  |
 **kycRecordUpdate** | [**KycRecordUpdate**](KycRecordUpdate.md)|  |

### Return type

ApiRequest[[**KycRecord**](KycRecord.md)]


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

