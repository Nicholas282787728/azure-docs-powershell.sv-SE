---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 4682807D-34E8-4057-8894-36820447067B
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightsworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsWorkspace.md
ms.openlocfilehash: a2e0bc21546dad414ee8782acd0a1505ed1e5489
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/14/2021
ms.locfileid: "100399132"
---
# New-AzOperationalInsightsWorkspace

## SYNOPSIS
Skapar en arbetsyta eller återställer en mjuk borttagna arbetsyta.

## SYNTAX

```
New-AzOperationalInsightsWorkspace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-Sku] <String>] [[-Tag] <Hashtable>] [[-RetentionInDays] <Int32>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [[-PublicNetworkAccessForIngestion] <String>]
 [[-PublicNetworkAccessForQuery] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## BESKRIVNING
Cmdleten **New-AzOperationalInsightsWorkspace** skapar en arbetsyta i den angivna resursgruppen och -platsen. Eller återställa en mjuk borttagna arbetsytor.

## EXEMPEL

### Exempel 1: Skapa en arbetsyta efter namn
```
PS C:\>New-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" -Location "East US" -Sku "Standard"
```

Med det här kommandot skapas en standardarbetsyta för SKU med namnet MyWorkspace i resursgruppen ContosoResourceGroup.

### Exempel 2: Skapa en arbetsyta och länka den till ett befintligt konto
```
PS C:\>$OILinkTargets = Get-AzOperationalInsightsLinkTargets

PS C:\>$OILinkTargets[0] | New-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" -Sku "Standard"
```

Det första kommandot använder cmdleten Get-AzOperationalInsightsLinkTargets få driftsinformationslänkmål och lagrar dem sedan i $OILinkTargets variabeln.
Det andra kommandot skickar det första kontolänkmålet i $OILinkTargets till cmdleten **New-AzOperationalInsightsWorkspace** med hjälp av pipelineoperatorn.
Med kommandot skapas en standardarbetsyta för SKU med namnet MyWorkspace som är kopplad till det första kontot för driftsinformation i $OILinkTargets.

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

### -Force
Tvingar kommandot att köras utan att användaren uppmanas att bekräfta.

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

### -Plats
Anger platsen där arbetsytan ska skapas, till exempel Öst- eller Västeuropa.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name
Anger namnet på arbetsytan.

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

### -PublicNetworkAccessForIngestion
Nätverksåtkomsttypen för åtkomst till arbetsytan igestion. Värdet ska vara Aktiverat eller Inaktiverat

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PublicNetworkAccessForQuery
Nätverksåtkomsttypen för åtkomst till arbetsytefråga. Värdet ska vara Aktiverat eller Inaktiverat

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Anger namnet på en Azure-resursgrupp.
Arbetsytan skapas i den här resursgruppen.

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

### -RetentionInDays
Arbetsytans datalagring i dagar. 730 dagar är det högsta tillåtna värdet för alla andra SKU:er.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SKU
Anger tjänstnivån för arbetsytan. Mer information om vilket värde du bör använda finns i https://docs.microsoft.com/en-us/azure/azure-monitor/platform/manage-cost-storage#legacy-pricing-tiers .
Giltiga värden är:
- kostnadsfritt
- pergb2018
- pernode
- premium
- fristående
- standard

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Tag
Resurstaggarna för arbetsytan.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
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

### System.Nullable'1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]

### System.Collections.Hashtable

### System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]

## UTDATA

### Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace

## ANTECKNINGAR

En ny prissättningsmodell har släppts. Om du är en CSP innebär det att du måste använda "fristående" för SKU. Bakom kulisserna ändras sKU:n till pergb2018. Mer information finns i följande avsnitt: https://docs.microsoft.com/en-us/azure/monitoring-and-diagnostics/monitoring-usage-and-estimated-costs#new-pricing-model

## RELATERADE LÄNKAR

[Azure Operational Insights-cmdlets](./Az.OperationalInsights.md)



