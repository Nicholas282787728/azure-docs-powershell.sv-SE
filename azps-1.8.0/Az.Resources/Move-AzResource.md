---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 60BED40A-EEA4-4667-93E9-8A9B35037726
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/move-azresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Move-AzResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Move-AzResource.md
ms.openlocfilehash: d885c4084390a46104267d7d39cb9e4f8a7a0924
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/08/2020
ms.locfileid: "93758454"
---
# Move-AzResource

## Sammanfattning
Flyttar en resurs till en annan resurs grupp eller prenumeration.

## FRÅGESYNTAXEN

```
Move-AzResource -DestinationResourceGroupName <String> [-DestinationSubscriptionId <Guid>]
 -ResourceId <String[]> [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Move-AzResource** flyttar befintliga resurser till en annan resurs grupp.
Resurs gruppen kan vara i ett annat abonnemang.

## BESKRIVS

### Exempel 1: flytta en resurs till en resurs grupp
```
PS C:\>$Resource = Get-AzResource -ResourceType "Microsoft.ClassicCompute/storageAccounts" -ResourceName "ContosoStorageAccount"
PS C:\> Move-AzResource -ResourceId $Resource.ResourceId -DestinationResourceGroupName "ResourceGroup14"
```

Det första kommandot får en resurs som heter ContosoStorageAccount med hjälp av Get-AzResource cmdlet och lagrar sedan resursen i $Resource-variabeln.
Det andra kommandot flyttar resursen till resurs gruppen med namnet ResourceGroup14.
Kommandot identifierar den resurs som ska flyttas genom att använda egenskapen **ResourceID** för $Resource.

## MALLPARAMETRAR

### -ApiVersion
Anger vilken version av API för Resource provider som ska användas.
Om du inte anger en version använder denna cmdlet den senaste tillgängliga versionen.

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

### -DestinationResourceGroupName
Anger namnet på den resurs grupp där cmdleten flyttas till resurserna.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TargetResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DestinationSubscriptionId
Anger ID för den prenumeration som den här cmdleten flyttar resurser till.

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: (All)
Aliases: Id, SubscriptionId

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### -För
Visar att denna cmdlet betraktar för hands version API-versioner när den automatiskt avgör vilken version som ska användas.

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

### -ResourceId
Anger en matris med ID: n för de resurser som den här cmdleten flyttar.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
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

### System. Nullable ' 1 [[system. GUID, system. Private. CoreLib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = 7cec85d7bea7798e]]

### System. string []

## VÄRDEN

### System. Boolean

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Get-AzResource](./Get-AzResource.md)

[New-AzResource](./New-AzResource.md)

[Remove-AzResource](./Remove-AzResource.md)

[Set-AzResource](./Set-AzResource.md)


