# MetersApi

All URIs are relative to *http://localhost:8000*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**eventsIngest**](MetersApi.md#eventsIngest) | **POST** /v1/meters/ingest | Ingest Events |
| [**metersCreate**](MetersApi.md#metersCreate) | **POST** /v1/meters | Create Meter |
| [**metersGet**](MetersApi.md#metersGet) | **GET** /v1/meters/{id} | Retrieve Meter |
| [**metersGetEvents**](MetersApi.md#metersGetEvents) | **GET** /v1/meters/{id}/events | List Meter Events |
| [**metersGetQuantities**](MetersApi.md#metersGetQuantities) | **GET** /v1/meters/{id}/quantities | Get Meter Quantities |
| [**metersList**](MetersApi.md#metersList) | **GET** /v1/meters | List Meters |
| [**metersUpdate**](MetersApi.md#metersUpdate) | **PATCH** /v1/meters/{id} | Update Meter |


<a id="eventsIngest"></a>
# **eventsIngest**
> MeterIngestResponseDto eventsIngest(meterIngestRequestDto)

Ingest Events

Ingest usage events for meters.

### Example
```java
// Import classes:
import com.solifyn.ApiClient;
import com.solifyn.ApiException;
import com.solifyn.Configuration;
import com.solifyn.auth.*;
import com.solifyn.models.*;
import com.solifyn.api.MetersApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:8000");
    
    // Configure HTTP bearer authorization: ApiKeyAuth
    HttpBearerAuth ApiKeyAuth = (HttpBearerAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setBearerToken("BEARER TOKEN");

    MetersApi apiInstance = new MetersApi(defaultClient);
    MeterIngestRequestDto meterIngestRequestDto = new MeterIngestRequestDto(); // MeterIngestRequestDto | 
    try {
      MeterIngestResponseDto result = apiInstance.eventsIngest(meterIngestRequestDto);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling MetersApi#eventsIngest");
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
| **meterIngestRequestDto** | [**MeterIngestRequestDto**](MeterIngestRequestDto.md)|  | |

### Return type

[**MeterIngestResponseDto**](MeterIngestResponseDto.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Events ingested successfully. |  -  |

<a id="metersCreate"></a>
# **metersCreate**
> MeterResponseDto metersCreate(createMeterDto)

Create Meter

Create a new usage meter for event-based billing and usage tracking.

### Example
```java
// Import classes:
import com.solifyn.ApiClient;
import com.solifyn.ApiException;
import com.solifyn.Configuration;
import com.solifyn.auth.*;
import com.solifyn.models.*;
import com.solifyn.api.MetersApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:8000");
    
    // Configure HTTP bearer authorization: ApiKeyAuth
    HttpBearerAuth ApiKeyAuth = (HttpBearerAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setBearerToken("BEARER TOKEN");

    MetersApi apiInstance = new MetersApi(defaultClient);
    CreateMeterDto createMeterDto = new CreateMeterDto(); // CreateMeterDto | 
    try {
      MeterResponseDto result = apiInstance.metersCreate(createMeterDto);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling MetersApi#metersCreate");
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
| **createMeterDto** | [**CreateMeterDto**](CreateMeterDto.md)|  | |

### Return type

[**MeterResponseDto**](MeterResponseDto.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Meter created successfully. |  -  |

<a id="metersGet"></a>
# **metersGet**
> MeterDetailResponseDto metersGet(id, startDate, endDate)

Retrieve Meter

Retrieve a meter and its most recent usage events.

### Example
```java
// Import classes:
import com.solifyn.ApiClient;
import com.solifyn.ApiException;
import com.solifyn.Configuration;
import com.solifyn.auth.*;
import com.solifyn.models.*;
import com.solifyn.api.MetersApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:8000");
    
    // Configure HTTP bearer authorization: ApiKeyAuth
    HttpBearerAuth ApiKeyAuth = (HttpBearerAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setBearerToken("BEARER TOKEN");

    MetersApi apiInstance = new MetersApi(defaultClient);
    String id = "mtr_8Z1aB2cD3eF4gH5iJ6kL7m"; // String | The unique meter ID.
    String startDate = "startDate_example"; // String | 
    String endDate = "endDate_example"; // String | 
    try {
      MeterDetailResponseDto result = apiInstance.metersGet(id, startDate, endDate);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling MetersApi#metersGet");
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
| **id** | **String**| The unique meter ID. | |
| **startDate** | **String**|  | |
| **endDate** | **String**|  | |

### Return type

[**MeterDetailResponseDto**](MeterDetailResponseDto.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Meter retrieved successfully. |  -  |

<a id="metersGetEvents"></a>
# **metersGetEvents**
> MeterEventsResponseDto metersGetEvents(id, limit)

List Meter Events

List recent usage events recorded for a meter.

### Example
```java
// Import classes:
import com.solifyn.ApiClient;
import com.solifyn.ApiException;
import com.solifyn.Configuration;
import com.solifyn.auth.*;
import com.solifyn.models.*;
import com.solifyn.api.MetersApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:8000");
    
    // Configure HTTP bearer authorization: ApiKeyAuth
    HttpBearerAuth ApiKeyAuth = (HttpBearerAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setBearerToken("BEARER TOKEN");

    MetersApi apiInstance = new MetersApi(defaultClient);
    String id = "mtr_8Z1aB2cD3eF4gH5iJ6kL7m"; // String | The unique meter ID.
    BigDecimal limit = new BigDecimal("100"); // BigDecimal | Maximum number of usage events to return.
    try {
      MeterEventsResponseDto result = apiInstance.metersGetEvents(id, limit);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling MetersApi#metersGetEvents");
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
| **id** | **String**| The unique meter ID. | |
| **limit** | **BigDecimal**| Maximum number of usage events to return. | [optional] [default to 100] |

### Return type

[**MeterEventsResponseDto**](MeterEventsResponseDto.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Meter events retrieved successfully. |  -  |

<a id="metersGetQuantities"></a>
# **metersGetQuantities**
> MeterQuantitiesResponseDto metersGetQuantities(id, startDate, endDate)

Get Meter Quantities

Get aggregated usage quantities for a meter within an optional date range.

### Example
```java
// Import classes:
import com.solifyn.ApiClient;
import com.solifyn.ApiException;
import com.solifyn.Configuration;
import com.solifyn.auth.*;
import com.solifyn.models.*;
import com.solifyn.api.MetersApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:8000");
    
    // Configure HTTP bearer authorization: ApiKeyAuth
    HttpBearerAuth ApiKeyAuth = (HttpBearerAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setBearerToken("BEARER TOKEN");

    MetersApi apiInstance = new MetersApi(defaultClient);
    String id = "mtr_8Z1aB2cD3eF4gH5iJ6kL7m"; // String | The unique meter ID.
    String startDate = "startDate_example"; // String | Inclusive start date in ISO 8601 format.
    String endDate = "endDate_example"; // String | Inclusive end date in ISO 8601 format.
    try {
      MeterQuantitiesResponseDto result = apiInstance.metersGetQuantities(id, startDate, endDate);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling MetersApi#metersGetQuantities");
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
| **id** | **String**| The unique meter ID. | |
| **startDate** | **String**| Inclusive start date in ISO 8601 format. | [optional] |
| **endDate** | **String**| Inclusive end date in ISO 8601 format. | [optional] |

### Return type

[**MeterQuantitiesResponseDto**](MeterQuantitiesResponseDto.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Meter quantities retrieved successfully. |  -  |

<a id="metersList"></a>
# **metersList**
> List&lt;MeterResponseDto&gt; metersList(status)

List Meters

List meters belonging to your active business. You can filter by archived status.

### Example
```java
// Import classes:
import com.solifyn.ApiClient;
import com.solifyn.ApiException;
import com.solifyn.Configuration;
import com.solifyn.auth.*;
import com.solifyn.models.*;
import com.solifyn.api.MetersApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:8000");
    
    // Configure HTTP bearer authorization: ApiKeyAuth
    HttpBearerAuth ApiKeyAuth = (HttpBearerAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setBearerToken("BEARER TOKEN");

    MetersApi apiInstance = new MetersApi(defaultClient);
    String status = "active"; // String | Filter by meter status.
    try {
      List<MeterResponseDto> result = apiInstance.metersList(status);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling MetersApi#metersList");
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
| **status** | **String**| Filter by meter status. | [optional] [enum: active, archived] |

### Return type

[**List&lt;MeterResponseDto&gt;**](MeterResponseDto.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Meters retrieved successfully. |  -  |

<a id="metersUpdate"></a>
# **metersUpdate**
> MeterResponseDto metersUpdate(id, updateMeterDto)

Update Meter

Update an existing meter definition.

### Example
```java
// Import classes:
import com.solifyn.ApiClient;
import com.solifyn.ApiException;
import com.solifyn.Configuration;
import com.solifyn.auth.*;
import com.solifyn.models.*;
import com.solifyn.api.MetersApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:8000");
    
    // Configure HTTP bearer authorization: ApiKeyAuth
    HttpBearerAuth ApiKeyAuth = (HttpBearerAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setBearerToken("BEARER TOKEN");

    MetersApi apiInstance = new MetersApi(defaultClient);
    String id = "mtr_8Z1aB2cD3eF4gH5iJ6kL7m"; // String | The unique meter ID.
    UpdateMeterDto updateMeterDto = new UpdateMeterDto(); // UpdateMeterDto | 
    try {
      MeterResponseDto result = apiInstance.metersUpdate(id, updateMeterDto);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling MetersApi#metersUpdate");
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
| **id** | **String**| The unique meter ID. | |
| **updateMeterDto** | [**UpdateMeterDto**](UpdateMeterDto.md)|  | |

### Return type

[**MeterResponseDto**](MeterResponseDto.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Meter updated successfully. |  -  |

