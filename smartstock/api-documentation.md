# API Documentation

## API Information

**Type:** BindableFunction\
**Location:** Child of Engine script\
**Execution method:**

```lua
API:Invoke("CommandName", ...) -- additional arguments can be added
```



## API Commands

### AreProductsRegistered

Returns a `boolean` if all products have been successfully registered by the system.

### FindProductUPIFromName

<mark style="color:red;">`RETURNS NIL IF PRODUCTS NOT REGISTERED`</mark>

Returns the product's Unique Product Identifier (UPI) as a `number`.\
Product's name required as first argument.

### GetProductInfo

<mark style="color:red;">`RETURNS NIL IF PRODUCTS NOT REGISTERED`</mark>

Returns a `Table` with stock information about a product.\
Product's Unique Product Identifier (UPI) required as first argument.

Response:

{% tabs %}
{% tab title="Name" %}
`string`
{% endtab %}

{% tab title="UniqueProductIdentifier" %}
`number`
{% endtab %}

{% tab title="MaxStock" %}
`number`
{% endtab %}

{% tab title="RemainingStock" %}
`number`
{% endtab %}
{% endtabs %}

### GetProducts

<mark style="color:red;">`RETURNS NIL IF PRODUCTS NOT REGISTERED`</mark>

Returns a `Dictionary` with stock information for all products registered in the system.\
Refer to [#getproductinfo](api-documentation.md#getproductinfo "mention") for response.

### Restock

<mark style="color:red;">`RETURNS NIL IF PRODUCTS NOT REGISTERED`</mark>

Restocks a product.\
Product's folder required as first argument. An `Player` can optionally be as the second argument if restocker whitelist is enabled.
