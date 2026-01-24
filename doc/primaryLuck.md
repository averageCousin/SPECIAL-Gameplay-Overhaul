<!-- author: @averageCousin -->

# Luck (primary) #

> AV: `Luck` | AVC: `11`

<details>

<summary>

##### Respective game settings parameters #####

</summary>

* [`fAVDSkillLuckBonusMult`](#all-skills-derived)
* [`fAVDCritLuckBase`](#critical-hit-chance-derived)
* [`fAVDCritLuckMult`](#critical-hit-chance-derived)

</details>

## Game Settings ##

### All Skills (derived) ###

> AV: `null` | AVC: `null`<br>
>
> Derivation:<br>
> `\*SKILLNAME\* = fAVDSkill\*SKILLNAME\*Base + (\*PRIMARYSTAT\* * fAVDSkillPrimaryBonusMult) + ceil(LCK * fAVDSkillLuckBonusMult)`
>
> Settings:
>
> | Config | `fAVDSkillLuckBonusMult` |
> | - | - |
> | Vanilla | 0.5 |
> | JSU | 0.5 |

### Critical Hit Chance (derived) ###

> AV: `CritChance` | AVC: `14`<br>
>
> Derivation:<br>
> `CritChance = fAVDCritLuckBase + (fAVDCritLuckMult * LCK)`
>
> Settings:
>
> | Config | `fAVDCritLuckBase` | `fAVDCritLuckMult` |
> | - | - | - |
> | Vanilla | 0.0 | 0.1 |
> | JSU | 0.0 | 0.1 |
