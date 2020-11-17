# OpenAPI\Client\BillingApi

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**autoCharge**](BillingApi.md#autoCharge) | **POST** /{org_key}/auto_charge/ | Auto charge a credit card
[**creditCharge**](BillingApi.md#creditCharge) | **POST** /{org_key}/credit_charge/ | Charge a credit card
[**getCreditCardDetails**](BillingApi.md#getCreditCardDetails) | **GET** /{org_key}/credit_card_details/ | Get credit card details



## autoCharge

> autoCharge($org_key, $auto_charge_request)

Auto charge a credit card

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


$apiInstance = new OpenAPI\Client\Api\BillingApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$org_key = 'org_key_example'; // string | 
$auto_charge_request = new \OpenAPI\Client\Model\AutoChargeRequest(); // \OpenAPI\Client\Model\AutoChargeRequest | 

try {
    $apiInstance->autoCharge($org_key, $auto_charge_request);
} catch (Exception $e) {
    echo 'Exception when calling BillingApi->autoCharge: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_key** | **string**|  |
 **auto_charge_request** | [**\OpenAPI\Client\Model\AutoChargeRequest**](../Model/AutoChargeRequest.md)|  |

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../../README.md#documentation-for-models)
[[Back to README]](../../README.md)


## creditCharge

> creditCharge($org_key, $credit_charge_request)

Charge a credit card

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


$apiInstance = new OpenAPI\Client\Api\BillingApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$org_key = 'org_key_example'; // string | 
$credit_charge_request = new \OpenAPI\Client\Model\CreditChargeRequest(); // \OpenAPI\Client\Model\CreditChargeRequest | 

try {
    $apiInstance->creditCharge($org_key, $credit_charge_request);
} catch (Exception $e) {
    echo 'Exception when calling BillingApi->creditCharge: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_key** | **string**|  |
 **credit_charge_request** | [**\OpenAPI\Client\Model\CreditChargeRequest**](../Model/CreditChargeRequest.md)|  |

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../../README.md#documentation-for-models)
[[Back to README]](../../README.md)


## getCreditCardDetails

> \OpenAPI\Client\Model\CreditCardDetailsResponse getCreditCardDetails($org_key, $is_test)

Get credit card details

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


$apiInstance = new OpenAPI\Client\Api\BillingApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$org_key = 'org_key_example'; // string | 
$is_test = false; // bool | 

try {
    $result = $apiInstance->getCreditCardDetails($org_key, $is_test);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BillingApi->getCreditCardDetails: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_key** | **string**|  |
 **is_test** | **bool**|  | [optional] [default to false]

### Return type

[**\OpenAPI\Client\Model\CreditCardDetailsResponse**](../Model/CreditCardDetailsResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../../README.md#documentation-for-models)
[[Back to README]](../../README.md)

