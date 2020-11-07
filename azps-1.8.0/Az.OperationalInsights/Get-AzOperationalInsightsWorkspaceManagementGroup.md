---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: F29E0B9C-2479-44FB-B196-EAF97B69E6A6
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightsworkspacemanagementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsWorkspaceManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsWorkspaceManagementGroup.md
ms.openlocfilehash: 679a6c434b037913ab5abb68f65b48c324d49b8b
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/13/2020
ms.locfileid: "93755163"
---
# Get-AzOperationalInsightsWorkspaceManagementGroup

## Sammanfattning
Hämtar information om hanterings grupper som är anslutna till en arbets yta.

## FRÅGESYNTAXEN

```
Get-AzOperationalInsightsWorkspaceManagementGroup [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Get-AzOperationalInsightsWorkspaceManagementGroup** visar de hanterings grupper som är anslutna till en arbets yta.

## BESKRIVS

### Exempel 1: Hämta hanterings grupper efter arbets ytans namn
```
PS C:\>Get-AzOperationalInsightsWorkspaceManagementGroup -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"
```

Det här kommandot får hanterings grupperna för arbets ytan med namnet min arbets yta i resurs gruppen som heter ContosoResourceGroup.

### Exempel 2: få hanterings grupper genom att använda pipeline
```
PS C:\>Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" | Get-AzOperationalInsightsWorkspaceManagementGroup
```

Det här kommandot använder cmdleten Get-AzOperationalInsightsWorkspace för att hämta arbets ytan med namnet min arbets yta och skickar sedan arbets ytan till den aktuella cmdleten, som hämtar hanterings grupperna för den arbets ytan.

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

### -Namn
Anger arbets ytans namn.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Anger namnet på en Azure-adressresurs.

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

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

### System. String

## VÄRDEN

### Microsoft. Azure. commands. OperationalInsights. Models. PSManagementGroup

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Cmdlets för Azure Operational Insights](/powershell/module/az.operationalinsights)

[Get-AzOperationalInsightsWorkspace](./Get-AzOperationalInsightsWorkspace.md)


