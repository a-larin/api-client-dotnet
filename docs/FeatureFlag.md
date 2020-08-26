# LaunchDarkly.Api.Model.FeatureFlag
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Key** | **string** |  | [optional] 
**Name** | **string** | Name of the feature flag. | [optional] 
**Description** | **string** | Description of the feature flag. | [optional] 
**Kind** | **string** | Whether the feature flag is a boolean flag or multivariate. | [optional] 
**CreationDate** | **long?** | A unix epoch time in milliseconds specifying the creation time of this flag. | [optional] 
**IncludeInSnippet** | **bool?** |  | [optional] 
**Temporary** | **bool?** | Whether or not this flag is temporary. | [optional] 
**MaintainerId** | **string** | The ID of the member that should maintain this flag. | [optional] 
**Tags** | **List&lt;string&gt;** | An array of tags for this feature flag. | [optional] 
**Variations** | [**List&lt;Variation&gt;**](Variation.md) | The variations for this feature flag. | [optional] 
**GoalIds** | **List&lt;string&gt;** | An array goals from all environments associated with this feature flag | [optional] 
**Version** | **int?** |  | [optional] 
**CustomProperties** | [**Dictionary&lt;string, CustomProperty&gt;**](CustomProperty.md) | A mapping of keys to CustomProperty entries. | [optional] 
**Links** | [**Links**](Links.md) |  | [optional] 
**Maintainer** | [**Member**](Member.md) |  | [optional] 
**Environments** | [**Dictionary&lt;string, FeatureFlagConfig&gt;**](FeatureFlagConfig.md) |  | [optional] 
**ArchivedDate** | **long?** | A unix epoch time in milliseconds specifying the archived time of this flag. | [optional] 
**Archived** | **bool?** | Whether or not this flag is archived. | [optional] 
**ClientSideAvailability** | [**ClientSideAvailability**](ClientSideAvailability.md) |  | [optional] 
**Defaults** | [**Defaults**](Defaults.md) |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

