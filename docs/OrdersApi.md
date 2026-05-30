# OrdersApi

All URIs are relative to *http://localhost:8000*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**ordersGet**](OrdersApi.md#ordersGet) | **GET** /v1/orders/{id} | Retrieve Order |
| [**ordersGetInvoice**](OrdersApi.md#ordersGetInvoice) | **GET** /v1/orders/{id}/invoice | Get Order Invoice |
| [**ordersList**](OrdersApi.md#ordersList) | **GET** /v1/orders | List Orders |
| [**ordersUpdate**](OrdersApi.md#ordersUpdate) | **PATCH** /v1/orders/{id} | Update Order Billing Address |
| [**refundsCreate**](OrdersApi.md#refundsCreate) | **POST** /v1/orders/{id}/refund | Create Refund |


<a id="ordersGet"></a>
# **ordersGet**
> Order ordersGet(id)

Retrieve Order

Retrieve details of a specific order/payment by ID.

### Example
```java
// Import classes:
import com.solifyn.ApiClient;
import com.solifyn.ApiException;
import com.solifyn.Configuration;
import com.solifyn.auth.*;
import com.solifyn.models.*;
import com.solifyn.api.OrdersApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:8000");
    
    // Configure HTTP bearer authorization: ApiKeyAuth
    HttpBearerAuth ApiKeyAuth = (HttpBearerAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setBearerToken("BEARER TOKEN");

    OrdersApi apiInstance = new OrdersApi(defaultClient);
    String id = "pay_123"; // String | The unique order/payment ID.
    try {
      Order result = apiInstance.ordersGet(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling OrdersApi#ordersGet");
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

### Return type

[**Order**](Order.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Order resolved successfully. |  -  |

<a id="ordersGetInvoice"></a>
# **ordersGetInvoice**
> Invoice ordersGetInvoice(id)

Get Order Invoice

Retrieve the generated invoice details for the specified order.

### Example
```java
// Import classes:
import com.solifyn.ApiClient;
import com.solifyn.ApiException;
import com.solifyn.Configuration;
import com.solifyn.models.*;
import com.solifyn.api.OrdersApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:8000");

    OrdersApi apiInstance = new OrdersApi(defaultClient);
    String id = "pay_123"; // String | The unique order/payment ID.
    try {
      Invoice result = apiInstance.ordersGetInvoice(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling OrdersApi#ordersGetInvoice");
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

### Return type

[**Invoice**](Invoice.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Invoice retrieved successfully. |  -  |

<a id="ordersList"></a>
# **ordersList**
> OrderList ordersList(createdAtLte, createdAtGte, productId, customerId, status, pageSize, pageNumber)

List Orders

List and query orders/payments belonging to your active business.

### Example
```java
// Import classes:
import com.solifyn.ApiClient;
import com.solifyn.ApiException;
import com.solifyn.Configuration;
import com.solifyn.auth.*;
import com.solifyn.models.*;
import com.solifyn.api.OrdersApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:8000");
    
    // Configure HTTP bearer authorization: ApiKeyAuth
    HttpBearerAuth ApiKeyAuth = (HttpBearerAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setBearerToken("BEARER TOKEN");

    OrdersApi apiInstance = new OrdersApi(defaultClient);
    String createdAtLte = "createdAtLte_example"; // String | Filter by creation date less than or equal to.
    String createdAtGte = "createdAtGte_example"; // String | Filter by creation date greater than or equal to.
    String productId = "productId_example"; // String | Filter by product identifier.
    String customerId = "customerId_example"; // String | Filter by customer identifier.
    String status = "status_example"; // String | Filter by order/payment status.
    BigDecimal pageSize = new BigDecimal("10"); // BigDecimal | Size of a page, defaults to 10. Maximum is 100.
    BigDecimal pageNumber = new BigDecimal("1"); // BigDecimal | Page number, defaults to 1.
    try {
      OrderList result = apiInstance.ordersList(createdAtLte, createdAtGte, productId, customerId, status, pageSize, pageNumber);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling OrdersApi#ordersList");
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
| **createdAtLte** | **String**| Filter by creation date less than or equal to. | [optional] |
| **createdAtGte** | **String**| Filter by creation date greater than or equal to. | [optional] |
| **productId** | **String**| Filter by product identifier. | [optional] |
| **customerId** | **String**| Filter by customer identifier. | [optional] |
| **status** | **String**| Filter by order/payment status. | [optional] |
| **pageSize** | **BigDecimal**| Size of a page, defaults to 10. Maximum is 100. | [optional] [default to 10] |
| **pageNumber** | **BigDecimal**| Page number, defaults to 1. | [optional] [default to 1] |

### Return type

[**OrderList**](OrderList.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | List of orders/payments retrieved successfully. |  -  |

<a id="ordersUpdate"></a>
# **ordersUpdate**
> Order ordersUpdate(id, orderUpdate)

Update Order Billing Address

Update the billing details of an existing order.

### Example
```java
// Import classes:
import com.solifyn.ApiClient;
import com.solifyn.ApiException;
import com.solifyn.Configuration;
import com.solifyn.auth.*;
import com.solifyn.models.*;
import com.solifyn.api.OrdersApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:8000");
    
    // Configure HTTP bearer authorization: ApiKeyAuth
    HttpBearerAuth ApiKeyAuth = (HttpBearerAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setBearerToken("BEARER TOKEN");

    OrdersApi apiInstance = new OrdersApi(defaultClient);
    String id = "pay_123"; // String | The unique order/payment ID.
    OrderUpdate orderUpdate = new OrderUpdate(); // OrderUpdate | 
    try {
      Order result = apiInstance.ordersUpdate(id, orderUpdate);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling OrdersApi#ordersUpdate");
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
| **orderUpdate** | [**OrderUpdate**](OrderUpdate.md)|  | |

### Return type

[**Order**](Order.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Order billing address updated successfully. |  -  |

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
import com.solifyn.api.OrdersApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:8000");
    
    // Configure HTTP bearer authorization: ApiKeyAuth
    HttpBearerAuth ApiKeyAuth = (HttpBearerAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setBearerToken("BEARER TOKEN");

    OrdersApi apiInstance = new OrdersApi(defaultClient);
    String id = "pay_123"; // String | The unique order/payment ID.
    OrderRefundCreate orderRefundCreate = new OrderRefundCreate(); // OrderRefundCreate | 
    try {
      apiInstance.refundsCreate(id, orderRefundCreate);
    } catch (ApiException e) {
      System.err.println("Exception when calling OrdersApi#refundsCreate");
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

