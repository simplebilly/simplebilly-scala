# BudgetsApi

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**budgetsApi**](BudgetsApi.md#budgetsApi) | **GET** /api/v1/bookkeeping/budgets | 
[**budgetsApiWithHttpInfo**](BudgetsApi.md#budgetsApiWithHttpInfo) | **GET** /api/v1/bookkeeping/budgets | 
[**upsertBudgetGoalApi**](BudgetsApi.md#upsertBudgetGoalApi) | **PUT** /api/v1/bookkeeping/budgets/goals/{category} | 
[**upsertBudgetGoalApiWithHttpInfo**](BudgetsApi.md#upsertBudgetGoalApiWithHttpInfo) | **PUT** /api/v1/bookkeeping/budgets/goals/{category} | 



## budgetsApi

> budgetsApi(budgetsApiRequest): ApiRequest[BudgetErgebnis]



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
    val apiInstance = BudgetsApi("https://demo.simplebilly.com")
    val year: Int = 56 // Int | 

    val month: Int = 56 // Int | 
    
    val request = apiInstance.budgetsApi(year, month)
    val response = apiInvoker.execute(request)

    response.onComplete {
        case Success(ApiResponse(code, content, headers)) =>
            System.out.println(s"Status code: $code}")
            System.out.println(s"Response headers: ${headers.mkString(", ")}")
            System.out.println(s"Response body: $content")
        
        case Failure(error @ ApiError(code, message, responseContent, cause, headers)) =>
            System.err.println("Exception when calling BudgetsApi#budgetsApi")
            System.err.println(s"Status code: $code}")
            System.err.println(s"Reason: $responseContent")
            System.err.println(s"Response headers: ${headers.mkString(", ")}")
            error.printStackTrace();

        case Failure(exception) => 
            System.err.println("Exception when calling BudgetsApi#budgetsApi")
            exception.printStackTrace();
    }
}
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **year** | **Int**|  |
 **month** | **Int**|  |

### Return type

ApiRequest[[**BudgetErgebnis**](BudgetErgebnis.md)]


### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Monats-Budget + Prognose |  -  |


## upsertBudgetGoalApi

> upsertBudgetGoalApi(upsertBudgetGoalApiRequest): ApiRequest[Budget]



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
    val apiInstance = BudgetsApi("https://demo.simplebilly.com")
    val category: String = category_example // String | 

    val budgetGoalRequest: BudgetGoalRequest =  // BudgetGoalRequest | 
    
    val request = apiInstance.upsertBudgetGoalApi(category, budgetGoalRequest)
    val response = apiInvoker.execute(request)

    response.onComplete {
        case Success(ApiResponse(code, content, headers)) =>
            System.out.println(s"Status code: $code}")
            System.out.println(s"Response headers: ${headers.mkString(", ")}")
            System.out.println(s"Response body: $content")
        
        case Failure(error @ ApiError(code, message, responseContent, cause, headers)) =>
            System.err.println("Exception when calling BudgetsApi#upsertBudgetGoalApi")
            System.err.println(s"Status code: $code}")
            System.err.println(s"Reason: $responseContent")
            System.err.println(s"Response headers: ${headers.mkString(", ")}")
            error.printStackTrace();

        case Failure(exception) => 
            System.err.println("Exception when calling BudgetsApi#upsertBudgetGoalApi")
            exception.printStackTrace();
    }
}
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **category** | **String**|  |
 **budgetGoalRequest** | [**BudgetGoalRequest**](BudgetGoalRequest.md)|  |

### Return type

ApiRequest[[**Budget**](Budget.md)]


### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Budget goal saved (upsert) |  -  |
| **400** | Negative goal |  -  |

