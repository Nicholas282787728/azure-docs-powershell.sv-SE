---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 8632A865-D4CC-4AE5-8307-055CDD776D26
online version: ''
schema: 2.0.0
ms.openlocfilehash: a2b79ee50bb5097896c2a120a9b7316adb2146b5
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093436"
---
# Add-AzureWorkerRole

## Sammanfattning
Skapar nödvändiga filer och konfiguration för en anpassad arbets roll.

## FRÅGESYNTAXEN

```
Add-AzureWorkerRole [-TemplateFolder <String>] [-Name <String>] [-Instances <Int32>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
I det här avsnittet beskrivs cmdleten i 0.8.10-versionen av Microsoft Azure PowerShell-modulen.
För att få den version av modulen du använder, gå till Azure PowerShell-konsolen och skriv `(Get-Module -Name Azure).Version` .

Cmdleten **Add-AzureWorkerRole** skapar nödvändiga filer och konfigurationer, som ibland kallas scaffolding, för en anpassad arbets roll.

## BESKRIVS

### Exempel 1: skapa en enskild instans arbets roll
```
PS C:\> Add-AzureWorkerRole -Name MyWorkerRole
```

I det här exemplet läggs scaffolding för en arbets roll som heter MyWorkerRole till det aktuella programmet.

### Exempel 2: skapa en roll för flera instanser
```
PS C:\> Add-AzureWorkerRole MyWorkerRole -I 2
```

I det här exemplet läggs scaffolding till för en ny arbets roll som heter MyWorkerRole i det aktuella programmet, med antal roller på en roll instans.

### Exempel 3: skapa arbets roll med anpassade scaffolding
```
PS C:\> Add-AzureWorkerRole MyWorkerRole -TemplateFoldr .\MyWorkerRoleTemplate
```

I det här exemplet skapas en arbets roll med anpassade scaffolding.

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
Det här värdet bestämmer mappnamnet som innehåller scaffolding för det anpassade program som finns i arbets rollen.
Standardvärdet är WorkerRolenumber, där tal är antalet arbets roller i tjänsten.

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

### -TemplateFolder
Anger den scaffolding som ska användas för att skapa arbets rollen.

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

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

## VÄRDEN

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Add-AzureWebRole](./Add-AzureWebRole.md)

[New-AzureRoleTemplate](./New-AzureRoleTemplate.md)


