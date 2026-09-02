# GenerateQrcodeApi

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**generateQrcodeApi**](GenerateQrcodeApi.md#generateQrcodeApi) | **GET** /api/v1/invoices/{id}/qrcode | 
[**generateQrcodeApiWithHttpInfo**](GenerateQrcodeApi.md#generateQrcodeApiWithHttpInfo) | **GET** /api/v1/invoices/{id}/qrcode | 



## generateQrcodeApi

> generateQrcodeApi(generateQrcodeApiRequest): ApiRequest[QRCodeResponse]



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
    val apiInstance = GenerateQrcodeApi("https://demo.simplebilly.com")
    val iban: String = iban_example // String | 

    val id: String = id_example // String | 

    val holderName: String = holderName_example // String | 

    val bic: String = bic_example // String | 

    val amount: String = amount_example // String | 

    val reference: String = reference_example // String | 

    val purpose: String = purpose_example // String | 
    
    val request = apiInstance.generateQrcodeApi(iban, id, holderName, bic, amount, reference, purpose)
    val response = apiInvoker.execute(request)

    response.onComplete {
        case Success(ApiResponse(code, content, headers)) =>
            System.out.println(s"Status code: $code}")
            System.out.println(s"Response headers: ${headers.mkString(", ")}")
            System.out.println(s"Response body: $content")
        
        case Failure(error @ ApiError(code, message, responseContent, cause, headers)) =>
            System.err.println("Exception when calling GenerateQrcodeApi#generateQrcodeApi")
            System.err.println(s"Status code: $code}")
            System.err.println(s"Reason: $responseContent")
            System.err.println(s"Response headers: ${headers.mkString(", ")}")
            error.printStackTrace();

        case Failure(exception) => 
            System.err.println("Exception when calling GenerateQrcodeApi#generateQrcodeApi")
            exception.printStackTrace();
    }
}
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **iban** | **String**|  |
 **id** | **String**|  |
 **holderName** | **String**|  | [optional]
 **bic** | **String**|  | [optional]
 **amount** | **String**|  | [optional]
 **reference** | **String**|  | [optional]
 **purpose** | **String**|  | [optional]

### Return type

ApiRequest[[**QRCodeResponse**](QRCodeResponse.md)]


### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | QR Code for invoice payment |  -  |
| **404** | Invoice not found |  -  |
| **500** | Internal server error |  -  |

