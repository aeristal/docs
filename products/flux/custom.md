# Custom Integrations

## Getting the integrations module

First, you will need to get the module which will "give" your integration for the system to install. You can find the Template Integration in the "Custom Integrations" folder.

<figure><img src="../../.gitbook/assets/image (20).png" alt=""><figcaption></figcaption></figure>

## Constructing your integration

{% hint style="info" %}
This section requires basic developer knowledge.
{% endhint %}

Now, before "giving" your integration for the system to install, you obviously can't give nothing! Let's get started with constructing the integration and creating it's functions.

1. First, rename the TemplateIntegration module. Keep in mind that the module's name will be the integration's short code.
2. Next, locate the "Construct" script inside of the integration module.\


<figure><img src="../../.gitbook/assets/image (22).png" alt=""><figcaption></figcaption></figure>

3. Open the script and take a look inside. You can see that an example integration has already been made for you. Delete everything in the script as we will be teaching you step-by-step on how to construct your integration!
4. For the first line, you need to require the Flux Integration Constructor module. So add the line of code below.

```lua
local constructor = require(script.Parent.FluxIntegrationConstructor)
```

5. Now at Line 3, add this line of code. What this will do is rename your integration which is currently by default called "Unnamed Integration". Replace "Test Integration" with the name of your choice, this doesn't affect anything and is the name of your integration which is shown to the user.

```lua
constructor:Rename("Test Integration")
```

6. At Line 5, add this line of code. We're now creating the first function of your integration.\
   In the first argument which is the apostrophes, enter the name of your function in it. For example, it could be "Open Gates" or "Turn Lights On".\
   In the second argument which is the function, enter the code you want to execute when the function is used.

```lua
constructor.newFunction(
	'',
	function()
		
	end
)
```

7. You have just made your first function! You can repeat Step 6 in a new line to create more functions.
8. Lastly when you're done creating all your functions, add this line of code at the end. The system will wait until your integration has been finalized before installing it so that it doesn't install too quickly.

```lua
constructor:Finalize()
```

That's it! You have just made the script to construct your integration.

## On Installation

The Integration module has already been coded for you for the system to install the integration. Optionally, you can enter your own code as annotated.

```lua
function Integration:GetIntegration()
	local constructor = require(script.FluxIntegrationConstructor)
	
	--// Enter your own code here
	
	return constructor:GetIntegration()
end
```

Note that this function should always return what "constructor:GetIntegration()" will return, basically passing it on.

If you do not want to let the system install the integration maybe because something is missing, you can throw an error and return nothing.

## Installing with arguments

Optionally. If the user has added arguments to be passed during installation, you can get those arguments by adding arguments to the GetIntegration function like below.

```lua
function Integration:GetIntegration(Arg1, Arg2, Arg3)
```

To add arguments to be passed during installation, add the integration to the CustomIntegrations dictionary in Config first, then add the additional arguments in the table. An example is shown below.

```lua
Config.CustomIntegrations = {
	-- Optionally add arguments for custom integration installations
	TemplateIntegration = {true, "arg1", "arg2", "arg3"}
}
```

TemplateIntegration should be replaced with the name of the integration module.

The first argument will not be passed to the integration module as it is an option to choose whether the integration will be installed or not.



That's all about custom integrations! To learn more about the Flux Integration Constructor, refer to the [Integration Constructor](constructor.md) doc. To share your custom integration with others as a global integration, create a Product Support ticket and we'll help you out.
