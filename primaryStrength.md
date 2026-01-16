<!-- TODO: Check for entry points -->

# Strength (primary) #

> AV: `Strength` | AVC: `5`

<details>

<summary>

##### Respective Game Settings Parameters #####

</summary>

* [`fAVDSkillMeleeWeaponsBase`](#melee-weapons-skill)
* [`fAVDCarryWeightsBase`](#carry-weight-derived)
* [`fAVDCarryWeightMult`](#carry-weight-derived)
* [`fAVDMeleeDamageStrengthMult`](#melee-damage-derived)
* [`fAVDMeleeDamageStrengthOffset`](#melee-damage-derived)

</details>

## Game Settings ##

### Melee Weapons (skill) ###

> AV: `MeleeWeapons` | AVC: `38`<br>
>
> Derivation:<br>
> `MeleeWeapons = fAVDSkillMeleeWeaponsBase + (STR * fAVDSkillPrimaryBonusMult) + ceil(LCK * fAVDSkillLuckBonusMult)`
>
> Settings:
>
> | Config | `fAVDSkillMeleeWeaponsBase` |
> | - | - |
> | Vanilla | 2.0 |
> | JSU | 2.0 |

### Carry Weight (derived) ###

> AV: `CarryWeight` | AVC: `17`<br>
>
> Derivation:<br>
> `CarryWeight = fAVDCarryWeightsBase + (STR * fAVDCarryWeightMult)`
>
> Settings:
>
> | Config | `fAVDCarryWeightsBase` | `fAVDCarryWeightMult` |
> | - | - | - |
> | Vanilla | 65.0 | 10.0 |
> | JSU | 50.0 | 10.0 |

### Melee Damage (derived) ###

> AV: `MeleeDamage` | AVC: `17`<br>
>
> Derivation:<br>
> `MeleeDamageActorValue = fAVDMeleeDamageStrengthMult + (fAVDMeleeDamageStrengthOffset * STR)`
>
> Settings:
>
> | Config | `fAVDMeleeDamageStrengthMult` | `fAVDMeleeDamageStrengthOffset` |
> | - | - | - |
> | Vanilla | 0.5 | 0.0 |
> | JSU | 0.5 | 0.0 |
