# Setup

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

## Adding an advertisement

All configuration settings have annotations beside them which explain the setting, but we'll teach you how to add an image ad to your system!

If you already have some basic scripting knowledge, here's 2 examples of ways you can add an advertisement to get you started.

#### **Example Ad Format 1**

```lua
['Example Advertisement'] = {
		DecalId = "", -- Image ID, not Asset ID
		SoundId = "0", -- Sound to play when the ad is shown
		ScaleType = "Stretch", -- The scale type for the ad (Stretch | Fit)
		Orientations = { -- Compatible orientations (Landscape | Portrait | Banner)
				Landscape = "Decal id here",
				Portrait = "Decal id here",
				Banner = "Decal id here",
		}
},
```

#### **Example Ad Format 2**

```lua
['Example Advertisement'] = {
		DecalId = "Decal id here", -- Image ID, not Asset ID
		SoundId = "0", -- Sound to play when the ad is shown
		ScaleType = "Stretch", -- The scale type for the ad (Stretch | Fit)
		Orientation = "Landscape" -- Compatible orientations (Landscape | Portrait | Banner)
},
```

### Step-by-step guide

1. If your advertisement is going to be for multiple orientations (eg. Portrait & Landscape), copy [#example-a-d-format-1](setup.md#example-a-d-format-1 "mention") and paste it into `SysConfig.Advertisements`. If your advertisement is going to be for a single orientation only, copy [#example-a-d-format-2](setup.md#example-a-d-format-2 "mention") and paste it into `SysConfig.Advertisements`.

{% hint style="success" %}
It's recommended to keep each advertisement separated by a newline.
{% endhint %}

2. Give your advertisement a name _**unique**_**&#x20;from other advertisements** by changing "Example Advertisement".

{% hint style="success" %}
The name will be underlined with red if the advertisement's name is the same as another advertisement. Watch out for red bars appearing on the scrollbar!
{% endhint %}

3. If your advertisement is for a single orientation, enter the **asset ID** of the **image** for your advertisement. Entering the asset id of the **decal** will not work.
4. If your advertisement is for multiple orientations, add the **asset ID** of the images for the orientations your advertisement is for in the `Orientations` table. Remove the orientations that you will not be using from the `Orientations` table.
5. If you'd like sound to be played during your advertisement, add the sound ID to `SoundId`.

{% hint style="success" %}
If you have `RandomizeAds`and `AutomaticallySync`enabled, all displays will wait if one or more displays are playing advertisements with sound until it's done and vice-versa.
{% endhint %}

6. Set the `ScaleType` of your advertisement to be either **Stretch** or **Fit**. Stretch will stretch your advertisement's image to maximize space on screen. Fit will maintain your advertisement's image's aspect ratio and will resize it to maximize space on screen.
