# LicenseKeysApi

All URIs are relative to *http://localhost:8000*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**licensesCreate**](LicenseKeysApi.md#licensesCreate) | **POST** /v1/licenses | Create License Key |
| [**licensesDeleteInstance**](LicenseKeysApi.md#licensesDeleteInstance) | **DELETE** /v1/licenses/instances/{instanceId} | Force Delete Instance |
| [**licensesGet**](LicenseKeysApi.md#licensesGet) | **GET** /v1/licenses/{id} | Get License Key |
| [**licensesGetInstance**](LicenseKeysApi.md#licensesGetInstance) | **GET** /v1/licenses/{id}/instances/{instanceId} | Get License Key Instance |
| [**licensesGetInstances**](LicenseKeysApi.md#licensesGetInstances) | **GET** /v1/licenses/{id}/instances | Get License Key Instances |
| [**licensesList**](LicenseKeysApi.md#licensesList) | **GET** /v1/licenses | List License Keys |
| [**licensesToggle**](LicenseKeysApi.md#licensesToggle) | **POST** /v1/licenses/{id}/toggle | Toggle License Status |
| [**licensesUpdate**](LicenseKeysApi.md#licensesUpdate) | **PATCH** /v1/licenses/{id} | Update License Key |
| [**licensesUpdateInstance**](LicenseKeysApi.md#licensesUpdateInstance) | **PATCH** /v1/licenses/{id}/instances/{instanceId} | Update License Key Instance |
| [**licensesUpdateInstancePost**](LicenseKeysApi.md#licensesUpdateInstancePost) | **POST** /v1/licenses/{id}/instances/{instanceId} | Update License Key Instance (POST) |


<a id="licensesCreate"></a>
# **licensesCreate**
> License licensesCreate(licensesCreateRequest)

Create License Key

Manually issue a new license key for a specific product.

### Example
```java
// Import classes:
import com.solifyn.ApiClient;
import com.solifyn.ApiException;
import com.solifyn.Configuration;
import com.solifyn.auth.*;
import com.solifyn.models.*;
import com.solifyn.api.LicenseKeysApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:8000");
    
    // Configure HTTP bearer authorization: ApiKeyAuth
    HttpBearerAuth ApiKeyAuth = (HttpBearerAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setBearerToken("BEARER TOKEN");

    LicenseKeysApi apiInstance = new LicenseKeysApi(defaultClient);
    LicensesCreateRequest licensesCreateRequest = new LicensesCreateRequest(); // LicensesCreateRequest | 
    try {
      License result = apiInstance.licensesCreate(licensesCreateRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling LicenseKeysApi#licensesCreate");
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
| **licensesCreateRequest** | [**LicensesCreateRequest**](LicensesCreateRequest.md)|  | |

### Return type

[**License**](License.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successfully created license. |  -  |

<a id="licensesDeleteInstance"></a>
# **licensesDeleteInstance**
> Instance licensesDeleteInstance(instanceId)

Force Delete Instance

Administrative endpoint to force-delete an instance globally by its database ID.

### Example
```java
// Import classes:
import com.solifyn.ApiClient;
import com.solifyn.ApiException;
import com.solifyn.Configuration;
import com.solifyn.auth.*;
import com.solifyn.models.*;
import com.solifyn.api.LicenseKeysApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:8000");
    
    // Configure HTTP bearer authorization: ApiKeyAuth
    HttpBearerAuth ApiKeyAuth = (HttpBearerAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setBearerToken("BEARER TOKEN");

    LicenseKeysApi apiInstance = new LicenseKeysApi(defaultClient);
    String instanceId = "inc_123"; // String | The unique hardware activation instance ID.
    try {
      Instance result = apiInstance.licensesDeleteInstance(instanceId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling LicenseKeysApi#licensesDeleteInstance");
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
| **instanceId** | **String**| The unique hardware activation instance ID. | |

### Return type

[**Instance**](Instance.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Instance deactivated/deleted successfully. |  -  |

<a id="licensesGet"></a>
# **licensesGet**
> License licensesGet(id)

Get License Key

Retrieve complete administrative details of a specific license key.

### Example
```java
// Import classes:
import com.solifyn.ApiClient;
import com.solifyn.ApiException;
import com.solifyn.Configuration;
import com.solifyn.auth.*;
import com.solifyn.models.*;
import com.solifyn.api.LicenseKeysApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:8000");
    
    // Configure HTTP bearer authorization: ApiKeyAuth
    HttpBearerAuth ApiKeyAuth = (HttpBearerAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setBearerToken("BEARER TOKEN");

    LicenseKeysApi apiInstance = new LicenseKeysApi(defaultClient);
    UUID id = UUID.randomUUID(); // UUID | The unique license key ID.
    try {
      License result = apiInstance.licensesGet(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling LicenseKeysApi#licensesGet");
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
| **id** | **UUID**| The unique license key ID. | |

### Return type

[**License**](License.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successfully retrieved license details. |  -  |

<a id="licensesGetInstance"></a>
# **licensesGetInstance**
> Instance licensesGetInstance(id, instanceId)

Get License Key Instance

Retrieve administrative details of a specific software license instance.

### Example
```java
// Import classes:
import com.solifyn.ApiClient;
import com.solifyn.ApiException;
import com.solifyn.Configuration;
import com.solifyn.auth.*;
import com.solifyn.models.*;
import com.solifyn.api.LicenseKeysApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:8000");
    
    // Configure HTTP bearer authorization: ApiKeyAuth
    HttpBearerAuth ApiKeyAuth = (HttpBearerAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setBearerToken("BEARER TOKEN");

    LicenseKeysApi apiInstance = new LicenseKeysApi(defaultClient);
    UUID id = UUID.randomUUID(); // UUID | The unique administrative identifier (ID) of the parent license key.
    String instanceId = "inc_123"; // String | The client-generated instance ID (hardware hash) or the internal database ID of the instance.
    try {
      Instance result = apiInstance.licensesGetInstance(id, instanceId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling LicenseKeysApi#licensesGetInstance");
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
| **id** | **UUID**| The unique administrative identifier (ID) of the parent license key. | |
| **instanceId** | **String**| The client-generated instance ID (hardware hash) or the internal database ID of the instance. | |

### Return type

[**Instance**](Instance.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successfully retrieved instance. |  -  |

<a id="licensesGetInstances"></a>
# **licensesGetInstances**
> List&lt;Instance&gt; licensesGetInstances(id)

Get License Key Instances

Retrieve all active devices/instances for a specific administrative license key.

### Example
```java
// Import classes:
import com.solifyn.ApiClient;
import com.solifyn.ApiException;
import com.solifyn.Configuration;
import com.solifyn.auth.*;
import com.solifyn.models.*;
import com.solifyn.api.LicenseKeysApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:8000");
    
    // Configure HTTP bearer authorization: ApiKeyAuth
    HttpBearerAuth ApiKeyAuth = (HttpBearerAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setBearerToken("BEARER TOKEN");

    LicenseKeysApi apiInstance = new LicenseKeysApi(defaultClient);
    String id = "lic_123"; // String | The unique administrative identifier (ID) of the parent license key.
    try {
      List<Instance> result = apiInstance.licensesGetInstances(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling LicenseKeysApi#licensesGetInstances");
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
| **id** | **String**| The unique administrative identifier (ID) of the parent license key. | |

### Return type

[**List&lt;Instance&gt;**](Instance.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successfully retrieved instances. |  -  |

<a id="licensesList"></a>
# **licensesList**
> List&lt;License&gt; licensesList()

List License Keys

List all administrative license keys belonging to products under your active business.

### Example
```java
// Import classes:
import com.solifyn.ApiClient;
import com.solifyn.ApiException;
import com.solifyn.Configuration;
import com.solifyn.auth.*;
import com.solifyn.models.*;
import com.solifyn.api.LicenseKeysApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:8000");
    
    // Configure HTTP bearer authorization: ApiKeyAuth
    HttpBearerAuth ApiKeyAuth = (HttpBearerAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setBearerToken("BEARER TOKEN");

    LicenseKeysApi apiInstance = new LicenseKeysApi(defaultClient);
    try {
      List<License> result = apiInstance.licensesList();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling LicenseKeysApi#licensesList");
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

[**List&lt;License&gt;**](License.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successfully retrieved licenses list. |  -  |

<a id="licensesToggle"></a>
# **licensesToggle**
> License licensesToggle(id)

Toggle License Status

Toggle the status of a specific license key between ACTIVE and DISABLED.

### Example
```java
// Import classes:
import com.solifyn.ApiClient;
import com.solifyn.ApiException;
import com.solifyn.Configuration;
import com.solifyn.auth.*;
import com.solifyn.models.*;
import com.solifyn.api.LicenseKeysApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:8000");
    
    // Configure HTTP bearer authorization: ApiKeyAuth
    HttpBearerAuth ApiKeyAuth = (HttpBearerAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setBearerToken("BEARER TOKEN");

    LicenseKeysApi apiInstance = new LicenseKeysApi(defaultClient);
    String id = "lic_123"; // String | The unique license key ID.
    try {
      License result = apiInstance.licensesToggle(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling LicenseKeysApi#licensesToggle");
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
| **id** | **String**| The unique license key ID. | |

### Return type

[**License**](License.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Status toggled successfully. |  -  |

<a id="licensesUpdate"></a>
# **licensesUpdate**
> License licensesUpdate(id, licensesUpdateRequest)

Update License Key

Update limits or status of an existing license key.

### Example
```java
// Import classes:
import com.solifyn.ApiClient;
import com.solifyn.ApiException;
import com.solifyn.Configuration;
import com.solifyn.auth.*;
import com.solifyn.models.*;
import com.solifyn.api.LicenseKeysApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:8000");
    
    // Configure HTTP bearer authorization: ApiKeyAuth
    HttpBearerAuth ApiKeyAuth = (HttpBearerAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setBearerToken("BEARER TOKEN");

    LicenseKeysApi apiInstance = new LicenseKeysApi(defaultClient);
    UUID id = UUID.randomUUID(); // UUID | The unique license key ID.
    LicensesUpdateRequest licensesUpdateRequest = new LicensesUpdateRequest(); // LicensesUpdateRequest | 
    try {
      License result = apiInstance.licensesUpdate(id, licensesUpdateRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling LicenseKeysApi#licensesUpdate");
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
| **id** | **UUID**| The unique license key ID. | |
| **licensesUpdateRequest** | [**LicensesUpdateRequest**](LicensesUpdateRequest.md)|  | |

### Return type

[**License**](License.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successfully updated license. |  -  |

<a id="licensesUpdateInstance"></a>
# **licensesUpdateInstance**
> Instance licensesUpdateInstance(instanceId, id, licensesUpdateInstancePostRequest)

Update License Key Instance

Update administrative details (like friendly display name or custom IP) of an active license device instance.

### Example
```java
// Import classes:
import com.solifyn.ApiClient;
import com.solifyn.ApiException;
import com.solifyn.Configuration;
import com.solifyn.auth.*;
import com.solifyn.models.*;
import com.solifyn.api.LicenseKeysApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:8000");
    
    // Configure HTTP bearer authorization: ApiKeyAuth
    HttpBearerAuth ApiKeyAuth = (HttpBearerAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setBearerToken("BEARER TOKEN");

    LicenseKeysApi apiInstance = new LicenseKeysApi(defaultClient);
    String instanceId = "inc_123"; // String | The client-generated instance ID (hardware hash) or the internal database ID of the instance.
    UUID id = UUID.randomUUID(); // UUID | The unique administrative identifier (ID) of the parent license key.
    LicensesUpdateInstancePostRequest licensesUpdateInstancePostRequest = new LicensesUpdateInstancePostRequest(); // LicensesUpdateInstancePostRequest | 
    try {
      Instance result = apiInstance.licensesUpdateInstance(instanceId, id, licensesUpdateInstancePostRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling LicenseKeysApi#licensesUpdateInstance");
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
| **instanceId** | **String**| The client-generated instance ID (hardware hash) or the internal database ID of the instance. | |
| **id** | **UUID**| The unique administrative identifier (ID) of the parent license key. | |
| **licensesUpdateInstancePostRequest** | [**LicensesUpdateInstancePostRequest**](LicensesUpdateInstancePostRequest.md)|  | |

### Return type

[**Instance**](Instance.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successfully updated instance. |  -  |

<a id="licensesUpdateInstancePost"></a>
# **licensesUpdateInstancePost**
> Instance licensesUpdateInstancePost(instanceId, id, licensesUpdateInstancePostRequest)

Update License Key Instance (POST)

Alternative POST endpoint to update administrative details (like friendly display name or custom IP) of an active license device instance.

### Example
```java
// Import classes:
import com.solifyn.ApiClient;
import com.solifyn.ApiException;
import com.solifyn.Configuration;
import com.solifyn.auth.*;
import com.solifyn.models.*;
import com.solifyn.api.LicenseKeysApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:8000");
    
    // Configure HTTP bearer authorization: ApiKeyAuth
    HttpBearerAuth ApiKeyAuth = (HttpBearerAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setBearerToken("BEARER TOKEN");

    LicenseKeysApi apiInstance = new LicenseKeysApi(defaultClient);
    String instanceId = "inc_123"; // String | The client-generated instance ID (hardware hash) or the internal database ID of the instance.
    UUID id = UUID.randomUUID(); // UUID | The unique administrative identifier (ID) of the parent license key.
    LicensesUpdateInstancePostRequest licensesUpdateInstancePostRequest = new LicensesUpdateInstancePostRequest(); // LicensesUpdateInstancePostRequest | 
    try {
      Instance result = apiInstance.licensesUpdateInstancePost(instanceId, id, licensesUpdateInstancePostRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling LicenseKeysApi#licensesUpdateInstancePost");
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
| **instanceId** | **String**| The client-generated instance ID (hardware hash) or the internal database ID of the instance. | |
| **id** | **UUID**| The unique administrative identifier (ID) of the parent license key. | |
| **licensesUpdateInstancePostRequest** | [**LicensesUpdateInstancePostRequest**](LicensesUpdateInstancePostRequest.md)|  | |

### Return type

[**Instance**](Instance.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successfully updated instance. |  -  |

