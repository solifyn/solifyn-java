# EntitlementsApi

All URIs are relative to *https://api.solifyn.com*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**entitlementsCreate**](EntitlementsApi.md#entitlementsCreate) | **POST** /v1/entitlements | Create Entitlement |
| [**entitlementsDelete**](EntitlementsApi.md#entitlementsDelete) | **DELETE** /v1/entitlements/{id} | Delete Entitlement |
| [**entitlementsGet**](EntitlementsApi.md#entitlementsGet) | **GET** /v1/entitlements/{id} | Retrieve Entitlement |
| [**entitlementsList**](EntitlementsApi.md#entitlementsList) | **GET** /v1/entitlements | List Entitlements |
| [**entitlementsUpdate**](EntitlementsApi.md#entitlementsUpdate) | **PATCH** /v1/entitlements/{id} | Update Entitlement |


<a id="entitlementsCreate"></a>
# **entitlementsCreate**
> EntitlementDetailResponseDto entitlementsCreate(createEntitlementDto)

Create Entitlement

Create a new independent access entitlement.

### Example
```java
// Import classes:
import com.solifyn.ApiClient;
import com.solifyn.ApiException;
import com.solifyn.Configuration;
import com.solifyn.models.*;
import com.solifyn.api.EntitlementsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.solifyn.com");

    EntitlementsApi apiInstance = new EntitlementsApi(defaultClient);
    CreateEntitlementDto createEntitlementDto = new CreateEntitlementDto(); // CreateEntitlementDto | 
    try {
      EntitlementDetailResponseDto result = apiInstance.entitlementsCreate(createEntitlementDto);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling EntitlementsApi#entitlementsCreate");
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
| **createEntitlementDto** | [**CreateEntitlementDto**](CreateEntitlementDto.md)|  | |

### Return type

[**EntitlementDetailResponseDto**](EntitlementDetailResponseDto.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Entitlement created successfully. |  -  |

<a id="entitlementsDelete"></a>
# **entitlementsDelete**
> EntitlementDetailResponseDto entitlementsDelete(id)

Delete Entitlement

Delete an independent entitlement and unlink all mapped products.

### Example
```java
// Import classes:
import com.solifyn.ApiClient;
import com.solifyn.ApiException;
import com.solifyn.Configuration;
import com.solifyn.models.*;
import com.solifyn.api.EntitlementsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.solifyn.com");

    EntitlementsApi apiInstance = new EntitlementsApi(defaultClient);
    String id = "ent_8Z1aB2cD3eF4gH5iJ6kL7m"; // String | The unique entitlement ID.
    try {
      EntitlementDetailResponseDto result = apiInstance.entitlementsDelete(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling EntitlementsApi#entitlementsDelete");
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
| **id** | **String**| The unique entitlement ID. | |

### Return type

[**EntitlementDetailResponseDto**](EntitlementDetailResponseDto.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Entitlement deleted successfully. |  -  |

<a id="entitlementsGet"></a>
# **entitlementsGet**
> EntitlementDetailResponseDto entitlementsGet(id)

Retrieve Entitlement

Retrieve a specific entitlement definition by ID.

### Example
```java
// Import classes:
import com.solifyn.ApiClient;
import com.solifyn.ApiException;
import com.solifyn.Configuration;
import com.solifyn.models.*;
import com.solifyn.api.EntitlementsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.solifyn.com");

    EntitlementsApi apiInstance = new EntitlementsApi(defaultClient);
    String id = "ent_8Z1aB2cD3eF4gH5iJ6kL7m"; // String | The unique entitlement ID.
    try {
      EntitlementDetailResponseDto result = apiInstance.entitlementsGet(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling EntitlementsApi#entitlementsGet");
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
| **id** | **String**| The unique entitlement ID. | |

### Return type

[**EntitlementDetailResponseDto**](EntitlementDetailResponseDto.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Entitlement retrieved successfully. |  -  |

<a id="entitlementsList"></a>
# **entitlementsList**
> List&lt;EntitlementDetailResponseDto&gt; entitlementsList()

List Entitlements

List all independent entitlements for the active business.

### Example
```java
// Import classes:
import com.solifyn.ApiClient;
import com.solifyn.ApiException;
import com.solifyn.Configuration;
import com.solifyn.models.*;
import com.solifyn.api.EntitlementsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.solifyn.com");

    EntitlementsApi apiInstance = new EntitlementsApi(defaultClient);
    try {
      List<EntitlementDetailResponseDto> result = apiInstance.entitlementsList();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling EntitlementsApi#entitlementsList");
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

[**List&lt;EntitlementDetailResponseDto&gt;**](EntitlementDetailResponseDto.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Entitlements retrieved successfully. |  -  |

<a id="entitlementsUpdate"></a>
# **entitlementsUpdate**
> EntitlementDetailResponseDto entitlementsUpdate(id, updateEntitlementDto)

Update Entitlement

Update details of an existing independent entitlement.

### Example
```java
// Import classes:
import com.solifyn.ApiClient;
import com.solifyn.ApiException;
import com.solifyn.Configuration;
import com.solifyn.models.*;
import com.solifyn.api.EntitlementsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.solifyn.com");

    EntitlementsApi apiInstance = new EntitlementsApi(defaultClient);
    String id = "ent_8Z1aB2cD3eF4gH5iJ6kL7m"; // String | The unique entitlement ID.
    UpdateEntitlementDto updateEntitlementDto = new UpdateEntitlementDto(); // UpdateEntitlementDto | 
    try {
      EntitlementDetailResponseDto result = apiInstance.entitlementsUpdate(id, updateEntitlementDto);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling EntitlementsApi#entitlementsUpdate");
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
| **id** | **String**| The unique entitlement ID. | |
| **updateEntitlementDto** | [**UpdateEntitlementDto**](UpdateEntitlementDto.md)|  | |

### Return type

[**EntitlementDetailResponseDto**](EntitlementDetailResponseDto.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Entitlement updated successfully. |  -  |

