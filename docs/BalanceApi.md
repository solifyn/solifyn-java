# BalanceApi

All URIs are relative to *https://api.solifyn.com*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**balanceControllerFindAll**](BalanceApi.md#balanceControllerFindAll) | **GET** /v1/balances |  |
| [**balanceControllerGenerateReport**](BalanceApi.md#balanceControllerGenerateReport) | **GET** /v1/balances/report |  |
| [**balanceControllerGetSummary**](BalanceApi.md#balanceControllerGetSummary) | **GET** /v1/balances/summary |  |


<a id="balanceControllerFindAll"></a>
# **balanceControllerFindAll**
> balanceControllerFindAll()



### Example
```java
// Import classes:
import com.solifyn.ApiClient;
import com.solifyn.ApiException;
import com.solifyn.Configuration;
import com.solifyn.models.*;
import com.solifyn.api.BalanceApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.solifyn.com");

    BalanceApi apiInstance = new BalanceApi(defaultClient);
    try {
      apiInstance.balanceControllerFindAll();
    } catch (ApiException e) {
      System.err.println("Exception when calling BalanceApi#balanceControllerFindAll");
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

<a id="balanceControllerGenerateReport"></a>
# **balanceControllerGenerateReport**
> balanceControllerGenerateReport()



### Example
```java
// Import classes:
import com.solifyn.ApiClient;
import com.solifyn.ApiException;
import com.solifyn.Configuration;
import com.solifyn.models.*;
import com.solifyn.api.BalanceApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.solifyn.com");

    BalanceApi apiInstance = new BalanceApi(defaultClient);
    try {
      apiInstance.balanceControllerGenerateReport();
    } catch (ApiException e) {
      System.err.println("Exception when calling BalanceApi#balanceControllerGenerateReport");
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

<a id="balanceControllerGetSummary"></a>
# **balanceControllerGetSummary**
> balanceControllerGetSummary()



### Example
```java
// Import classes:
import com.solifyn.ApiClient;
import com.solifyn.ApiException;
import com.solifyn.Configuration;
import com.solifyn.models.*;
import com.solifyn.api.BalanceApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.solifyn.com");

    BalanceApi apiInstance = new BalanceApi(defaultClient);
    try {
      apiInstance.balanceControllerGetSummary();
    } catch (ApiException e) {
      System.err.println("Exception when calling BalanceApi#balanceControllerGetSummary");
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

