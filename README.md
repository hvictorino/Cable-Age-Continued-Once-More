### Fix for the mod 'Cable Age Continued' for Cosmoteer from the author Commissar[GSF] (Steam)

Wanted to use the mod on the new version of the game,
but it was causing the game to crash, so i worked around a fix to it.

## Installation

##### Paste it in the mods folder and play

### Changes made for it to work on 0.30.0:

##### Added the following fields in the file component_power_proxy.rules

```
MinResourcesPickUp  
MaxResourcesPickUp  
MinResources  
MaxResources  
PickUpRate  
```

##### Also created a separate node in the file component_power_proxy.rules for each reactor tier(small, medium and large), each one with the respective ammount of resources and pickupRate

##### Fixed in the file mod.rules the referenced value of

```
(&<./Data/ships/terran/reactor_med/reactor_small.rules>/Part/Components/BatteryProducer/ToQuantity/)

```

##### to

```
(&<./Data/ships/terran/reactor_med/reactor_small.rules>/Part/Components/BatteryProducer/ToQuantity/BaseValue)
```

##### Because it was pointing to a field that was not of a numerical value.
