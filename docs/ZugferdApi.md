# ZugferdApi

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**generateZugferdApi**](ZugferdApi.md#generateZugferdApi) | **GET** /api/v1/invoices/{id}/zugferd | 
[**generateZugferdApiWithHttpInfo**](ZugferdApi.md#generateZugferdApiWithHttpInfo) | **GET** /api/v1/invoices/{id}/zugferd | 



## generateZugferdApi

> generateZugferdApi(generateZugferdApiRequest): ApiRequest[Unit]



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
    val apiInstance = ZugferdApi("https://demo.simplebilly.com")
    val id: String = id_example // String | 

    val supplierName: String = supplierName_example // String | 

    val supplierStreet: String = supplierStreet_example // String | 

    val supplierCity: String = supplierCity_example // String | 

    val supplierZip: String = supplierZip_example // String | 

    val supplierCountry: String = supplierCountry_example // String | 

    val supplierVatId: String = supplierVatId_example // String | 
    
    val request = apiInstance.generateZugferdApi(id, supplierName, supplierStreet, supplierCity, supplierZip, supplierCountry, supplierVatId)
    val response = apiInvoker.execute(request)

    response.onComplete {
        case Success(ApiResponse(code, content, headers)) =>
            System.out.println(s"Status code: $code}")
            System.out.println(s"Response headers: ${headers.mkString(", ")}")
        
        case Failure(error @ ApiError(code, message, responseContent, cause, headers)) =>
            System.err.println("Exception when calling ZugferdApi#generateZugferdApi")
            System.err.println(s"Status code: $code}")
            System.err.println(s"Reason: $responseContent")
            System.err.println(s"Response headers: ${headers.mkString(", ")}")
            error.printStackTrace();

        case Failure(exception) => 
            System.err.println("Exception when calling ZugferdApi#generateZugferdApi")
            exception.printStackTrace();
    }
}
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **String**|  |
 **supplierName** | **String**|  | [optional]
 **supplierStreet** | **String**|  | [optional]
 **supplierCity** | **String**|  | [optional]
 **supplierZip** | **String**|  | [optional]
 **supplierCountry** | **String**|  | [optional]
 **supplierVatId** | **String**|  | [optional]

### Return type


ApiRequest[Unit] (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/pdf

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | ZUGFeRD/Factur-X hybrid PDF (PDF/A-3 with embedded EN 16931 XML) |  -  |
| **404** | Invoice not found |  -  |
| **500** | Internal server error |  -  |

