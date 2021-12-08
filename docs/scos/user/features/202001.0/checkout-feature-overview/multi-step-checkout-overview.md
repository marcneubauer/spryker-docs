---
title: Multi-Step Checkout
description: The checkout is based on a flexible step engine and can be adjusted to any use case.
last_updated: Aug 13, 2020
template: concept-topic-template
originalLink: https://documentation.spryker.com/v4/docs/multi-step-checkout
originalArticleId: 2317299d-3cf9-4832-93d4-f1278ca68553
redirect_from:
  - /v4/docs/multi-step-checkout
  - /v4/docs/en/multi-step-checkout
  - /v4/docs/define-payment-shipment-methods
  - /v4/docs/en/define-payment-shipment-methods
---

The Checkout workflow is a multi-step process that can be fully customized to fit your needs. The standard steps include customer registration and login, shipping and billing address, shipment method and costs, payment method, checkout overview and checkout success. You can easily design the process to accommodate different checkout types and to adapt to different preferences, such as one-page checkout or an invoice page replacing the payment page, by means of our step-engine.

The checkout is based on a flexible step engine and can be adjusted to any use case:

* Highly customizable because of underlying step engine
* Checkout as guest, registered customer or register in the checkout flow
* Hooks for the integration of any payment or shipment methods
* Progress bar to navigate between checkout steps

<div class="mr-container">
    <div class="mr-list-container">
        <!-- col1 -->
        <div class="mr-col">
            <ul class="mr-list mr-list-green">
                <li class="mr-title">Developer</li>
                <li><a href="/docs/scos/dev/back-end-development/data-manipulation/datapayload-conversion/checkout/checkout-steps.html" class="mr-link">Get a general idea of the Checkout steps</a></li>
                <li><a href="/docs/scos/user/features/{{page.version}}/checkout-feature-overview/checkout-feature-overview.html" class="mr-link">Get a general idea of the Checkout process</a></li>  
                <li><a href="/docs/scos/dev/module-migration-guides/migration-guide-checkout.html#upgrading-from-version-4-to-version-600" class="mr-link">Migrate the Checkout module from version 4.* to version 6.0.0</a></li>
                <li><a href="/docs/scos/dev/module-migration-guides/migration-guide-checkoutpage.html" class="mr-link">Migrate the CheckoutPage module from version 2.* to version 3.*</a></li>
            </ul>
        </div>
        <!-- col3 -->
        <div class="mr-col">
            <ul class="mr-list mr-list-red">
                <li class="mr-title">Shop User</li>
                <li><a href="/docs/scos/dev/back-end-development/data-manipulation/datapayload-conversion/checkout/checkout-steps.html" class="mr-link">Get a general idea of the Checkout steps</a></li>
                <li><a href="/docs/scos/user/features/{{page.version}}/checkout-feature-overview/checkout-feature-overview.html" class="mr-link">Get a general idea of the Checkout process</a></li>
                <li><a href="/docs/scos/user/shop-user-guides/{{page.version}}/shop-guide-checkout/shop-guide-address-step.html" class="mr-link">Perform the Address Step</a></li>
                <li><a href="/docs/scos/user/shop-user-guides/{{page.version}}/shop-guide-checkout/shop-guide-shipment-step.html" class="mr-link">Perform the Shipment Step</a></li>
                <li><a href="payment-step-shop-guide-201911" class="mr-link">Perform the Payment Step</a></li>
                 <li><a href="/docs/scos/user/shop-user-guides/{{page.version}}/shop-guide-checkout/shop-guide-summary-step.html" class="mr-link">Perform the Summary Step</a></li>
            </ul>
        </div>
    </div>
</div>
