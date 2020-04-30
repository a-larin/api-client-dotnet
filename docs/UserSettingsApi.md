# LaunchDarkly.Api.Api.UserSettingsApi

All URIs are relative to *https://app.launchdarkly.com/api/v2*

Method | HTTP request | Description
------------- | ------------- | -------------
[**GetExpiringUserTargetsForUser**](UserSettingsApi.md#getexpiringusertargetsforuser) | **GET** /users/{projectKey}/{userKey}/expiring-user-targets/{environmentKey} | Get expiring dates on flags for user
[**GetUserFlagSetting**](UserSettingsApi.md#getuserflagsetting) | **GET** /users/{projectKey}/{environmentKey}/{userKey}/flags/{featureFlagKey} | Fetch a single flag setting for a user by key.
[**GetUserFlagSettings**](UserSettingsApi.md#getuserflagsettings) | **GET** /users/{projectKey}/{environmentKey}/{userKey}/flags | Fetch a single flag setting for a user by key.
[**PatchExpiringUserTargetsForFlags**](UserSettingsApi.md#patchexpiringusertargetsforflags) | **PATCH** /users/{projectKey}/{userKey}/expiring-user-targets/{environmentKey} | Update, add, or delete expiring user targets for a single user on all flags
[**PutFlagSetting**](UserSettingsApi.md#putflagsetting) | **PUT** /users/{projectKey}/{environmentKey}/{userKey}/flags/{featureFlagKey} | Specifically enable or disable a feature flag for a user based on their key.


<a name="getexpiringusertargetsforuser"></a>
# **GetExpiringUserTargetsForUser**
> UserTargetingExpirationOnFlagsForUser GetExpiringUserTargetsForUser (string projectKey, string environmentKey, string userKey)

Get expiring dates on flags for user

### Example
```csharp
using System;
using System.Diagnostics;
using LaunchDarkly.Api.Api;
using LaunchDarkly.Api.Client;
using LaunchDarkly.Api.Model;

namespace Example
{
    public class GetExpiringUserTargetsForUserExample
    {
        public void main()
        {
            
            // Configure API key authorization: Token
            Configuration.Default.ApiKey.Add("Authorization", "YOUR_API_KEY");
            // Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
            // Configuration.Default.ApiKeyPrefix.Add("Authorization", "Bearer");

            var apiInstance = new UserSettingsApi();
            var projectKey = projectKey_example;  // string | The project key, used to tie the flags together under one project so they can be managed together.
            var environmentKey = environmentKey_example;  // string | The environment key, used to tie together flag configuration and users under one environment so they can be managed together.
            var userKey = userKey_example;  // string | The user's key.

            try
            {
                // Get expiring dates on flags for user
                UserTargetingExpirationOnFlagsForUser result = apiInstance.GetExpiringUserTargetsForUser(projectKey, environmentKey, userKey);
                Debug.WriteLine(result);
            }
            catch (Exception e)
            {
                Debug.Print("Exception when calling UserSettingsApi.GetExpiringUserTargetsForUser: " + e.Message );
            }
        }
    }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **projectKey** | **string**| The project key, used to tie the flags together under one project so they can be managed together. | 
 **environmentKey** | **string**| The environment key, used to tie together flag configuration and users under one environment so they can be managed together. | 
 **userKey** | **string**| The user&#39;s key. | 

### Return type

[**UserTargetingExpirationOnFlagsForUser**](UserTargetingExpirationOnFlagsForUser.md)

### Authorization

[Token](../README.md#Token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a name="getuserflagsetting"></a>
# **GetUserFlagSetting**
> UserFlagSetting GetUserFlagSetting (string projectKey, string environmentKey, string userKey, string featureFlagKey)

Fetch a single flag setting for a user by key.

### Example
```csharp
using System;
using System.Diagnostics;
using LaunchDarkly.Api.Api;
using LaunchDarkly.Api.Client;
using LaunchDarkly.Api.Model;

namespace Example
{
    public class GetUserFlagSettingExample
    {
        public void main()
        {
            
            // Configure API key authorization: Token
            Configuration.Default.ApiKey.Add("Authorization", "YOUR_API_KEY");
            // Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
            // Configuration.Default.ApiKeyPrefix.Add("Authorization", "Bearer");

            var apiInstance = new UserSettingsApi();
            var projectKey = projectKey_example;  // string | The project key, used to tie the flags together under one project so they can be managed together.
            var environmentKey = environmentKey_example;  // string | The environment key, used to tie together flag configuration and users under one environment so they can be managed together.
            var userKey = userKey_example;  // string | The user's key.
            var featureFlagKey = featureFlagKey_example;  // string | The feature flag's key. The key identifies the flag in your code.

            try
            {
                // Fetch a single flag setting for a user by key.
                UserFlagSetting result = apiInstance.GetUserFlagSetting(projectKey, environmentKey, userKey, featureFlagKey);
                Debug.WriteLine(result);
            }
            catch (Exception e)
            {
                Debug.Print("Exception when calling UserSettingsApi.GetUserFlagSetting: " + e.Message );
            }
        }
    }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **projectKey** | **string**| The project key, used to tie the flags together under one project so they can be managed together. | 
 **environmentKey** | **string**| The environment key, used to tie together flag configuration and users under one environment so they can be managed together. | 
 **userKey** | **string**| The user&#39;s key. | 
 **featureFlagKey** | **string**| The feature flag&#39;s key. The key identifies the flag in your code. | 

### Return type

[**UserFlagSetting**](UserFlagSetting.md)

### Authorization

[Token](../README.md#Token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a name="getuserflagsettings"></a>
# **GetUserFlagSettings**
> UserFlagSettings GetUserFlagSettings (string projectKey, string environmentKey, string userKey)

Fetch a single flag setting for a user by key.

### Example
```csharp
using System;
using System.Diagnostics;
using LaunchDarkly.Api.Api;
using LaunchDarkly.Api.Client;
using LaunchDarkly.Api.Model;

namespace Example
{
    public class GetUserFlagSettingsExample
    {
        public void main()
        {
            
            // Configure API key authorization: Token
            Configuration.Default.ApiKey.Add("Authorization", "YOUR_API_KEY");
            // Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
            // Configuration.Default.ApiKeyPrefix.Add("Authorization", "Bearer");

            var apiInstance = new UserSettingsApi();
            var projectKey = projectKey_example;  // string | The project key, used to tie the flags together under one project so they can be managed together.
            var environmentKey = environmentKey_example;  // string | The environment key, used to tie together flag configuration and users under one environment so they can be managed together.
            var userKey = userKey_example;  // string | The user's key.

            try
            {
                // Fetch a single flag setting for a user by key.
                UserFlagSettings result = apiInstance.GetUserFlagSettings(projectKey, environmentKey, userKey);
                Debug.WriteLine(result);
            }
            catch (Exception e)
            {
                Debug.Print("Exception when calling UserSettingsApi.GetUserFlagSettings: " + e.Message );
            }
        }
    }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **projectKey** | **string**| The project key, used to tie the flags together under one project so they can be managed together. | 
 **environmentKey** | **string**| The environment key, used to tie together flag configuration and users under one environment so they can be managed together. | 
 **userKey** | **string**| The user&#39;s key. | 

### Return type

[**UserFlagSettings**](UserFlagSettings.md)

### Authorization

[Token](../README.md#Token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a name="patchexpiringusertargetsforflags"></a>
# **PatchExpiringUserTargetsForFlags**
> UserTargetingExpirationOnFlagsForUser PatchExpiringUserTargetsForFlags (string projectKey, string environmentKey, string userKey, PatchComment patchComment)

Update, add, or delete expiring user targets for a single user on all flags

### Example
```csharp
using System;
using System.Diagnostics;
using LaunchDarkly.Api.Api;
using LaunchDarkly.Api.Client;
using LaunchDarkly.Api.Model;

namespace Example
{
    public class PatchExpiringUserTargetsForFlagsExample
    {
        public void main()
        {
            
            // Configure API key authorization: Token
            Configuration.Default.ApiKey.Add("Authorization", "YOUR_API_KEY");
            // Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
            // Configuration.Default.ApiKeyPrefix.Add("Authorization", "Bearer");

            var apiInstance = new UserSettingsApi();
            var projectKey = projectKey_example;  // string | The project key, used to tie the flags together under one project so they can be managed together.
            var environmentKey = environmentKey_example;  // string | The environment key, used to tie together flag configuration and users under one environment so they can be managed together.
            var userKey = userKey_example;  // string | The user's key.
            var patchComment = new PatchComment(); // PatchComment | Requires a JSON Patch representation of the desired changes to the project, and an optional comment. 'http://jsonpatch.com/' Feature flag patches also support JSON Merge Patch format. 'https://tools.ietf.org/html/rfc7386' The addition of comments is also supported.

            try
            {
                // Update, add, or delete expiring user targets for a single user on all flags
                UserTargetingExpirationOnFlagsForUser result = apiInstance.PatchExpiringUserTargetsForFlags(projectKey, environmentKey, userKey, patchComment);
                Debug.WriteLine(result);
            }
            catch (Exception e)
            {
                Debug.Print("Exception when calling UserSettingsApi.PatchExpiringUserTargetsForFlags: " + e.Message );
            }
        }
    }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **projectKey** | **string**| The project key, used to tie the flags together under one project so they can be managed together. | 
 **environmentKey** | **string**| The environment key, used to tie together flag configuration and users under one environment so they can be managed together. | 
 **userKey** | **string**| The user&#39;s key. | 
 **patchComment** | [**PatchComment**](PatchComment.md)| Requires a JSON Patch representation of the desired changes to the project, and an optional comment. &#39;http://jsonpatch.com/&#39; Feature flag patches also support JSON Merge Patch format. &#39;https://tools.ietf.org/html/rfc7386&#39; The addition of comments is also supported. | 

### Return type

[**UserTargetingExpirationOnFlagsForUser**](UserTargetingExpirationOnFlagsForUser.md)

### Authorization

[Token](../README.md#Token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a name="putflagsetting"></a>
# **PutFlagSetting**
> void PutFlagSetting (string projectKey, string environmentKey, string userKey, string featureFlagKey, UserSettingsBody userSettingsBody)

Specifically enable or disable a feature flag for a user based on their key.

### Example
```csharp
using System;
using System.Diagnostics;
using LaunchDarkly.Api.Api;
using LaunchDarkly.Api.Client;
using LaunchDarkly.Api.Model;

namespace Example
{
    public class PutFlagSettingExample
    {
        public void main()
        {
            
            // Configure API key authorization: Token
            Configuration.Default.ApiKey.Add("Authorization", "YOUR_API_KEY");
            // Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
            // Configuration.Default.ApiKeyPrefix.Add("Authorization", "Bearer");

            var apiInstance = new UserSettingsApi();
            var projectKey = projectKey_example;  // string | The project key, used to tie the flags together under one project so they can be managed together.
            var environmentKey = environmentKey_example;  // string | The environment key, used to tie together flag configuration and users under one environment so they can be managed together.
            var userKey = userKey_example;  // string | The user's key.
            var featureFlagKey = featureFlagKey_example;  // string | The feature flag's key. The key identifies the flag in your code.
            var userSettingsBody = new UserSettingsBody(); // UserSettingsBody | 

            try
            {
                // Specifically enable or disable a feature flag for a user based on their key.
                apiInstance.PutFlagSetting(projectKey, environmentKey, userKey, featureFlagKey, userSettingsBody);
            }
            catch (Exception e)
            {
                Debug.Print("Exception when calling UserSettingsApi.PutFlagSetting: " + e.Message );
            }
        }
    }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **projectKey** | **string**| The project key, used to tie the flags together under one project so they can be managed together. | 
 **environmentKey** | **string**| The environment key, used to tie together flag configuration and users under one environment so they can be managed together. | 
 **userKey** | **string**| The user&#39;s key. | 
 **featureFlagKey** | **string**| The feature flag&#39;s key. The key identifies the flag in your code. | 
 **userSettingsBody** | [**UserSettingsBody**](UserSettingsBody.md)|  | 

### Return type

void (empty response body)

### Authorization

[Token](../README.md#Token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

