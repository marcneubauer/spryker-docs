---
title: Adyen - Filtering Payment Methods
description: Enable filtering available payment methods depending on the result of /paymentMethods API call in the Spryker Commerce OS.
last_updated: May 14, 2020
template: concept-topic-template
originalLink: https://documentation.spryker.com/v5/docs/adyen-filter-payment-methods
originalArticleId: 49464b8f-9788-4edf-a44c-992245d22862
redirect_from:
  - /v5/docs/adyen-filter-payment-methods
  - /v5/docs/en/adyen-filter-payment-methods
related:
  - title: Payment Integration - Adyen
    link: docs/scos/user/technology-partners/page.version/payment-partners/adyen/adyen.html
  - title: Adyen - Integration
    link: docs/scos/user/technology-partners/page.version/payment-partners/adyen/adyen-integration-into-a-project.html
  - title: Adyen - Installation and Configuration
    link: docs/scos/user/technology-partners/page.version/payment-partners/adyen/adyen-installation-and-configuration.html
  - title: Adyen - Provided Payment Methods
    link: docs/scos/user/technology-partners/page.version/payment-partners/adyen/adyen-provided-payment-methods.html
---

Adyen module provides filtering available payment methods depend on result of `/paymentMethods` API call.

To enable this add `\SprykerEco\Zed\Adyen\Communication\Plugin\AdyenPaymentMethodFilterPlugin` to filter plugins list in `src/Pyz/Zed/Payment/PaymentDependencyProvider.php`:

```php
<?php

/**
 * This file is part of the Spryker Suite.
 * For full license information, please view the LICENSE file that was distributed with this source code.
 */

namespace Pyz\Zed\Payment;

...
use SprykerEco\Zed\Adyen\Communication\Plugin\AdyenPaymentMethodFilterPlugin;

class PaymentDependencyProvider extends SprykerPaymentDependencyProvider
{
    /**
     * @return \Spryker\Zed\Payment\Dependency\Plugin\Payment\PaymentMethodFilterPluginInterface[]
     */
    protected function getPaymentMethodFilterPlugins()
    {
        return [
            ...
            new AdyenPaymentMethodFilterPlugin('toggler-radio'),
        ];
    }
}
 ```

