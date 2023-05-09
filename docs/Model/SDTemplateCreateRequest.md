# # SDTemplateCreateRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **string** | The name of the template (ex. Bronze Axe) |
**cap** | **string** | u96 Number as String (ex. 200000000) |
**contract_type** | **string** | The type of custom contract to use for this template. Default will use a shared contract. | [optional]
**type** | **string** | FT is a currency where every instance is the same, NFT is where every token instance differes (ex. FT) |
**owner_address** | **string** | Blockchain address to set as owner of the custom contract. Required if contractType is set. | [optional]
**props** | [**\Stardust\Core\Stardust\Core\Model\SDTemplateCreateRequestProps**](SDTemplateCreateRequestProps.md) |  |
**public_contract_metadata** | **object** | Returned to marketplaces as contract metadata | [optional]
**symbol** | **string** | For ERC20 contracts, this is the ticker symbol | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
