---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/invoke-azoperationalinsightsquery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Invoke-AzOperationalInsightsQuery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Invoke-AzOperationalInsightsQuery.md
ms.openlocfilehash: 0b2b27855e0c8248f0e7ceb9f1c096370a54e2fb
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100236406"
---
# Invoke-AzOperationalInsightsQuery

## SYNOPSIS
Returnerar sökresultat baserat på angivna parametrar.

## SYNTAX

### ByWorkspaceId (standard)
```
Invoke-AzOperationalInsightsQuery -WorkspaceId <String> -Query <String> [-Timespan <TimeSpan>] [-Wait <Int32>]
 [-IncludeRender] [-IncludeStatistics] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByWorkspaceObject
```
Invoke-AzOperationalInsightsQuery -Workspace <PSWorkspace> -Query <String> [-Timespan <TimeSpan>]
 [-Wait <Int32>] [-IncludeRender] [-IncludeStatistics] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## BESKRIVNING
Cmdleten **Invoke-AzOperationalInsightsQuery** returnerar sökresultatet baserat på angivna parametrar.
Du kan komma åt statusen för sökningen i egenskapen Metadata för det returnerade objektet.
Om statusen är Väntande har sökningen inte slutförts och resultatet kommer från arkivet.
Du kan hämta sökresultatet från egenskapen Värde för det returnerade objektet.
Läs mer om allmänna frågebegränsningar här: https://docs.microsoft.com/en-us/azure/azure-monitor/service-limits#log-queries-and-language .

## EXEMPEL

### Exempel 1: Få sökresultat med hjälp av en fråga
```
PS C:\> $queryResults = Invoke-AzOperationalInsightsQuery -WorkspaceId "63613592-b6f7-4c3d-a390-22ba13102111" -Query "union * | take 10"
PS C:\> $queryResults.Results
...
```

När den anropas $queryResults.Results innehåller alla resulterande rader från frågan.

### Exempel 2: Konvertera $results. Result IEnumerable to an array
```
PS C:\> $queryResults = Invoke-AzOperationalInsightsQuery -WorkspaceId "63613592-b6f7-4c3d-a390-22ba13102111" -Query "union * | take 10"
PS C:\> $resultsArray = [System.Linq.Enumerable]::ToArray($queryResults.Results)
...
```

Vissa frågor kan resultera i att mycket stora datauppsättningar returneras. På grund av detta är standardbeteendet för cmdleten att returnera en IEnumerbar för att minska minneskostnader. Om du föredrar att ha en matris med resultat kan du använda tilläggsmetoden LINQ Enumerable.ToArray() för att konvertera den IEnumerable till en matris.

### Exempel 3: Få sökresultat med hjälp av en fråga över en viss tidsperiod
```
PS C:\> $queryResults = Invoke-AzOperationalInsightsQuery -WorkspaceId "63613592-b6f7-4c3d-a390-22ba13102111" -Query "union * | take 10" -Timespan (New-TimeSpan -Hours 24)
PS C:\> $queryResults.Results
...
```

Resultaten från den här frågan kommer att vara begränsade till de senaste 24 timmarna.

### Exempel 4: Inkludera rendering & statistik i frågeresultatet
```
PS C:\> $queryResults = Invoke-AzOperationalInsightsQuery -WorkspaceId "63613592-b6f7-4c3d-a390-22ba13102111" -Query "union * | take 10" -IncludeRender -IncludeStatistics
PS C:\> $queryResults.Results
...
PS C:\> $queryResults.Render
...
PS C:\> $queryResults.Statistics
...
```

Mer [https://dev.loganalytics.io/documentation/Using-the-API/RequestOptions](https://dev.loganalytics.io/documentation/Using-the-API/RequestOptions) information om återgivningen och statistikinformation finns i

## PARAMETERS

### -As Ent
Kör cmdleten i bakgrunden

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
Autentiseringsuppgifterna, kontot, klientorganisationen och prenumerationen som används för kommunikation med Azure.

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

### -IncludeRender
Om den anges inkluderas renderingsinformation för metriska frågor i svaret.

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

### -IncludeStatistics
Om den anges inkluderas frågestatistik i svaret.

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

### -Query
Frågan som ska utföras.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Timespan
Tidsspann som frågan begränsas av.

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Wait
Sätter en övre gräns för hur lång tid servern kommer att ägna åt bearbetningen av frågan.
Mer information: https://dev.loganalytics.io/documentation/Using-the-API/Timeouts

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Workspace
Arbetsytan

```yaml
Type: Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace
Parameter Sets: ByWorkspaceObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -WorkspaceId
Arbetsyte-ID.

```yaml
Type: System.String
Parameter Sets: ByWorkspaceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten stöder vanliga parametrar: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction och -WarningVariable. Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INDATA

### Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace

## UTDATA

### Microsoft.Azure.Commands.OperationalInsights.Models.PSQueryResponse

## ANTECKNINGAR

## RELATERADE LÄNKAR
