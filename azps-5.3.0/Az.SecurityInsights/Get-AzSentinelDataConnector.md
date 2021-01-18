---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/get-azsentineldataconnector
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelDataConnector.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelDataConnector.md
ms.openlocfilehash: e2505d53b0443bd048fb5d15df225adb0cba0980
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98525590"
---
# Get-AzSentinelDataConnector

## Sammanfattning
Skaffa en data koppling.

## FRÅGESYNTAXEN

### WorkspaceScope (standard)
```
Get-AzSentinelDataConnector -ResourceGroupName <String> -WorkspaceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### DataConnectorId
```
Get-AzSentinelDataConnector -ResourceGroupName <String> -WorkspaceName <String> -DataConnectorId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ID
```
Get-AzSentinelDataConnector -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Get-AzSentinelDataConnector** hämtar en data koppling från den angivna arbets ytan.
Om du anger parametern *DataConnectorId* returneras ett enskilt **DataConnector** -objekt.
Om du inte anger parametern *DataConnectorId* returneras en matris med alla data kopplingar på den angivna arbets ytan.
Du kan använda **DataConnector** -objektet för att uppdatera data anslutningen, till exempel om du vill inaktivera funktionen **DataConnector**.

## BESKRIVS

### Exempel 1
```powershell
PS C:\> $DataConnectors = Get-AzSentinelDataConnector -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName"
```

Det här exemplet får alla **DataConnectors** på den angivna arbets ytan och lagrar dem sedan i $DataConnectors variabel.

### Exempel 2
```powershell
PS C:\> $DataConnector = Get-AzSentinelDataConnector -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -DataConnectorId "MyDataConnectorId"
```

Det här exemplet får en **DataConnector** på den angivna arbets ytan och lagrar den sedan i $DataConnector variabel.

## MALLPARAMETRAR

### -DataConnectorId
ID för data anslutning.

```yaml
Type: System.String
Parameter Sets: DataConnectorId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### -ResourceGroupName
Resurs grupps namn.

```yaml
Type: System.String
Parameter Sets: WorkspaceScope, DataConnectorId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceId
Resurs-ID.

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -WorkspaceName
Namn på arbets ytan.

```yaml
Type: System.String
Parameter Sets: WorkspaceScope, DataConnectorId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## KOSTNADS

### System. String
## VÄRDEN

### Microsoft. Azure. commands. SecurityInsights. Models. DataConnectors. PSSentinelDataConnector
## ANMÄRKNINGAR

## RELATERADE LÄNKAR
