# API Documentation

## Information

**Type:** BindableEvent\
**Location:** ServerScriptService -> Noren Ranking Sticks -> AG\_RSRequest\
**Execution example:**

```lua
local API = game:GetService("ServerScriptService"):WaitForChild("AG_RSRequest", 10)

API:Fire(CommandName, ...) -- additional parameters can be added if needed
```

## Commands

### Rank

Sends a request to the Engine to rank a target player.

**Parameters:**

| Ranker: Player     | The Player who is responsible for the rank request. |
| ------------------ | --------------------------------------------------- |
| Target: Player     | The Player that is being ranked.                    |
| RankAction: string | Promote/Demote                                      |

**Code example:**

```lua
local RankEvent = game:GetService("ServerScriptService"):WaitForChild("AG_RSRequest", 10)
local RankAction = "Promote"

RankEvent:Fire("Rank", Ranker, Target, RankAction)
```

### equippedMessage

Sends a banner notification to the Ranker that the tool they equipped is for ranking.

**Parameters:**

| Ranker: Player   | The Player who is equipping the tool. |
| ---------------- | ------------------------------------- |
| ToolName: string | The name of the tool being equipped.  |

**Code example:**

```lua
local RankEvent = game:GetService("ServerScriptService"):WaitForChild("AG_RSRequest", 10)

RankEvent:Fire("equippedMessage", Ranker, ToolName)
```
