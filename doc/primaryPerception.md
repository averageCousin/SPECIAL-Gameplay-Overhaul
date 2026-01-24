<!-- author: @averageCousin -->
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
> $\text{EnergyWeapons}\ =$ <br>
> $\ \ \text{fAVDSkillEnergyWeaponsBase}\ +$ <br>
> $\ \ (\text{PER} * \text{fAVDSkillPrimaryBonusMult})\ +$ <br>
> $\ \ \text{ceil}(\text{LCK} * \text{fAVDSkillLuckBonusMult})$ <br>
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
> $\text{Explosives}\ =$ <br>
> $\ \ \text{fAVDSkillExplosivesBase}\ +$ <br>
> $\ \ (\text{PER} * \text{fAVDSkillPrimaryBonusMult})\ +$ <br>
> $\ \ \text{ceil}(\text{LCK} * \text{fAVDSkillLuckBonusMult})$ <br>
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
> **Derivation:**<br>
> `Lockpick`$\ =$ <br>
> `fAVDSkillLockpickBase`$\ +$ <br>
> $($`PER` $\cdotp$ `fAVDSkillPrimaryBonusMult`$)\ +$ <br>
> $\text{ceil}($`LCK` $\cdotp$ `fAVDSkillLuckBonusMult`$)$ <br>
>
> **Settings:**
>
> | Config | `fAVDSkillLockpickBase` |
> | - | - |
> | Vanilla | 2.0 |
> | JSU | 2.0 |
