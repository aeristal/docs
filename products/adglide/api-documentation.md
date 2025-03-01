# API Documentation

## Information

**Type:** BindableEvent\
**Location:** Product folder -> API\
**Execution example:**

```lua
API:Fire(CommandName, ...) -- additional parameters can be added if needed
```

## Commands

### QueueAd

Adds an advertisement to the queue of all devices. If advertisements fail the validation check, they will not be queued.

**Parameters:**

| Advertisement: table | The advertisement to queue (see "Code example").                              |
| -------------------- | ----------------------------------------------------------------------------- |
| Prioritize: boolean  | Whether the advertisement should be added to the first position in the queue. |

**Code example:**

<pre class="language-lua"><code class="lang-lua">local API = workspace["Atelier AdGlide Advertisement System"].API

API:Fire("QueueAd", {
	Name = "Example Advertisement",
	DecalId = "", -- Image ID, not Asset ID
<strong>	SoundId = "0", -- Sound to play when the ad is shown
</strong>	ScaleType = "Stretch", -- The scale type for the ad (Stretch | Fit)
	Orientations = { -- Compatible orientations (Landscape | Portrait | Banner)
		Landscape = "0",
		Portrait = "0",
	}
}, true)
</code></pre>

### SetTopbar

Sets the topbar text on all Portrait advertisement displays.

**Parameters:**

| Text: string | The text to be set as the topbar text. |
| ------------ | -------------------------------------- |

**Code example:**

```lua
local API = workspace["Atelier AdGlide Advertisement System"].API

API:Fire("SetTopbar", "Hello world!")
```
