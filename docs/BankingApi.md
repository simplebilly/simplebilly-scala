# BankingApi

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**bankLookupApi**](BankingApi.md#bankLookupApi) | **GET** /api/v1/bookkeeping/banking/lookup | 
[**bankLookupApiWithHttpInfo**](BankingApi.md#bankLookupApiWithHttpInfo) | **GET** /api/v1/bookkeeping/banking/lookup | 
[**bankTransactionsApi**](BankingApi.md#bankTransactionsApi) | **GET** /api/v1/bookkeeping/banking/transactions | 
[**bankTransactionsApiWithHttpInfo**](BankingApi.md#bankTransactionsApiWithHttpInfo) | **GET** /api/v1/bookkeeping/banking/transactions | 
[**hebesatzLookupApi**](BankingApi.md#hebesatzLookupApi) | **GET** /api/v1/bookkeeping/hebesatz | 
[**hebesatzLookupApiWithHttpInfo**](BankingApi.md#hebesatzLookupApiWithHttpInfo) | **GET** /api/v1/bookkeeping/hebesatz | 



## bankLookupApi

> bankLookupApi(bankLookupApiRequest): ApiRequest[BankLookup]



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
    val apiInstance = BankingApi("https://demo.simplebilly.com")
    val iban: String = iban_example // String | 
    
    val request = apiInstance.bankLookupApi(iban)
    val response = apiInvoker.execute(request)

    response.onComplete {
        case Success(ApiResponse(code, content, headers)) =>
            System.out.println(s"Status code: $code}")
            System.out.println(s"Response headers: ${headers.mkString(", ")}")
            System.out.println(s"Response body: $content")
        
        case Failure(error @ ApiError(code, message, responseContent, cause, headers)) =>
            System.err.println("Exception when calling BankingApi#bankLookupApi")
            System.err.println(s"Status code: $code}")
            System.err.println(s"Reason: $responseContent")
            System.err.println(s"Response headers: ${headers.mkString(", ")}")
            error.printStackTrace();

        case Failure(exception) => 
            System.err.println("Exception when calling BankingApi#bankLookupApi")
            exception.printStackTrace();
    }
}
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **iban** | **String**|  |

### Return type

ApiRequest[[**BankLookup**](BankLookup.md)]


### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Bank-Lookup Ergebnis |  -  |


## bankTransactionsApi

> bankTransactionsApi(): ApiRequest[Unit]



### Example

```scala
// Import classes:
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
    val apiInstance = BankingApi("https://demo.simplebilly.com")    
    val request = apiInstance.bankTransactionsApi()
    val response = apiInvoker.execute(request)

    response.onComplete {
        case Success(ApiResponse(code, content, headers)) =>
            System.out.println(s"Status code: $code}")
            System.out.println(s"Response headers: ${headers.mkString(", ")}")
        
        case Failure(error @ ApiError(code, message, responseContent, cause, headers)) =>
            System.err.println("Exception when calling BankingApi#bankTransactionsApi")
            System.err.println(s"Status code: $code}")
            System.err.println(s"Reason: $responseContent")
            System.err.println(s"Response headers: ${headers.mkString(", ")}")
            error.printStackTrace();

        case Failure(exception) => 
            System.err.println("Exception when calling BankingApi#bankTransactionsApi")
            exception.printStackTrace();
    }
}
```

### Parameters

This endpoint does not need any parameter.

### Return type


ApiRequest[Unit] (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: Not defined

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Bank-Transaktionen |  -  |


## hebesatzLookupApi

> hebesatzLookupApi(hebesatzLookupApiRequest): ApiRequest[Seq[HebesatzLookup]]



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
    val apiInstance = BankingApi("https://demo.simplebilly.com")
    val gemeindeschluessel: String = gemeindeschluessel_example // String | 

    val plz: String = plz_example // String | 

    val name: String = name_example // String | 

    val stichtag: String = stichtag_example // String | Stichtag for validity (YYYY-MM-DD); defaults to today. Picks row where valid_from <= date <= valid_to.

    val countryCode: String = countryCode_example // String | 
    
    val request = apiInstance.hebesatzLookupApi(gemeindeschluessel, plz, name, stichtag, countryCode)
    val response = apiInvoker.execute(request)

    response.onComplete {
        case Success(ApiResponse(code, content, headers)) =>
            System.out.println(s"Status code: $code}")
            System.out.println(s"Response headers: ${headers.mkString(", ")}")
            System.out.println(s"Response body: $content")
        
        case Failure(error @ ApiError(code, message, responseContent, cause, headers)) =>
            System.err.println("Exception when calling BankingApi#hebesatzLookupApi")
            System.err.println(s"Status code: $code}")
            System.err.println(s"Reason: $responseContent")
            System.err.println(s"Response headers: ${headers.mkString(", ")}")
            error.printStackTrace();

        case Failure(exception) => 
            System.err.println("Exception when calling BankingApi#hebesatzLookupApi")
            exception.printStackTrace();
    }
}
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **gemeindeschluessel** | **String**|  | [optional]
 **plz** | **String**|  | [optional]
 **name** | **String**|  | [optional]
 **stichtag** | **String**| Stichtag for validity (YYYY-MM-DD); defaults to today. Picks row where valid_from &lt;&#x3D; date &lt;&#x3D; valid_to. | [optional]
 **countryCode** | **String**|  | [optional]

### Return type

ApiRequest[[**Seq[HebesatzLookup]**](HebesatzLookup.md)]


### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Hebesatz Lookup |  -  |

