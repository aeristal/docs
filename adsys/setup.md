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

* No animations.
* No image ads with sound.
* Ad Scaling unavailable.

## Configuration

All configuration settings have annotations beside them which explain the setting, but we'll teach you how to add image ads to your system!



**Example Ad Format**

```lua
["AdSys Ad (Landscape)"] = { -- You can set any name you'd like, it's for your own reference only.
		["DecalId"] = "rbxassetid://18256906384", -- The ad's decal, Decal and Image IDs supported
		["SoundId"] = "", -- Optional Sound ID, leave empty if no sound
		["ScaleType"] = "Stretch", -- The scale type for the ad, Stretch or Fit only
		["Orientation"] = "Landscape", -- The orientation of the ad (Portrait, Landscape, Banner)
	},
```

1. In the text at the top, enter the name of the ad.

{% hint style="success" %}
Tip: Your ads will be played in alphabetical order following it's set name. Replace the name with numbers like 1, 2 or 3 to sort them!
{% endhint %}

2. At the DecalId field, you have to add the IMAGE ID (not to be confused with asset id) of the ad or else the screen will appear as blank. This issue will be solved soon.
3. If you want to have sound played when your ad is displayed, add the sound. The system will wait until the sound has finished playing before displaying the next ad.
4. Optionally, you can enter your own scaling preference for your ad. Stretch will stretch your ad across the screen and Fit will fit your ad onto the screen without stretching it.
5. Different ads may have different sizes. Make sure you set the Orientation to Portrait, Landscape or Banner so your ad is shown on the appropriate screens.
