---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azserviceendpointpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzServiceEndpointPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzServiceEndpointPolicyDefinition.md
ms.openlocfilehash: 3677b580629360a9f38d808af8df9ec0694bcc61
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93748414"
---
# Add-AzServiceEndpointPolicyDefinition

## Sammanfattning
Lägger till en princip definition för tjänste slut punkter till en angiven princip.

## FRÅGESYNTAXEN

```
Add-AzServiceEndpointPolicyDefinition -Name <String> -ServiceEndpointPolicy <PSServiceEndpointPolicy>
 [-Description <String>] [-ServiceResource <String[]>] [-Service <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Add-AzServiceEndpointPolicyDefinition** lägger till en definition för tjänste slut punkter till principen.

## BESKRIVS

### Exempel 1: uppdaterar en princip definition för tjänste slut punkter i en policy för tjänst slut punkter
```
$policydef= New-AzServiceEndpointPolicyDefinition -Name "ServiceEndpointPolicyDefinition1" -ResourceGroupName "ResourceGroup01" -Service "Microsoft.Storage" -ServiceResources "subscriptions/sub1" -Description "New Definition"
```

Det här kommandot uppdaterade policy definitionen för tjänste slut punkten med namnet ServiceEndpointPolicyDefinition1, service Microsoft. Storage, tjänst resurser prenumerationer/sub1 och beskrivning "ny definition" som tillhör resurs gruppen som heter ResourceGroup01 och lagrar den i $policydef variabeln.

## MALLPARAMETRAR

### -DefaultProfile
Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.

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

### -Beskrivning
Beskrivning av definitionen

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Namn
Namnet på princip definitionen för tjänste slut punkten

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Service
Namn på tjänsten

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServiceEndpointPolicy
ServiceEndpointPolicy

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ServiceResource
Lista över tjänst resurser

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
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
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Visar vad som händer om cmdleten körs. Cmdleten körs inte.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

### Microsoft. Azure. commands. Networks. Models. PSServiceEndpointPolicy

## VÄRDEN

### Microsoft. Azure. commands. Networks. Models. PSServiceEndpointPolicy

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Get-AzServiceEndpointPolicyDefinition](./Get-AzServiceEndpointPolicyDefinition.md)

[New-AzServiceEndpointPolicyDefinition](./New-AzServiceEndpointPolicyDefinition.md)

[Remove-AzServiceEndpointPolicyDefinition](./Remove-AzServiceEndpointPolicyDefinition.md)

[Set-AzServiceEndpointPolicyDefinition](./Set-AzServiceEndpointPolicyDefinition.md)
