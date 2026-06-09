# WebhookApi

All URIs are relative to *https://api.solifyn.com*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**webhookControllerHandleSvixWebhook**](WebhookApi.md#webhookControllerHandleSvixWebhook) | **POST** /v1/webhook/svix |  |
| [**webhookControllerHandleWebhook**](WebhookApi.md#webhookControllerHandleWebhook) | **POST** /v1/webhook |  |


<a id="webhookControllerHandleSvixWebhook"></a>
# **webhookControllerHandleSvixWebhook**
> webhookControllerHandleSvixWebhook()



### Example
```java
// Import classes:
import com.solifyn.ApiClient;
import com.solifyn.ApiException;
import com.solifyn.Configuration;
import com.solifyn.models.*;
import com.solifyn.api.WebhookApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.solifyn.com");

    WebhookApi apiInstance = new WebhookApi(defaultClient);
    try {
      apiInstance.webhookControllerHandleSvixWebhook();
    } catch (ApiException e) {
      System.err.println("Exception when calling WebhookApi#webhookControllerHandleSvixWebhook");
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

<a id="webhookControllerHandleWebhook"></a>
# **webhookControllerHandleWebhook**
> webhookControllerHandleWebhook(businessId)



### Example
```java
// Import classes:
import com.solifyn.ApiClient;
import com.solifyn.ApiException;
import com.solifyn.Configuration;
import com.solifyn.models.*;
import com.solifyn.api.WebhookApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.solifyn.com");

    WebhookApi apiInstance = new WebhookApi(defaultClient);
    String businessId = "businessId_example"; // String | 
    try {
      apiInstance.webhookControllerHandleWebhook(businessId);
    } catch (ApiException e) {
      System.err.println("Exception when calling WebhookApi#webhookControllerHandleWebhook");
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
| **businessId** | **String**|  | |

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

