# TimeEntriesApi

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**clockInTimeEntry**](TimeEntriesApi.md#clockInTimeEntry) | **POST** /api/v1/time-entries | Clock in for the authenticated user (resolved via their employee profile).
[**clockInTimeEntryWithHttpInfo**](TimeEntriesApi.md#clockInTimeEntryWithHttpInfo) | **POST** /api/v1/time-entries | Clock in for the authenticated user (resolved via their employee profile).
[**clockOutTimeEntry**](TimeEntriesApi.md#clockOutTimeEntry) | **PATCH** /api/v1/time-entries/{id} | Clock out an entry: the entry&#39;s owner, or anyone with &#x60;time_entries:write&#x60;.
[**clockOutTimeEntryWithHttpInfo**](TimeEntriesApi.md#clockOutTimeEntryWithHttpInfo) | **PATCH** /api/v1/time-entries/{id} | Clock out an entry: the entry&#39;s owner, or anyone with &#x60;time_entries:write&#x60;.
[**getLaborCosts**](TimeEntriesApi.md#getLaborCosts) | **GET** /api/v1/labor-costs | Labor-cost report: worked hours aggregated per employee / order / day, valued at the employee&#39;s hourly cost rate.
[**getLaborCostsWithHttpInfo**](TimeEntriesApi.md#getLaborCostsWithHttpInfo) | **GET** /api/v1/labor-costs | Labor-cost report: worked hours aggregated per employee / order / day, valued at the employee&#39;s hourly cost rate.
[**listTimeEntries**](TimeEntriesApi.md#listTimeEntries) | **GET** /api/v1/time-entries | List time entries with optional date-range / active / employee filters.
[**listTimeEntriesWithHttpInfo**](TimeEntriesApi.md#listTimeEntriesWithHttpInfo) | **GET** /api/v1/time-entries | List time entries with optional date-range / active / employee filters.



## clockInTimeEntry

> clockInTimeEntry(clockInTimeEntryRequest): ApiRequest[TimeEntryDto]

Clock in for the authenticated user (resolved via their employee profile).

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
    val apiInstance = TimeEntriesApi("https://demo.simplebilly.com")
    val timeEntryClockIn: TimeEntryClockIn =  // TimeEntryClockIn | 
    
    val request = apiInstance.clockInTimeEntry(timeEntryClockIn)
    val response = apiInvoker.execute(request)

    response.onComplete {
        case Success(ApiResponse(code, content, headers)) =>
            System.out.println(s"Status code: $code}")
            System.out.println(s"Response headers: ${headers.mkString(", ")}")
            System.out.println(s"Response body: $content")
        
        case Failure(error @ ApiError(code, message, responseContent, cause, headers)) =>
            System.err.println("Exception when calling TimeEntriesApi#clockInTimeEntry")
            System.err.println(s"Status code: $code}")
            System.err.println(s"Reason: $responseContent")
            System.err.println(s"Response headers: ${headers.mkString(", ")}")
            error.printStackTrace();

        case Failure(exception) => 
            System.err.println("Exception when calling TimeEntriesApi#clockInTimeEntry")
            exception.printStackTrace();
    }
}
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **timeEntryClockIn** | [**TimeEntryClockIn**](TimeEntryClockIn.md)|  |

### Return type

ApiRequest[[**TimeEntryDto**](TimeEntryDto.md)]


### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Created |  -  |
| **400** | No employee profile for this user |  -  |
| **500** | Internal server error |  -  |


## clockOutTimeEntry

> clockOutTimeEntry(clockOutTimeEntryRequest): ApiRequest[TimeEntryDto]

Clock out an entry: the entry&#39;s owner, or anyone with &#x60;time_entries:write&#x60;.

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
    val apiInstance = TimeEntriesApi("https://demo.simplebilly.com")
    val id: UUID = 38400000-8cf0-11bd-b23e-10b96e4ef00d // UUID | 

    val timeEntryClockOut: TimeEntryClockOut =  // TimeEntryClockOut | 
    
    val request = apiInstance.clockOutTimeEntry(id, timeEntryClockOut)
    val response = apiInvoker.execute(request)

    response.onComplete {
        case Success(ApiResponse(code, content, headers)) =>
            System.out.println(s"Status code: $code}")
            System.out.println(s"Response headers: ${headers.mkString(", ")}")
            System.out.println(s"Response body: $content")
        
        case Failure(error @ ApiError(code, message, responseContent, cause, headers)) =>
            System.err.println("Exception when calling TimeEntriesApi#clockOutTimeEntry")
            System.err.println(s"Status code: $code}")
            System.err.println(s"Reason: $responseContent")
            System.err.println(s"Response headers: ${headers.mkString(", ")}")
            error.printStackTrace();

        case Failure(exception) => 
            System.err.println("Exception when calling TimeEntriesApi#clockOutTimeEntry")
            exception.printStackTrace();
    }
}
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **UUID**|  |
 **timeEntryClockOut** | [**TimeEntryClockOut**](TimeEntryClockOut.md)|  |

### Return type

ApiRequest[[**TimeEntryDto**](TimeEntryDto.md)]


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
| **403** | Forbidden |  -  |
| **404** | Not found |  -  |
| **500** | Internal server error |  -  |


## getLaborCosts

> getLaborCosts(getLaborCostsRequest): ApiRequest[Seq[LaborCostRow]]

Labor-cost report: worked hours aggregated per employee / order / day, valued at the employee&#39;s hourly cost rate.

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
    val apiInstance = TimeEntriesApi("https://demo.simplebilly.com")
    val from: LocalDate = 2013-10-20 // LocalDate | 

    val to: LocalDate = 2013-10-20 // LocalDate | 

    val groupBy: String = groupBy_example // String | One of \"employee\", \"order\" or \"day\".
    
    val request = apiInstance.getLaborCosts(from, to, groupBy)
    val response = apiInvoker.execute(request)

    response.onComplete {
        case Success(ApiResponse(code, content, headers)) =>
            System.out.println(s"Status code: $code}")
            System.out.println(s"Response headers: ${headers.mkString(", ")}")
            System.out.println(s"Response body: $content")
        
        case Failure(error @ ApiError(code, message, responseContent, cause, headers)) =>
            System.err.println("Exception when calling TimeEntriesApi#getLaborCosts")
            System.err.println(s"Status code: $code}")
            System.err.println(s"Reason: $responseContent")
            System.err.println(s"Response headers: ${headers.mkString(", ")}")
            error.printStackTrace();

        case Failure(exception) => 
            System.err.println("Exception when calling TimeEntriesApi#getLaborCosts")
            exception.printStackTrace();
    }
}
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **from** | **LocalDate**|  |
 **to** | **LocalDate**|  |
 **groupBy** | **String**| One of \&quot;employee\&quot;, \&quot;order\&quot; or \&quot;day\&quot;. |

### Return type

ApiRequest[[**Seq[LaborCostRow]**](LaborCostRow.md)]


### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |
| **400** | Bad request |  -  |
| **500** | Internal server error |  -  |


## listTimeEntries

> listTimeEntries(listTimeEntriesRequest): ApiRequest[Seq[TimeEntryDto]]

List time entries with optional date-range / active / employee filters.

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
    val apiInstance = TimeEntriesApi("https://demo.simplebilly.com")
    val from: LocalDate = 2013-10-20 // LocalDate | 

    val to: LocalDate = 2013-10-20 // LocalDate | 

    val active: Boolean = true // Boolean | Only currently running shifts (clock_in set, clock_out null).

    val employeeId: UUID = 38400000-8cf0-11bd-b23e-10b96e4ef00d // UUID | 
    
    val request = apiInstance.listTimeEntries(from, to, active, employeeId)
    val response = apiInvoker.execute(request)

    response.onComplete {
        case Success(ApiResponse(code, content, headers)) =>
            System.out.println(s"Status code: $code}")
            System.out.println(s"Response headers: ${headers.mkString(", ")}")
            System.out.println(s"Response body: $content")
        
        case Failure(error @ ApiError(code, message, responseContent, cause, headers)) =>
            System.err.println("Exception when calling TimeEntriesApi#listTimeEntries")
            System.err.println(s"Status code: $code}")
            System.err.println(s"Reason: $responseContent")
            System.err.println(s"Response headers: ${headers.mkString(", ")}")
            error.printStackTrace();

        case Failure(exception) => 
            System.err.println("Exception when calling TimeEntriesApi#listTimeEntries")
            exception.printStackTrace();
    }
}
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **from** | **LocalDate**|  | [optional]
 **to** | **LocalDate**|  | [optional]
 **active** | **Boolean**| Only currently running shifts (clock_in set, clock_out null). | [optional]
 **employeeId** | **UUID**|  | [optional]

### Return type

ApiRequest[[**Seq[TimeEntryDto]**](TimeEntryDto.md)]


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

