# BusinessesApi

All URIs are relative to *http://localhost:8000*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**businessesBillingHistory**](BusinessesApi.md#businessesBillingHistory) | **GET** /v1/user/billing/history | Get Platform Billing History |
| [**merchantsGenerateApiKeys**](BusinessesApi.md#merchantsGenerateApiKeys) | **POST** /v1/user/whop-api-keys | Rotate Whop API Keys |
| [**merchantsUpdatePage**](BusinessesApi.md#merchantsUpdatePage) | **PATCH** /v1/user/page | Update Page configuration |
| [**merchantsUpdateSettings**](BusinessesApi.md#merchantsUpdateSettings) | **PATCH** /v1/user/settings | Update Merchant Settings |
| [**merchantsUpdateTheme**](BusinessesApi.md#merchantsUpdateTheme) | **PATCH** /v1/user/theme | Update Theme |


<a id="businessesBillingHistory"></a>
# **businessesBillingHistory**
> businessesBillingHistory()

Get Platform Billing History

Retrieve history of SaaS subscription payments paid by this business to the platform.

### Example
```java
// Import classes:
import com.solifyn.ApiClient;
import com.solifyn.ApiException;
import com.solifyn.Configuration;
import com.solifyn.auth.*;
import com.solifyn.models.*;
import com.solifyn.api.BusinessesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:8000");
    
    // Configure HTTP bearer authorization: ApiKeyAuth
    HttpBearerAuth ApiKeyAuth = (HttpBearerAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setBearerToken("BEARER TOKEN");

    BusinessesApi apiInstance = new BusinessesApi(defaultClient);
    try {
      apiInstance.businessesBillingHistory();
    } catch (ApiException e) {
      System.err.println("Exception when calling BusinessesApi#businessesBillingHistory");
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

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** |  |  -  |

<a id="merchantsGenerateApiKeys"></a>
# **merchantsGenerateApiKeys**
> WhopApiKeysRotation merchantsGenerateApiKeys()

Rotate Whop API Keys

Generate and sync a new Whop Child Company API key (restricted to business owners).

### Example
```java
// Import classes:
import com.solifyn.ApiClient;
import com.solifyn.ApiException;
import com.solifyn.Configuration;
import com.solifyn.auth.*;
import com.solifyn.models.*;
import com.solifyn.api.BusinessesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:8000");
    
    // Configure HTTP bearer authorization: ApiKeyAuth
    HttpBearerAuth ApiKeyAuth = (HttpBearerAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setBearerToken("BEARER TOKEN");

    BusinessesApi apiInstance = new BusinessesApi(defaultClient);
    try {
      WhopApiKeysRotation result = apiInstance.merchantsGenerateApiKeys();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling BusinessesApi#merchantsGenerateApiKeys");
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

[**WhopApiKeysRotation**](WhopApiKeysRotation.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Whop child API credentials successfully rotated. |  -  |

<a id="merchantsUpdatePage"></a>
# **merchantsUpdatePage**
> UserPage merchantsUpdatePage(userThemeUpdate)

Update Page configuration

Modify store page content configs, banner images, or avatar details.

### Example
```java
// Import classes:
import com.solifyn.ApiClient;
import com.solifyn.ApiException;
import com.solifyn.Configuration;
import com.solifyn.auth.*;
import com.solifyn.models.*;
import com.solifyn.api.BusinessesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:8000");
    
    // Configure HTTP bearer authorization: ApiKeyAuth
    HttpBearerAuth ApiKeyAuth = (HttpBearerAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setBearerToken("BEARER TOKEN");

    BusinessesApi apiInstance = new BusinessesApi(defaultClient);
    UserThemeUpdate userThemeUpdate = new UserThemeUpdate(); // UserThemeUpdate | 
    try {
      UserPage result = apiInstance.merchantsUpdatePage(userThemeUpdate);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling BusinessesApi#merchantsUpdatePage");
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
| **userThemeUpdate** | [**UserThemeUpdate**](UserThemeUpdate.md)|  | |

### Return type

[**UserPage**](UserPage.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Store page settings updated successfully. |  -  |

<a id="merchantsUpdateSettings"></a>
# **merchantsUpdateSettings**
> UserSettings merchantsUpdateSettings(userSettingsUpdate)

Update Merchant Settings

Update profile parameters, SEO, Google analytics, and email notification properties.

### Example
```java
// Import classes:
import com.solifyn.ApiClient;
import com.solifyn.ApiException;
import com.solifyn.Configuration;
import com.solifyn.auth.*;
import com.solifyn.models.*;
import com.solifyn.api.BusinessesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:8000");
    
    // Configure HTTP bearer authorization: ApiKeyAuth
    HttpBearerAuth ApiKeyAuth = (HttpBearerAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setBearerToken("BEARER TOKEN");

    BusinessesApi apiInstance = new BusinessesApi(defaultClient);
    UserSettingsUpdate userSettingsUpdate = new UserSettingsUpdate(); // UserSettingsUpdate | 
    try {
      UserSettings result = apiInstance.merchantsUpdateSettings(userSettingsUpdate);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling BusinessesApi#merchantsUpdateSettings");
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
| **userSettingsUpdate** | [**UserSettingsUpdate**](UserSettingsUpdate.md)|  | |

### Return type

[**UserSettings**](UserSettings.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | User settings successfully updated. |  -  |

<a id="merchantsUpdateTheme"></a>
# **merchantsUpdateTheme**
> UserTheme merchantsUpdateTheme(userThemeUpdate)

Update Theme

Update colors, fonts, avatar, or banner settings for the store.

### Example
```java
// Import classes:
import com.solifyn.ApiClient;
import com.solifyn.ApiException;
import com.solifyn.Configuration;
import com.solifyn.auth.*;
import com.solifyn.models.*;
import com.solifyn.api.BusinessesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:8000");
    
    // Configure HTTP bearer authorization: ApiKeyAuth
    HttpBearerAuth ApiKeyAuth = (HttpBearerAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setBearerToken("BEARER TOKEN");

    BusinessesApi apiInstance = new BusinessesApi(defaultClient);
    UserThemeUpdate userThemeUpdate = new UserThemeUpdate(); // UserThemeUpdate | 
    try {
      UserTheme result = apiInstance.merchantsUpdateTheme(userThemeUpdate);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling BusinessesApi#merchantsUpdateTheme");
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
| **userThemeUpdate** | [**UserThemeUpdate**](UserThemeUpdate.md)|  | |

### Return type

[**UserTheme**](UserTheme.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Theme settings successfully updated. |  -  |

