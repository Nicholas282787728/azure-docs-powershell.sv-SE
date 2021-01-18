---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/remove-azblueprintassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Remove-AzBlueprintAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Remove-AzBlueprintAssignment.md
ms.openlocfilehash: 40452c250b58edf4d1e45f54c953dee8c433c436
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98524656"
---
# Remove-AzBlueprintAssignment

## Sammanfattning
Ta bort en skiss tilldelning från ett abonnemang eller en hanterings grupp.

## FRÅGESYNTAXEN

### BySubscriptionAndName (standard)
```
Remove-AzBlueprintAssignment [-Name] <String> [[-SubscriptionId] <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByManagementGroupAndName
```
Remove-AzBlueprintAssignment [-Name] <String> [-ManagementGroupId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### DeleteBlueprintAssignmentByObject
```
Remove-AzBlueprintAssignment -InputObject <PSBlueprintAssignment> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Ta bort en skiss som har tilldelats till ett abonnemang.

## BESKRIVS

### Exempel 1
```powershell
PS C:\> Remove-AzBlueprintAssignment -Name "myAssignment" -Subscription "00000000-1111-0000-1111-000000000000" -Confirm
```

Ta bort den skiss tilldelning som anges av namnet från det angivna abonnemanget. Cmdleten uppmanas att bekräfta innan kommandot körs.

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

### -InputObject
Objekt för skiss.

```yaml
Type: Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintAssignment
Parameter Sets: DeleteBlueprintAssignmentByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ManagementGroupId
ID för hanterings gruppen där skiss tilldelningen har sparats.

```yaml
Type: System.String
Parameter Sets: ByManagementGroupAndName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Namn
Namn på skiss tilldelningen.

```yaml
Type: System.String
Parameter Sets: BySubscriptionAndName, ByManagementGroupAndName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PassThru
När den är aktive rad returnerar cmdleten ett objekt som representerar den borttagna skiss uppgiften. Denna cmdlet genererar som standard inga utdata.

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

### -SubscriptionId
Abonnemangs-ID som skiss uppgiften distribueras till.

```yaml
Type: System.String
Parameter Sets: BySubscriptionAndName
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
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
Visar vad som händer om cmdleten körs.
Cmdleten körs inte.

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
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## KOSTNADS

### System. String

### Microsoft. Azure. commands. skissa. Models. PSBlueprintAssignment []

## VÄRDEN

### System. Object
## ANMÄRKNINGAR

## RELATERADE LÄNKAR
