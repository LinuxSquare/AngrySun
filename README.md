# AngrySun
You will burn under the Sun! ~ MJaroslav<br/>
Credits to the original mod goes to: [Mjaroslav](https://github.com/MJaroslav/AngrySun)

## About this mod
The AngrySun mod will do what the name tells you. The sun is angry at you and wants to kill you.

Whenever you try to go out to the surface during daytime while not wearing some protective thermal armour (configurable), you will immediately start burning and get some nasty effects such as blindness, nausea and weakness (configurable).

You can, however look for shelter under a block, where the sunrays can't reach you.

## My modifications
I've forked this mod and modified it a little. Somehow purged a few bugs (such as getting the effects while being in spectator mode) and exchanged reeds (sugar cane) to iron ingots within the stitched_reed recipe for my (maybe) modpack.

## Configuration

And here, the configuration of this fork:

```
# Configuration file

general {
    # Alternative check of the sun. If there is any block above your head, you will not burn. [default: true]
    B:alt_solar_checking=true

    # Use thermal underwear. If it's disabled, then any armor is used.
    B:enable_thermal_underwear=true

    # Excluded Dimensions
    S:excluded_dimensions={-1,1}

    # Use effects when the player is under the sun. [default: true]
    B:use_effects=true

    thermalunderwear {
        # To cause damage to thermal underwear. [default: true]
        B:damage=true

        # Maximum random damage value when thermal underwear using. [range: 1 ~ 64, default: 2]
        I:damage_value=2

        # Strength factor of hood (11) and cloak (16).
        I:durability=80

        # Use the cloak in conjunction with the hood.
        B:use_cloack=true

        # Use the standard recipe for crafting thermal underwear.
        B:use_recipe=true
    }

    effects {
        # Use the blindness effect when the player is under the sun. [default: true]
        B:use_blindness=true

        # Use the nausea effect when the player is under the sun. [default: true]
        B:use_nausea=true

        # Use the weakness effect when the player is under the sun. [default: true]
        B:use_weakness=true
    }

}
```