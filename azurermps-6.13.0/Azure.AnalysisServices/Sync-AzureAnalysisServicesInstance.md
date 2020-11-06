---
external help file: Microsoft.Azure.Commands.AnalysisServices.Dataplane.dll-Help.xml
Module Name: Azure.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.analysisservices/sync-azureanalysisservicesinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices.Dataplane/help/Sync-AzureAnalysisServicesInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices.Dataplane/help/Sync-AzureAnalysisServicesInstance.md
ms.openlocfilehash: 732eb92a46fa7e69ba5274398de648c16142ae75
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574108"
---
# Sync-AzureAnalysisServicesInstance

## Sammanfattning

Synkroniserar en angiven databas på den angivna instansen av Analysis Services-servern till alla instanser av den aktuella inloggade miljön enligt vad som anges i Add-AzureAnalysisServicesAccount kommando

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

```
Sync-AzureAnalysisServicesInstance [-Instance] <String> [-Database] <String> [-PassThru] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## PROBLEMBESKRIVNING

Sync-AzureAnalysisServicesInstance-cmdleten synkroniserar en angiven databas på den angivna instansen av Analysis Services-servern till alla förekomster av den aktuella inloggade miljön enligt vad som anges i Add-AzureAnalysisServicesAccount kommando

## BESKRIVS

### Exempel 1

```
PS C:\>Sync-AzureAnalysisServicesInstance -Instance asazure://westus.asazure.windows.net/contoso -Database SalesOrders
```

Det här kommandot synkroniserar databasen med namnet SalesOrders i servern med namnet "contoso" i miljön westus.asazure.windows.net förutsatt att användaren har loggat in på den här enviroment med kommandot Add-AzureAnalysisServicesAccount.

## MALLPARAMETRAR

### -Databas

Identitet för databasen som ska synkroniseras

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Instance

Namn på Analysis Services-serverinstansen som ska startas om

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -PassThru

Om du anger detta returneras sant om kommandot lyckades.

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

### System. String
Parametrar: databas (ByValue), instans (ByValue)

## VÄRDEN

### Microsoft. Azure. commands. AnalysisServices. Dataplane. Models. ScaleOutServerDatabaseSyncDetails

## ANMÄRKNINGAR

Alias: Sync-AzureAsInstance

## RELATERADE LÄNKAR
