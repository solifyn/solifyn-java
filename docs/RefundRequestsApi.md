# RefundRequestsApi

All URIs are relative to *http://localhost:8000*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**refundRequestsList**](RefundRequestsApi.md#refundRequestsList) | **GET** /v1/refund-requests | List Refund Requests (Merchant) |
| [**refundRequestsListMessages**](RefundRequestsApi.md#refundRequestsListMessages) | **GET** /v1/refund-requests/{id}/messages | List Messages for Refund Request (Merchant) |
| [**refundRequestsSendMessage**](RefundRequestsApi.md#refundRequestsSendMessage) | **POST** /v1/refund-requests/{id}/messages | Send Refund Request Message (Merchant) |
| [**refundRequestsUpdateStatus**](RefundRequestsApi.md#refundRequestsUpdateStatus) | **PATCH** /v1/refund-requests/{id}/status | Update Refund Request Status (Merchant) |
| [**refundRequestsUploadEvidence**](RefundRequestsApi.md#refundRequestsUploadEvidence) | **POST** /v1/refund-requests/upload-evidence | Upload Dispute Evidence File (Merchant) |


<a id="refundRequestsList"></a>
# **refundRequestsList**
> refundRequestsList()

List Refund Requests (Merchant)

### Example
```java
// Import classes:
import com.solifyn.ApiClient;
import com.solifyn.ApiException;
import com.solifyn.Configuration;
import com.solifyn.models.*;
import com.solifyn.api.RefundRequestsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:8000");

    RefundRequestsApi apiInstance = new RefundRequestsApi(defaultClient);
    try {
      apiInstance.refundRequestsList();
    } catch (ApiException e) {
      System.err.println("Exception when calling RefundRequestsApi#refundRequestsList");
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

<a id="refundRequestsListMessages"></a>
# **refundRequestsListMessages**
> refundRequestsListMessages(id)

List Messages for Refund Request (Merchant)

### Example
```java
// Import classes:
import com.solifyn.ApiClient;
import com.solifyn.ApiException;
import com.solifyn.Configuration;
import com.solifyn.models.*;
import com.solifyn.api.RefundRequestsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:8000");

    RefundRequestsApi apiInstance = new RefundRequestsApi(defaultClient);
    String id = "id_example"; // String | 
    try {
      apiInstance.refundRequestsListMessages(id);
    } catch (ApiException e) {
      System.err.println("Exception when calling RefundRequestsApi#refundRequestsListMessages");
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
| **id** | **String**|  | |

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

<a id="refundRequestsSendMessage"></a>
# **refundRequestsSendMessage**
> refundRequestsSendMessage(id)

Send Refund Request Message (Merchant)

### Example
```java
// Import classes:
import com.solifyn.ApiClient;
import com.solifyn.ApiException;
import com.solifyn.Configuration;
import com.solifyn.models.*;
import com.solifyn.api.RefundRequestsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:8000");

    RefundRequestsApi apiInstance = new RefundRequestsApi(defaultClient);
    String id = "id_example"; // String | 
    try {
      apiInstance.refundRequestsSendMessage(id);
    } catch (ApiException e) {
      System.err.println("Exception when calling RefundRequestsApi#refundRequestsSendMessage");
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
| **id** | **String**|  | |

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
| **201** |  |  -  |

<a id="refundRequestsUpdateStatus"></a>
# **refundRequestsUpdateStatus**
> refundRequestsUpdateStatus(id)

Update Refund Request Status (Merchant)

### Example
```java
// Import classes:
import com.solifyn.ApiClient;
import com.solifyn.ApiException;
import com.solifyn.Configuration;
import com.solifyn.models.*;
import com.solifyn.api.RefundRequestsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:8000");

    RefundRequestsApi apiInstance = new RefundRequestsApi(defaultClient);
    String id = "id_example"; // String | 
    try {
      apiInstance.refundRequestsUpdateStatus(id);
    } catch (ApiException e) {
      System.err.println("Exception when calling RefundRequestsApi#refundRequestsUpdateStatus");
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
| **id** | **String**|  | |

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

<a id="refundRequestsUploadEvidence"></a>
# **refundRequestsUploadEvidence**
> refundRequestsUploadEvidence()

Upload Dispute Evidence File (Merchant)

### Example
```java
// Import classes:
import com.solifyn.ApiClient;
import com.solifyn.ApiException;
import com.solifyn.Configuration;
import com.solifyn.models.*;
import com.solifyn.api.RefundRequestsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:8000");

    RefundRequestsApi apiInstance = new RefundRequestsApi(defaultClient);
    try {
      apiInstance.refundRequestsUploadEvidence();
    } catch (ApiException e) {
      System.err.println("Exception when calling RefundRequestsApi#refundRequestsUploadEvidence");
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
| **201** |  |  -  |

