---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: E499868E-A745-4CA4-A717-C33C3B94A2C8
online version: ''
schema: 2.0.0
ms.openlocfilehash: b80071bb82ebbb960be5b5b4fcc854dc47c9ed9d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099222"
---
# New-AzureRoleTemplate

## Sammanfattning
Skapar roller för webb och arbetare.

## FRÅGESYNTAXEN

### Webroll
```
New-AzureRoleTemplate [-Web] [-Output <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### WorkerRole
```
New-AzureRoleTemplate [-Worker] [-Output <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
I det här avsnittet beskrivs cmdleten i 0.8.10-versionen av Microsoft Azure PowerShell-modulen.
För att få den version av modulen du använder, gå till Azure PowerShell-konsolen och skriv `(Get-Module -Name Azure).Version` .

Cmdleten **New-AzureRoleTemplate** skapar roller för webb och arbetare.

## BESKRIVS

### Exempel 1: skapa en mall för webb roller
```
PS C:\> New-AzureRoleTemplate -Web
```

I det här exemplet skapas en ny mall för webb roller i en mapp med namnet WebRoleTemplate i den aktuella katalogen.

### Exempel 2: skapa en mall för arbets tagare
```
PS C:\> New-AzureRoleTemplate -Worker
```

I det här exemplet skapas en ny roll mal len i en mapp med namnet WebRoleTemplate i den aktuella katalogen.

### Exempel 3: skapa en rollprovider i en anpassad katalog
```
PS C:\> New-AzureRoleTemplate -Web -Output C:\MyWebRoleTemplate
```

I det här exemplet skapas en ny webb Rolls mal len i katalogen MyWebRoleTemplate i stället för i den aktuella katalogen.

## MALLPARAMETRAR

### -Utdata
Anger utgångs Sök vägen för den genererade mallen.

```yaml
Type: String
Parameter Sets: (All)
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

### -Webb
Anger att du vill skapa en mall för webb roller.

```yaml
Type: SwitchParameter
Parameter Sets: WebRole
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Arbeta
Anger att du vill skapa en mall för en arbets roll.

```yaml
Type: SwitchParameter
Parameter Sets: WorkerRole
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

## VÄRDEN

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Add-AzureWebRole](./Add-AzureWebRole.md)

[Add-AzureWorkerRole](./Add-AzureWorkerRole.md)


