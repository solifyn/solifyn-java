# TicketApi

All URIs are relative to *http://localhost:8000*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**ticketControllerCreateTicket**](TicketApi.md#ticketControllerCreateTicket) | **POST** /v1/tickets |  |
| [**ticketControllerGetTicketDetails**](TicketApi.md#ticketControllerGetTicketDetails) | **GET** /v1/tickets/{id} |  |
| [**ticketControllerGetTickets**](TicketApi.md#ticketControllerGetTickets) | **GET** /v1/tickets |  |
| [**ticketControllerReplyTicket**](TicketApi.md#ticketControllerReplyTicket) | **POST** /v1/tickets/{id}/replies |  |
| [**ticketControllerUpdateTicket**](TicketApi.md#ticketControllerUpdateTicket) | **PATCH** /v1/tickets/{id} |  |


<a id="ticketControllerCreateTicket"></a>
# **ticketControllerCreateTicket**
> ticketControllerCreateTicket(body)



### Example
```java
// Import classes:
import com.solifyn.ApiClient;
import com.solifyn.ApiException;
import com.solifyn.Configuration;
import com.solifyn.models.*;
import com.solifyn.api.TicketApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:8000");

    TicketApi apiInstance = new TicketApi(defaultClient);
    Object body = null; // Object | 
    try {
      apiInstance.ticketControllerCreateTicket(body);
    } catch (ApiException e) {
      System.err.println("Exception when calling TicketApi#ticketControllerCreateTicket");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **body** | **Object**|  | |

### Return type

null (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** |  |  -  |

<a id="ticketControllerGetTicketDetails"></a>
# **ticketControllerGetTicketDetails**
> ticketControllerGetTicketDetails(id)



### Example
```java
// Import classes:
import com.solifyn.ApiClient;
import com.solifyn.ApiException;
import com.solifyn.Configuration;
import com.solifyn.models.*;
import com.solifyn.api.TicketApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:8000");

    TicketApi apiInstance = new TicketApi(defaultClient);
    String id = "id_example"; // String | 
    try {
      apiInstance.ticketControllerGetTicketDetails(id);
    } catch (ApiException e) {
      System.err.println("Exception when calling TicketApi#ticketControllerGetTicketDetails");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **id** | **String**|  | |

### Return type

null (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** |  |  -  |

<a id="ticketControllerGetTickets"></a>
# **ticketControllerGetTickets**
> ticketControllerGetTickets()



### Example
```java
// Import classes:
import com.solifyn.ApiClient;
import com.solifyn.ApiException;
import com.solifyn.Configuration;
import com.solifyn.models.*;
import com.solifyn.api.TicketApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:8000");

    TicketApi apiInstance = new TicketApi(defaultClient);
    try {
      apiInstance.ticketControllerGetTickets();
    } catch (ApiException e) {
      System.err.println("Exception when calling TicketApi#ticketControllerGetTickets");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

null (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** |  |  -  |

<a id="ticketControllerReplyTicket"></a>
# **ticketControllerReplyTicket**
> ticketControllerReplyTicket(id, body)



### Example
```java
// Import classes:
import com.solifyn.ApiClient;
import com.solifyn.ApiException;
import com.solifyn.Configuration;
import com.solifyn.models.*;
import com.solifyn.api.TicketApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:8000");

    TicketApi apiInstance = new TicketApi(defaultClient);
    String id = "id_example"; // String | 
    Object body = null; // Object | 
    try {
      apiInstance.ticketControllerReplyTicket(id, body);
    } catch (ApiException e) {
      System.err.println("Exception when calling TicketApi#ticketControllerReplyTicket");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **id** | **String**|  | |
| **body** | **Object**|  | |

### Return type

null (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** |  |  -  |

<a id="ticketControllerUpdateTicket"></a>
# **ticketControllerUpdateTicket**
> ticketControllerUpdateTicket(id, body)



### Example
```java
// Import classes:
import com.solifyn.ApiClient;
import com.solifyn.ApiException;
import com.solifyn.Configuration;
import com.solifyn.models.*;
import com.solifyn.api.TicketApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:8000");

    TicketApi apiInstance = new TicketApi(defaultClient);
    String id = "id_example"; // String | 
    Object body = null; // Object | 
    try {
      apiInstance.ticketControllerUpdateTicket(id, body);
    } catch (ApiException e) {
      System.err.println("Exception when calling TicketApi#ticketControllerUpdateTicket");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **id** | **String**|  | |
| **body** | **Object**|  | |

### Return type

null (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** |  |  -  |

