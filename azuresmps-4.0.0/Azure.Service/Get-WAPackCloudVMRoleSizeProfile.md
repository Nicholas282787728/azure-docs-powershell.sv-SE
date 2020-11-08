---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 453AEA42-E29C-4FF2-9210-0DD88B77DC07
online version: ''
schema: 2.0.0
ms.openlocfilehash: 29c7f8bc814ddf5295064d89eeaf34c8e7274916
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099738"
---
# Get-WAPackCloudVMRoleSizeProfile

## Sammanfattning
Hämtar profil objekt för den virtuella dator rollen.

## FRÅGESYNTAXEN

### Tom (standard)
```
Get-WAPackCloudVMRoleSizeProfile [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### FromName
```
Get-WAPackCloudVMRoleSizeProfile [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Get-WAPackCloudVMRoleSizeProfile** hämtar den virtuella dator rollens storleks profil objekt för virtuella datorer.

## BESKRIVS

### Exempel 1: skaffa en profil för den virtuella dator rollen för en moln genom att använda ett namn
```
PS C:\> Get-WAPackCloudVMRoleSizeProfile -Name "Small"
```

Det här kommandot får storleks profilen liten.

### Exempel 2: Hämta alla storleks profiler för rollen virtuella dator roller
```
PS C:\> Get-WAPackCloudVMRoleSizeProfile
```

Det här kommandot får alla storleks profiler.

## MALLPARAMETRAR

### -Namn
Anger namnet på en profil för den virtuella dator rollen.

```yaml
Type: String
Parameter Sets: FromName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Profil
Anger den Azure-profil från vilken denna cmdlet läser.
Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.

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
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

## VÄRDEN

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Get-WAPackVM](./Get-WAPackVM.md)


