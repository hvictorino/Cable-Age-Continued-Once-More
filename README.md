# Original author: Commissar[GSF] (Steam)

Some friends wanted to use the mod on the new version of the game,
but it was causing the game to crash, so they asked me to fix it, which i did.

# Basic changes that were made for it to work:

Added the following fields in the file component_power_proxy.rules

MinResourcesPickUp
MaxResourcesPickUp
MinResources
MaxResources
PickUpRate

Fixed in the file mod.rules the referenced value of

(&<./Data/ships/terran/reactor_med/reactor_med.rules>/Part/Components/BatteryProducer/ToQuantity/)

to

(&<./Data/ships/terran/reactor_med/reactor_med.rules>/Part/Components/BatteryProducer/ToQuantity/BaseValue)

Because it was pointing to a field that was not of a numerical value.