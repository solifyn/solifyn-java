# PartnerApi

All URIs are relative to *http://localhost:8000*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**partnerControllerGetPartnerCommissions**](PartnerApi.md#partnerControllerGetPartnerCommissions) | **GET** /v1/partner/commissions |  |
| [**partnerControllerGetPartnerStats**](PartnerApi.md#partnerControllerGetPartnerStats) | **GET** /v1/partner/stats |  |


<a id="partnerControllerGetPartnerCommissions"></a>
# **partnerControllerGetPartnerCommissions**
> partnerControllerGetPartnerCommissions()



### Example
```java
// Import classes:
import com.solifyn.ApiClient;
import com.solifyn.ApiException;
import com.solifyn.Configuration;
import com.solifyn.models.*;
import com.solifyn.api.PartnerApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:8000");

    PartnerApi apiInstance = new PartnerApi(defaultClient);
    try {
      apiInstance.partnerControllerGetPartnerCommissions();
    } catch (ApiException e) {
      System.err.println("Exception when calling PartnerApi#partnerControllerGetPartnerCommissions");
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

<a id="partnerControllerGetPartnerStats"></a>
# **partnerControllerGetPartnerStats**
> partnerControllerGetPartnerStats()



### Example
```java
// Import classes:
import com.solifyn.ApiClient;
import com.solifyn.ApiException;
import com.solifyn.Configuration;
import com.solifyn.models.*;
import com.solifyn.api.PartnerApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:8000");

    PartnerApi apiInstance = new PartnerApi(defaultClient);
    try {
      apiInstance.partnerControllerGetPartnerStats();
    } catch (ApiException e) {
      System.err.println("Exception when calling PartnerApi#partnerControllerGetPartnerStats");
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

