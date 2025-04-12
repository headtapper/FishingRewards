# FishingRewards
Grant additional items to players for catching fish with configurable loot table.

# Permissions
*  `fishingrewards.use` Required for players to receieve additional rewards when fishing.

# Configuration
**Configuration Example**
```json
{
  "PercentChanceOfReward": 75,
  "Drop Rates": {
    "rifle.ak": 1,
    "rifle.bolt": 2,
    "rifle.sks": 2,
    "rifle.m39": 4,
    "rifle.lr300": 2,
    "rifle.semiauto": 11,
    "rifle.l96": 1,
    "weapon.mod.8x.scope": 2,
    "lmg.m249": 1,
    "shotgun.spas12": 2,
    "shotgun.m4": 1,
    "t1_smg": 11,
    "smg.2": 7,
    "smg.thompson": 5,
    "smg.mp5": 2,
    "pistol.revolver": 20,
    "pistol.semiauto": 10,
    "pistol.python": 5,
    "pistol.m92": 5,
    "pistol.prototype17": 3
  }
}
```

**Configuration Properties**
* `PercentChanceOfReward` (int) Chance of giving grant additional reward to player when they catch a fish.
* `Drop Rates` (Dictionary<string, int>) Loot tables for fishing rewards. Item shortnames paired with a weight value for the random item selection. The weight value is not a percentage. The odds of one item are `item weight / sum(all weights)`.
