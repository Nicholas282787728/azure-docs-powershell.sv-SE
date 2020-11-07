---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
ms.assetid: 87A79215-5688-474D-822A-6B84B3D10E3F
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/remove-azcognitiveservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Remove-AzCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Remove-AzCognitiveServicesAccount.md
ms.openlocfilehash: ad3c5359d80f3133e6bb48ea73c1d6a93501288a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93754616"
---
# Remove-AzCognitiveServicesAccount

## Sammanfattning
Tar bort ett konto för kognitiva tjänster.

## FRÅGESYNTAXEN

```
Remove-AzCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Remove-AzCognitiveServicesAccount** tar bort det angivna kontot för kognitiva tjänster.

## BESKRIVS

### Exempel 1
Det här kommandot returnerar ingenting.

```powershell
PS C:\> Remove-AzCognitiveServicesAccount -ResourceGroupName cognitive-services-resource-group -name myluis
PS C:\>
```

## MALLPARAMETRAR

### -DefaultProfile
Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
Tvingar kommandot att köras utan att fråga efter bekräftelse.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Namn
Anger namnet på kontot som ska tas bort.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CognitiveServicesAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Anger namnet på resurs gruppen som är kopplat till det här kontot.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Bekräfta
Du uppmanas att bekräfta innan du kör cmdleten.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Visar vad som händer om cmdleten körs.
Cmdleten körs inte.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

### System. String

## VÄRDEN

### System. Void

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Get-AzCognitiveServicesAccount](./Get-AzCognitiveServicesAccount.md)

[New-AzCognitiveServicesAccount](./New-AzCognitiveServicesAccount.md)

[Set-AzCognitiveServicesAccount](./Set-AzCognitiveServicesAccount.md)


