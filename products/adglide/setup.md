# Setup

{% hint style="danger" %}
A paid license is required to use this product.
{% endhint %}

## Immersive Ads

If your game is eligible for Immersive Ads, it's recommended that you enable Immersive Ads on your system. But take note of the changes when you enable Immersive Ads:

**Pros**

* Earn ad revenue from your advertisement screens.
* Automatically show image ads when Immersive Ads aren't being served.

**Cons**

* No tweens for image ads.
* Image ads will not have sound (if set).
* ScaleType will not take effect.

## Resolutions

For your information, here are the best resolutions to be used with Advertisement System in pixels (width x height).

* Landscape: 1920 x 1080
* Portrait: 1080 x 1920
* Banner: 1500 x 1000

## Old Configuration Compatibility (for v1 users)

As AdGlide was rewritten from scratch, a part of the script that reads the **Advertisements** configuration was scripted incorrectly.

Your advertisements' `Orientations` key should look like this:

```lua
["Orientation"] = "Portrait", -- The orientation of the ad (Portrait, Landscape, Banner)
```

Unfortunately, the part of the script that's supposed to make old configuration compatible with Version 2 was scripted incorrectly and only accepts the new format in [#configuration](setup.md#configuration "mention") or:

```lua
Orientations = { -- Compatible orientations (Landscape | Portrait | Banner)
		"Landscape",
		"Portrait",
		"Banner",
}
```

We are actively working on AdGlide V2.0.1 to resolve any found bugs and issues immediately and we aim to release it by next week.

## Configuration

All configuration settings have annotations beside them which explain the setting, but we'll teach you how to add image ads to your system!

**Example Ad Format**

```lua
['Example Advertisement'] = {
		DecalId = "", -- Image ID, not Asset ID
		SoundId = "0", -- Sound to play when the ad is shown
		ScaleType = "Stretch", -- The scale type for the ad (Stretch | Fit)
		Orientations = { -- Compatible orientations (Landscape | Portrait | Banner)
			Landscape = "0",
			Portrait = "0",
		}
	},
```

1. In the `string` at the top, enter the name of the ad.

{% hint style="success" %}
Tip: Your ads will be played in alphabetical order following it's set name. Replace the name with numbers like 1, 2 or 3 to sort them!
{% endhint %}

2. In the `DecalId` field, you have to add the **Image ID** (not to be confused with **Asset ID**) of the ad or else the screen will appear as blank.
3. If you want to have sound played when your ad is displayed, add the **Sound ID** in the `SoundId`field. The display will wait for the sound to finish before moving onto the next ad.

{% hint style="warning" %}
If you have `AutomaticallySync` enabled, an ad with sound will cause that display to go out of sync. An fix will be implemented for this soon.
{% endhint %}

4. Optionally, you can enter your own scaling preference for your ad. Stretch will stretch your ad across the screen and Fit will fit your ad onto the screen without stretching it.
5. Different ads may have different sizes. Make sure you set the Orientation to Portrait, Landscape or Banner so your ad is shown on the appropriate screens.
