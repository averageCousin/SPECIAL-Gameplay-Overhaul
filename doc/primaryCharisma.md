<!-- Author: @averageCousin -->
<!-- TODO: Check for entry points -->

# Charisma (primary) #

> AV: `Charisma` | AVC: `8`

<details>

<summary>

##### Respective Game Settings Parameters #####

</summary>

* [`fAVDSkillBarterBase`](#barter-skill)
* [`fAVDSkillSpeechBase`](#speech-skill)

</details>

## Game Settings ##

### Barter (skill) ###

> AV: `Barter` | AVC: `32`<br>
>
> Derivation:<br>
> `Barter = fAVDSkillBarterBase + (CHR * fAVDSkillPrimaryBonusMult) + ceil(LCK * fAVDSkillLuckBonusMult)`
>
> Settings:
>
> | Config | `fAVDSkillBarterBase` |
> | - | - |
> | Vanilla | 2.0 |
> | JSU | 2.0 |

### Speech (skill) ###

> AV: `Speech` | AVC: `43`<br>
>
> Derivation:<br>
> `Speech = fAVDSkillSpeechBase + (CHR * fAVDSkillPrimaryBonusMult) + ceil(LCK * fAVDSkillLuckBonusMult)`
>
> Settings:
>
> | Config | `fAVDSkillSpeechBase` |
> | - | - |
> | Vanilla | 2.0 |
> | JSU | 2.0 |

<!-- TODO -->

### Price (XX) ###

> AV: `XX` | AVC: `##`<br>
>
> Derivation:<br>
> `XX`
>
> Settings:
>
> | Config | `` |
> | - | - |
> | Vanilla | 0.0 |
> | JSU | 0.0 |

<!-- TODO -->

### Companion Nerve (derived) ###

> AV: `null` | AVC: `null`<br>
>
> Derivation:<br>
> `Nerve = (CHA * 5) / 100`
