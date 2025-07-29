---
icon: repeat
---

# Updating Your Products

Don't know how to update your products to their latest version? We got you. Here's a step-by-step tutorial.

Before we start, ensure that you have already **retrieved the latest version** of the product from [myParcel](https://my.parcelroblox.com/) and **imported the file** into your game. Ensure that you **do not delete** the old version yet.

{% hint style="warning" %}
If the product's new version features a full system rewrite, model changes, it is recommended that you delete your existing product and set it up again using the new version to prevent complications.
{% endhint %}

## 1. Updating the main script

To update the main script of your product, look inside the product's folder and locate a "**Initialize**" or "**Engine**" script.

{% hint style="info" %}
Configuration modules and values refer to objects like `StringValue`, `ModuleScript`, etc. Not your **SysConfig module**.
{% endhint %}

Once you've found it, make sure there is no configuration modules or values in it. If there is, put it somewhere else and then delete the old main script.

Now, move the main script from the product's new version into your product and replace configuration modules or values if any.

Your update process is likely done here. If there are changes to the system's configuration like new features or config options, move on to the next step.

## 2. Updating the system configuration

To update your SysConfig or similar module(s), we recommend replacing your old module with the new module so that you'll be able to easily identify configs that were added or removed.

Move the SysConfig or similar module(s) from the new product's folder into your old product's folder.

For each module, open the old and new versions to make it easier.

There may be configs which were unchanged in the new version, so you can copy the configs from the old module and paste it in the new module if any.

If there are new configs, configure them accordingly. Refer to the annotations if you need help.

## 3. Done!

Congratulations! You're now done updating your product to the latest version.

If you are experiencing issues **with** or **after** updating your product, please [contact us](../support/contact-us.md). We're always here to help!
