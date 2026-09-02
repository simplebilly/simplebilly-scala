# AiApi

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**aiSuggestApi**](AiApi.md#aiSuggestApi) | **POST** /api/v1/support/ai/suggest | 
[**aiSuggestApiWithHttpInfo**](AiApi.md#aiSuggestApiWithHttpInfo) | **POST** /api/v1/support/ai/suggest | 
[**createWorkerApi**](AiApi.md#createWorkerApi) | **POST** /api/v1/support/ai/workers | 
[**createWorkerApiWithHttpInfo**](AiApi.md#createWorkerApiWithHttpInfo) | **POST** /api/v1/support/ai/workers | 
[**listWorkersApi**](AiApi.md#listWorkersApi) | **GET** /api/v1/support/ai/workers | 
[**listWorkersApiWithHttpInfo**](AiApi.md#listWorkersApiWithHttpInfo) | **GET** /api/v1/support/ai/workers | 
[**runWorkerApi**](AiApi.md#runWorkerApi) | **POST** /api/v1/support/ai/workers/{worker_id}/run | 
[**runWorkerApiWithHttpInfo**](AiApi.md#runWorkerApiWithHttpInfo) | **POST** /api/v1/support/ai/workers/{worker_id}/run | 



## aiSuggestApi

> aiSuggestApi(aiSuggestApiRequest): ApiRequest[AiSuggestion]



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
    val apiInstance = AiApi("https://demo.simplebilly.com")
    val aiSuggestionRequest: AiSuggestionRequest =  // AiSuggestionRequest | 
    
    val request = apiInstance.aiSuggestApi(aiSuggestionRequest)
    val response = apiInvoker.execute(request)

    response.onComplete {
        case Success(ApiResponse(code, content, headers)) =>
            System.out.println(s"Status code: $code}")
            System.out.println(s"Response headers: ${headers.mkString(", ")}")
            System.out.println(s"Response body: $content")
        
        case Failure(error @ ApiError(code, message, responseContent, cause, headers)) =>
            System.err.println("Exception when calling AiApi#aiSuggestApi")
            System.err.println(s"Status code: $code}")
            System.err.println(s"Reason: $responseContent")
            System.err.println(s"Response headers: ${headers.mkString(", ")}")
            error.printStackTrace();

        case Failure(exception) => 
            System.err.println("Exception when calling AiApi#aiSuggestApi")
            exception.printStackTrace();
    }
}
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **aiSuggestionRequest** | [**AiSuggestionRequest**](AiSuggestionRequest.md)|  |

### Return type

ApiRequest[[**AiSuggestion**](AiSuggestion.md)]


### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | AI suggestion |  -  |
| **500** | AI error |  -  |


## createWorkerApi

> createWorkerApi(createWorkerApiRequest): ApiRequest[AiWorkerConfig]



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
    val apiInstance = AiApi("https://demo.simplebilly.com")
    val aiConfigDto: AiConfigDto =  // AiConfigDto | 
    
    val request = apiInstance.createWorkerApi(aiConfigDto)
    val response = apiInvoker.execute(request)

    response.onComplete {
        case Success(ApiResponse(code, content, headers)) =>
            System.out.println(s"Status code: $code}")
            System.out.println(s"Response headers: ${headers.mkString(", ")}")
            System.out.println(s"Response body: $content")
        
        case Failure(error @ ApiError(code, message, responseContent, cause, headers)) =>
            System.err.println("Exception when calling AiApi#createWorkerApi")
            System.err.println(s"Status code: $code}")
            System.err.println(s"Reason: $responseContent")
            System.err.println(s"Response headers: ${headers.mkString(", ")}")
            error.printStackTrace();

        case Failure(exception) => 
            System.err.println("Exception when calling AiApi#createWorkerApi")
            exception.printStackTrace();
    }
}
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **aiConfigDto** | [**AiConfigDto**](AiConfigDto.md)|  |

### Return type

ApiRequest[[**AiWorkerConfig**](AiWorkerConfig.md)]


### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Worker created |  -  |


## listWorkersApi

> listWorkersApi(): ApiRequest[Seq[AiWorkerConfig]]



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
    val apiInstance = AiApi("https://demo.simplebilly.com")    
    val request = apiInstance.listWorkersApi()
    val response = apiInvoker.execute(request)

    response.onComplete {
        case Success(ApiResponse(code, content, headers)) =>
            System.out.println(s"Status code: $code}")
            System.out.println(s"Response headers: ${headers.mkString(", ")}")
            System.out.println(s"Response body: $content")
        
        case Failure(error @ ApiError(code, message, responseContent, cause, headers)) =>
            System.err.println("Exception when calling AiApi#listWorkersApi")
            System.err.println(s"Status code: $code}")
            System.err.println(s"Reason: $responseContent")
            System.err.println(s"Response headers: ${headers.mkString(", ")}")
            error.printStackTrace();

        case Failure(exception) => 
            System.err.println("Exception when calling AiApi#listWorkersApi")
            exception.printStackTrace();
    }
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

ApiRequest[[**Seq[AiWorkerConfig]**](AiWorkerConfig.md)]


### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | List AI workers |  -  |


## runWorkerApi

> runWorkerApi(runWorkerApiRequest): ApiRequest[AiSuggestion]



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
    val apiInstance = AiApi("https://demo.simplebilly.com")
    val workerId: UUID = 38400000-8cf0-11bd-b23e-10b96e4ef00d // UUID | 

    val aiSuggestionRequest: AiSuggestionRequest =  // AiSuggestionRequest | 
    
    val request = apiInstance.runWorkerApi(workerId, aiSuggestionRequest)
    val response = apiInvoker.execute(request)

    response.onComplete {
        case Success(ApiResponse(code, content, headers)) =>
            System.out.println(s"Status code: $code}")
            System.out.println(s"Response headers: ${headers.mkString(", ")}")
            System.out.println(s"Response body: $content")
        
        case Failure(error @ ApiError(code, message, responseContent, cause, headers)) =>
            System.err.println("Exception when calling AiApi#runWorkerApi")
            System.err.println(s"Status code: $code}")
            System.err.println(s"Reason: $responseContent")
            System.err.println(s"Response headers: ${headers.mkString(", ")}")
            error.printStackTrace();

        case Failure(exception) => 
            System.err.println("Exception when calling AiApi#runWorkerApi")
            exception.printStackTrace();
    }
}
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workerId** | **UUID**|  |
 **aiSuggestionRequest** | [**AiSuggestionRequest**](AiSuggestionRequest.md)|  |

### Return type

ApiRequest[[**AiSuggestion**](AiSuggestion.md)]


### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Worker executed |  -  |

