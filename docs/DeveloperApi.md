# DeveloperApi

All URIs are relative to *http://localhost:8000*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**developerControllerCreateApiKey**](DeveloperApi.md#developerControllerCreateApiKey) | **POST** /v1/developer/api-keys |  |
| [**developerControllerCreateWebhookEndpoint**](DeveloperApi.md#developerControllerCreateWebhookEndpoint) | **POST** /v1/developer/webhooks |  |
| [**developerControllerDeleteApiKey**](DeveloperApi.md#developerControllerDeleteApiKey) | **DELETE** /v1/developer/api-keys/{id} |  |
| [**developerControllerDeleteWebhookEndpoint**](DeveloperApi.md#developerControllerDeleteWebhookEndpoint) | **DELETE** /v1/developer/webhooks/{id} |  |
| [**developerControllerGetApiKeys**](DeveloperApi.md#developerControllerGetApiKeys) | **GET** /v1/developer/api-keys |  |
| [**developerControllerGetAppPortalUrl**](DeveloperApi.md#developerControllerGetAppPortalUrl) | **GET** /v1/developer/webhooks/app-portal |  |
| [**developerControllerGetWebhookDeliveries**](DeveloperApi.md#developerControllerGetWebhookDeliveries) | **GET** /v1/developer/webhooks/{id}/deliveries |  |
| [**developerControllerGetWebhookEndpoints**](DeveloperApi.md#developerControllerGetWebhookEndpoints) | **GET** /v1/developer/webhooks |  |
| [**developerControllerUpdateWebhookEndpoint**](DeveloperApi.md#developerControllerUpdateWebhookEndpoint) | **PATCH** /v1/developer/webhooks/{id} |  |


<a id="developerControllerCreateApiKey"></a>
# **developerControllerCreateApiKey**
> developerControllerCreateApiKey()



### Example
```java
// Import classes:
import com.solifyn.ApiClient;
import com.solifyn.ApiException;
import com.solifyn.Configuration;
import com.solifyn.models.*;
import com.solifyn.api.DeveloperApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:8000");

    DeveloperApi apiInstance = new DeveloperApi(defaultClient);
    try {
      apiInstance.developerControllerCreateApiKey();
    } catch (ApiException e) {
      System.err.println("Exception when calling DeveloperApi#developerControllerCreateApiKey");
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

<a id="developerControllerCreateWebhookEndpoint"></a>
# **developerControllerCreateWebhookEndpoint**
> developerControllerCreateWebhookEndpoint()



### Example
```java
// Import classes:
import com.solifyn.ApiClient;
import com.solifyn.ApiException;
import com.solifyn.Configuration;
import com.solifyn.models.*;
import com.solifyn.api.DeveloperApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:8000");

    DeveloperApi apiInstance = new DeveloperApi(defaultClient);
    try {
      apiInstance.developerControllerCreateWebhookEndpoint();
    } catch (ApiException e) {
      System.err.println("Exception when calling DeveloperApi#developerControllerCreateWebhookEndpoint");
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

<a id="developerControllerDeleteApiKey"></a>
# **developerControllerDeleteApiKey**
> developerControllerDeleteApiKey(id)



### Example
```java
// Import classes:
import com.solifyn.ApiClient;
import com.solifyn.ApiException;
import com.solifyn.Configuration;
import com.solifyn.models.*;
import com.solifyn.api.DeveloperApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:8000");

    DeveloperApi apiInstance = new DeveloperApi(defaultClient);
    String id = "id_example"; // String | 
    try {
      apiInstance.developerControllerDeleteApiKey(id);
    } catch (ApiException e) {
      System.err.println("Exception when calling DeveloperApi#developerControllerDeleteApiKey");
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

<a id="developerControllerDeleteWebhookEndpoint"></a>
# **developerControllerDeleteWebhookEndpoint**
> developerControllerDeleteWebhookEndpoint(id)



### Example
```java
// Import classes:
import com.solifyn.ApiClient;
import com.solifyn.ApiException;
import com.solifyn.Configuration;
import com.solifyn.models.*;
import com.solifyn.api.DeveloperApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:8000");

    DeveloperApi apiInstance = new DeveloperApi(defaultClient);
    String id = "id_example"; // String | 
    try {
      apiInstance.developerControllerDeleteWebhookEndpoint(id);
    } catch (ApiException e) {
      System.err.println("Exception when calling DeveloperApi#developerControllerDeleteWebhookEndpoint");
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

<a id="developerControllerGetApiKeys"></a>
# **developerControllerGetApiKeys**
> developerControllerGetApiKeys()



### Example
```java
// Import classes:
import com.solifyn.ApiClient;
import com.solifyn.ApiException;
import com.solifyn.Configuration;
import com.solifyn.models.*;
import com.solifyn.api.DeveloperApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:8000");

    DeveloperApi apiInstance = new DeveloperApi(defaultClient);
    try {
      apiInstance.developerControllerGetApiKeys();
    } catch (ApiException e) {
      System.err.println("Exception when calling DeveloperApi#developerControllerGetApiKeys");
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

<a id="developerControllerGetAppPortalUrl"></a>
# **developerControllerGetAppPortalUrl**
> developerControllerGetAppPortalUrl()



### Example
```java
// Import classes:
import com.solifyn.ApiClient;
import com.solifyn.ApiException;
import com.solifyn.Configuration;
import com.solifyn.models.*;
import com.solifyn.api.DeveloperApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:8000");

    DeveloperApi apiInstance = new DeveloperApi(defaultClient);
    try {
      apiInstance.developerControllerGetAppPortalUrl();
    } catch (ApiException e) {
      System.err.println("Exception when calling DeveloperApi#developerControllerGetAppPortalUrl");
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

<a id="developerControllerGetWebhookDeliveries"></a>
# **developerControllerGetWebhookDeliveries**
> developerControllerGetWebhookDeliveries(id)



### Example
```java
// Import classes:
import com.solifyn.ApiClient;
import com.solifyn.ApiException;
import com.solifyn.Configuration;
import com.solifyn.models.*;
import com.solifyn.api.DeveloperApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:8000");

    DeveloperApi apiInstance = new DeveloperApi(defaultClient);
    String id = "id_example"; // String | 
    try {
      apiInstance.developerControllerGetWebhookDeliveries(id);
    } catch (ApiException e) {
      System.err.println("Exception when calling DeveloperApi#developerControllerGetWebhookDeliveries");
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

<a id="developerControllerGetWebhookEndpoints"></a>
# **developerControllerGetWebhookEndpoints**
> developerControllerGetWebhookEndpoints()



### Example
```java
// Import classes:
import com.solifyn.ApiClient;
import com.solifyn.ApiException;
import com.solifyn.Configuration;
import com.solifyn.models.*;
import com.solifyn.api.DeveloperApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:8000");

    DeveloperApi apiInstance = new DeveloperApi(defaultClient);
    try {
      apiInstance.developerControllerGetWebhookEndpoints();
    } catch (ApiException e) {
      System.err.println("Exception when calling DeveloperApi#developerControllerGetWebhookEndpoints");
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

<a id="developerControllerUpdateWebhookEndpoint"></a>
# **developerControllerUpdateWebhookEndpoint**
> developerControllerUpdateWebhookEndpoint(id)



### Example
```java
// Import classes:
import com.solifyn.ApiClient;
import com.solifyn.ApiException;
import com.solifyn.Configuration;
import com.solifyn.models.*;
import com.solifyn.api.DeveloperApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:8000");

    DeveloperApi apiInstance = new DeveloperApi(defaultClient);
    String id = "id_example"; // String | 
    try {
      apiInstance.developerControllerUpdateWebhookEndpoint(id);
    } catch (ApiException e) {
      System.err.println("Exception when calling DeveloperApi#developerControllerUpdateWebhookEndpoint");
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

