---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 02396628-5E3E-49A6-8377-3F6DC488FEF8
online version: ''
schema: 2.0.0
ms.openlocfilehash: ee948161f101b83a4892441286b760a044e64358
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/14/2021
ms.locfileid: "100405830"
---
# Get-AzureSiteRecoveryProtectionContainer

## SYNOPSIS
Får skyddsbehållare för ett Site Recovery-valv.

## SYNTAX

### Standard (standard)
```
Get-AzureSiteRecoveryProtectionContainer [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### ById
```
Get-AzureSiteRecoveryProtectionContainer -Id <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### ByName
```
Get-AzureSiteRecoveryProtectionContainer -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## BESKRIVNING
Cmdleten **Get-AzureSiteRecoveryProtectionContainer** får skyddsbehållare för det aktuella Azure Site Recovery-valvet.
En skyddsbehållare är en logisk behållare för skyddade objekt, till exempel virtuella maskiner.
Skyddsprinciper definierar replikeringsinställningar för skyddade objekt och kan associeras med en skyddsbehållare och tillämpas på en skyddad enhet.

## EXEMPEL

### Exempel 1: Hämta skyddade behållare
```
PS C:\> Get-AzureSiteRecoveryProtectionContainer
Name                        : PrimaryCloud
ID                          : fd00d920-79e4-4f2d-a282-a779c0cecb7f_ce995917-c962-45d0-b7f3-9f408a4e1429
FabricObjectId              : fd00d920-79e4-4f2d-a282-a779c0cecb7f
FabricType                  : VMM
Type                        : VMM
ServerId                    : fd00d920-79e4-4f2d-a282-a779c0cecb7f
Role                        : Primary
AvailableProtectionProfiles : {ab01dcbe-9da0-4c31-9564-d6904cfadfde, ad388147-83de-4d2f-a09d-fa46c626747e}
```

Det här kommandot hämtar de skyddade behållarna för det aktuella valvet.

## PARAMETERS

### -Id
Anger ID för en skyddad behållare som ska hämtas.

```yaml
Type: String
Parameter Sets: ById
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Anger namnet på en skyddsbehållare som ska hämtas.

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Profile
Anger den Azure-profil som cmdleten läser upp.
Om du inte anger en profil läser den här cmdleten från den lokala standardprofilen.

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten stöder vanliga parametrar: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction och -WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INDATA

## UTDATA

## ANTECKNINGAR

## RELATERADE LÄNKAR




