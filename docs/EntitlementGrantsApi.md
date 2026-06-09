# EntitlementGrantsApi

All URIs are relative to *https://api.solifyn.com*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**entitlementGrantsGet**](EntitlementGrantsApi.md#entitlementGrantsGet) | **GET** /v1/entitlement-grants/{id} | Retrieve Entitlement Grant |
| [**entitlementGrantsList**](EntitlementGrantsApi.md#entitlementGrantsList) | **GET** /v1/entitlement-grants | List Entitlement Grants |
| [**entitlementGrantsRetry**](EntitlementGrantsApi.md#entitlementGrantsRetry) | **POST** /v1/entitlement-grants/{id}/retry | Retry Entitlement Grant Delivery |
| [**entitlementGrantsRevoke**](EntitlementGrantsApi.md#entitlementGrantsRevoke) | **POST** /v1/entitlement-grants/{id}/revoke | Manually Revoke Entitlement Grant |


<a id="entitlementGrantsGet"></a>
# **entitlementGrantsGet**
> EntitlementGrantResponseDto entitlementGrantsGet(id)

Retrieve Entitlement Grant

Retrieve details of a specific entitlement grant.

### Example
```java
// Import classes:
import com.solifyn.ApiClient;
import com.solifyn.ApiException;
import com.solifyn.Configuration;
import com.solifyn.auth.*;
import com.solifyn.models.*;
import com.solifyn.api.EntitlementGrantsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.solifyn.com");
    
    // Configure HTTP bearer authorization: ApiKeyAuth
    HttpBearerAuth ApiKeyAuth = (HttpBearerAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setBearerToken("BEARER TOKEN");

    EntitlementGrantsApi apiInstance = new EntitlementGrantsApi(defaultClient);
    String id = "id_example"; // String | The unique grant ID
    try {
      EntitlementGrantResponseDto result = apiInstance.entitlementGrantsGet(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling EntitlementGrantsApi#entitlementGrantsGet");
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
| **id** | **String**| The unique grant ID | |

### Return type

[**EntitlementGrantResponseDto**](EntitlementGrantResponseDto.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Details of the grant. |  -  |

<a id="entitlementGrantsList"></a>
# **entitlementGrantsList**
> List&lt;EntitlementGrantResponseDto&gt; entitlementGrantsList(status)

List Entitlement Grants

Retrieve all GitHub repository entitlement grants for the active business.

### Example
```java
// Import classes:
import com.solifyn.ApiClient;
import com.solifyn.ApiException;
import com.solifyn.Configuration;
import com.solifyn.auth.*;
import com.solifyn.models.*;
import com.solifyn.api.EntitlementGrantsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.solifyn.com");
    
    // Configure HTTP bearer authorization: ApiKeyAuth
    HttpBearerAuth ApiKeyAuth = (HttpBearerAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setBearerToken("BEARER TOKEN");

    EntitlementGrantsApi apiInstance = new EntitlementGrantsApi(defaultClient);
    String status = "status_example"; // String | Filter by status (PENDING, DELIVERED, FAILED, REVOKED)
    try {
      List<EntitlementGrantResponseDto> result = apiInstance.entitlementGrantsList(status);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling EntitlementGrantsApi#entitlementGrantsList");
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
| **status** | **String**| Filter by status (PENDING, DELIVERED, FAILED, REVOKED) | [optional] |

### Return type

[**List&lt;EntitlementGrantResponseDto&gt;**](EntitlementGrantResponseDto.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successfully retrieved list of grants. |  -  |

<a id="entitlementGrantsRetry"></a>
# **entitlementGrantsRetry**
> EntitlementGrantResponseDto entitlementGrantsRetry(id)

Retry Entitlement Grant Delivery

Attempts to re-invite the collaborator if GitHub username is already connected, or resets the OAuth URL redirect.

### Example
```java
// Import classes:
import com.solifyn.ApiClient;
import com.solifyn.ApiException;
import com.solifyn.Configuration;
import com.solifyn.auth.*;
import com.solifyn.models.*;
import com.solifyn.api.EntitlementGrantsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.solifyn.com");
    
    // Configure HTTP bearer authorization: ApiKeyAuth
    HttpBearerAuth ApiKeyAuth = (HttpBearerAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setBearerToken("BEARER TOKEN");

    EntitlementGrantsApi apiInstance = new EntitlementGrantsApi(defaultClient);
    String id = "id_example"; // String | The unique grant ID
    try {
      EntitlementGrantResponseDto result = apiInstance.entitlementGrantsRetry(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling EntitlementGrantsApi#entitlementGrantsRetry");
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
| **id** | **String**| The unique grant ID | |

### Return type

[**EntitlementGrantResponseDto**](EntitlementGrantResponseDto.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Grant delivery retried. |  -  |

<a id="entitlementGrantsRevoke"></a>
# **entitlementGrantsRevoke**
> EntitlementGrantResponseDto entitlementGrantsRevoke(id)

Manually Revoke Entitlement Grant

Manually remove the customer collaborator access from the repository and revoke the grant.

### Example
```java
// Import classes:
import com.solifyn.ApiClient;
import com.solifyn.ApiException;
import com.solifyn.Configuration;
import com.solifyn.auth.*;
import com.solifyn.models.*;
import com.solifyn.api.EntitlementGrantsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.solifyn.com");
    
    // Configure HTTP bearer authorization: ApiKeyAuth
    HttpBearerAuth ApiKeyAuth = (HttpBearerAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setBearerToken("BEARER TOKEN");

    EntitlementGrantsApi apiInstance = new EntitlementGrantsApi(defaultClient);
    String id = "id_example"; // String | The unique grant ID
    try {
      EntitlementGrantResponseDto result = apiInstance.entitlementGrantsRevoke(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling EntitlementGrantsApi#entitlementGrantsRevoke");
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
| **id** | **String**| The unique grant ID | |

### Return type

[**EntitlementGrantResponseDto**](EntitlementGrantResponseDto.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Grant successfully revoked. |  -  |

