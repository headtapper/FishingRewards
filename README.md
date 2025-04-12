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

# Loot Drop Tests
```
Total Items Rewarded: 1000000
**1 000 000 Drop Rewards**
Chance of Reward: 100%
Item                    Actual Drops            Original Chance         Config Weight
rifle.ak                       10206                       1.03                     1
rifle.l96                      10320                       1.03                     1
lmg.m249                       10169                       1.03                     1
shotgun.m4                     10369                       1.03                     1
rifle.bolt                     20789                       2.06                     2
rifle.sks                      20619                       2.06                     2
rifle.lr300                    20672                       2.06                     2
weapon.mod.8x.scope            20429                       2.06                     2
shotgun.spas12                 20594                       2.06                     2
smg.mp5                        20540                       2.06                     2
pistol.prototype17             30960                       3.09                     3
rifle.m39                      41335                       4.12                     4
smg.thompson                   51422                       5.15                     5
pistol.python                  51503                       5.15                     5
pistol.m92                     51946                       5.15                     5
smg.2                          71722                       7.22                     7
pistol.semiauto               103610                      10.31                    10
rifle.semiauto                113319                      11.34                    11
t1_smg                        113464                      11.34                    11
pistol.revolver               206012                      20.62                    20
```

```
**1 000 000 Drop Rewards**
Chance of Reward: 75%
Total Items Rewarded: 760500
Item                    Actual Drops            Original Chance         Config Weight
rifle.ak                        7851                       1.03                     1
rifle.l96                       7937                       1.03                     1
lmg.m249                        8057                       1.03                     1
shotgun.m4                      7909                       1.03                     1
rifle.bolt                     15684                       2.06                     2
rifle.sks                      15572                       2.06                     2
rifle.lr300                    15686                       2.06                     2
weapon.mod.8x.scope            15736                       2.06                     2
shotgun.spas12                 15810                       2.06                     2
smg.mp5                        15499                       2.06                     2
pistol.prototype17             23585                       3.09                     3
rifle.m39                      31589                       4.12                     4
smg.thompson                   39128                       5.15                     5
pistol.python                  38816                       5.15                     5
pistol.m92                     38901                       5.15                     5
smg.2                          54821                       7.22                     7
pistol.semiauto                78479                      10.31                    10
rifle.semiauto                 86268                      11.34                    11
t1_smg                         86500                      11.34                    11
pistol.revolver               156672                      20.62                    20
```
