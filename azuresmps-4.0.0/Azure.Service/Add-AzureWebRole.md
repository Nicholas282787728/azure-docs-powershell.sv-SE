---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: FB5CD696-108D-4A3E-8983-1C6562E8795A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 25ade8ccf395d37ab0856742fe473a6508c9d63b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093437"
---
# Add-AzureWebRole

## Sammanfattning
Lägger till en webb roll.

## FRÅGESYNTAXEN

```
Add-AzureWebRole [-TemplateFolder <String>] [-Name <String>] [-Instances <Int32>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## PROBLEMBESKRIVNING
I det här avsnittet beskrivs cmdleten i 0.8.10-versionen av Microsoft Azure PowerShell-modulen.
För att få den version av modulen du använder, gå till Azure PowerShell-konsolen och skriv `(Get-Module -Name Azure).Version` .

Cmdleten **Add-AzureWebRole** lägger till en webb jobb roll.

## BESKRIVS

### Exempel 1: lägga till en standard roll
```
PS C:\> Add-AzureWebRole
```

Det här kommandot Lägg till webb roll med standard konfigurationen för Webrole1 som namnet och en enda instans.

### Exempel 2: lägga till en roll med ett namn
```
PS C:\> Add-AzureWebRole -Name "MyWebRole"
```

Det här kommandot lägger till en enskild webb roll med namnet MyWebRole i det aktuella programmet.

### Exempel 3: lägga till en roll med namn och instans antal
```
PS C:\> Add-AzureWebRole -Name "MyWebRole" -Instance 2
```

Det här kommandot lägger till en webb roll med namnet MyWebRole i det aktuella programmet.
Cmdleten har en roll instans räkning på 2.

### Exempel 4: lägga till en roll med ett namn och en mall
```
PS C:\> Add-AzureWebRole -Name "MyWebRole" -TemplateFolder ".\MyWebTemplateFolder"
```

Det här kommandot lägger till en enskild webb roll med namnet MyWebRole i det aktuella programmet.
Kommandot anger en mapp med namnet MyWebTemplateFolder som en scaffolding-mall.

## MALLPARAMETRAR

### -Instanser
Anger antalet instanser.

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
Anger namnet på webb rollen.

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
Anger mappen för mallen.

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

[Add-AzureWorkerRole](./Add-AzureWorkerRole.md)

[New-AzureRoleTemplate](./New-AzureRoleTemplate.md)


