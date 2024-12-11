# Custom Tools

{% hint style="success" %}
You are expected to have basic scripting experience and knowledge in order to follow this guide.
{% endhint %}

The step-by-step guide below shows you what you need to script into your tool to transform it into your own custom ranking stick.

1. Make sure your tool has a `Script`, otherwise insert a new `Script`.
2. In your script, it should fire the equippedMessage command to the API whenever the tool is equipped. We highly recommend you to utilize the[ API Documentation](api-documentation.md).
3. Your script should have a way to detect players that are hit by the ranking stick. Keep in mind that it usually should only detect players when the Ranker has activated the sword, etc (depending on your tool).
4. Make sure your script has a _local_ variable to store the RankAction. This is so third-party scripts can't tamper with your ranking sticks.
5. Your script should fire the Rank command to the API whenever a `Player` is detected. Make sure that the tool also does not deal damage to the `Player`.
6. Done. You now have made your own custom ranking tool!
