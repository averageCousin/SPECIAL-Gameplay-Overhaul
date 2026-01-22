<!-- Author: @averageCousin -->
<!-- TODO: Check for entry points -->

# Intelligence (primary) #

> AV: `Intelligence` | AVC: `9`

<details>

<summary>

##### Respective Pame Settings Parameters #####

</summary>

* [`fAVDSkillMedicineBase`](#medicine-skill)
* [`fAVDSkillRepairBase`](#repair-skill)
* [`fAVDSkillScienceBase`](#science-skill)

</details>

## Game Settings ##

### Medicine (skill) ###

> AV: `Medicine` | AVC: `37`<br>
>
> Derivation:<br>
> `Medicine = fAVDSkillMedicineBase + (XXX * fAVDSkillPrimaryBonusMult) + ceil(LCK * fAVDSkillLuckBonusMult)`
>
> Settings:
>
> | Config | `fAVDSkillMedicineBase` |
> | - | - |
> | Vanilla | 2.0 |
> | JSU | 2.0 |

### Repair (skill) ###

> AV: `Repair` | AVC: `39`<br>
>
> Derivation:<br>
> `Repair = fAVDSkillRepairBase + (XXX * fAVDSkillPrimaryBonusMult) + ceil(LCK * fAVDSkillLuckBonusMult)`
>
> Settings:
>
> | Config | `fAVDSkillRepairBase` |
> | - | - |
> | Vanilla | 2.0 |
> | JSU | 2.0 |

### Science (skill) ###

> AV: `Science` | AVC: `40`<br>
>
> Derivation:<br>
> `Science = fAVDSkillScienceBase + (XXX * fAVDSkillPrimaryBonusMult) + ceil(LCK * fAVDSkillLuckBonusMult)`
>
> Settings:
>
> | Config | `fAVDSkillScienceBase` |
> | - | - |
> | Vanilla | 2.0 |
> | JSU | 2.0 |

### Skill Point Rate (derived) ###

> AV: `null` | AVC: `null`<br>
>
> Derivation:<br>
> `Skill Rate = floor(min(INT, 9) * 0.5 + 10)`

## Secondary Settings ##

### Medicine Effects (derived) ###

> AV: `null` | AVC: `null`<br>
>
> Derivation:<br>
> `Potency = fMagicMedicineSkillBase + (fMagicMedicineSkillMult * (Medicine / 100))`<br>
> <sub>*\* Where `Potency` is effect of the medical item; **not** an ActorValue.*</sub>
>
> Settings:
>
> | Config | `fMagicMedicineSkillBase` | `fMagicMedicineSkillMult` |
> | - | - | - |
> | Vanilla | 1.0 | 2.0 |
> | JSU | 1.0 | 2.0 |
