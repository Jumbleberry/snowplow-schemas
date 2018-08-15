# Jumbleberry Tracking Events

Jumbleberry tracking events are based on [Facebook Custom Audience pixels](https://developers.facebook.com/docs/ads-for-websites/pixel-events/v3.0)

## Events

| Event Name | Event Description | Parameters | 
| --- | --- | --- |
| `engagement` | When a key page is viewed prior to lead generation (ie. Bridge Page) | `c1`,<br/> `c2`,<br/> `c3` |
| `view_content` | When a key page is viewed such as a product page, e.g. landing on a product detail page | `value`,<br/> `currency`,<br/> `content_name`,<br/> `content_type`,<br/> `content_ids`,<br/> `contents` |
`add_to_cart` | When a product is added to the shopping cart, e.g. click on add to cart button | `value`,<br/> `currency`,<br/> `content_name`,<br/> `content_type`,<br/> `content_ids`,<br/> `contents` |
`remove_from_cart` | When a product is removed from the shopping cart, e.g. click on add to cart button | `value`,<br/> `currency`,<br/> `content_name`,<br/> `content_type`,<br/> `content_ids`,<br/> `contents` |
`initiate_checkout` | When a person enters the checkout flow prior to completing the checkout flow, e.g. click on checkout button | `value`,<br/> `currency`,<br/> `content_name`,<br/> `content_type`,<br/> `content_ids`,<br/> `contents`,<br/> `num_items` |
`add_payment_info` | When a payment information is added in the checkout flow, e.g. click / LP on save billing info button | `value`,<br/> `currency`,<br/> `content_category`,<br/> `content_ids`,<br/> `contents` |
`purchase` | When a purchase is made or checkout flow is completed, e.g. landing on thank you/confirmation page | `value`,<br/> `currency`,<br/> `content_name`,<br/> `content_type`,<br/> `content_ids`,<br/> `contents`,<br/> `num_items`,<br/> `transaction_id` |
`upsell` | When a secondary purchase is made (not credited back to Jumbleberry) | `value`,<br/> `currency`,<br/> `content_name`,<br/> `content_type`,<br/> `content_ids`,<br/> `contents`,<br/> `num_items`,<br/> `transaction_id` |
`lead` | When a user has shown interest in the product (ie. Post click) | `value`,<br/> `currency`,<br/> `content_name`,<br/> `content_category` |
`complete_registration` | When a registration form is completed, e.g. complete subscription/signup for a service | `value`,<br/> `currency`,<br/> `content_name`,<br/> `status` |
`decline` | When a transaction is declined | `value`,<br/> `currency`,<br/> `reason`,<br/> `transaction_id`  |
`chargeback` | When a transaction is charged back | `value`,<br/> `currency`,<br/> `reason`,<br/> `transaction_id`  |


## Parameters

| Parameter Name | Parameter Description | 
| --- | --- |
`value` | value of a user performing this event to the business |
`currency` | currency for the `value` specified |
`content_name` | Name of the page/product |
`content_category` | Category of the page/product |
`content_ids` | Product ids associated with the event. e.g. SKUs of products  for AddToCart event: ['ABC123', 'XYZ789 |
`contents` | A list of JSON object that contains the International Article Number (EAN) when applicable, or other product or content identifier(s) associated with the event as well as quantities and prices of the products. `id`, `quantity`, and `item_price` are the required fields. e.g. [{'id': 'ABC123', 'quantity': 2, 'item_price': 5.99}, {'id': 'XYZ789', 'quantity': 2, 'item_price': 9.99}]. Note that `item_price` is the price of a single item, not cumulative price |
`content_type` | Either 'product' or 'product_group' based on the `content_ids` or `contents` being passed. If the ids being passed in `content_ids` or `contents` parameter are ids of products then the value should be 'product'. If product group ids are being passed, then the value should be 'product_group |
`num_items` | Used with `initiate_checkout` event. The number of items that checkout was initiated for |
`status` | Used with the `complete_registration` event, to show the status of the registration |
`reason` | Reaons for `decline`, `chargeback` etc. |
`transaction_id` | A identifier for uniquely identifying a specific transaction attempt |
`c1` | Publisher sub id #1 |
`c2` | Publisher sub id #2 |
`c3` | Publisher sub id #3 |
