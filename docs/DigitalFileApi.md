# DigitalFileApi

All URIs are relative to *http://localhost:8000*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**digitalFileControllerCreate**](DigitalFileApi.md#digitalFileControllerCreate) | **POST** /v1/digital-files |  |
| [**digitalFileControllerFindAll**](DigitalFileApi.md#digitalFileControllerFindAll) | **GET** /v1/digital-files |  |
| [**digitalFileControllerRemove**](DigitalFileApi.md#digitalFileControllerRemove) | **DELETE** /v1/digital-files/{id} |  |


<a id="digitalFileControllerCreate"></a>
# **digitalFileControllerCreate**
> digitalFileControllerCreate()



### Example
```java
// Import classes:
import com.solifyn.ApiClient;
import com.solifyn.ApiException;
import com.solifyn.Configuration;
import com.solifyn.models.*;
import com.solifyn.api.DigitalFileApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:8000");

    DigitalFileApi apiInstance = new DigitalFileApi(defaultClient);
    try {
      apiInstance.digitalFileControllerCreate();
    } catch (ApiException e) {
      System.err.println("Exception when calling DigitalFileApi#digitalFileControllerCreate");
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

<a id="digitalFileControllerFindAll"></a>
# **digitalFileControllerFindAll**
> digitalFileControllerFindAll()



### Example
```java
// Import classes:
import com.solifyn.ApiClient;
import com.solifyn.ApiException;
import com.solifyn.Configuration;
import com.solifyn.models.*;
import com.solifyn.api.DigitalFileApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:8000");

    DigitalFileApi apiInstance = new DigitalFileApi(defaultClient);
    try {
      apiInstance.digitalFileControllerFindAll();
    } catch (ApiException e) {
      System.err.println("Exception when calling DigitalFileApi#digitalFileControllerFindAll");
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

<a id="digitalFileControllerRemove"></a>
# **digitalFileControllerRemove**
> digitalFileControllerRemove(id)



### Example
```java
// Import classes:
import com.solifyn.ApiClient;
import com.solifyn.ApiException;
import com.solifyn.Configuration;
import com.solifyn.models.*;
import com.solifyn.api.DigitalFileApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:8000");

    DigitalFileApi apiInstance = new DigitalFileApi(defaultClient);
    String id = "id_example"; // String | 
    try {
      apiInstance.digitalFileControllerRemove(id);
    } catch (ApiException e) {
      System.err.println("Exception when calling DigitalFileApi#digitalFileControllerRemove");
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

