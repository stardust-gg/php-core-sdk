# Stardust

No description provided (generated by Openapi Generator https://github.com/openapitools/openapi-generator)


## Installation & Usage

### Requirements

PHP 7.4 and later.
Should also work with PHP 8.0.

### Composer

To install the bindings via [Composer](https://getcomposer.org/), add the following to `composer.json`:

```json
{
  "repositories": [
    {
      "type": "vcs",
      "url": "https://github.com/stardust-gg/php-core-sdk.git"
    }
  ],
  "require": {
    "stardust-gg/php-core-sdk": "*@dev"
  }
}
```

Then run `composer install`

### Manual Installation

Download the files and include `autoload.php`:

```php
<?php
require_once('/path/to/Stardust/vendor/autoload.php');
```

## Getting Started

Please follow the [installation procedure](#installation--usage) and then run the following:

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



// Configure API key authorization: api_key
$config = Stardust\Core\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Stardust\Core\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');


$apiInstance = new Stardust\Core\Api\GameEndpointsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->gameGetGet();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GameEndpointsApi->gameGetGet: ', $e->getMessage(), PHP_EOL;
}

```

## API Endpoints

All URIs are relative to *https://core-api.stardust.gg/v1*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*GameEndpointsApi* | [**gameGetGet**](docs/Api/GameEndpointsApi.md#gamegetget) | **GET** /game/get | Get Game
*GameEndpointsApi* | [**gameMutatePut**](docs/Api/GameEndpointsApi.md#gamemutateput) | **PUT** /game/mutate | Mutate Game
*HealthEndpointsApi* | [**healthGet**](docs/Api/HealthEndpointsApi.md#healthget) | **GET** /health | Get Health
*OrderEndpointsApi* | [**orderBuyPost**](docs/Api/OrderEndpointsApi.md#orderbuypost) | **POST** /order/buy | Buy Order
*OrderEndpointsApi* | [**orderCancelDelete**](docs/Api/OrderEndpointsApi.md#ordercanceldelete) | **DELETE** /order/cancel | Cancel Order
*OrderEndpointsApi* | [**orderCreatePost**](docs/Api/OrderEndpointsApi.md#ordercreatepost) | **POST** /order/create | Create Order
*OrderEndpointsApi* | [**orderGetAllGet**](docs/Api/OrderEndpointsApi.md#ordergetallget) | **GET** /order/get-all | Get All Orders
*OrderEndpointsApi* | [**orderGetGet**](docs/Api/OrderEndpointsApi.md#ordergetget) | **GET** /order/get | Get Order
*PlayerEndpointsApi* | [**playerCountGet**](docs/Api/PlayerEndpointsApi.md#playercountget) | **GET** /player/count | Get Player Count
*PlayerEndpointsApi* | [**playerCreatePost**](docs/Api/PlayerEndpointsApi.md#playercreatepost) | **POST** /player/create | Create Player
*PlayerEndpointsApi* | [**playerGetAllGet**](docs/Api/PlayerEndpointsApi.md#playergetallget) | **GET** /player/get-all | Get All Players
*PlayerEndpointsApi* | [**playerGetGet**](docs/Api/PlayerEndpointsApi.md#playergetget) | **GET** /player/get | Get Player
*PlayerEndpointsApi* | [**playerGetIdGet**](docs/Api/PlayerEndpointsApi.md#playergetidget) | **GET** /player/get-id | Get Player ID
*PlayerEndpointsApi* | [**playerGetIdsGet**](docs/Api/PlayerEndpointsApi.md#playergetidsget) | **GET** /player/get-ids | Get All Player IDs
*PlayerEndpointsApi* | [**playerGetInventoryGet**](docs/Api/PlayerEndpointsApi.md#playergetinventoryget) | **GET** /player/get-inventory | Get Player Inventory
*PlayerEndpointsApi* | [**playerMutatePut**](docs/Api/PlayerEndpointsApi.md#playermutateput) | **PUT** /player/mutate | Mutate Player
*PlayerEndpointsApi* | [**playerRemoveDelete**](docs/Api/PlayerEndpointsApi.md#playerremovedelete) | **DELETE** /player/remove | Remove Player
*PlayerEndpointsApi* | [**playerWalletGetGet**](docs/Api/PlayerEndpointsApi.md#playerwalletgetget) | **GET** /player/wallet-get | Get Player Wallet
*PlayerEndpointsApi* | [**playerWithdrawPost**](docs/Api/PlayerEndpointsApi.md#playerwithdrawpost) | **POST** /player/withdraw | Withdraw From Player
*TemplateEndpointsApi* | [**templateCountGet**](docs/Api/TemplateEndpointsApi.md#templatecountget) | **GET** /template/count | Get Template Count
*TemplateEndpointsApi* | [**templateCreatePost**](docs/Api/TemplateEndpointsApi.md#templatecreatepost) | **POST** /template/create | Create Template
*TemplateEndpointsApi* | [**templateGetAllGet**](docs/Api/TemplateEndpointsApi.md#templategetallget) | **GET** /template/get-all | Get All Templates
*TemplateEndpointsApi* | [**templateGetGet**](docs/Api/TemplateEndpointsApi.md#templategetget) | **GET** /template/get | Get Template
*TemplateEndpointsApi* | [**templateGetTokensGet**](docs/Api/TemplateEndpointsApi.md#templategettokensget) | **GET** /template/get-tokens | Get Template Tokens
*TemplateEndpointsApi* | [**templateMutatePut**](docs/Api/TemplateEndpointsApi.md#templatemutateput) | **PUT** /template/mutate | Mutate Template
*TemplateEndpointsApi* | [**templatePropsRemoveDelete**](docs/Api/TemplateEndpointsApi.md#templatepropsremovedelete) | **DELETE** /template/props-remove | Remove Template Property
*TemplateEndpointsApi* | [**templateRemoveDelete**](docs/Api/TemplateEndpointsApi.md#templateremovedelete) | **DELETE** /template/remove | Remove Template
*TokenEndpointsApi* | [**tokenBurnPost**](docs/Api/TokenEndpointsApi.md#tokenburnpost) | **POST** /token/burn | Burn Token
*TokenEndpointsApi* | [**tokenGetGet**](docs/Api/TokenEndpointsApi.md#tokengetget) | **GET** /token/get | Get Token
*TokenEndpointsApi* | [**tokenMintBulkPost**](docs/Api/TokenEndpointsApi.md#tokenmintbulkpost) | **POST** /token/mint-bulk | Mint Tokens
*TokenEndpointsApi* | [**tokenMutatePut**](docs/Api/TokenEndpointsApi.md#tokenmutateput) | **PUT** /token/mutate | Mutate Token
*TokenEndpointsApi* | [**tokenPropsRemoveDelete**](docs/Api/TokenEndpointsApi.md#tokenpropsremovedelete) | **DELETE** /token/props-remove | Remove Token Property
*TokenEndpointsApi* | [**tokenTransferPost**](docs/Api/TokenEndpointsApi.md#tokentransferpost) | **POST** /token/transfer | Transfer Tokens
*TokenEndpointsApi* | [**tokenWithdrawPost**](docs/Api/TokenEndpointsApi.md#tokenwithdrawpost) | **POST** /token/withdraw | Withdraw Token

## Models

- [Error](docs/Model/Error.md)
- [SDGameGetResponse](docs/Model/SDGameGetResponse.md)
- [SDGameGetResponseFeesInner](docs/Model/SDGameGetResponseFeesInner.md)
- [SDGameMutateRequest](docs/Model/SDGameMutateRequest.md)
- [SDHealthResponse](docs/Model/SDHealthResponse.md)
- [SDOrderBuyRequest](docs/Model/SDOrderBuyRequest.md)
- [SDOrderCancelRequest](docs/Model/SDOrderCancelRequest.md)
- [SDOrderCancelResponse](docs/Model/SDOrderCancelResponse.md)
- [SDOrderCreateRequest](docs/Model/SDOrderCreateRequest.md)
- [SDOrderCreateResponse](docs/Model/SDOrderCreateResponse.md)
- [SDOrderCreateTokens](docs/Model/SDOrderCreateTokens.md)
- [SDOrderGetAllResponse](docs/Model/SDOrderGetAllResponse.md)
- [SDOrderGetAllResponseTokensRequestedInner](docs/Model/SDOrderGetAllResponseTokensRequestedInner.md)
- [SDOrderGetResponse](docs/Model/SDOrderGetResponse.md)
- [SDPlayerCountResponse](docs/Model/SDPlayerCountResponse.md)
- [SDPlayerCreateJWTObject](docs/Model/SDPlayerCreateJWTObject.md)
- [SDPlayerCreateRequest](docs/Model/SDPlayerCreateRequest.md)
- [SDPlayerCreateResponse](docs/Model/SDPlayerCreateResponse.md)
- [SDPlayerGetAllResponse](docs/Model/SDPlayerGetAllResponse.md)
- [SDPlayerGetIdResponse](docs/Model/SDPlayerGetIdResponse.md)
- [SDPlayerGetIdsResponse](docs/Model/SDPlayerGetIdsResponse.md)
- [SDPlayerGetInventoryResponse](docs/Model/SDPlayerGetInventoryResponse.md)
- [SDPlayerGetResponse](docs/Model/SDPlayerGetResponse.md)
- [SDPlayerMutateRequest](docs/Model/SDPlayerMutateRequest.md)
- [SDPlayerWalletGetResponse](docs/Model/SDPlayerWalletGetResponse.md)
- [SDPlayerWalletGetResponseWalletInner](docs/Model/SDPlayerWalletGetResponseWalletInner.md)
- [SDPlayerWalletGetResponseWalletInnerMoniesInner](docs/Model/SDPlayerWalletGetResponseWalletInnerMoniesInner.md)
- [SDPlayerWithdrawObject](docs/Model/SDPlayerWithdrawObject.md)
- [SDPlayerWithdrawRequest](docs/Model/SDPlayerWithdrawRequest.md)
- [SDTemplateCountResponse](docs/Model/SDTemplateCountResponse.md)
- [SDTemplateCreateBulk](docs/Model/SDTemplateCreateBulk.md)
- [SDTemplateCreateBulkProps](docs/Model/SDTemplateCreateBulkProps.md)
- [SDTemplateCreateRequest](docs/Model/SDTemplateCreateRequest.md)
- [SDTemplateCreateRequestProps](docs/Model/SDTemplateCreateRequestProps.md)
- [SDTemplateCreateResponse](docs/Model/SDTemplateCreateResponse.md)
- [SDTemplateGetAllResponse](docs/Model/SDTemplateGetAllResponse.md)
- [SDTemplateGetAllResponseProps](docs/Model/SDTemplateGetAllResponseProps.md)
- [SDTemplateGetResponse](docs/Model/SDTemplateGetResponse.md)
- [SDTemplateGetTokensResponse](docs/Model/SDTemplateGetTokensResponse.md)
- [SDTemplateGetTokensResponsePlayer](docs/Model/SDTemplateGetTokensResponsePlayer.md)
- [SDTemplateGetTokensResponseToken](docs/Model/SDTemplateGetTokensResponseToken.md)
- [SDTemplateGetTokensResponseTokenProps](docs/Model/SDTemplateGetTokensResponseTokenProps.md)
- [SDTemplateMutateRequest](docs/Model/SDTemplateMutateRequest.md)
- [SDTokenBurnRequest](docs/Model/SDTokenBurnRequest.md)
- [SDTokenBurnRequestTokenObjectsInner](docs/Model/SDTokenBurnRequestTokenObjectsInner.md)
- [SDTokenGetResponse](docs/Model/SDTokenGetResponse.md)
- [SDTokenMintBulkRequest](docs/Model/SDTokenMintBulkRequest.md)
- [SDTokenMintBulkTokenObject](docs/Model/SDTokenMintBulkTokenObject.md)
- [SDTokenMintBulkTokenObjectProps](docs/Model/SDTokenMintBulkTokenObjectProps.md)
- [SDTokenMutateRequest](docs/Model/SDTokenMutateRequest.md)
- [SDTokenTransferRequest](docs/Model/SDTokenTransferRequest.md)
- [SDTokenWithdrawObject](docs/Model/SDTokenWithdrawObject.md)
- [SDTokenWithdrawRequest](docs/Model/SDTokenWithdrawRequest.md)

## Authorization

### api_key

- **Type**: API key
- **API key parameter name**: x-api-key
- **Location**: HTTP header


## Tests

To run the tests, use:

```bash
composer install
vendor/bin/phpunit
```

## Author



## About this package

This PHP package is automatically generated by the [OpenAPI Generator](https://openapi-generator.tech) project:

- API version: `2023-05-08T04:33:59Z`
    - Package version: `0.0.3`
- Build package: `org.openapitools.codegen.languages.PhpClientCodegen`
