# Sending a notification

## Notification functions

The Lumina module has 2 functions you can use to send notifications.

1. `Notify`
2. `NotifyAll`

The `Notify` function allows you to send a notification to more than 1 Players while the `NotifyAll` function will send a notification to all present Players in the server.

Both notification functions accept the same arguments, but the notification target parameters are different.

### `Notify`

| Players: {Player}                         | `Player` objects who will receive the notification.                                                                                                               |
| ----------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Header: string                            | The notification's header.                                                                                                                                        |
| Description: string                       | The notification's description.                                                                                                                                   |
| Customization: NotificationCustomization? | Optional customization options you can set for the notification. See [#notificationcustomization](sending-a-notification.md#notificationcustomization "mention"). |

### `NotifyAll`

| Header: string                            | The notification's header.                                                                                                                                        |
| ----------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Description: string                       | The notification's description.                                                                                                                                   |
| Customization: NotificationCustomization? | Optional customization options you can set for the notification. See [#notificationcustomization](sending-a-notification.md#notificationcustomization "mention"). |

### `NotificationCustomization`&#x20;

| Header: TextStyle?      | Optional customization options you can set for the notification's header. See [#textstyle](sending-a-notification.md#textstyle "mention").           |
| ----------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------- |
| Description: TextStyle? | Optional customization options you can set for the notification's description. See [#textstyle](sending-a-notification.md#textstyle "mention").      |
| TweenInfo: TweenInfo?   | Optional `TweenInfo` you can set to override the module's default TweenInfo. Only used when the notification slides down onto the `Player`'s screen. |
| CornerRoundness: UDim?  | Optional `UDim` you can set for the notification's `UICorner` CornerRadius.                                                                          |

### `TextStyle`

| Font: Enum.Font?         | Optional Enum.Font you can set to override the default font (`Builder Sans`) |
| ------------------------ | ---------------------------------------------------------------------------- |
| TextColor: Color3?       | Optional Color3 you can set to override the default TextColor.               |
| BackgroundColor: Color3? | Optional Color3 you can set to override the default BackgroundColor.         |

{% hint style="warning" %}
When the Lumina module is running in a Client environment, both the `Notify` and `NotifyAll` functions will only send the notification to the `LocalPlayer`.
{% endhint %}

The `Notify` function's first argument `Players` accepts a table of `Player` objects who will receive the notification you send while the `NotifyAll` function will send the notification to all present `Player` objects.

## Code example

Here's a code example of how to send a notification using the module's default customizaation options to the `LocalPlayer` in a `LocalScript` assuming that the Lumina module is parented to it.

```lua
local Lumina = require(script.NorenLumina)

Lumina:Notify(
    {}, -- Empty table because it will automatically send to the LocalPlayer.
    "Welcome to Aveny Park",
    "Thanks for joining, enjoy your time here!"
)
```
