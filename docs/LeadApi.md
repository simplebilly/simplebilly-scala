# LeadApi

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**listLeadsApi**](LeadApi.md#listLeadsApi) | **GET** /api/v1/support/leads | 
[**listLeadsApiWithHttpInfo**](LeadApi.md#listLeadsApiWithHttpInfo) | **GET** /api/v1/support/leads | 
[**updateLeadApi**](LeadApi.md#updateLeadApi) | **PUT** /api/v1/support/leads/{lead_id} | 
[**updateLeadApiWithHttpInfo**](LeadApi.md#updateLeadApiWithHttpInfo) | **PUT** /api/v1/support/leads/{lead_id} | 



## listLeadsApi

> listLeadsApi(listLeadsApiRequest): ApiRequest[Seq[Lead]]



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
    val apiInstance = LeadApi("https://demo.simplebilly.com")
    val status: String = status_example // String | 

    val source: String = source_example // String | 

    val search: String = search_example // String | 

    val page: Int = 56 // Int | 

    val pageSize: Int = 56 // Int | 
    
    val request = apiInstance.listLeadsApi(status, source, search, page, pageSize)
    val response = apiInvoker.execute(request)

    response.onComplete {
        case Success(ApiResponse(code, content, headers)) =>
            System.out.println(s"Status code: $code}")
            System.out.println(s"Response headers: ${headers.mkString(", ")}")
            System.out.println(s"Response body: $content")
        
        case Failure(error @ ApiError(code, message, responseContent, cause, headers)) =>
            System.err.println("Exception when calling LeadApi#listLeadsApi")
            System.err.println(s"Status code: $code}")
            System.err.println(s"Reason: $responseContent")
            System.err.println(s"Response headers: ${headers.mkString(", ")}")
            error.printStackTrace();

        case Failure(exception) => 
            System.err.println("Exception when calling LeadApi#listLeadsApi")
            exception.printStackTrace();
    }
}
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **status** | **String**|  | [optional]
 **source** | **String**|  | [optional]
 **search** | **String**|  | [optional]
 **page** | **Int**|  | [optional]
 **pageSize** | **Int**|  | [optional]

### Return type

ApiRequest[[**Seq[Lead]**](Lead.md)]


### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Leads list |  -  |


## updateLeadApi

> updateLeadApi(updateLeadApiRequest): ApiRequest[Lead]



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
    val apiInstance = LeadApi("https://demo.simplebilly.com")
    val leadId: UUID = 38400000-8cf0-11bd-b23e-10b96e4ef00d // UUID | 

    val leadUpdate: LeadUpdate =  // LeadUpdate | 
    
    val request = apiInstance.updateLeadApi(leadId, leadUpdate)
    val response = apiInvoker.execute(request)

    response.onComplete {
        case Success(ApiResponse(code, content, headers)) =>
            System.out.println(s"Status code: $code}")
            System.out.println(s"Response headers: ${headers.mkString(", ")}")
            System.out.println(s"Response body: $content")
        
        case Failure(error @ ApiError(code, message, responseContent, cause, headers)) =>
            System.err.println("Exception when calling LeadApi#updateLeadApi")
            System.err.println(s"Status code: $code}")
            System.err.println(s"Reason: $responseContent")
            System.err.println(s"Response headers: ${headers.mkString(", ")}")
            error.printStackTrace();

        case Failure(exception) => 
            System.err.println("Exception when calling LeadApi#updateLeadApi")
            exception.printStackTrace();
    }
}
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **leadId** | **UUID**|  |
 **leadUpdate** | [**LeadUpdate**](LeadUpdate.md)|  |

### Return type

ApiRequest[[**Lead**](Lead.md)]


### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Lead updated |  -  |

