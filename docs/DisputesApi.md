# DisputesApi

All URIs are relative to *https://api.solifyn.com*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**disputesGenerateReport**](DisputesApi.md#disputesGenerateReport) | **GET** /v1/transactions/disputes/report | Generate Dispute CSV Report |
| [**disputesGet**](DisputesApi.md#disputesGet) | **GET** /v1/transactions/disputes/{id} | Retrieve Dispute |
| [**disputesList**](DisputesApi.md#disputesList) | **GET** /v1/transactions/disputes | List Disputes |
| [**disputesSubmitEvidence**](DisputesApi.md#disputesSubmitEvidence) | **POST** /v1/transactions/disputes/{id}/submit | Submit Dispute Evidence |
| [**disputesUpdateEvidence**](DisputesApi.md#disputesUpdateEvidence) | **PATCH** /v1/transactions/disputes/{id}/evidence | Update Dispute Evidence |
| [**disputesUploadEvidenceFile**](DisputesApi.md#disputesUploadEvidenceFile) | **POST** /v1/transactions/disputes/upload | Upload Evidence File |


<a id="disputesGenerateReport"></a>
# **disputesGenerateReport**
> disputesGenerateReport(createdAtGte, createdAtLte, status)

Generate Dispute CSV Report

Generates a downloadable CSV report of disputes matching the filters.

### Example
```java
// Import classes:
import com.solifyn.ApiClient;
import com.solifyn.ApiException;
import com.solifyn.Configuration;
import com.solifyn.auth.*;
import com.solifyn.models.*;
import com.solifyn.api.DisputesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.solifyn.com");
    
    // Configure HTTP bearer authorization: ApiKeyAuth
    HttpBearerAuth ApiKeyAuth = (HttpBearerAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setBearerToken("BEARER TOKEN");

    DisputesApi apiInstance = new DisputesApi(defaultClient);
    String createdAtGte = "createdAtGte_example"; // String | Filter disputes created after this ISO date-time string
    String createdAtLte = "createdAtLte_example"; // String | Filter disputes created before this ISO date-time string
    String status = "status_example"; // String | Filter disputes by status
    try {
      apiInstance.disputesGenerateReport(createdAtGte, createdAtLte, status);
    } catch (ApiException e) {
      System.err.println("Exception when calling DisputesApi#disputesGenerateReport");
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
| **createdAtGte** | **String**| Filter disputes created after this ISO date-time string | [optional] |
| **createdAtLte** | **String**| Filter disputes created before this ISO date-time string | [optional] |
| **status** | **String**| Filter disputes by status | [optional] |

### Return type

null (empty response body)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | CSV report file contents generated successfully. |  -  |

<a id="disputesGet"></a>
# **disputesGet**
> Dispute disputesGet(id)

Retrieve Dispute

Retrieve details of a specific dispute by ID.

### Example
```java
// Import classes:
import com.solifyn.ApiClient;
import com.solifyn.ApiException;
import com.solifyn.Configuration;
import com.solifyn.auth.*;
import com.solifyn.models.*;
import com.solifyn.api.DisputesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.solifyn.com");
    
    // Configure HTTP bearer authorization: ApiKeyAuth
    HttpBearerAuth ApiKeyAuth = (HttpBearerAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setBearerToken("BEARER TOKEN");

    DisputesApi apiInstance = new DisputesApi(defaultClient);
    String id = "dsp_123"; // String | The dispute ID
    try {
      Dispute result = apiInstance.disputesGet(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DisputesApi#disputesGet");
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
| **id** | **String**| The dispute ID | |

### Return type

[**Dispute**](Dispute.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Dispute details retrieved successfully. |  -  |

<a id="disputesList"></a>
# **disputesList**
> DisputeList disputesList(page, limit, status, type)

List Disputes

Retrieve disputes associated with the active business.

### Example
```java
// Import classes:
import com.solifyn.ApiClient;
import com.solifyn.ApiException;
import com.solifyn.Configuration;
import com.solifyn.auth.*;
import com.solifyn.models.*;
import com.solifyn.api.DisputesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.solifyn.com");
    
    // Configure HTTP bearer authorization: ApiKeyAuth
    HttpBearerAuth ApiKeyAuth = (HttpBearerAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setBearerToken("BEARER TOKEN");

    DisputesApi apiInstance = new DisputesApi(defaultClient);
    String page = "1"; // String | Page number for pagination
    String limit = "10"; // String | Page size limit for pagination
    String status = "status_example"; // String | Filter disputes by status
    String type = "type_example"; // String | Filter by type: dispute or alert
    try {
      DisputeList result = apiInstance.disputesList(page, limit, status, type);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DisputesApi#disputesList");
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
| **page** | **String**| Page number for pagination | [optional] |
| **limit** | **String**| Page size limit for pagination | [optional] |
| **status** | **String**| Filter disputes by status | [optional] |
| **type** | **String**| Filter by type: dispute or alert | [optional] |

### Return type

[**DisputeList**](DisputeList.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Dispute list retrieved successfully. |  -  |

<a id="disputesSubmitEvidence"></a>
# **disputesSubmitEvidence**
> Dispute disputesSubmitEvidence(id)

Submit Dispute Evidence

Finalize and submit the uploaded evidence for review.

### Example
```java
// Import classes:
import com.solifyn.ApiClient;
import com.solifyn.ApiException;
import com.solifyn.Configuration;
import com.solifyn.auth.*;
import com.solifyn.models.*;
import com.solifyn.api.DisputesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.solifyn.com");
    
    // Configure HTTP bearer authorization: ApiKeyAuth
    HttpBearerAuth ApiKeyAuth = (HttpBearerAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setBearerToken("BEARER TOKEN");

    DisputesApi apiInstance = new DisputesApi(defaultClient);
    String id = "dsp_123"; // String | The dispute ID
    try {
      Dispute result = apiInstance.disputesSubmitEvidence(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DisputesApi#disputesSubmitEvidence");
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
| **id** | **String**| The dispute ID | |

### Return type

[**Dispute**](Dispute.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Dispute evidence successfully submitted. |  -  |

<a id="disputesUpdateEvidence"></a>
# **disputesUpdateEvidence**
> Dispute disputesUpdateEvidence(id, disputeEvidenceUpdate)

Update Dispute Evidence

Upload and update evidence attachments for a dispute.

### Example
```java
// Import classes:
import com.solifyn.ApiClient;
import com.solifyn.ApiException;
import com.solifyn.Configuration;
import com.solifyn.auth.*;
import com.solifyn.models.*;
import com.solifyn.api.DisputesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.solifyn.com");
    
    // Configure HTTP bearer authorization: ApiKeyAuth
    HttpBearerAuth ApiKeyAuth = (HttpBearerAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setBearerToken("BEARER TOKEN");

    DisputesApi apiInstance = new DisputesApi(defaultClient);
    String id = "dsp_123"; // String | The dispute ID
    DisputeEvidenceUpdate disputeEvidenceUpdate = new DisputeEvidenceUpdate(); // DisputeEvidenceUpdate | 
    try {
      Dispute result = apiInstance.disputesUpdateEvidence(id, disputeEvidenceUpdate);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DisputesApi#disputesUpdateEvidence");
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
| **id** | **String**| The dispute ID | |
| **disputeEvidenceUpdate** | [**DisputeEvidenceUpdate**](DisputeEvidenceUpdate.md)|  | |

### Return type

[**Dispute**](Dispute.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Dispute evidence successfully updated. |  -  |

<a id="disputesUploadEvidenceFile"></a>
# **disputesUploadEvidenceFile**
> DisputeFileUpload disputesUploadEvidenceFile(_file)

Upload Evidence File

Upload a support file (image, PDF, video) to use as dispute evidence.

### Example
```java
// Import classes:
import com.solifyn.ApiClient;
import com.solifyn.ApiException;
import com.solifyn.Configuration;
import com.solifyn.auth.*;
import com.solifyn.models.*;
import com.solifyn.api.DisputesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.solifyn.com");
    
    // Configure HTTP bearer authorization: ApiKeyAuth
    HttpBearerAuth ApiKeyAuth = (HttpBearerAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setBearerToken("BEARER TOKEN");

    DisputesApi apiInstance = new DisputesApi(defaultClient);
    File _file = new File("/path/to/file"); // File | The evidence file to upload (Max 25MB: JPEG, PNG, GIF, WEBP, PDF, MP4, WEBM, QuickTime)
    try {
      DisputeFileUpload result = apiInstance.disputesUploadEvidenceFile(_file);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DisputesApi#disputesUploadEvidenceFile");
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
| **_file** | **File**| The evidence file to upload (Max 25MB: JPEG, PNG, GIF, WEBP, PDF, MP4, WEBM, QuickTime) | |

### Return type

[**DisputeFileUpload**](DisputeFileUpload.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | File upload details successfully created. |  -  |

