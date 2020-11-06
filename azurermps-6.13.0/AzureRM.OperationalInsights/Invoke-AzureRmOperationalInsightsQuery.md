---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/invoke-azurermoperationalinsightsquery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Invoke-AzureRmOperationalInsightsQuery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Invoke-AzureRmOperationalInsightsQuery.md
ms.openlocfilehash: 6672bb6f788b06896fdfe9cde44c68639077e5c5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576142"
---
# <span data-ttu-id="02628-101">Invoke-AzureRmOperationalInsightsQuery</span><span class="sxs-lookup"><span data-stu-id="02628-101">Invoke-AzureRmOperationalInsightsQuery</span></span>

## <span data-ttu-id="02628-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="02628-102">SYNOPSIS</span></span>
<span data-ttu-id="02628-103">Returnerar Sök resultat baserat på angivna parametrar.</span><span class="sxs-lookup"><span data-stu-id="02628-103">Returns search results based on the specified parameters.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="02628-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="02628-104">SYNTAX</span></span>

### <span data-ttu-id="02628-105">ByWorkspaceId (standard)</span><span class="sxs-lookup"><span data-stu-id="02628-105">ByWorkspaceId (Default)</span></span>
```
Invoke-AzureRmOperationalInsightsQuery -WorkspaceId <String> -Query <String> [-Timespan <TimeSpan>]
 [-Wait <Int32>] [-IncludeRender] [-IncludeStatistics] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="02628-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="02628-106">ByWorkspaceObject</span></span>
```
Invoke-AzureRmOperationalInsightsQuery -Workspace <PSWorkspace> -Query <String> [-Timespan <TimeSpan>]
 [-Wait <Int32>] [-IncludeRender] [-IncludeStatistics] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="02628-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="02628-107">DESCRIPTION</span></span>
<span data-ttu-id="02628-108">Cmdleten **Invoke-AzureRmOperationalInsightsQuery** returnerar Sök resultaten baserat på angivna parametrar.</span><span class="sxs-lookup"><span data-stu-id="02628-108">The **Invoke-AzureRmOperationalInsightsQuery** cmdlet returns the search results based on the specified parameters.</span></span>
<span data-ttu-id="02628-109">Du kan komma åt statusen för sökningen i egenskapen metadata för det returnerade objektet.</span><span class="sxs-lookup"><span data-stu-id="02628-109">You can access the status of the search in the Metadata property of the returned object.</span></span>
<span data-ttu-id="02628-110">Om statusen är väntande har sökningen inte slutförts och resultatet kommer från arkivet.</span><span class="sxs-lookup"><span data-stu-id="02628-110">If the status is Pending, then the search has not completed, and the results will be from the archive.</span></span>
<span data-ttu-id="02628-111">Du kan hämta Sök resultaten från egenskapen Value för det returnerade objektet.</span><span class="sxs-lookup"><span data-stu-id="02628-111">You can retrieve the results of the search from the Value property of the returned object.</span></span>

## <span data-ttu-id="02628-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="02628-112">EXAMPLES</span></span>

### <span data-ttu-id="02628-113">Exempel 1: Hämta Sök resultat med en fråga</span><span class="sxs-lookup"><span data-stu-id="02628-113">Example 1: Get search results using a query</span></span>
```
PS C:\> $queryResults = Invoke-AzureRmOperationalInsightsQuery -WorkspaceId "63613592-b6f7-4c3d-a390-22ba13102111" -Query "union * | take 10"
PS C:\> $queryResults.Results
...
```

<span data-ttu-id="02628-114">När $queryResults. Results innehåller alla resulterande rader från frågan.</span><span class="sxs-lookup"><span data-stu-id="02628-114">Once invoked, $queryResults.Results will contain all of the resulting rows from your query.</span></span>

### <span data-ttu-id="02628-115">Exempel 2: konvertera $results. Resultat IEnumberable till en matris</span><span class="sxs-lookup"><span data-stu-id="02628-115">Example 2: Convert $results.Result IEnumberable to an array</span></span>
```
PS C:\> $queryResults = Invoke-AzureRmOperationalInsightsQuery -WorkspaceId "63613592-b6f7-4c3d-a390-22ba13102111" -Query "union * | take 10"
PS C:\> $resultsArray = [System.Linq.Enumerable]::ToArray($results.Results)
...
```

<span data-ttu-id="02628-116">Vissa frågor kan leda till att mycket stora data uppsättningar returneras.</span><span class="sxs-lookup"><span data-stu-id="02628-116">Some queries can result in very large data sets being returned.</span></span> <span data-ttu-id="02628-117">På grund av det här är standard beteendet för cmdleten att returnera en IEnumerable för att minska minnes kostnaderna.</span><span class="sxs-lookup"><span data-stu-id="02628-117">Because of this, the default behavior of the cmdlet is to return an IEnumerable to reduce memory costs.</span></span> <span data-ttu-id="02628-118">Om du föredrar att ha en matris med resultat kan du använda tillägget LINQ enumerable. ToArray () för att konvertera IEnumerable till en matris.</span><span class="sxs-lookup"><span data-stu-id="02628-118">If you'd prefer to have an array of results, you can use the LINQ Enumerable.ToArray() extension method to convert the IEnumerable to an array.</span></span>

### <span data-ttu-id="02628-119">Exempel 3: Hämta Sök resultat med en fråga under en viss tids period</span><span class="sxs-lookup"><span data-stu-id="02628-119">Example 3: Get search results using a query over a specific timeframe</span></span>
```
PS C:\> $queryResults = Invoke-AzureRmOperationalInsightsQuery -WorkspaceId "63613592-b6f7-4c3d-a390-22ba13102111" -Query "union * | take 10" -Timespan (New-TimeSpan -Hours 24)
PS C:\> $queryResults.Results
...
```

<span data-ttu-id="02628-120">Resultatet från den här frågan begränsas till de senaste 24 timmarna.</span><span class="sxs-lookup"><span data-stu-id="02628-120">The results from this query will be limited to the past 24 hours.</span></span>

### <span data-ttu-id="02628-121">Exempel 4: ta med rendera & statistik i frågeresultatet</span><span class="sxs-lookup"><span data-stu-id="02628-121">Example 4: Include render & statistics in query result</span></span>
```
PS C:\> $queryResults = Invoke-AzureRmOperationalInsightsQuery -WorkspaceId "63613592-b6f7-4c3d-a390-22ba13102111" -Query "union * | take 10" -IncludeRender -IncludeStatistics
PS C:\> $queryResults.Results
...
PS C:\> $queryResults.Render
...
PS C:\> $queryResults.Statistics
...
```

<span data-ttu-id="02628-122">Se [https://dev.loganalytics.io/documentation/Using-the-API/RequestOptions](https://dev.loganalytics.io/documentation/Using-the-API/RequestOptions) Mer information om åter givnings-och statistik informationen.</span><span class="sxs-lookup"><span data-stu-id="02628-122">See [https://dev.loganalytics.io/documentation/Using-the-API/RequestOptions](https://dev.loganalytics.io/documentation/Using-the-API/RequestOptions) for details on the render and statistics info.</span></span>

## <span data-ttu-id="02628-123">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="02628-123">PARAMETERS</span></span>

### <span data-ttu-id="02628-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="02628-124">-AsJob</span></span>
<span data-ttu-id="02628-125">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="02628-125">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="02628-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02628-126">-DefaultProfile</span></span>
<span data-ttu-id="02628-127">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="02628-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02628-128">-IncludeRender</span><span class="sxs-lookup"><span data-stu-id="02628-128">-IncludeRender</span></span>
<span data-ttu-id="02628-129">Om du anger ett värde tas åter givnings information för metriska frågor i svaret.</span><span class="sxs-lookup"><span data-stu-id="02628-129">If specified, rendering information for metric queries will be included in the response.</span></span>

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

### <span data-ttu-id="02628-130">-IncludeStatistics</span><span class="sxs-lookup"><span data-stu-id="02628-130">-IncludeStatistics</span></span>
<span data-ttu-id="02628-131">Om du anger en fråga kommer statistik att ingå i svaret.</span><span class="sxs-lookup"><span data-stu-id="02628-131">If specified, query statistics will be included in the response.</span></span>

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

### <span data-ttu-id="02628-132">-Fråga</span><span class="sxs-lookup"><span data-stu-id="02628-132">-Query</span></span>
<span data-ttu-id="02628-133">Fråga att köra.</span><span class="sxs-lookup"><span data-stu-id="02628-133">The query to execute.</span></span>

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

### <span data-ttu-id="02628-134">– TimeSpan</span><span class="sxs-lookup"><span data-stu-id="02628-134">-Timespan</span></span>
<span data-ttu-id="02628-135">TimeSpan som ska bindas till frågan med.</span><span class="sxs-lookup"><span data-stu-id="02628-135">The timespan to bound the query by.</span></span>

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

### <span data-ttu-id="02628-136">-Vänta</span><span class="sxs-lookup"><span data-stu-id="02628-136">-Wait</span></span>
<span data-ttu-id="02628-137">Placerar en övre gräns för hur mycket tid som servern ska spendera bearbetningen av frågan.</span><span class="sxs-lookup"><span data-stu-id="02628-137">Puts an upper bound on the amount of time the server will spend processing the query.</span></span>
<span data-ttu-id="02628-138">Se https://dev.loganalytics.io/documentation/Using-the-API/Timeouts</span><span class="sxs-lookup"><span data-stu-id="02628-138">See: https://dev.loganalytics.io/documentation/Using-the-API/Timeouts</span></span>

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

### <span data-ttu-id="02628-139">-Arbets yta</span><span class="sxs-lookup"><span data-stu-id="02628-139">-Workspace</span></span>
<span data-ttu-id="02628-140">Arbets ytan</span><span class="sxs-lookup"><span data-stu-id="02628-140">The workspace</span></span>

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

### <span data-ttu-id="02628-141">-WorkspaceId</span><span class="sxs-lookup"><span data-stu-id="02628-141">-WorkspaceId</span></span>
<span data-ttu-id="02628-142">Arbetsyte-ID.</span><span class="sxs-lookup"><span data-stu-id="02628-142">The workspace ID.</span></span>

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

### <span data-ttu-id="02628-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02628-143">CommonParameters</span></span>
<span data-ttu-id="02628-144">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="02628-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02628-145">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="02628-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02628-146">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="02628-146">INPUTS</span></span>

### <span data-ttu-id="02628-147">Microsoft. Azure. commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="02628-147">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>
<span data-ttu-id="02628-148">Parametrar: arbets yta (ByValue)</span><span class="sxs-lookup"><span data-stu-id="02628-148">Parameters: Workspace (ByValue)</span></span>

## <span data-ttu-id="02628-149">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="02628-149">OUTPUTS</span></span>

### <span data-ttu-id="02628-150">Microsoft. Azure. commands. OperationalInsights. Models. PSQueryResponse</span><span class="sxs-lookup"><span data-stu-id="02628-150">Microsoft.Azure.Commands.OperationalInsights.Models.PSQueryResponse</span></span>

## <span data-ttu-id="02628-151">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="02628-151">NOTES</span></span>

## <span data-ttu-id="02628-152">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="02628-152">RELATED LINKS</span></span>
