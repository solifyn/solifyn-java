# DeveloperApi

All URIs are relative to *https://api.solifyn.com*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**developerCreateApiKey**](DeveloperApi.md#developerCreateApiKey) | **POST** /v1/developer/api-keys | Create Developer API Key |
| [**developerCreateWebhook**](DeveloperApi.md#developerCreateWebhook) | **POST** /v1/developer/webhooks | Create Webhook Endpoint |
| [**developerDeleteWebhook**](DeveloperApi.md#developerDeleteWebhook) | **DELETE** /v1/developer/webhooks/{id} | Delete Webhook Endpoint |
| [**developerGetAppPortal**](DeveloperApi.md#developerGetAppPortal) | **GET** /v1/developer/webhooks/app-portal | Retrieve Hosted Webhooks Portal URL |
| [**developerGetWebhook**](DeveloperApi.md#developerGetWebhook) | **GET** /v1/developer/webhooks/{id} | Retrieve Webhook Endpoint Details |
| [**developerListApiKeys**](DeveloperApi.md#developerListApiKeys) | **GET** /v1/developer/api-keys | List Developer API Keys |
| [**developerListWebhookDeliveries**](DeveloperApi.md#developerListWebhookDeliveries) | **GET** /v1/developer/webhooks/{id}/deliveries | Retrieve Webhook Delivery Logs |
| [**developerListWebhooks**](DeveloperApi.md#developerListWebhooks) | **GET** /v1/developer/webhooks | List Webhook Endpoints |
| [**developerRevokeApiKey**](DeveloperApi.md#developerRevokeApiKey) | **DELETE** /v1/developer/api-keys/{id} | Revoke API Key |
| [**developerUpdateWebhook**](DeveloperApi.md#developerUpdateWebhook) | **PATCH** /v1/developer/webhooks/{id} | Update Webhook Endpoint |


<a id="developerCreateApiKey"></a>
# **developerCreateApiKey**
> ApiKeyResponseDto developerCreateApiKey(createApiKeyDto)

Create Developer API Key

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
    defaultClient.setBasePath("https://api.solifyn.com");

    DeveloperApi apiInstance = new DeveloperApi(defaultClient);
    CreateApiKeyDto createApiKeyDto = new CreateApiKeyDto(); // CreateApiKeyDto | 
    try {
      ApiKeyResponseDto result = apiInstance.developerCreateApiKey(createApiKeyDto);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DeveloperApi#developerCreateApiKey");
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
| **createApiKeyDto** | [**CreateApiKeyDto**](CreateApiKeyDto.md)|  | |

### Return type

[**ApiKeyResponseDto**](ApiKeyResponseDto.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** |  |  -  |

<a id="developerCreateWebhook"></a>
# **developerCreateWebhook**
> WebhookEndpointResponseDto developerCreateWebhook(createWebhookEndpointDto)

Create Webhook Endpoint

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
    defaultClient.setBasePath("https://api.solifyn.com");

    DeveloperApi apiInstance = new DeveloperApi(defaultClient);
    CreateWebhookEndpointDto createWebhookEndpointDto = new CreateWebhookEndpointDto(); // CreateWebhookEndpointDto | 
    try {
      WebhookEndpointResponseDto result = apiInstance.developerCreateWebhook(createWebhookEndpointDto);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DeveloperApi#developerCreateWebhook");
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
| **createWebhookEndpointDto** | [**CreateWebhookEndpointDto**](CreateWebhookEndpointDto.md)|  | |

### Return type

[**WebhookEndpointResponseDto**](WebhookEndpointResponseDto.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** |  |  -  |

<a id="developerDeleteWebhook"></a>
# **developerDeleteWebhook**
> developerDeleteWebhook(id)

Delete Webhook Endpoint

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
    defaultClient.setBasePath("https://api.solifyn.com");

    DeveloperApi apiInstance = new DeveloperApi(defaultClient);
    String id = "id_example"; // String | The webhook endpoint ID
    try {
      apiInstance.developerDeleteWebhook(id);
    } catch (ApiException e) {
      System.err.println("Exception when calling DeveloperApi#developerDeleteWebhook");
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
| **id** | **String**| The webhook endpoint ID | |

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

<a id="developerGetAppPortal"></a>
# **developerGetAppPortal**
> AppPortalUrlResponseDto developerGetAppPortal()

Retrieve Hosted Webhooks Portal URL

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
    defaultClient.setBasePath("https://api.solifyn.com");

    DeveloperApi apiInstance = new DeveloperApi(defaultClient);
    try {
      AppPortalUrlResponseDto result = apiInstance.developerGetAppPortal();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DeveloperApi#developerGetAppPortal");
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

[**AppPortalUrlResponseDto**](AppPortalUrlResponseDto.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** |  |  -  |

<a id="developerGetWebhook"></a>
# **developerGetWebhook**
> WebhookEndpointResponseDto developerGetWebhook(id)

Retrieve Webhook Endpoint Details

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
    defaultClient.setBasePath("https://api.solifyn.com");

    DeveloperApi apiInstance = new DeveloperApi(defaultClient);
    String id = "id_example"; // String | The webhook endpoint ID
    try {
      WebhookEndpointResponseDto result = apiInstance.developerGetWebhook(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DeveloperApi#developerGetWebhook");
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
| **id** | **String**| The webhook endpoint ID | |

### Return type

[**WebhookEndpointResponseDto**](WebhookEndpointResponseDto.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** |  |  -  |

<a id="developerListApiKeys"></a>
# **developerListApiKeys**
> List&lt;ApiKeyResponseDto&gt; developerListApiKeys()

List Developer API Keys

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
    defaultClient.setBasePath("https://api.solifyn.com");

    DeveloperApi apiInstance = new DeveloperApi(defaultClient);
    try {
      List<ApiKeyResponseDto> result = apiInstance.developerListApiKeys();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DeveloperApi#developerListApiKeys");
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

[**List&lt;ApiKeyResponseDto&gt;**](ApiKeyResponseDto.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** |  |  -  |

<a id="developerListWebhookDeliveries"></a>
# **developerListWebhookDeliveries**
> List&lt;WebhookDeliveryResponseDto&gt; developerListWebhookDeliveries(id)

Retrieve Webhook Delivery Logs

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
    defaultClient.setBasePath("https://api.solifyn.com");

    DeveloperApi apiInstance = new DeveloperApi(defaultClient);
    String id = "id_example"; // String | The webhook endpoint ID
    try {
      List<WebhookDeliveryResponseDto> result = apiInstance.developerListWebhookDeliveries(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DeveloperApi#developerListWebhookDeliveries");
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
| **id** | **String**| The webhook endpoint ID | |

### Return type

[**List&lt;WebhookDeliveryResponseDto&gt;**](WebhookDeliveryResponseDto.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** |  |  -  |

<a id="developerListWebhooks"></a>
# **developerListWebhooks**
> List&lt;WebhookEndpointResponseDto&gt; developerListWebhooks()

List Webhook Endpoints

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
    defaultClient.setBasePath("https://api.solifyn.com");

    DeveloperApi apiInstance = new DeveloperApi(defaultClient);
    try {
      List<WebhookEndpointResponseDto> result = apiInstance.developerListWebhooks();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DeveloperApi#developerListWebhooks");
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

[**List&lt;WebhookEndpointResponseDto&gt;**](WebhookEndpointResponseDto.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** |  |  -  |

<a id="developerRevokeApiKey"></a>
# **developerRevokeApiKey**
> developerRevokeApiKey(id)

Revoke API Key

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
    defaultClient.setBasePath("https://api.solifyn.com");

    DeveloperApi apiInstance = new DeveloperApi(defaultClient);
    String id = "id_example"; // String | The API key ID
    try {
      apiInstance.developerRevokeApiKey(id);
    } catch (ApiException e) {
      System.err.println("Exception when calling DeveloperApi#developerRevokeApiKey");
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
| **id** | **String**| The API key ID | |

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

<a id="developerUpdateWebhook"></a>
# **developerUpdateWebhook**
> WebhookEndpointResponseDto developerUpdateWebhook(id, updateWebhookEndpointDto)

Update Webhook Endpoint

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
    defaultClient.setBasePath("https://api.solifyn.com");

    DeveloperApi apiInstance = new DeveloperApi(defaultClient);
    String id = "id_example"; // String | The webhook endpoint ID
    UpdateWebhookEndpointDto updateWebhookEndpointDto = new UpdateWebhookEndpointDto(); // UpdateWebhookEndpointDto | 
    try {
      WebhookEndpointResponseDto result = apiInstance.developerUpdateWebhook(id, updateWebhookEndpointDto);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DeveloperApi#developerUpdateWebhook");
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
| **id** | **String**| The webhook endpoint ID | |
| **updateWebhookEndpointDto** | [**UpdateWebhookEndpointDto**](UpdateWebhookEndpointDto.md)|  | |

### Return type

[**WebhookEndpointResponseDto**](WebhookEndpointResponseDto.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** |  |  -  |

