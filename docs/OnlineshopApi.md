# OnlineshopApi

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**getSmtpConfigApi**](OnlineshopApi.md#getSmtpConfigApi) | **GET** /api/v1/settings/smtp | 
[**getSmtpConfigApiWithHttpInfo**](OnlineshopApi.md#getSmtpConfigApiWithHttpInfo) | **GET** /api/v1/settings/smtp | 
[**saveSmtpConfigApi**](OnlineshopApi.md#saveSmtpConfigApi) | **PUT** /api/v1/settings/smtp | 
[**saveSmtpConfigApiWithHttpInfo**](OnlineshopApi.md#saveSmtpConfigApiWithHttpInfo) | **PUT** /api/v1/settings/smtp | 



## getSmtpConfigApi

> getSmtpConfigApi(): ApiRequest[SmtpConfig]



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
    val apiInstance = OnlineshopApi("https://demo.simplebilly.com")    
    val request = apiInstance.getSmtpConfigApi()
    val response = apiInvoker.execute(request)

    response.onComplete {
        case Success(ApiResponse(code, content, headers)) =>
            System.out.println(s"Status code: $code}")
            System.out.println(s"Response headers: ${headers.mkString(", ")}")
            System.out.println(s"Response body: $content")
        
        case Failure(error @ ApiError(code, message, responseContent, cause, headers)) =>
            System.err.println("Exception when calling OnlineshopApi#getSmtpConfigApi")
            System.err.println(s"Status code: $code}")
            System.err.println(s"Reason: $responseContent")
            System.err.println(s"Response headers: ${headers.mkString(", ")}")
            error.printStackTrace();

        case Failure(exception) => 
            System.err.println("Exception when calling OnlineshopApi#getSmtpConfigApi")
            exception.printStackTrace();
    }
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

ApiRequest[[**SmtpConfig**](SmtpConfig.md)]


### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Tenant SMTP config (null if unset) |  -  |
| **500** | Internal server error |  -  |


## saveSmtpConfigApi

> saveSmtpConfigApi(saveSmtpConfigApiRequest): ApiRequest[SmtpConfig]



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
    val apiInstance = OnlineshopApi("https://demo.simplebilly.com")
    val smtpConfig: SmtpConfig =  // SmtpConfig | 
    
    val request = apiInstance.saveSmtpConfigApi(smtpConfig)
    val response = apiInvoker.execute(request)

    response.onComplete {
        case Success(ApiResponse(code, content, headers)) =>
            System.out.println(s"Status code: $code}")
            System.out.println(s"Response headers: ${headers.mkString(", ")}")
            System.out.println(s"Response body: $content")
        
        case Failure(error @ ApiError(code, message, responseContent, cause, headers)) =>
            System.err.println("Exception when calling OnlineshopApi#saveSmtpConfigApi")
            System.err.println(s"Status code: $code}")
            System.err.println(s"Reason: $responseContent")
            System.err.println(s"Response headers: ${headers.mkString(", ")}")
            error.printStackTrace();

        case Failure(exception) => 
            System.err.println("Exception when calling OnlineshopApi#saveSmtpConfigApi")
            exception.printStackTrace();
    }
}
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **smtpConfig** | [**SmtpConfig**](SmtpConfig.md)|  | [optional]

### Return type

ApiRequest[[**SmtpConfig**](SmtpConfig.md)]


### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Tenant SMTP config saved |  -  |
| **500** | Internal server error |  -  |

