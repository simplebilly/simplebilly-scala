# TenantSettingsApi

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**getTenantSettings**](TenantSettingsApi.md#getTenantSettings) | **GET** /api/v1/settings/tenant | 
[**getTenantSettingsWithHttpInfo**](TenantSettingsApi.md#getTenantSettingsWithHttpInfo) | **GET** /api/v1/settings/tenant | 
[**updateTenantSettings**](TenantSettingsApi.md#updateTenantSettings) | **PUT** /api/v1/settings/tenant | 
[**updateTenantSettingsWithHttpInfo**](TenantSettingsApi.md#updateTenantSettingsWithHttpInfo) | **PUT** /api/v1/settings/tenant | 



## getTenantSettings

> getTenantSettings(): ApiRequest[TenantSettings]



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
    val apiInstance = TenantSettingsApi("https://demo.simplebilly.com")    
    val request = apiInstance.getTenantSettings()
    val response = apiInvoker.execute(request)

    response.onComplete {
        case Success(ApiResponse(code, content, headers)) =>
            System.out.println(s"Status code: $code}")
            System.out.println(s"Response headers: ${headers.mkString(", ")}")
            System.out.println(s"Response body: $content")
        
        case Failure(error @ ApiError(code, message, responseContent, cause, headers)) =>
            System.err.println("Exception when calling TenantSettingsApi#getTenantSettings")
            System.err.println(s"Status code: $code}")
            System.err.println(s"Reason: $responseContent")
            System.err.println(s"Response headers: ${headers.mkString(", ")}")
            error.printStackTrace();

        case Failure(exception) => 
            System.err.println("Exception when calling TenantSettingsApi#getTenantSettings")
            exception.printStackTrace();
    }
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

ApiRequest[[**TenantSettings**](TenantSettings.md)]


### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Tenant settings |  -  |
| **500** | Internal server error |  -  |


## updateTenantSettings

> updateTenantSettings(updateTenantSettingsRequest): ApiRequest[TenantSettings]



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
    val apiInstance = TenantSettingsApi("https://demo.simplebilly.com")
    val updateTenantSettings: UpdateTenantSettings =  // UpdateTenantSettings | 
    
    val request = apiInstance.updateTenantSettings(updateTenantSettings)
    val response = apiInvoker.execute(request)

    response.onComplete {
        case Success(ApiResponse(code, content, headers)) =>
            System.out.println(s"Status code: $code}")
            System.out.println(s"Response headers: ${headers.mkString(", ")}")
            System.out.println(s"Response body: $content")
        
        case Failure(error @ ApiError(code, message, responseContent, cause, headers)) =>
            System.err.println("Exception when calling TenantSettingsApi#updateTenantSettings")
            System.err.println(s"Status code: $code}")
            System.err.println(s"Reason: $responseContent")
            System.err.println(s"Response headers: ${headers.mkString(", ")}")
            error.printStackTrace();

        case Failure(exception) => 
            System.err.println("Exception when calling TenantSettingsApi#updateTenantSettings")
            exception.printStackTrace();
    }
}
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **updateTenantSettings** | [**UpdateTenantSettings**](UpdateTenantSettings.md)|  |

### Return type

ApiRequest[[**TenantSettings**](TenantSettings.md)]


### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Updated tenant settings |  -  |
| **400** | Bad request |  -  |
| **500** | Internal server error |  -  |

