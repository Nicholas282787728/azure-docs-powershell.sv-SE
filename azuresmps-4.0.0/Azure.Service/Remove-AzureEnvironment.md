---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: 4B8B56B4-511B-45BD-9595-B47187C76E03
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5af23a3ef727aa54e8223b2d07e60c2d8dbc7b8d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099707"
---
# Remove-AzureEnvironment

## Sammanfattning
Tar bort en Azure-miljö från Windows PowerShell.

## FRÅGESYNTAXEN

```
Remove-AzureEnvironment -Name <String> [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Remove-AzureEnvironment** tar bort en Azure-miljö från din centrala profil så att Windows PowerShell inte hittar den.
Denna cmdlet tar inte bort miljön från Microsoft Azure eller ändrar den faktiska miljön på något sätt.

En Azure-miljö en oberoende distribution av Microsoft Azure, till exempel AzureCloud för globala Azure-och AzureChinaCloud för Azure som drivs av 21Vianet i Kina.
Du kan också skapa lokala Azure-miljöer med Azure Pack och WAPack cmdlets.
Mer information finns i [Azure Pack](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx) ( https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx) .

## BESKRIVS

### Exempel 1: ta bort en miljö
```
PS C:\> Remove-AzureEnvironment -Name ContosoEnv
```

Det här kommandot tar bort ContosoEnv-miljön från Windows PowerShell.

### Exempel 2: ta bort flera miljöer
```
PS C:\> Get-AzureEnvironment | Where-Object EnvironmentName -like "Contoso*" | ForEach-Object {Remove-AzureEnvironment -Name $_.EnvironmentName }
```

Det här kommandot tar bort miljöer vars namn börjar med "contoso" från Windows PowerShell.

## MALLPARAMETRAR

### -Force
Inaktiverar uppmaningen om att bekräfta.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Namn
Anger namnet på den miljö som ska tas bort.
Denna parameter är obligatorisk.
Det här parametervärdet är Skift läges känsligt.
Jokertecken är inte tillåtna.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Profil
Anger den Azure-profil från vilken denna cmdlet läser. Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.

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

### Ingen
Du kan ange indata för denna cmdlet efter egenskaps namn, men inte efter värde.

## VÄRDEN

### Ingen eller system. Boolean
Om du använder parametern *Passthru* returnerar denna cmdlet ett Boolean-värde.
Annars returnerar den inte några resultat.

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Add-AzureEnvironment](./Add-AzureEnvironment.md)

[Get-AzureEnvironment](./Get-AzureEnvironment.md)

[Set-AzureEnvironment](./Set-AzureEnvironment.md)


