---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 7190C668-6A0C-4E1D-9B5A-0CEEF53E3F85
online version: ''
schema: 2.0.0
ms.openlocfilehash: 93573caf43a6c711e1aa1308c851c82faaef5bcd
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099619"
---
# Add-AzureNodeWorkerRole

## Sammanfattning
Skapar de filer och mappar som behövs för att ett Node.js program ska finnas med i molnet via node.exe

## FRÅGESYNTAXEN

```
Add-AzureNodeWorkerRole [-Name <String>] [-Instances <Int32>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
I det här avsnittet beskrivs cmdleten i 0.8.10-versionen av Microsoft Azure PowerShell-modulen.
För att få den version av modulen du använder, gå till Azure PowerShell-konsolen och skriv `(Get-Module -Name Azure).Version` .

Cmdleten **Add-AzureNodeWorkerRole** skapar nödvändiga filer och mappar, som ibland kallas för scaffolding, för ett Node.js-program som ska finnas i molnet via node.exe.

## BESKRIVS

### Exempel 1: roll för en instans arbetare
```
PS C:\> Add-AzureWorkerRole MyWorkerRole
```

I det här exemplet läggs scaffolding för en arbets roll som heter **MyWorkerRole** till det aktuella programmet.

### Exempel 2: roll för flera instanser
```
PS C:\> Add-AzureNodeWorkerRole MyWorkerRole -I 2
```

I det här exemplet läggs scaffolding för en arbets roll som heter **MyWorkerRole** till det aktuella programmet med en roll instans räkning på 2.

## MALLPARAMETRAR

### -Instanser
Anger antalet roll instanser för denna arbets roll.
Standardvärdet är 1.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: i

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Namn
Anger namnet på arbets rollen.
Värdet bestämmer mappnamnet som innehåller scaffolding för den node.js tjänst som är värd för arbets rollen.
Standard är WorkerRole1.

```yaml
Type: String
Parameter Sets: (All)
Aliases: n

Required: False
Position: Named
Default value: None
Accept pipeline input: False
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

[Add-AzureNodeWebRole](./Add-AzureNodeWebRole.md)

[New-AzureServiceProject](./New-AzureServiceProject.md)


