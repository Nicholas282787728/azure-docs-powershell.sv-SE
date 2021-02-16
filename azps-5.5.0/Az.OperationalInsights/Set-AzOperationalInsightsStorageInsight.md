---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 010328F9-C878-4F16-AFD7-2135465A1968
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/set-azoperationalinsightsstorageinsight
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsStorageInsight.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsStorageInsight.md
ms.openlocfilehash: 53482eade80e1fdc3d719160185941741e447258
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100220766"
---
# Set-AzOperationalInsightsStorageInsight

## SYNOPSIS
Uppdaterar en lagringsinsikt.

## SYNTAX

### ByWorkspaceName (standard)
```
Set-AzOperationalInsightsStorageInsight [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [[-StorageAccountKey] <String>] [[-Tables] <String[]>] [[-Containers] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByWorkspaceObject
```
Set-AzOperationalInsightsStorageInsight [-Workspace] <PSWorkspace> [-Name] <String>
 [[-StorageAccountKey] <String>] [[-Tables] <String[]>] [[-Containers] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESKRIVNING
**Cmdleten Set-AzOperationalInsightsStorageInsight** ändrar konfigurationen av en Storage Insight.

## EXEMPEL

### Exempel 1: Ändra en lagringsinsikt efter namn
```
PS C:\>Set-AzOperationalInsightsStorageInsight -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "MyWorkspace" -Name "MyStorageInsight" -Tables @("WADWindowsEventLogsTable")
```

Det här kommandot ändrar tabellerna som lagringsinsikten med namnet MyStorageInsight läser upp.

### Exempel 2: Ändra en lagringsinsikt med hjälp av ett arbetsyteobjekt
```
PS C:\>$Workspace = Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"

PS C:\>Set-AzOperationalInsightsStorageInsight -Workspace $Workspace -Name "MyStorageInsight" -Containers @("wad-iis-logfiles")
```

Det första kommandot använder cmdleten Get-AzOperationalInsightsWorkspace för att få arbetsytan MyWorkspace och lagrar den sedan i $Workspace variabeln.
Det andra kommandot ändrar de behållare som lagringsinsikten med namnet MyStorageInsight läser upp.

## PARAMETERS

### -Behållare
Anger listan över behållare som tillhandahåller data.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Autentiseringsuppgifter, konto, klientorganisation och prenumeration som används för kommunikation med Azure

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

### -Name
Anger namnet på en lagringsinsikt.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Anger namnet på en Azure-resursgrupp som innehåller en arbetsyta.

```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageAccountKey
Anger åtkomstnyckeln för lagringskontot.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Tabeller
Anger listan med tabeller som innehåller data.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Workspace
Anger vilken arbetsyta som innehåller Lagringsinsikter.

```yaml
Type: Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace
Parameter Sets: ByWorkspaceObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -WorkspaceName
Anger namnet på en arbetsyta.

```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten stöder vanliga parametrar: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction och -WarningVariable. Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INDATA

### Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace

### System.String

### System.String[]

## UTDATA

### Microsoft.Azure.Commands.OperationalInsights.Models.PSStorageInsight

## ANTECKNINGAR

## RELATERADE LÄNKAR

[Azure Operational Insights-cmdlets](./Az.OperationalInsights.md)

[Get-AzOperationalInsightsWorkspace](./Get-AzOperationalInsightsWorkspace.md)


