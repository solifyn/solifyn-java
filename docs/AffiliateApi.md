# AffiliateApi

All URIs are relative to *http://localhost:8000*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**affiliateControllerApproveConnection**](AffiliateApi.md#affiliateControllerApproveConnection) | **POST** /v1/affiliate/program/connections/{id}/approve |  |
| [**affiliateControllerArchiveConnection**](AffiliateApi.md#affiliateControllerArchiveConnection) | **POST** /v1/affiliate/program/connections/{id}/archive |  |
| [**affiliateControllerDeleteOverride**](AffiliateApi.md#affiliateControllerDeleteOverride) | **DELETE** /v1/affiliate/program/override/{id} |  |
| [**affiliateControllerGetEarningsConnections**](AffiliateApi.md#affiliateControllerGetEarningsConnections) | **GET** /v1/affiliate/earnings/connections |  |
| [**affiliateControllerGetEarningsLedger**](AffiliateApi.md#affiliateControllerGetEarningsLedger) | **GET** /v1/affiliate/earnings/ledger |  |
| [**affiliateControllerGetEarningsStats**](AffiliateApi.md#affiliateControllerGetEarningsStats) | **GET** /v1/affiliate/earnings/stats |  |
| [**affiliateControllerGetMarketplace**](AffiliateApi.md#affiliateControllerGetMarketplace) | **GET** /v1/affiliate/marketplace |  |
| [**affiliateControllerGetProgramConnections**](AffiliateApi.md#affiliateControllerGetProgramConnections) | **GET** /v1/affiliate/program/connections |  |
| [**affiliateControllerGetProgramLedger**](AffiliateApi.md#affiliateControllerGetProgramLedger) | **GET** /v1/affiliate/program/ledger |  |
| [**affiliateControllerGetProgramSettings**](AffiliateApi.md#affiliateControllerGetProgramSettings) | **GET** /v1/affiliate/program/settings |  |
| [**affiliateControllerJoinProgram**](AffiliateApi.md#affiliateControllerJoinProgram) | **POST** /v1/affiliate/marketplace/join |  |
| [**affiliateControllerRejectConnection**](AffiliateApi.md#affiliateControllerRejectConnection) | **POST** /v1/affiliate/program/connections/{id}/reject |  |
| [**affiliateControllerSaveOverride**](AffiliateApi.md#affiliateControllerSaveOverride) | **POST** /v1/affiliate/program/override |  |
| [**affiliateControllerSaveProgramSettings**](AffiliateApi.md#affiliateControllerSaveProgramSettings) | **POST** /v1/affiliate/program/settings |  |


<a id="affiliateControllerApproveConnection"></a>
# **affiliateControllerApproveConnection**
> affiliateControllerApproveConnection(id)



### Example
```java
// Import classes:
import com.solifyn.ApiClient;
import com.solifyn.ApiException;
import com.solifyn.Configuration;
import com.solifyn.models.*;
import com.solifyn.api.AffiliateApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:8000");

    AffiliateApi apiInstance = new AffiliateApi(defaultClient);
    String id = "id_example"; // String | 
    try {
      apiInstance.affiliateControllerApproveConnection(id);
    } catch (ApiException e) {
      System.err.println("Exception when calling AffiliateApi#affiliateControllerApproveConnection");
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

<a id="affiliateControllerArchiveConnection"></a>
# **affiliateControllerArchiveConnection**
> affiliateControllerArchiveConnection(id)



### Example
```java
// Import classes:
import com.solifyn.ApiClient;
import com.solifyn.ApiException;
import com.solifyn.Configuration;
import com.solifyn.models.*;
import com.solifyn.api.AffiliateApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:8000");

    AffiliateApi apiInstance = new AffiliateApi(defaultClient);
    String id = "id_example"; // String | 
    try {
      apiInstance.affiliateControllerArchiveConnection(id);
    } catch (ApiException e) {
      System.err.println("Exception when calling AffiliateApi#affiliateControllerArchiveConnection");
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

<a id="affiliateControllerDeleteOverride"></a>
# **affiliateControllerDeleteOverride**
> affiliateControllerDeleteOverride(id)



### Example
```java
// Import classes:
import com.solifyn.ApiClient;
import com.solifyn.ApiException;
import com.solifyn.Configuration;
import com.solifyn.models.*;
import com.solifyn.api.AffiliateApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:8000");

    AffiliateApi apiInstance = new AffiliateApi(defaultClient);
    String id = "id_example"; // String | 
    try {
      apiInstance.affiliateControllerDeleteOverride(id);
    } catch (ApiException e) {
      System.err.println("Exception when calling AffiliateApi#affiliateControllerDeleteOverride");
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

<a id="affiliateControllerGetEarningsConnections"></a>
# **affiliateControllerGetEarningsConnections**
> affiliateControllerGetEarningsConnections()



### Example
```java
// Import classes:
import com.solifyn.ApiClient;
import com.solifyn.ApiException;
import com.solifyn.Configuration;
import com.solifyn.models.*;
import com.solifyn.api.AffiliateApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:8000");

    AffiliateApi apiInstance = new AffiliateApi(defaultClient);
    try {
      apiInstance.affiliateControllerGetEarningsConnections();
    } catch (ApiException e) {
      System.err.println("Exception when calling AffiliateApi#affiliateControllerGetEarningsConnections");
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

<a id="affiliateControllerGetEarningsLedger"></a>
# **affiliateControllerGetEarningsLedger**
> affiliateControllerGetEarningsLedger()



### Example
```java
// Import classes:
import com.solifyn.ApiClient;
import com.solifyn.ApiException;
import com.solifyn.Configuration;
import com.solifyn.models.*;
import com.solifyn.api.AffiliateApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:8000");

    AffiliateApi apiInstance = new AffiliateApi(defaultClient);
    try {
      apiInstance.affiliateControllerGetEarningsLedger();
    } catch (ApiException e) {
      System.err.println("Exception when calling AffiliateApi#affiliateControllerGetEarningsLedger");
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

<a id="affiliateControllerGetEarningsStats"></a>
# **affiliateControllerGetEarningsStats**
> affiliateControllerGetEarningsStats()



### Example
```java
// Import classes:
import com.solifyn.ApiClient;
import com.solifyn.ApiException;
import com.solifyn.Configuration;
import com.solifyn.models.*;
import com.solifyn.api.AffiliateApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:8000");

    AffiliateApi apiInstance = new AffiliateApi(defaultClient);
    try {
      apiInstance.affiliateControllerGetEarningsStats();
    } catch (ApiException e) {
      System.err.println("Exception when calling AffiliateApi#affiliateControllerGetEarningsStats");
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

<a id="affiliateControllerGetMarketplace"></a>
# **affiliateControllerGetMarketplace**
> affiliateControllerGetMarketplace()



### Example
```java
// Import classes:
import com.solifyn.ApiClient;
import com.solifyn.ApiException;
import com.solifyn.Configuration;
import com.solifyn.models.*;
import com.solifyn.api.AffiliateApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:8000");

    AffiliateApi apiInstance = new AffiliateApi(defaultClient);
    try {
      apiInstance.affiliateControllerGetMarketplace();
    } catch (ApiException e) {
      System.err.println("Exception when calling AffiliateApi#affiliateControllerGetMarketplace");
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

<a id="affiliateControllerGetProgramConnections"></a>
# **affiliateControllerGetProgramConnections**
> affiliateControllerGetProgramConnections()



### Example
```java
// Import classes:
import com.solifyn.ApiClient;
import com.solifyn.ApiException;
import com.solifyn.Configuration;
import com.solifyn.models.*;
import com.solifyn.api.AffiliateApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:8000");

    AffiliateApi apiInstance = new AffiliateApi(defaultClient);
    try {
      apiInstance.affiliateControllerGetProgramConnections();
    } catch (ApiException e) {
      System.err.println("Exception when calling AffiliateApi#affiliateControllerGetProgramConnections");
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

<a id="affiliateControllerGetProgramLedger"></a>
# **affiliateControllerGetProgramLedger**
> affiliateControllerGetProgramLedger()



### Example
```java
// Import classes:
import com.solifyn.ApiClient;
import com.solifyn.ApiException;
import com.solifyn.Configuration;
import com.solifyn.models.*;
import com.solifyn.api.AffiliateApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:8000");

    AffiliateApi apiInstance = new AffiliateApi(defaultClient);
    try {
      apiInstance.affiliateControllerGetProgramLedger();
    } catch (ApiException e) {
      System.err.println("Exception when calling AffiliateApi#affiliateControllerGetProgramLedger");
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

<a id="affiliateControllerGetProgramSettings"></a>
# **affiliateControllerGetProgramSettings**
> affiliateControllerGetProgramSettings()



### Example
```java
// Import classes:
import com.solifyn.ApiClient;
import com.solifyn.ApiException;
import com.solifyn.Configuration;
import com.solifyn.models.*;
import com.solifyn.api.AffiliateApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:8000");

    AffiliateApi apiInstance = new AffiliateApi(defaultClient);
    try {
      apiInstance.affiliateControllerGetProgramSettings();
    } catch (ApiException e) {
      System.err.println("Exception when calling AffiliateApi#affiliateControllerGetProgramSettings");
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

<a id="affiliateControllerJoinProgram"></a>
# **affiliateControllerJoinProgram**
> affiliateControllerJoinProgram()



### Example
```java
// Import classes:
import com.solifyn.ApiClient;
import com.solifyn.ApiException;
import com.solifyn.Configuration;
import com.solifyn.models.*;
import com.solifyn.api.AffiliateApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:8000");

    AffiliateApi apiInstance = new AffiliateApi(defaultClient);
    try {
      apiInstance.affiliateControllerJoinProgram();
    } catch (ApiException e) {
      System.err.println("Exception when calling AffiliateApi#affiliateControllerJoinProgram");
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

<a id="affiliateControllerRejectConnection"></a>
# **affiliateControllerRejectConnection**
> affiliateControllerRejectConnection(id)



### Example
```java
// Import classes:
import com.solifyn.ApiClient;
import com.solifyn.ApiException;
import com.solifyn.Configuration;
import com.solifyn.models.*;
import com.solifyn.api.AffiliateApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:8000");

    AffiliateApi apiInstance = new AffiliateApi(defaultClient);
    String id = "id_example"; // String | 
    try {
      apiInstance.affiliateControllerRejectConnection(id);
    } catch (ApiException e) {
      System.err.println("Exception when calling AffiliateApi#affiliateControllerRejectConnection");
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

<a id="affiliateControllerSaveOverride"></a>
# **affiliateControllerSaveOverride**
> affiliateControllerSaveOverride()



### Example
```java
// Import classes:
import com.solifyn.ApiClient;
import com.solifyn.ApiException;
import com.solifyn.Configuration;
import com.solifyn.models.*;
import com.solifyn.api.AffiliateApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:8000");

    AffiliateApi apiInstance = new AffiliateApi(defaultClient);
    try {
      apiInstance.affiliateControllerSaveOverride();
    } catch (ApiException e) {
      System.err.println("Exception when calling AffiliateApi#affiliateControllerSaveOverride");
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

<a id="affiliateControllerSaveProgramSettings"></a>
# **affiliateControllerSaveProgramSettings**
> affiliateControllerSaveProgramSettings()



### Example
```java
// Import classes:
import com.solifyn.ApiClient;
import com.solifyn.ApiException;
import com.solifyn.Configuration;
import com.solifyn.models.*;
import com.solifyn.api.AffiliateApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:8000");

    AffiliateApi apiInstance = new AffiliateApi(defaultClient);
    try {
      apiInstance.affiliateControllerSaveProgramSettings();
    } catch (ApiException e) {
      System.err.println("Exception when calling AffiliateApi#affiliateControllerSaveProgramSettings");
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

