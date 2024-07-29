# Integration Constructor

## Constructor:Rename(Name)

<mark style="color:red;">`INACTIVE AFTER FINALIZATION`</mark>

Renames the integration.

#### Arguments

| Arguments | Type   | Description                 |
| --------- | ------ | --------------------------- |
| Name      | string | The integration's new name. |

#### Response

N/A



## Constructor.newFunction(Name, Function)

<mark style="color:red;">`INACTIVE AFTER FINALIZATION`</mark>

Creates a new function in the integration.

#### Arguments

| Arguments | Type     | Description                |
| --------- | -------- | -------------------------- |
| Name      | string   | The function's name.       |
| Function  | function | The function to be called. |

#### Response

N/A



## Constructor:Finalize()

<mark style="color:red;">`INACTIVE AFTER FINALIZATION`</mark>

Finalizes the integration.

#### Arguments

N/A

#### Response

N/A



## Constructor:GetIntegration()

<mark style="color:orange;">`FOR SYSTEM USE`</mark>

Returns the integration's Frame for the system to install.

#### Arguments

N/A

#### Response

{% tabs %}
{% tab title="Normal" %}
Frame (Instance)
{% endtab %}
{% endtabs %}
