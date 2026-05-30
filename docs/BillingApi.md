# BillingApi

All URIs are relative to *http://localhost:8000*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**billingGetPlans**](BillingApi.md#billingGetPlans) | **GET** /v1/billing/plans | Get Platform Plans |


<a id="billingGetPlans"></a>
# **billingGetPlans**
> billingGetPlans()

Get Platform Plans

Returns all available platform subscription plans with fees and features.

### Example
```java
// Import classes:
import com.solifyn.ApiClient;
import com.solifyn.ApiException;
import com.solifyn.Configuration;
import com.solifyn.models.*;
import com.solifyn.api.BillingApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:8000");

    BillingApi apiInstance = new BillingApi(defaultClient);
    try {
      apiInstance.billingGetPlans();
    } catch (ApiException e) {
      System.err.println("Exception when calling BillingApi#billingGetPlans");
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
| **200** | List of available platform plans. |  -  |

