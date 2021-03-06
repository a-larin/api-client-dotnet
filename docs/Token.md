# LaunchDarkly.Api.Model.Token
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Links** | [**Links**](Links.md) |  | [optional] 
**Id** | **string** | The unique resource id. | [optional] 
**OwnerId** | **string** | The unique resource id. | [optional] 
**MemberId** | **string** | The unique resource id. | [optional] 
**Member** | [**Member**](Member.md) |  | [optional] 
**CreationDate** | **long?** | A unix epoch time in milliseconds specifying the creation time of this access token. | [optional] 
**LastModified** | **long?** | A unix epoch time in milliseconds specifying the last time this access token was modified. | [optional] 
**LastUsed** | **long?** | A unix epoch time in milliseconds specifying the last time this access token was used to authorize access to the LaunchDarkly REST API. | [optional] 
**_Token** | **string** | The last 4 digits of the unique secret key for this access token. If creating or resetting the token, this will be the full token secret. | [optional] 
**Name** | **string** | A human-friendly name for the access token | [optional] 
**Role** | **string** | The name of a built-in role for the token | [optional] 
**CustomRoleIds** | **List&lt;string&gt;** | A list of custom role IDs to use as access limits for the access token | [optional] 
**InlineRole** | [**List&lt;Statement&gt;**](Statement.md) |  | [optional] 
**ServiceToken** | **bool?** | Whether the token will be a service token https://docs.launchdarkly.com/home/account-security/api-access-tokens#service-tokens | [optional] 
**DefaultApiVersion** | **int?** | The default API version for this token | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

