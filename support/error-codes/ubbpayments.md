# ubbPayments

{% hint style="info" %}
This module at the moment is only meant to be used by Parcel Kiosk to process purchases. Please contact support if your Parcel Kiosk is triggering ubbPayments errors for help.
{% endhint %}

{% hint style="info" %}
Error codes are returned by every ubbPayments function as `StatusCode`.
{% endhint %}

| Error code            | What it means                                                               | Solution                                                                       |
| --------------------- | --------------------------------------------------------------------------- | ------------------------------------------------------------------------------ |
| invalid\_argument     | Incorrect arguments are being passed to a function.                         | Ensure you call functions with valid parameters.                               |
| purchase\_ongoing     | The Player is currently paying for something else.                          | Wait until the player is done with their current purchase using WaitForPlayer. |
| unallowed\_infotype   | An unallowed EnumItem is being passed to argument #3.                       | Ensure argument #3 is `Enum.InfoType.Product` or `Enum.InfoType.GamePass`.     |
| getproductinfo\_error | MarketplaceService failed to fetch a product's information after 3 retries. | Contact support.                                                               |
| payment\_cancelled    | The Player cancelled the payment.                                           | N/A                                                                            |

