---
title: Managing wishlist items
description: Add and delete items from wishlists via Glue API.
last_updated: Jun 16, 2021
template: glue-api-storefront-guide-template
originalLink: https://documentation.spryker.com/2021080/docs/managing-wishlist-items
originalArticleId: 2ce23129-3ad7-4053-9e9d-8f5bf697aa87
redirect_from:
  - /2021080/docs/managing-wishlist-items
  - /2021080/docs/en/managing-wishlist-items
  - /docs/managing-wishlist-items
  - /docs/en/managing-wishlist-items
related:
  - title: Managing wishlists
    link: docs/scos/dev/glue-api-guides/page.version/managing-wishlists/managing-wishlists.html
  - title: Authenticating as a customer
    link: docs/scos/dev/glue-api-guides/page.version/managing-customers/authenticating-as-a-customer.html
---

This endpoint allows to add and remove items from wishlists.

## Installation

For detailed information on the modules that provide the API functionality and related installation instructions, see [Wishlist API Feature Integration](/docs/scos/dev/feature-integration-guides/{{page.version}}/glue-api/glue-api-wishlist-feature-integration.html).

## Add an item to a wishlist

To add an item to a wishlist, send the request:

---
`POST` **/wishlists/*{% raw %}{{{% endraw %}wishlist_id{% raw %}}}{% endraw %}*/wishlist-items**

---

| PATH PARAMETER | DESCRIPTION |
| --- | --- |
| ***{% raw %}{{{% endraw %}wishlist_id{% raw %}}}{% endraw %}*** | Unique identifier of the wishlist to add the items to. [Create a wishlist](/docs/scos/dev/glue-api-guides/{{page.version}}/managing-wishlists/managing-wishlists.html#create-a-wishlist) or [retrieve all wishlists](/docs/scos/dev/glue-api-guides/{{page.version}}/managing-wishlists/managing-wishlists.html#retrieve-wishlists) to get it. |

### Request

Request sample: `POST https://glue.mysprykershop.com/wishlists/09264b7f-1894-58ed-81f4-d52d683e910a/wishlist-items`

```json
{
		"data": {
			"type": "wishlist-items",
			"attributes": {
				"sku": "064_18404924"
			}
		}
	}
```

| ATTRIBUTE | TYPE | DESCRIPTION |
| --- | --- | --- |
| sku | String | SKU of a concrete product to add. |

### Response

```json
{
		"data": {
			"type": "wishlist-items",
			"id": "064_18404924",
			"attributes": {
				"sku": "064_18404924"
			},
			"links": {
				"self": "https://glue.mysprykershop.com/wishlists/c917e65b-e8c3-5c8b-bec6-892529c64b30/wishlist-items/064_18404924"
			}
		}
	}
```

<a name="wishlishlist-items-response-attributes"></a>

| ATTRIBUTE | TYPE | DESCRIPTION |
| --- | --- | --- |
| sku | String | SKU of the concrete product in the wishlist. |

## Delete a wishlist item

To delete wishlist item, send the request:

---
`DELETE` **/wishlists/*{% raw %}{{{% endraw %}wishlist_id{% raw %}}}{% endraw %}*/wishlist-items/*{% raw %}{{{% endraw %}item_sku{% raw %}}}{% endraw %}***

---

| PATH PARAMETER | DESCRIPTION |
| --- | --- |
| ***{% raw %}{{{% endraw %}wishlist_id{% raw %}}}{% endraw %}*** | Unique identifier of the wishlist to delete an item from. [Create a wishlist](/docs/scos/dev/glue-api-guides/{{page.version}}/managing-wishlists/managing-wishlists.html#create-a-wishlist) or [retrieve all wishlists](/docs/scos/dev/glue-api-guides/{{page.version}}/managing-wishlists/managing-wishlists.html#retrieve-wishlists) to get it. |
| ***{% raw %}{{{% endraw %}item_sku{% raw %}}}{% endraw %}*** | Unique identifier of the product to delete. |

### Request

Request sample: `DELETE https://glue.mysprykershop.com/wishlists/09264b7f-1894-58ed-81f4-d52d683e910a/wishlist-items/064_18404924`

### Response

If the item is removed successfully, the endpoint returns the `204 No Content` status code.

## Possible errors

| CODE | REASON |
| --- | --- |
| 201 | Cannot find the wishlist. |
| 206 | Cannot add an item to the wishlist. |
| 207 | Cannot remove the item. |
| 208 | An item with the provided SKU does not exist in the wishlist. |

To view generic errors that originate from the Glue Application, see [Reference information: GlueApplication errors](/docs/scos/dev/glue-api-guides/{{page.version}}/reference-information-glueapplication-errors.html).
