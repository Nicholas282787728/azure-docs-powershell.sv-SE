---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-Azmanagementgroup/
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Remove-AzManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Remove-AzManagementGroup.md
ms.openlocfilehash: 9ac7717769cef1ad147ea122ddedde3efd1e389f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93923837"
---
# Remove-AzManagementGroup

## Sammanfattning
Tar bort en hanterings grupp

## FRÅGESYNTAXEN

### GroupOperations (standard)
```
Remove-AzManagementGroup [-GroupName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ManagementGroupObject
```
Remove-AzManagementGroup -InputObject <PSManagementGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Remove-AzManagementGroup** tar bort en hanterings grupp.

## BESKRIVS

### Exempel 1 – ta bort en hanterings grupp
```
PS C:\> Remove-AzManagementGroup -GroupName "TestGroup"
```

### Exempel 2 – ta bort en hanterings grupp efter rör PSManagementGroup-objekt
```
PS C:\> Get-Remove-AzManagementGroup -GroupName "TestGroup" | Remove-AzManagementGroup
```

## MALLPARAMETRAR

### -DefaultProfile
Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Grupp namn
Hanterings grupp-ID

```yaml
Type: System.String
Parameter Sets: GroupOperations
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Infoga objekt från get-samtalet

```yaml
Type: Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup
Parameter Sets: ManagementGroupObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -PassThru
Retur `true` vid lyckad körning

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
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

### Microsoft. Azure. commands. Resources. Models. ManagementGroups. PSManagementGroup
Parametrar: InputObject (ByValue)

## VÄRDEN

### System. Boolean

## ANMÄRKNINGAR

## RELATERADE LÄNKAR
