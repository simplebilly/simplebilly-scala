# CreateSepaDirectDebitApi

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**createSepaDirectDebitApi**](CreateSepaDirectDebitApi.md#createSepaDirectDebitApi) | **POST** /api/v1/bookkeeping/sepa-direct-debit | 
[**createSepaDirectDebitApiWithHttpInfo**](CreateSepaDirectDebitApi.md#createSepaDirectDebitApiWithHttpInfo) | **POST** /api/v1/bookkeeping/sepa-direct-debit | 



## createSepaDirectDebitApi

> createSepaDirectDebitApi(createSepaDirectDebitApiRequest): ApiRequest[SepaDirectDebitResponse]



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
    val apiInstance = CreateSepaDirectDebitApi("https://demo.simplebilly.com")
    val creditorName: String = creditorName_example // String | 

    val creditorIban: String = creditorIban_example // String | 

    val creditorId: String = creditorId_example // String | 

    val mandateId: String = mandateId_example // String | 

    val mandateDate: String = mandateDate_example // String | 

    val debtorName: String = debtorName_example // String | 

    val debtorIban: String = debtorIban_example // String | 

    val amount: String = amount_example // String | 

    val collectionDate: String = collectionDate_example // String | 

    val creditorBic: String = creditorBic_example // String | 

    val debtorBic: String = debtorBic_example // String | 

    val description: String = description_example // String | 
    
    val request = apiInstance.createSepaDirectDebitApi(creditorName, creditorIban, creditorId, mandateId, mandateDate, debtorName, debtorIban, amount, collectionDate, creditorBic, debtorBic, description)
    val response = apiInvoker.execute(request)

    response.onComplete {
        case Success(ApiResponse(code, content, headers)) =>
            System.out.println(s"Status code: $code}")
            System.out.println(s"Response headers: ${headers.mkString(", ")}")
            System.out.println(s"Response body: $content")
        
        case Failure(error @ ApiError(code, message, responseContent, cause, headers)) =>
            System.err.println("Exception when calling CreateSepaDirectDebitApi#createSepaDirectDebitApi")
            System.err.println(s"Status code: $code}")
            System.err.println(s"Reason: $responseContent")
            System.err.println(s"Response headers: ${headers.mkString(", ")}")
            error.printStackTrace();

        case Failure(exception) => 
            System.err.println("Exception when calling CreateSepaDirectDebitApi#createSepaDirectDebitApi")
            exception.printStackTrace();
    }
}
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **creditorName** | **String**|  |
 **creditorIban** | **String**|  |
 **creditorId** | **String**|  |
 **mandateId** | **String**|  |
 **mandateDate** | **String**|  |
 **debtorName** | **String**|  |
 **debtorIban** | **String**|  |
 **amount** | **String**|  |
 **collectionDate** | **String**|  |
 **creditorBic** | **String**|  | [optional]
 **debtorBic** | **String**|  | [optional]
 **description** | **String**|  | [optional]

### Return type

ApiRequest[[**SepaDirectDebitResponse**](SepaDirectDebitResponse.md)]


### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | SEPA Direct Debit XML |  -  |
| **500** | Internal server error |  -  |

