# API Documentation

## Information

**Type:** BindableEvent\
**Location:** Product folder -> API\
**Execution example:**

```lua
API:Fire(ZoneName, CommandName, ...) -- additional parameters can be added if needed
```

## Commands

### TurnOn

Turns on all the lights in the zone.

**Parameters:**

| Brightness: number | Optional brightness to set. |
| ------------------ | --------------------------- |
| Color: Color3      | Optional color to set.      |

**Code example:**

```lua
API:Fire("ExampleZone", "TurnOn", 1.2, Color3.fromRGB(255, 255, 255))
```

### TurnOff

Turns off all the lights in the zone.

### Toggle

Toggles all the lights in the zone.

**Parameters:**

| Brightness: number | Optional brightness to set. |
| ------------------ | --------------------------- |
| Color: Color3      | Optional color to set.      |

**Code example:**

```lua
API:Fire("ExampleZone", "Toggle", 1.2, Color3.fromRGB(255, 255, 255))
```

### SetColor

Sets the color of all the lights in the zone.

**Parameters:**

| Color: Color3 | Optional color to set. |
| ------------- | ---------------------- |

**Code example:**

```lua
API:Fire("ExampleZone", "SetColor", Color3.fromRGB(255, 255, 255))
```

### SetBrightness

Sets the brightness of all lights in the zone.

**Parameters:**

| Brightness: number | Optional brightness to set. |
| ------------------ | --------------------------- |

**Code example:**

```lua
API:Fire("ExampleZone", "SetBrightness", 1.2)
```

