---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/remove-azdatashare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShare.md
ms.openlocfilehash: 2679a3f63be3b7332020354e325e33573911334b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100211127"
---
# Remove-AzDataShare

## SYNOPSIS
Tar bort en dataresurs.

## SYNTAX

### ByFieldsParameterSet (standard)
```
Remove-AzDataShare -ResourceGroupName <String> -AccountName <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByResourceIdParameterSet
```
Remove-AzDataShare -ResourceId <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByObjectParameterSet
```
Remove-AzDataShare -InputObject <PSDataShare> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## BESKRIVNING
Cmdleten **Remove-AzDataShare** tar bort en dataresurs.

## EXEMPEL

### Exempel 1
```
PS C:\> Remove-AzDataShare -ResourceGroupName "ADS" -AccountName "WikiAds" -Name "AdsShare"
Are you sure you want to remove data share "AdsShare"? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

Med de här kommandona tas dataresursen med namnet AdsShare bort från Azure Data Share-kontot WikiAds. 

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

### -As Ent fån
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
Azure data share object' ''yaml Type: PSDataShare Parameter Sets: ByObjectParameterSet Aliases: 

Obligatoriskt: Sant läge: Namngivet standardvärde: Ingen acceptera pipelineindata: Sant (ByValue) Acceptera jokertecken: Falskt

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
Namn på Azure-dataresurs

yaml-typ: Uppsättningar av strängparameter: AvFieldsParameterSet-alias: 

Obligatoriskt: Sant läge: Namngivet standardvärde: Ingen acceptera rörledningsinmatning: Falskt acceptera jokertecken: Falskt

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

### -PassThru
Returobjekt (om det anges).

yaml-typ: Parameteruppsättningar av typen SwitchParameter: (Alla) alias: 

Obligatoriskt: Falsk position: Namngivet standardvärde: Ingen acceptera rörledningsinmatning: Falskt acceptera jokertecken: Falskt

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

### -ResourceGroupName
Resursgruppnamnet för azure-kontot för dataresurs

yaml-typ: Strängparameteruppsättningar: AvFieldsParameterSet-alias: 

Obligatoriskt: Sant läge: Namngivet standardvärde: Ingen acceptera rörledningsinmatning: Falskt acceptera jokertecken: Falskt

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
Resurs-ID för Azure-dataresursen

yaml-typ: Uppsättningar av strängparameter: ByResourceIdParameterSet-alias: 

Obligatoriskt: Sant läge: Namngivet standardvärde: Ingen acceptera pipelineindata: Sant (ByPropertyName) Acceptera jokertecken: Falskt

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

### -Bekräfta
Frågar dig om bekräftelse innan du kör cmdleten.

yaml-typ: Parameteruppsättningar av typen SwitchParameter: (Alla) alias: cf

Obligatoriskt: Falsk position: Namngivet standardvärde: Ingen acceptera rörledningsinmatning: Falskt acceptera jokertecken: Falskt

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

yaml-typ: Parameteruppsättningar av typen SwitchParameter: (Alla) alias: wi

Obligatoriskt: Falsk position: Namngivet standardvärde: Ingen acceptera rörledningsinmatning: Falskt acceptera jokertecken: Falskt




yaml Type: Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare Parameter Sets: ByObjectParameterSet Aliases:

Obligatoriskt: Sant läge: Namngivet standardvärde: Ingen acceptera pipelineindata: Sant (ByValue) Acceptera jokertecken: Falskt

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

### Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare

## UTDATA

### System.Boolean

## ANTECKNINGAR

## RELATERADE LÄNKAR
