# RefundsChargebacksApi

All URIs are relative to *http://localhost:8000*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**refundsCreate**](RefundsChargebacksApi.md#refundsCreate) | **POST** /v1/orders/{id}/refund | Create Refund |
| [**refundsGet**](RefundsChargebacksApi.md#refundsGet) | **GET** /v1/refunds/{id} | Retrieve Refund details |
| [**refundsList**](RefundsChargebacksApi.md#refundsList) | **GET** /v1/refunds | List Refunds |


<a id="refundsCreate"></a>
# **refundsCreate**
> refundsCreate(id, orderRefundCreate)

Create Refund

Initiate a full or partial refund for a specific payment/order.

### Example
```java
// Import classes:
import com.solifyn.ApiClient;
import com.solifyn.ApiException;
import com.solifyn.Configuration;
import com.solifyn.auth.*;
import com.solifyn.models.*;
import com.solifyn.api.RefundsChargebacksApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:8000");
    
    // Configure HTTP bearer authorization: ApiKeyAuth
    HttpBearerAuth ApiKeyAuth = (HttpBearerAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setBearerToken("BEARER TOKEN");

    RefundsChargebacksApi apiInstance = new RefundsChargebacksApi(defaultClient);
    String id = "pay_123"; // String | The unique order/payment ID.
    OrderRefundCreate orderRefundCreate = new OrderRefundCreate(); // OrderRefundCreate | 
    try {
      apiInstance.refundsCreate(id, orderRefundCreate);
    } catch (ApiException e) {
      System.err.println("Exception when calling RefundsChargebacksApi#refundsCreate");
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
| **id** | **String**| The unique order/payment ID. | |
| **orderRefundCreate** | [**OrderRefundCreate**](OrderRefundCreate.md)|  | |

### Return type

null (empty response body)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Refund processed successfully. |  -  |

<a id="refundsGet"></a>
# **refundsGet**
> Refund refundsGet(id)

Retrieve Refund details

Get parameters of a specific processed refund by database ID.

### Example
```java
// Import classes:
import com.solifyn.ApiClient;
import com.solifyn.ApiException;
import com.solifyn.Configuration;
import com.solifyn.auth.*;
import com.solifyn.models.*;
import com.solifyn.api.RefundsChargebacksApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:8000");
    
    // Configure HTTP bearer authorization: ApiKeyAuth
    HttpBearerAuth ApiKeyAuth = (HttpBearerAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setBearerToken("BEARER TOKEN");

    RefundsChargebacksApi apiInstance = new RefundsChargebacksApi(defaultClient);
    String id = "ref_123"; // String | Refund ID
    try {
      Refund result = apiInstance.refundsGet(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling RefundsChargebacksApi#refundsGet");
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
| **id** | **String**| Refund ID | |

### Return type

[**Refund**](Refund.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Refund resolved successfully. |  -  |

<a id="refundsList"></a>
# **refundsList**
> List&lt;Refund&gt; refundsList()

List Refunds

Retrieve a list of processed refunds and chargeback transactions.

### Example
```java
// Import classes:
import com.solifyn.ApiClient;
import com.solifyn.ApiException;
import com.solifyn.Configuration;
import com.solifyn.auth.*;
import com.solifyn.models.*;
import com.solifyn.api.RefundsChargebacksApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:8000");
    
    // Configure HTTP bearer authorization: ApiKeyAuth
    HttpBearerAuth ApiKeyAuth = (HttpBearerAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setBearerToken("BEARER TOKEN");

    RefundsChargebacksApi apiInstance = new RefundsChargebacksApi(defaultClient);
    try {
      List<Refund> result = apiInstance.refundsList();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling RefundsChargebacksApi#refundsList");
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

[**List&lt;Refund&gt;**](Refund.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Refunds list retrieved successfully. |  -  |

