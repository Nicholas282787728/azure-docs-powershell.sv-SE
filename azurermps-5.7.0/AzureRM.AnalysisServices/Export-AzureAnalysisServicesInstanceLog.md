---
external help file: Microsoft.Azure.Commands.AnalysisServices.Dataplane.dll-Help.xml
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.analysisservices/export-azureanalysisservicesinstancelog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices.Dataplane/help/Export-AzureAnalysisServicesInstanceLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices.Dataplane/help/Export-AzureAnalysisServicesInstanceLog.md
ms.openlocfilehash: e93e38ef2914635cab61bf225c0d905d011ae643
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574961"
---
# Export-AzureAnalysisServicesInstance

## Sammanfattning
Exporterar en logg från en instans av Analysis Services-servern i den aktuella inloggade miljön som angiven i Add-AzureAnalysisServicesAccount kommando

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

```
Export-AzureAnalysisServicesInstanceLog [-Instance] <String> [-OutputPath] <String> [-WhatIf] [-Force]
```

## PROBLEMBESKRIVNING
Export-AzureAnalysisServicesInstance cmdlet exporterar loggen från en instans av Azure Analysis Services-servern till filen

## BESKRIVS

### Exempel 1
```
PS C:\>Export-AzureAnalysisServicesInstanceLog -Instance testserver -OuptutPath C:\path\to\log\testserver.log
```

Det här kommandot exporterar logg från servern ' testserver ' i den miljö som anges i kommandot Add-AzureAnalysisServicesAccount och sparar den i filen som anges i OutputPath ' C:\path\to\log\testserver.log '

## MALLPARAMETRAR

### -Instance
Namn på Analysis Services-serverinstansen

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OutputPath
Sökväg till fil som ska exporteras

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
Skriv över filen om den finns utan att fråga

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

## KOSTNADS

### Ingen
Denna cmdlet accepterar inte indata.

## VÄRDEN

## ANMÄRKNINGAR
Alias: Export-AzureAsInstanceLog

## RELATERADE LÄNKAR

