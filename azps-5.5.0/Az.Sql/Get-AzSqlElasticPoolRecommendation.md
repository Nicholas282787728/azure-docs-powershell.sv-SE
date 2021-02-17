---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: A1E19A66-CD70-467E-8C59-1F88453905A4
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlelasticpoolrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticPoolRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticPoolRecommendation.md
ms.openlocfilehash: 7e0d8e55b5a4ab3ab22081fde94bac10f4550730
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100222166"
---
# Get-AzSqlElasticPoolRecommendation

## SYNOPSIS
Får rekommendationerna om pooler med pooler av olika pooler.

## SYNTAX

```
Get-AzSqlElasticPoolRecommendation [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## BESKRIVNING
**Cmdleten Get-AzSqlElasticPoolRecommendation** får rekommendationerna om pooler av olika kvaliteter för en server.
Dessa rekommendationer omfattar följande värden:
- DatabaseCollection. Samling med databasnamn som tillhör poolen. 
- DatabaseDtuMin. DTU-garanti (Data Transmission Unit) för databaser i poolen med dataöverföring. 
 -- DatabaseDtuMax. DTU-ändpunkt för databaser i poolen med pooler för pooler med pooler. 
- Dtu. DTU-garanti för poolen med pooler. 
- StorageMb. Lagring i megabyte för poolen med pooler med pooler. 
- Utgåva. Version för poolen med pooler med pooler för pooler med pooler och pooler. De godtagbara värdena för den här parametern är: Basic, Standard och Premium. 
- IncludeAllDatabases. Anger om alla databaser i poolen med pooler för pooler returneras. 
- Namn. Namn på poolen med poolen med pooler.

## EXEMPEL

### Exempel 1: Få rekommendationer för en server
```
PS C:\>Get-AzSqlElasticPoolRecommendation -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

Det här kommandot får rekommendationerna om pooler med rekommendationer om poolen för servern Server01.

## PARAMETERS

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

### -ResourceGroupName
Anger namnet på resursgruppen som servern är tilldelad till.

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

### -Servernamn
Anger namnet på den server som cmdleten får rekommendationer för.

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

### -Bekräfta
Frågar dig om bekräftelse innan du kör cmdleten.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
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
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten stöder vanliga parametrar: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction och -WarningVariable. Mer information finns i [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INDATA

### System.String

## UTDATA

### Microsoft.Azure.Management.Sql.LegacySdk.Models.UpgradeRecomstyrningElasticPoolProperties

## ANTECKNINGAR

## RELATERADE LÄNKAR
