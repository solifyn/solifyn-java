# WebhookEndpointApi

All URIs are relative to *http://localhost:8000*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**operationalWebhookControllerCreate**](WebhookEndpointApi.md#operationalWebhookControllerCreate) | **POST** /v1/operational-webhook/endpoint | Create Operational Webhook Endpoint |
| [**operationalWebhookControllerDelete**](WebhookEndpointApi.md#operationalWebhookControllerDelete) | **DELETE** /v1/operational-webhook/endpoint/{id} | Delete Operational Webhook Endpoint |
| [**operationalWebhookControllerGet**](WebhookEndpointApi.md#operationalWebhookControllerGet) | **GET** /v1/operational-webhook/endpoint/{id} | Get Operational Webhook Endpoint |
| [**operationalWebhookControllerGetHeaders**](WebhookEndpointApi.md#operationalWebhookControllerGetHeaders) | **GET** /v1/operational-webhook/endpoint/{id}/headers | Get Operational Webhook Endpoint Headers |
| [**operationalWebhookControllerGetSecret**](WebhookEndpointApi.md#operationalWebhookControllerGetSecret) | **GET** /v1/operational-webhook/endpoint/{id}/secret | Get Operational Webhook Endpoint Secret |
| [**operationalWebhookControllerList**](WebhookEndpointApi.md#operationalWebhookControllerList) | **GET** /v1/operational-webhook/endpoint | List Operational Webhook Endpoints |
| [**operationalWebhookControllerRotateSecret**](WebhookEndpointApi.md#operationalWebhookControllerRotateSecret) | **POST** /v1/operational-webhook/endpoint/{id}/secret/rotate | Rotate Operational Webhook Endpoint Secret |
| [**operationalWebhookControllerUpdate**](WebhookEndpointApi.md#operationalWebhookControllerUpdate) | **PUT** /v1/operational-webhook/endpoint/{id} | Update Operational Webhook Endpoint |
| [**operationalWebhookControllerUpdateHeaders**](WebhookEndpointApi.md#operationalWebhookControllerUpdateHeaders) | **PUT** /v1/operational-webhook/endpoint/{id}/headers | Set Operational Webhook Endpoint Headers |


<a id="operationalWebhookControllerCreate"></a>
# **operationalWebhookControllerCreate**
> OperationalWebhookEndpointResponseDto operationalWebhookControllerCreate(operationalWebhookEndpointInDto)

Create Operational Webhook Endpoint

### Example
```java
// Import classes:
import com.solifyn.ApiClient;
import com.solifyn.ApiException;
import com.solifyn.Configuration;
import com.solifyn.models.*;
import com.solifyn.api.WebhookEndpointApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:8000");

    WebhookEndpointApi apiInstance = new WebhookEndpointApi(defaultClient);
    OperationalWebhookEndpointInDto operationalWebhookEndpointInDto = new OperationalWebhookEndpointInDto(); // OperationalWebhookEndpointInDto | 
    try {
      OperationalWebhookEndpointResponseDto result = apiInstance.operationalWebhookControllerCreate(operationalWebhookEndpointInDto);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling WebhookEndpointApi#operationalWebhookControllerCreate");
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
| **operationalWebhookEndpointInDto** | [**OperationalWebhookEndpointInDto**](OperationalWebhookEndpointInDto.md)|  | |

### Return type

[**OperationalWebhookEndpointResponseDto**](OperationalWebhookEndpointResponseDto.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** |  |  -  |

<a id="operationalWebhookControllerDelete"></a>
# **operationalWebhookControllerDelete**
> operationalWebhookControllerDelete(id)

Delete Operational Webhook Endpoint

### Example
```java
// Import classes:
import com.solifyn.ApiClient;
import com.solifyn.ApiException;
import com.solifyn.Configuration;
import com.solifyn.models.*;
import com.solifyn.api.WebhookEndpointApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:8000");

    WebhookEndpointApi apiInstance = new WebhookEndpointApi(defaultClient);
    String id = "id_example"; // String | The endpoint ID or UID
    try {
      apiInstance.operationalWebhookControllerDelete(id);
    } catch (ApiException e) {
      System.err.println("Exception when calling WebhookEndpointApi#operationalWebhookControllerDelete");
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
| **id** | **String**| The endpoint ID or UID | |

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
| **204** | Deleted |  -  |

<a id="operationalWebhookControllerGet"></a>
# **operationalWebhookControllerGet**
> OperationalWebhookEndpointResponseDto operationalWebhookControllerGet(id)

Get Operational Webhook Endpoint

### Example
```java
// Import classes:
import com.solifyn.ApiClient;
import com.solifyn.ApiException;
import com.solifyn.Configuration;
import com.solifyn.models.*;
import com.solifyn.api.WebhookEndpointApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:8000");

    WebhookEndpointApi apiInstance = new WebhookEndpointApi(defaultClient);
    String id = "id_example"; // String | The endpoint ID or UID
    try {
      OperationalWebhookEndpointResponseDto result = apiInstance.operationalWebhookControllerGet(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling WebhookEndpointApi#operationalWebhookControllerGet");
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
| **id** | **String**| The endpoint ID or UID | |

### Return type

[**OperationalWebhookEndpointResponseDto**](OperationalWebhookEndpointResponseDto.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** |  |  -  |

<a id="operationalWebhookControllerGetHeaders"></a>
# **operationalWebhookControllerGetHeaders**
> OperationalWebhookEndpointHeadersResponseDto operationalWebhookControllerGetHeaders(id)

Get Operational Webhook Endpoint Headers

### Example
```java
// Import classes:
import com.solifyn.ApiClient;
import com.solifyn.ApiException;
import com.solifyn.Configuration;
import com.solifyn.models.*;
import com.solifyn.api.WebhookEndpointApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:8000");

    WebhookEndpointApi apiInstance = new WebhookEndpointApi(defaultClient);
    String id = "id_example"; // String | The endpoint ID or UID
    try {
      OperationalWebhookEndpointHeadersResponseDto result = apiInstance.operationalWebhookControllerGetHeaders(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling WebhookEndpointApi#operationalWebhookControllerGetHeaders");
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
| **id** | **String**| The endpoint ID or UID | |

### Return type

[**OperationalWebhookEndpointHeadersResponseDto**](OperationalWebhookEndpointHeadersResponseDto.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** |  |  -  |

<a id="operationalWebhookControllerGetSecret"></a>
# **operationalWebhookControllerGetSecret**
> OperationalWebhookEndpointSecretResponseDto operationalWebhookControllerGetSecret(id)

Get Operational Webhook Endpoint Secret

### Example
```java
// Import classes:
import com.solifyn.ApiClient;
import com.solifyn.ApiException;
import com.solifyn.Configuration;
import com.solifyn.models.*;
import com.solifyn.api.WebhookEndpointApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:8000");

    WebhookEndpointApi apiInstance = new WebhookEndpointApi(defaultClient);
    String id = "id_example"; // String | The endpoint ID or UID
    try {
      OperationalWebhookEndpointSecretResponseDto result = apiInstance.operationalWebhookControllerGetSecret(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling WebhookEndpointApi#operationalWebhookControllerGetSecret");
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
| **id** | **String**| The endpoint ID or UID | |

### Return type

[**OperationalWebhookEndpointSecretResponseDto**](OperationalWebhookEndpointSecretResponseDto.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** |  |  -  |

<a id="operationalWebhookControllerList"></a>
# **operationalWebhookControllerList**
> OperationalWebhookEndpointListResponseDto operationalWebhookControllerList()

List Operational Webhook Endpoints

### Example
```java
// Import classes:
import com.solifyn.ApiClient;
import com.solifyn.ApiException;
import com.solifyn.Configuration;
import com.solifyn.models.*;
import com.solifyn.api.WebhookEndpointApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:8000");

    WebhookEndpointApi apiInstance = new WebhookEndpointApi(defaultClient);
    try {
      OperationalWebhookEndpointListResponseDto result = apiInstance.operationalWebhookControllerList();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling WebhookEndpointApi#operationalWebhookControllerList");
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

[**OperationalWebhookEndpointListResponseDto**](OperationalWebhookEndpointListResponseDto.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** |  |  -  |

<a id="operationalWebhookControllerRotateSecret"></a>
# **operationalWebhookControllerRotateSecret**
> operationalWebhookControllerRotateSecret(id, operationalWebhookEndpointSecretInDto)

Rotate Operational Webhook Endpoint Secret

### Example
```java
// Import classes:
import com.solifyn.ApiClient;
import com.solifyn.ApiException;
import com.solifyn.Configuration;
import com.solifyn.models.*;
import com.solifyn.api.WebhookEndpointApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:8000");

    WebhookEndpointApi apiInstance = new WebhookEndpointApi(defaultClient);
    String id = "id_example"; // String | The endpoint ID or UID
    OperationalWebhookEndpointSecretInDto operationalWebhookEndpointSecretInDto = new OperationalWebhookEndpointSecretInDto(); // OperationalWebhookEndpointSecretInDto | 
    try {
      apiInstance.operationalWebhookControllerRotateSecret(id, operationalWebhookEndpointSecretInDto);
    } catch (ApiException e) {
      System.err.println("Exception when calling WebhookEndpointApi#operationalWebhookControllerRotateSecret");
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
| **id** | **String**| The endpoint ID or UID | |
| **operationalWebhookEndpointSecretInDto** | [**OperationalWebhookEndpointSecretInDto**](OperationalWebhookEndpointSecretInDto.md)|  | |

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
| **204** | Secret rotated |  -  |

<a id="operationalWebhookControllerUpdate"></a>
# **operationalWebhookControllerUpdate**
> OperationalWebhookEndpointResponseDto operationalWebhookControllerUpdate(id, operationalWebhookEndpointUpdateDto)

Update Operational Webhook Endpoint

### Example
```java
// Import classes:
import com.solifyn.ApiClient;
import com.solifyn.ApiException;
import com.solifyn.Configuration;
import com.solifyn.models.*;
import com.solifyn.api.WebhookEndpointApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:8000");

    WebhookEndpointApi apiInstance = new WebhookEndpointApi(defaultClient);
    String id = "id_example"; // String | The endpoint ID or UID
    OperationalWebhookEndpointUpdateDto operationalWebhookEndpointUpdateDto = new OperationalWebhookEndpointUpdateDto(); // OperationalWebhookEndpointUpdateDto | 
    try {
      OperationalWebhookEndpointResponseDto result = apiInstance.operationalWebhookControllerUpdate(id, operationalWebhookEndpointUpdateDto);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling WebhookEndpointApi#operationalWebhookControllerUpdate");
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
| **id** | **String**| The endpoint ID or UID | |
| **operationalWebhookEndpointUpdateDto** | [**OperationalWebhookEndpointUpdateDto**](OperationalWebhookEndpointUpdateDto.md)|  | |

### Return type

[**OperationalWebhookEndpointResponseDto**](OperationalWebhookEndpointResponseDto.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** |  |  -  |

<a id="operationalWebhookControllerUpdateHeaders"></a>
# **operationalWebhookControllerUpdateHeaders**
> operationalWebhookControllerUpdateHeaders(id, operationalWebhookEndpointHeadersInDto)

Set Operational Webhook Endpoint Headers

### Example
```java
// Import classes:
import com.solifyn.ApiClient;
import com.solifyn.ApiException;
import com.solifyn.Configuration;
import com.solifyn.models.*;
import com.solifyn.api.WebhookEndpointApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:8000");

    WebhookEndpointApi apiInstance = new WebhookEndpointApi(defaultClient);
    String id = "id_example"; // String | The endpoint ID or UID
    OperationalWebhookEndpointHeadersInDto operationalWebhookEndpointHeadersInDto = new OperationalWebhookEndpointHeadersInDto(); // OperationalWebhookEndpointHeadersInDto | 
    try {
      apiInstance.operationalWebhookControllerUpdateHeaders(id, operationalWebhookEndpointHeadersInDto);
    } catch (ApiException e) {
      System.err.println("Exception when calling WebhookEndpointApi#operationalWebhookControllerUpdateHeaders");
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
| **id** | **String**| The endpoint ID or UID | |
| **operationalWebhookEndpointHeadersInDto** | [**OperationalWebhookEndpointHeadersInDto**](OperationalWebhookEndpointHeadersInDto.md)|  | |

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
| **204** | Headers set |  -  |

