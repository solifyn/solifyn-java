# ChatApi

All URIs are relative to *http://localhost:8000*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**chatControllerGetMerchantMessages**](ChatApi.md#chatControllerGetMerchantMessages) | **GET** /v1/chat/merchant/messages/{customerId} |  |
| [**chatControllerGetMerchantSessions**](ChatApi.md#chatControllerGetMerchantSessions) | **GET** /v1/chat/merchant/sessions |  |
| [**chatControllerSendCustomerMessage**](ChatApi.md#chatControllerSendCustomerMessage) | **POST** /v1/chat/customer/message |  |
| [**chatControllerSendMerchantMessage**](ChatApi.md#chatControllerSendMerchantMessage) | **POST** /v1/chat/merchant/message |  |


<a id="chatControllerGetMerchantMessages"></a>
# **chatControllerGetMerchantMessages**
> chatControllerGetMerchantMessages(customerId)



### Example
```java
// Import classes:
import com.solifyn.ApiClient;
import com.solifyn.ApiException;
import com.solifyn.Configuration;
import com.solifyn.models.*;
import com.solifyn.api.ChatApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:8000");

    ChatApi apiInstance = new ChatApi(defaultClient);
    String customerId = "customerId_example"; // String | 
    try {
      apiInstance.chatControllerGetMerchantMessages(customerId);
    } catch (ApiException e) {
      System.err.println("Exception when calling ChatApi#chatControllerGetMerchantMessages");
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
| **customerId** | **String**|  | |

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

<a id="chatControllerGetMerchantSessions"></a>
# **chatControllerGetMerchantSessions**
> chatControllerGetMerchantSessions()



### Example
```java
// Import classes:
import com.solifyn.ApiClient;
import com.solifyn.ApiException;
import com.solifyn.Configuration;
import com.solifyn.models.*;
import com.solifyn.api.ChatApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:8000");

    ChatApi apiInstance = new ChatApi(defaultClient);
    try {
      apiInstance.chatControllerGetMerchantSessions();
    } catch (ApiException e) {
      System.err.println("Exception when calling ChatApi#chatControllerGetMerchantSessions");
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

<a id="chatControllerSendCustomerMessage"></a>
# **chatControllerSendCustomerMessage**
> chatControllerSendCustomerMessage()



### Example
```java
// Import classes:
import com.solifyn.ApiClient;
import com.solifyn.ApiException;
import com.solifyn.Configuration;
import com.solifyn.models.*;
import com.solifyn.api.ChatApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:8000");

    ChatApi apiInstance = new ChatApi(defaultClient);
    try {
      apiInstance.chatControllerSendCustomerMessage();
    } catch (ApiException e) {
      System.err.println("Exception when calling ChatApi#chatControllerSendCustomerMessage");
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
| **201** |  |  -  |

<a id="chatControllerSendMerchantMessage"></a>
# **chatControllerSendMerchantMessage**
> chatControllerSendMerchantMessage()



### Example
```java
// Import classes:
import com.solifyn.ApiClient;
import com.solifyn.ApiException;
import com.solifyn.Configuration;
import com.solifyn.models.*;
import com.solifyn.api.ChatApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:8000");

    ChatApi apiInstance = new ChatApi(defaultClient);
    try {
      apiInstance.chatControllerSendMerchantMessage();
    } catch (ApiException e) {
      System.err.println("Exception when calling ChatApi#chatControllerSendMerchantMessage");
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
| **201** |  |  -  |

