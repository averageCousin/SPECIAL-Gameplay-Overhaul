<!-- author: @averageCousin -->
<!-- TODO: Check for entry points -->

# Agility (primary) #

> AV: `Agility` | AVC: `10`

<details>

<summary>

##### Respective Game Settings Parameters #####

</summary>

* [`fAVDSkillGunsBase`](#small-guns-skill)
* [`fAVDSkillSneakBase`](#sneak-skill)
* [`fAVDActionPointsBase`](#action-points-derived)
* [`fAVDActionPointsMult`](#action-points-derived)
* [`fActionPointsRestoreRate`](#action-point-regeneration-derived)
* [`fActionPointsReload`](#reload-action-point-cost-derived)
* [`fPlayerWeaponReloadTimer`](#reload-speed-derived)
* [`fAgilityReloadModifier`](#reload-speed-derived)
<!-- * [`XX`](#) -->

</details>

## Game Settings ##

### (Small) Guns (skill) ###

> AV: `Guns` | AVC: `41`<br>
>
> Derivation:<br>
> `Guns = fAVDSkillGunsBase + (AGL * fAVDSkillPrimaryBonusMult) + ceil(LCK * fAVDSkillLuckBonusMult)`
>
> Settings:
>
> | Config | `fAVDSkillGunsBase` |
> | - | - |
> | Vanilla | 2.0 |
> | JSU | 2.0 |

### Sneak (skill) ###

> AV: `Sneak` | AVC: `42`<br>
>
> Derivation:<br>
> `Sneak = fAVDSkillSneakBase + (XXX * fAVDSkillPrimaryBonusMult) + ceil(LCK * fAVDSkillLuckBonusMult)`
>
> Settings:
>
> | Config | `fAVDSkillSneakBase` |
> | - | - |
> | Vanilla | 2.0 |
> | JSU | 2.0 |

### Action Points (derived) ###

> AV: `ActionPoints` | AVC: `12`<br>
>
> Derivation:<br>
> `ActionPoints = fAVDActionPointsBase + (AGL * fAVDActionPointsMult)`
>
> Settings:
>
> | Config | `fAVDActionPointsBase` | `fAVDActionPointsMult` |
> | - | - | - |
> | Vanilla | 65.0 | 3.0 |
> | JSU | 65.0 | 3.0 |
>
> <sub>*\*`fAVDActionPointsMult` <a href="https://geckwiki.com/index.php?title=FAVDActionPointsMult">GECK Wiki entry</a> is incorrect; 2.0 $\rarr$ 3.0*</sub>

### Action Point Regeneration (derived) ###

> Restores Action Points relative to the player's maximum base Action Points *(before perks, traits, etc.)*.<br>
> *i.e.* Restores a percentage of the total *not* as individual points.<br>
>
> AV: `null` | AVC: `null`<br>
>
> Derivation:<br>
> `Seconds to Max = 1 / fActionPointsRestoreRate`
>
> Settings:
>
> | Config | `fActionPointsRestoreRate` |
> | - | - |
> | Vanilla | 0.06 |
> | JSU | 0.06 |

### Reload Action Point Cost (derived) ###

> AV: `null` | AVC: `null`<br>
>
> Derivation:<br>
> `Cost = round(fActionPointsReload * ENTRYPOINT{Action Point Cost})`
>
> Settings:
>
> | Config | `fActionPointsReload` |
> | - | - |
> | Vanilla | 10.0 |
> | JSU | 10.0 |

<!-- TODO: Figure out how the fuck this works -->

### Agility Animation Speed Modifier (derived) ###

<!-- https://fallout.wiki/wiki/Agility_(Fallout:_New_Vegas)#Modifies -->

> <sub></sub>
>
> AV: `null` | AVC: `null`<br>
>
> Derivation:<br>
> `AGILITYMODIFIER =`

### Reload Speed (derived) ###

> AV: `null` | AVC: `null`<br>
>
> Derivation:<br>
> `Reload Time = WeaponReloadTime / ((fPlayerWeaponReloadTimer + AGL * fAgilityReloadModifier) * ENTRYPOINT{Reload Speed})`
>
> <sub>*\* Where "Reload Time" and "WeaponReloadTime" are in seconds.*</sub><br>
> <sub>*\* "WeaponReloadTime" derived from the attributes of the specific weapon in use*</sub><br>
>
> Settings:
>
> | Config | `fPlayerWeaponReloadTimer` | `fAgilityReloadModifier` |
> | - | - | - |
> | Vanilla | 0.5 | 0.1 |
> | JSU | 0.5 | 0.1 |

<!-- TODO -->

### Unholster Speed (derived) ###

> AV: `null` | AVC: `null`<br>
>
> Derivation:<br>
> `XX`

<!-- TODO -->

### Unholster Cost (derived) ###

`fActionPointsToggleWeaponDrawn`
