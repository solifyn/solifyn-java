# UserProfileThemesApi

All URIs are relative to *http://localhost:8000*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**usersGetMyPage**](UserProfileThemesApi.md#usersGetMyPage) | **GET** /v1/user/my-page | Get My Page details |
| [**usersGetMyTheme**](UserProfileThemesApi.md#usersGetMyTheme) | **GET** /v1/user/my-theme | Get My Theme |
| [**usersGetSettings**](UserProfileThemesApi.md#usersGetSettings) | **GET** /v1/user/settings | Retrieve User Settings |
| [**usersGetStats**](UserProfileThemesApi.md#usersGetStats) | **GET** /v1/user/dashboard-stats | Get Dashboard Statistics |
| [**usersGetThemeBySubdomain**](UserProfileThemesApi.md#usersGetThemeBySubdomain) | **GET** /v1/user/theme/{subdomain} | Get Theme by Subdomain |


<a id="usersGetMyPage"></a>
# **usersGetMyPage**
> UserPage usersGetMyPage()

Get My Page details

Retrieve page settings and custom content configured for the store.

### Example
```java
// Import classes:
import com.solifyn.ApiClient;
import com.solifyn.ApiException;
import com.solifyn.Configuration;
import com.solifyn.auth.*;
import com.solifyn.models.*;
import com.solifyn.api.UserProfileThemesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:8000");
    
    // Configure HTTP bearer authorization: ApiKeyAuth
    HttpBearerAuth ApiKeyAuth = (HttpBearerAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setBearerToken("BEARER TOKEN");

    UserProfileThemesApi apiInstance = new UserProfileThemesApi(defaultClient);
    try {
      UserPage result = apiInstance.usersGetMyPage();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling UserProfileThemesApi#usersGetMyPage");
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

[**UserPage**](UserPage.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Store page configuration data. |  -  |

<a id="usersGetMyTheme"></a>
# **usersGetMyTheme**
> UserTheme usersGetMyTheme()

Get My Theme

Retrieve theme configurations for the active business context.

### Example
```java
// Import classes:
import com.solifyn.ApiClient;
import com.solifyn.ApiException;
import com.solifyn.Configuration;
import com.solifyn.auth.*;
import com.solifyn.models.*;
import com.solifyn.api.UserProfileThemesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:8000");
    
    // Configure HTTP bearer authorization: ApiKeyAuth
    HttpBearerAuth ApiKeyAuth = (HttpBearerAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setBearerToken("BEARER TOKEN");

    UserProfileThemesApi apiInstance = new UserProfileThemesApi(defaultClient);
    try {
      UserTheme result = apiInstance.usersGetMyTheme();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling UserProfileThemesApi#usersGetMyTheme");
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

[**UserTheme**](UserTheme.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Active theme settings details. |  -  |

<a id="usersGetSettings"></a>
# **usersGetSettings**
> UserSettings usersGetSettings()

Retrieve User Settings

Retrieve profile settings and notification preferences for the user.

### Example
```java
// Import classes:
import com.solifyn.ApiClient;
import com.solifyn.ApiException;
import com.solifyn.Configuration;
import com.solifyn.auth.*;
import com.solifyn.models.*;
import com.solifyn.api.UserProfileThemesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:8000");
    
    // Configure HTTP bearer authorization: ApiKeyAuth
    HttpBearerAuth ApiKeyAuth = (HttpBearerAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setBearerToken("BEARER TOKEN");

    UserProfileThemesApi apiInstance = new UserProfileThemesApi(defaultClient);
    try {
      UserSettings result = apiInstance.usersGetSettings();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling UserProfileThemesApi#usersGetSettings");
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

[**UserSettings**](UserSettings.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | User settings profile details retrieved. |  -  |

<a id="usersGetStats"></a>
# **usersGetStats**
> UserStats usersGetStats()

Get Dashboard Statistics

Retrieve general analytics stats (revenue, order counts, etc.) for dashboard graphs.

### Example
```java
// Import classes:
import com.solifyn.ApiClient;
import com.solifyn.ApiException;
import com.solifyn.Configuration;
import com.solifyn.auth.*;
import com.solifyn.models.*;
import com.solifyn.api.UserProfileThemesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:8000");
    
    // Configure HTTP bearer authorization: ApiKeyAuth
    HttpBearerAuth ApiKeyAuth = (HttpBearerAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setBearerToken("BEARER TOKEN");

    UserProfileThemesApi apiInstance = new UserProfileThemesApi(defaultClient);
    try {
      UserStats result = apiInstance.usersGetStats();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling UserProfileThemesApi#usersGetStats");
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

[**UserStats**](UserStats.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Dashboard analytics statistics data. |  -  |

<a id="usersGetThemeBySubdomain"></a>
# **usersGetThemeBySubdomain**
> UserTheme usersGetThemeBySubdomain(subdomain)

Get Theme by Subdomain

Retrieve public theme configuration details by store subdomain.

### Example
```java
// Import classes:
import com.solifyn.ApiClient;
import com.solifyn.ApiException;
import com.solifyn.Configuration;
import com.solifyn.auth.*;
import com.solifyn.models.*;
import com.solifyn.api.UserProfileThemesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:8000");
    
    // Configure HTTP bearer authorization: ApiKeyAuth
    HttpBearerAuth ApiKeyAuth = (HttpBearerAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setBearerToken("BEARER TOKEN");

    UserProfileThemesApi apiInstance = new UserProfileThemesApi(defaultClient);
    String subdomain = "acme"; // String | The subdomain of the store
    try {
      UserTheme result = apiInstance.usersGetThemeBySubdomain(subdomain);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling UserProfileThemesApi#usersGetThemeBySubdomain");
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
| **subdomain** | **String**| The subdomain of the store | |

### Return type

[**UserTheme**](UserTheme.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Theme configurations retrieved successfully. |  -  |

