---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/start-azdatasharesubscriptionsynchronization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Start-AzDataShareSubscriptionSynchronization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Start-AzDataShareSubscriptionSynchronization.md
ms.openlocfilehash: bbbcab1e4355667681acf1cc09a51ec6d6174103
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100220158"
---
# Start-AzDataShareSubscriptionSynchronization

## SYNOPSIS
Initierar synkronisering av en delningsprenumeration. En delningsprenumeration kan anges med hjälp av dess resurs-ID eller namn.

## SYNTAX

### ByFieldsParameterSet (standard)
```
Start-AzDataShareSubscriptionSynchronization -ResourceGroupName <String> -AccountName <String>
 -ShareSubscriptionName <String> -SynchronizationMode <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByResourceIdParameterSet
```
Start-AzDataShareSubscriptionSynchronization -SynchronizationMode <String> -ResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByObjectParameterSet
```
Start-AzDataShareSubscriptionSynchronization -InputObject <PSDataShareSubscription> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## BESKRIVNING
**Cmdleten Start-AzDataShareSubscriptionSynchronization** initierar synkronisering för en delningsprenumeration

## EXEMPEL

### Exempel 1
```
PS C:\> Start-AzDataShareSubscriptionSynchronization -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareSubscriptionName "AdsShareSubscription" -SynchronizationMode Incremental

Confirm
AdsShareSubscription
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y

durationMs        : 231869
endTime           : 7/9/2019 11:44:41 PM
message           :
startTime         : 7/9/2019 11:40:53 PM
status            : Succeeded
synchronizationId : 20a4416b-b33b-4539-a908-71dc8ef698fb
```

Dessa kommandon initierar synkroniseringen för en delningsdelbeskrivning med namnet AdsShareSubscription i kontot WikiAds. 

## PARAMETERS

### -AccountName
Azure Data Share-kontonamn

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -As Ent
{{Fill As En beskrivning}}

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

### -DefaultProfile
Autentiseringsuppgifter, konto, klientorganisation och prenumeration som används för kommunikation med Azure.

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
Prenumerationsobjekt för Azure-dataresurs


```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscription
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ResourceGroupName
Resursgruppnamnet för azure-kontot för dataresurs

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceId
Resurs-ID för Azure Share-prenumerationen

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ShareSubscriptionName
Prenumerationsnamn för Azure-dataresurs

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SynchronizationMode
Synkroniseringsläge (FullSync eller stegvis)

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Bekräfta
Frågar dig om bekräftelse innan du kör cmdleten.

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
Visar vad som skulle hända om cmdleten körs.
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
Den här cmdleten stöder vanliga parametrar: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction och -WarningVariable. Mer information finns i [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INDATA

### System.String

### Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscription

## UTDATA

### Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscriptionSynchronization

## ANTECKNINGAR

## RELATERADE LÄNKAR
