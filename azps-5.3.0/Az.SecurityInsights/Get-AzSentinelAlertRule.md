---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/get-azsentinelalertrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelAlertRule.md
ms.openlocfilehash: 02dc3b58d9cd4b4be58b83f36cc6e42e11008812
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98525602"
---
# Get-AzSentinelAlertRule

## Sammanfattning
Hämtar en analys (varnings regel).

## FRÅGESYNTAXEN

### WorkspaceScope (standard)
```
Get-AzSentinelAlertRule -ResourceGroupName <String> -WorkspaceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### AlertRuleId
```
Get-AzSentinelAlertRule -ResourceGroupName <String> -WorkspaceName <String> -AlertRuleId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ID
```
Get-AzSentinelAlertRule -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Get-AzSentinelAlertRule** får en analys (notifieringsregel) från den angivna arbets ytan.
Om du anger parametern *AlertRuleId* returneras ett enskilt **AlertRule** -objekt.
Om du inte anger parametern *AlertRuleId* returneras en matris med alla varnings regler på den angivna arbets ytan.
Du kan använda **AlertRule** -objektet för att uppdatera AlertRule, till exempel om du vill inaktivera **AlertRule**.

## BESKRIVS

### Exempel 1
```powershell
PS C:\> $AlertRules = Get-AzSentinelAlertRule -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName"
```

Det här exemplet får alla **AlertRules** på den angivna arbets ytan och lagrar dem sedan i $AlertRules variabel.

### Exempel 2
```powershell
PS C:\> $AlertRule = Get-AzSentinelAlertRule -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -AlertRuleId "MyAlertRuleId"
```

Det här exemplet får en **AlertRule** på den angivna arbets ytan och lagrar den sedan i $AlertRule variabel.

## MALLPARAMETRAR

### -AlertRuleId
ID för notifieringsregel.

```yaml
Type: System.String
Parameter Sets: AlertRuleId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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
Parameter Sets: WorkspaceScope, AlertRuleId
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
Parameter Sets: WorkspaceScope, AlertRuleId
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

### Microsoft. Azure. commands. SecurityInsights. Models. AlertRules. PSSentinelAlertRule
## ANMÄRKNINGAR

## RELATERADE LÄNKAR
