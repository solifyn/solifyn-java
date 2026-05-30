# LicenseKeysClientApi

All URIs are relative to *http://localhost:8000*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**licensesActivate**](LicenseKeysClientApi.md#licensesActivate) | **POST** /v1/licenses/activate | Activate License Key |
| [**licensesDeactivate**](LicenseKeysClientApi.md#licensesDeactivate) | **POST** /v1/licenses/deactivate/{instanceId} | Deactivate Instance |
| [**licensesInstances**](LicenseKeysClientApi.md#licensesInstances) | **GET** /v1/licenses/instances/{licenseId} | Get Active Instances |
| [**licensesVerify**](LicenseKeysClientApi.md#licensesVerify) | **POST** /v1/licenses/verify | Validate License Key |


<a id="licensesActivate"></a>
# **licensesActivate**
> Instance licensesActivate(licensesActivateRequest)

Activate License Key

Register and activate a device or instance for a specific license key.

### Example
```java
// Import classes:
import com.solifyn.ApiClient;
import com.solifyn.ApiException;
import com.solifyn.Configuration;
import com.solifyn.auth.*;
import com.solifyn.models.*;
import com.solifyn.api.LicenseKeysClientApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:8000");
    
    // Configure HTTP bearer authorization: ApiKeyAuth
    HttpBearerAuth ApiKeyAuth = (HttpBearerAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setBearerToken("BEARER TOKEN");

    LicenseKeysClientApi apiInstance = new LicenseKeysClientApi(defaultClient);
    LicensesActivateRequest licensesActivateRequest = new LicensesActivateRequest(); // LicensesActivateRequest | 
    try {
      Instance result = apiInstance.licensesActivate(licensesActivateRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling LicenseKeysClientApi#licensesActivate");
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
| **licensesActivateRequest** | [**LicensesActivateRequest**](LicensesActivateRequest.md)|  | |

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
| **200** | Activation successful. |  -  |

<a id="licensesDeactivate"></a>
# **licensesDeactivate**
> LicensesDeactivate200Response licensesDeactivate(instanceId, licensesDeactivateRequest)

Deactivate Instance

Deactivate or unregister an active device instance from a license key.

### Example
```java
// Import classes:
import com.solifyn.ApiClient;
import com.solifyn.ApiException;
import com.solifyn.Configuration;
import com.solifyn.auth.*;
import com.solifyn.models.*;
import com.solifyn.api.LicenseKeysClientApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:8000");
    
    // Configure HTTP bearer authorization: ApiKeyAuth
    HttpBearerAuth ApiKeyAuth = (HttpBearerAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setBearerToken("BEARER TOKEN");

    LicenseKeysClientApi apiInstance = new LicenseKeysClientApi(defaultClient);
    UUID instanceId = UUID.randomUUID(); // UUID | The unique device instance ID.
    LicensesDeactivateRequest licensesDeactivateRequest = new LicensesDeactivateRequest(); // LicensesDeactivateRequest | 
    try {
      LicensesDeactivate200Response result = apiInstance.licensesDeactivate(instanceId, licensesDeactivateRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling LicenseKeysClientApi#licensesDeactivate");
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
| **instanceId** | **UUID**| The unique device instance ID. | |
| **licensesDeactivateRequest** | [**LicensesDeactivateRequest**](LicensesDeactivateRequest.md)|  | |

### Return type

[**LicensesDeactivate200Response**](LicensesDeactivate200Response.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Instance deactivated successfully. |  -  |

<a id="licensesInstances"></a>
# **licensesInstances**
> List&lt;Instance&gt; licensesInstances(licenseId)

Get Active Instances

List all active devices or server instances linked to a specific license key.

### Example
```java
// Import classes:
import com.solifyn.ApiClient;
import com.solifyn.ApiException;
import com.solifyn.Configuration;
import com.solifyn.auth.*;
import com.solifyn.models.*;
import com.solifyn.api.LicenseKeysClientApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:8000");
    
    // Configure HTTP bearer authorization: ApiKeyAuth
    HttpBearerAuth ApiKeyAuth = (HttpBearerAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setBearerToken("BEARER TOKEN");

    LicenseKeysClientApi apiInstance = new LicenseKeysClientApi(defaultClient);
    UUID licenseId = UUID.randomUUID(); // UUID | The unique license key ID.
    try {
      List<Instance> result = apiInstance.licensesInstances(licenseId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling LicenseKeysClientApi#licensesInstances");
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
| **licenseId** | **UUID**| The unique license key ID. | |

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
| **200** | Successfully retrieved active instances. |  -  |

<a id="licensesVerify"></a>
# **licensesVerify**
> LicenseValidationResponse licensesVerify(licensesVerifyRequest)

Validate License Key

Verify if a software license key is valid, active, and has not exceeded its limits.

### Example
```java
// Import classes:
import com.solifyn.ApiClient;
import com.solifyn.ApiException;
import com.solifyn.Configuration;
import com.solifyn.auth.*;
import com.solifyn.models.*;
import com.solifyn.api.LicenseKeysClientApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:8000");
    
    // Configure HTTP bearer authorization: ApiKeyAuth
    HttpBearerAuth ApiKeyAuth = (HttpBearerAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setBearerToken("BEARER TOKEN");

    LicenseKeysClientApi apiInstance = new LicenseKeysClientApi(defaultClient);
    LicensesVerifyRequest licensesVerifyRequest = new LicensesVerifyRequest(); // LicensesVerifyRequest | 
    try {
      LicenseValidationResponse result = apiInstance.licensesVerify(licensesVerifyRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling LicenseKeysClientApi#licensesVerify");
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
| **licensesVerifyRequest** | [**LicensesVerifyRequest**](LicensesVerifyRequest.md)|  | |

### Return type

[**LicenseValidationResponse**](LicenseValidationResponse.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | License is valid. |  -  |

