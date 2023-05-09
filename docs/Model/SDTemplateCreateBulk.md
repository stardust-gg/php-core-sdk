# # SDTemplateCreateBulk

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **string** | The name of the template (ex. Bronze Axe) |
**cap** | **string** | u96 Number as String (ex. 200000000), default 39614081257132168796771975168 | [optional]
**contract_type** | **string** | The type of custom contract to use for this template. Default will use a shared contract. | [optional]
**type** | **string** | FT is a currency where every instance is the same, NFT is where every token instance differes (ex. FT) | [optional]
**image** | **string** | image url |
**description** | **string** | Description of template | [optional]
**active_listing** | **bool** | Set if the Template is active or not | [optional]
**owner_address** | **string** | Blockchain address to set as owner of the custom contract, if contractType is passed in. | [optional]
**props** | [**\Stardust\Core\Stardust\Core\Model\SDTemplateCreateBulkProps**](SDTemplateCreateBulkProps.md) |  | [optional]
**public_contract_metadata** | **object** | Returned to marketplaces as contract metadata | [optional]
**public_token_metadata** | **object** | Inherited by tokens, and returned to marketplaces as token metadata | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
