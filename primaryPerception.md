<!-- TODO: Check for entry points -->

# Perception (primary) #

> AV: `Perception` | AVC: `6`

<details>

<summary>

##### Respective Game Settings Parameters #####

</summary>

* [`fAVDSkillEnergyWeaponsBase`](#energy-weapons-skill)
* [`fAVDSkillExplosivesBase`](#explosives-skill)
* [`fAVDSkillLockpickBase`](#lockpick-skill)

</details>

## Game Settings ##

### Energy Weapons (skill) ###

> AV: `EnergyWeapons` | AVC: `34`<br>
>
> Derivation:<br>
> `EnergyWeapons = fAVDSkillEnergyWeaponsBase + (PER * fAVDSkillPrimaryBonusMult) + ceil(LCK * fAVDSkillLuckBonusMult)`
>
> Settings:
>
> | Config | `fAVDSkillEnergyWeaponsBase` |
> | - | - |
> | Vanilla | 2.0 |
> | JSU | 2.0 |

### Explosives (skill) ###

> AV: `Explosives` | AVC: `35`<br>
>
> Derivation:<br>
> `Explosives = fAVDSkillExplosivesBase + (PER * fAVDSkillPrimaryBonusMult) + ceil(LCK * fAVDSkillLuckBonusMult)`
>
> Settings:
>
> | Config | `fAVDSkillExplosivesBase` |
> | - | - |
> | Vanilla | 2.0 |
> | JSU | 2.0 |

### Lockpick (skill) ###

> AV: `Lockpick` | AVC: `36`<br>
>
> Derivation:<br>
> `Lockpick = fAVDSkillLockpickBase + (PER * fAVDSkillPrimaryBonusMult) + ceil(LCK * fAVDSkillLuckBonusMult)`
>
> Settings:
>
> | Config | `fAVDSkillLockpickBase` |
> | - | - |
> | Vanilla | 2.0 |
> | JSU | 2.0 |
