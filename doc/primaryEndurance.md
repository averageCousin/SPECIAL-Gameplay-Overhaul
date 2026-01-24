<!-- author: @averageCousin -->
<!-- TODO: Check for entry points -->

# Endurance (primary) #

> AV: `Endurance` | AVC: `7`

<details>

<summary>

##### Respective Game Settings Parameters #####

</summary>

* [`fAVDSkillSurvivalBase`](#survival-skill)
* [`fAVDSkillUnarmedBase`](#unarmed-skill)
* [`fAVDHealthEnduranceMult`](#hit-points-derived)
* [`fAVDHealthEnduranceOffset`](#hit-points-derived)
* [`fAVDHealthLevelMult`](#hit-points-derived)
* [`fAVDHealRateEndurance6Bonus`](#healing-rate-derived)
* [`fAVDHealRateEndurance7Bonus`](#healing-rate-derived)
* [`fAVDHealRateEndurance8Bonus`](#healing-rate-derived)
* [`fAVDHealRateEndurance9Bonus`](#healing-rate-derived)
* [`fAVDHealRateEndurance10Bonus`](#healing-rate-derived)
* [`fAVDPoisonResistEnduranceOffset`](#poison-resistance-derived)
* [`fAVDPoisonResistEnduranceMult`](#poison-resistance-derived)
* [`fAVDRadResistEnduranceOffset`](#radiation-resistance-derived)
* [`fAVDRadResistEnduranceMult`](#radiation-resistance-derived)
* [`fHCDehydrationRate`](#dehydration-derived-hardcore)
* [`fHCStarvationRate`](#hunger-derived-hardcore)
* [`fHCSleepDeprivationRate`](#sleep-deprivation-derived-hardcore)

<br>

* [`fAVDSkillBigGunsBase`](#big-guns-skill)
* [`fMagicSurvivalSkillBase`](#fatigue-derived)
* [`fMagicSurvivalSkillMult`](#fatigue-derived)
* [`fAVDFatigueBase`](#fatigue-derived)
* [`fAVDFatigueEnduranceMult`](#fatigue-derived)
* [`fAVDFatigueLevelMult`](#fatigue-derived)
* [`fMinFatigue`](#fatigue-derived)

</details>

## Game Settings ##

### Survival (skill) ###

> AV: `Survival` | AVC: `44`<br>
>
> Derivation:<br>
> `Survival = fAVDSkillSurvivalBase + (END * fAVDSkillPrimaryBonusMult) + ceil(LCK * fAVDSkillLuckBonusMult)`
>
> Settings:
>
> | Config | `fAVDSkillSurvivalBase` |
> | - | - |
> | Vanilla | 2.0 |
> | JSU | 2.0 |

### Unarmed (skill) ###

> AV: `Unarmed` | AVC: `45`<br>
>
> Derivation:<br>
> `Unarmed = fAVDSkillUnarmedBase + (END * fAVDSkillPrimaryBonusMult) + ceil(LCK * fAVDSkillLuckBonusMult)`
>
> Settings:
>
> | Config | `fAVDSkillUnarmedBase` |
> | - | - |
> | Vanilla | 2.0 |
> | JSU | 2.0 |

### Hit Points (derived) ###

> AV: `Health` | AVC: `16`<br>
>
> Derivation:<br>
> `Health = 100 + (fAVDHealthEnduranceMult * fAVDHealthEnduranceOffset) + (END * fAVDHealthEnduranceMult) + ((LVL - 1) * fAVDHealthLevelMult)`
>
> Settings:
>
> | Config | `fAVDHealthEnduranceMult` | `fAVDHealthEnduranceOffset` | `fAVDHealthLevelMult` |
> | - | - | - | - |
> | Vanilla | 20.0 | 0.0 | 5.0 |
> | JSU | 10.0 | -5.0 | 5.0 |

### Healing Rate (derived) ###

> AV: `HealRate` | AVC: `15`<br>
>
> Derivation:<br>
> `HealRate = (0.066 * fAVDHealRateEndurance#Bonus) / 60`<br>
> <sub>*\* Where `#` is the respective level of END*</sub>
>
> Settings:
>
> | Config | `fAVDHealRateEndurance6Bonus` | `fAVDHealRateEndurance7Bonus` | `fAVDHealRateEndurance8Bonus` | `fAVDHealRateEndurance9Bonus` | `fAVDHealRateEndurance10Bonus` |
> | - | - | - | - | - | - |
> | Vanilla | 5.0 | 5.0 | 5.0 | 10.0 | 10.0 |
> | JSU | 5.0 | 5.0 | 5.0 | 10.0 | 10.0 |

### Poison Resistance (derived) ###

> <sub>*0-100, treated as a percentage.*</sub><br>
> <sub>*Capped at 85%: `fPlayerMaxResistance`.*</sub><br>
>
> AV: `PoisonResist` | AVC: `19`<br>
>
> Derivation:<br>
> `PoisonResist = (END - fAVDPoisonResistEnduranceOffset) * fAVDPoisonResistEnduranceMult`
>
> Settings:
>
> | Config | `fAVDPoisonResistEnduranceOffset` | `fAVDPoisonResistEnduranceMult` |
> | - | - | - |
> | Vanilla | -1.0 | 5.0 |
> | JSU | -1.0 | 5.0 |

### Radiation Resistance (derived) ###

> <sub>*0-100, treated as a percentage.*</sub><br>
> <sub>*Capped at 85%: `fPlayerMaxResistance`.*</sub><br>
>
> AV: `RadResist` | AVC: `20`<br>
>
> Derivation:<br>
> `RadResist = (END - fAVDRadResistEnduranceOffset) * fAVDRadResistEnduranceMult`
>
> Settings:
>
> | Config | `fAVDRadResistEnduranceOffset` | `fAVDRadResistEnduranceMult` |
> | - | - | - |
> | Vanilla | -1.0 | 2.0 |
> | JSU | -1.0 | 2.0 |

---------------

### Dehydration (derived-hardcore) ###

> AV: `Dehydration` | AVC: `73`<br>
>
> Derivation:<br>
> `Dehydration = (1 * t) / fHCDehydrationRate`<br>
> <sub>*\* Where `t` is real time in seconds.*</sub>
>
> Settings:
>
> | Config | `fHCDehydrationRate` |
> | - | - |
> | Vanilla | 10.0 |
> | JSU | 5.0 |

### Hunger (derived-hardcore) ###

> AV: `Hunger` | AVC: `74`
>
> Derivation:<br>
> `Hunger = (1 * t) / fHCStarvationRate`<br>
> <sub>*\* Where `t` is real time in seconds.*</sub>
>
> Settings:
>
> | Config | `fHCStarvationRate` |
> | - | - |
> | Vanilla | 25.0 |
> | JSU | 12.5 |

### Sleep Deprivation (derived-hardcore) ###

> AV: `SleepDeprevation` | AVC: `75`<br>
> <sub>\* *lol typo, couldn't be me*</sub><br>
>
> Derivation:<br>
> `SleepDeprevation = (1 * t) / fHCSleepDeprivationRate`<br>
> <sub>*\* Where `t` is real time in seconds.*</sub>
>
> Settings:
>
> | Config | `fHCSleepDeprivationRate` |
> | - | - |
> | Vanilla | 50.0 |
> | JSU | 18.0 |

---------------

## Secondary Settings ##

### Big Guns (skill) ###

> AV: `BigGuns` | AVC: `33`<br>
>
> Derivation:<br>
> `BigGuns = fAVDSkillBigGunsBase + (END * fAVDSkillPrimaryBonusMult) + ceil(LCK * fAVDSkillLuckBonusMult)`
>
> Settings:
>
> | Config | `fAVDSkillBigGunsBase` |
> | - | - |
> | Vanilla | 2.0 |
> | JSU | 2.0 |

### Food Effects (derived) ###

> AV: `null` | AVC: `null`<br>
>
> Derivation:<br>
> `Potency = fMagicSurvivalSkillBase + (fMagicSurvivalSkillMult * (Survival / 100))`<br>
> <sub>*\* Where `Potency` is effect of the food item; **not** an ActorValue.*</sub>
>
> Settings:
>
> | Config | `fMagicSurvivalSkillBase` | `fMagicSurvivalSkillMult` |
> | - | - | - |
> | Vanilla | 1.0 | 2.0 |
> | JSU | 1.0 | 2.0 |

### Fatigue (derived) ###

> AV: `Fatigue` | AVC: `22`<br>
>
> Derivation:<br>
> `Fatigue = fAVDFatigueBase + (END * fAVDFatigueEnduranceMult) + (LVL * fAVDFatigueLevelMult)`
>
> Settings:
>
> | Config | `fAVDFatigueBase` | `fAVDFatigueEnduranceMult` | `fAVDFatigueLevelMult` | `fMinFatigue` |
> | - | - | - | - | - |
> | Vanilla | 90.0 | 20.0 | 10.0 | -30.0 |
> | JSU | 90.0 | 20.0 | 10.0 | -30.0 |
