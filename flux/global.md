# Global Integrations

## Installing global integrations

1. First, open the Config and locate the GlobalIntegrations table.

```lua
Config.GlobalIntegrations = {
	DWProxGlobalAPI = {true},
	floGates = {false, "pathToAPIHere"}
}
```

2. Check if the global integration's short name is in the table. If not, add the line of code below to the table. Replace IntegrationShortName with the global integration's short name. If you do not want the global integration, replace "true" with "false".

```lua
IntegrationShortName = {true}
```

3. If your global integration requires additional arguments, add them to the table like shown below.

```lua
IntegrationShortName = {true, "arg1", "arg2", "arg3"}
```

## Global Integrations List



{% tabs %}
{% tab title="DWProx Global API" %}
Short Name: DWProxGlobalAPI\
Description: Simple integration powered by the DWProx Global API.\
Additional Arguments (in order): N/A
{% endtab %}

{% tab title="flo Gates" %}
Short Name: floGates\
Description: Simple integration powered by the flo Gate API.\
Additional Arguments (in order):

* Path to flo Gate API (Network)
{% endtab %}
{% endtabs %}
