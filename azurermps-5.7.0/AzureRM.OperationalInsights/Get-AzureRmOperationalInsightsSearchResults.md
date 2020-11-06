---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 438F549D-1AF6-49FE-83AC-B45BAB701AB6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/get-azurermoperationalinsightssearchresults
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsSearchResults.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsSearchResults.md
ms.openlocfilehash: f4f0ee7a7ab98835e438ffd3d993d0d2bfd7833c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575581"
---
# <span data-ttu-id="f2788-101">Get-AzureRmOperationalInsightsSearchResults</span><span class="sxs-lookup"><span data-stu-id="f2788-101">Get-AzureRmOperationalInsightsSearchResults</span></span>

## <span data-ttu-id="f2788-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f2788-102">SYNOPSIS</span></span>
<span data-ttu-id="f2788-103">Returnerar Sök resultat baserat på angivna parametrar.</span><span class="sxs-lookup"><span data-stu-id="f2788-103">Returns search results based on the specified parameters.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f2788-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f2788-104">SYNTAX</span></span>

```
Get-AzureRmOperationalInsightsSearchResults [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [[-Top] <Int64>] [[-PreHighlight] <String>] [[-PostHighlight] <String>] [[-Query] <String>]
 [[-Start] <DateTime>] [[-End] <DateTime>] [[-Id] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f2788-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f2788-105">DESCRIPTION</span></span>
<span data-ttu-id="f2788-106">Cmdleten **Get-AzureRmOperationalInsightsSearchResults** returnerar Sök resultaten baserat på angivna parametrar.</span><span class="sxs-lookup"><span data-stu-id="f2788-106">The **Get-AzureRmOperationalInsightsSearchResults** cmdlet returns the search results based on the specified parameters.</span></span>

<span data-ttu-id="f2788-107">Du kan komma åt statusen för sökningen i egenskapen metadata för det returnerade objektet.</span><span class="sxs-lookup"><span data-stu-id="f2788-107">You can access the status of the search in the Metadata property of the returned object.</span></span>
<span data-ttu-id="f2788-108">Om statusen är väntande har sökningen inte slutförts och resultatet kommer från arkivet.</span><span class="sxs-lookup"><span data-stu-id="f2788-108">If the status is Pending, then the search has not completed, and the results will be from the archive.</span></span>

<span data-ttu-id="f2788-109">Du kan hämta Sök resultaten från egenskapen Value för det returnerade objektet.</span><span class="sxs-lookup"><span data-stu-id="f2788-109">You can retrieve the results of the search from the Value property of the returned object.</span></span>

## <span data-ttu-id="f2788-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f2788-110">EXAMPLES</span></span>

### <span data-ttu-id="f2788-111">Exempel 1: Hämta Sök resultat med en fråga</span><span class="sxs-lookup"><span data-stu-id="f2788-111">Example 1: Get search results using a query</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsSearchResults -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -Query "Type=Event" -Top 100
```

<span data-ttu-id="f2788-112">Det här kommandot får alla Sök resultat med hjälp av en fråga.</span><span class="sxs-lookup"><span data-stu-id="f2788-112">This command gets all search results by using a query.</span></span>

### <span data-ttu-id="f2788-113">Exempel 2: Hämta Sök resultat med ett ID</span><span class="sxs-lookup"><span data-stu-id="f2788-113">Example 2: Get search results using an ID</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsSearchResults -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -Id "ContosoSearchId"
```

<span data-ttu-id="f2788-114">Det här kommandot får Sök resultat genom att använda ett ID.</span><span class="sxs-lookup"><span data-stu-id="f2788-114">This command gets search results by using an ID.</span></span>

### <span data-ttu-id="f2788-115">Exempel 3: vänta tills en sökning har slutförts innan resultat visas</span><span class="sxs-lookup"><span data-stu-id="f2788-115">Example 3: Wait for a search to complete before displaying results</span></span>
```
PS C:\>$error.clear()
$response = @{}
$StartTime = Get-Date

$resGroup = "ContosoResourceGroup"
$wrkspace = "ContosoWorkspace"

# Sample Query
$query = "Type=Event"

# Get Initial response
$response = Get-AzureRmOperationalInsightsSearchResults -WorkspaceName $wrkspace -ResourceGroupName $resGroup -Query $query -Top 15000
$elapsedTime = $(get-date) - $script:StartTime
Write-Host "Elapsed: " $elapsedTime "Status: " $response.Metadata.Status

# Split and extract request Id
$reqIdParts = $response.Id.Split("/")
$reqId = $reqIdParts[$reqIdParts.Count -1]

# Poll if pending
while($response.Metadata.Status -eq "Pending" -and $error.Count -eq 0) {
    $response = Get-AzureRmOperationalInsightsSearchResults -WorkspaceName $wrkspace -ResourceGroupName $resGroup -Id $reqId
    $elapsedTime = $(get-date) - $script:StartTime
    Write-Host "Elapsed: " $elapsedTime "Status: " $response.Metadata.Status
}

Write-Host "Returned " $response.Value.Count " documents"
Write-Host $error
```

<span data-ttu-id="f2788-116">Det här manuset startar en sökning och väntar tills det är färdigt innan resultatet visas.</span><span class="sxs-lookup"><span data-stu-id="f2788-116">This script starts a search and waits until it completes before displaying the results.</span></span>

## <span data-ttu-id="f2788-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f2788-117">PARAMETERS</span></span>

### <span data-ttu-id="f2788-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2788-118">-DefaultProfile</span></span>
<span data-ttu-id="f2788-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="f2788-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2788-120">-Slut</span><span class="sxs-lookup"><span data-stu-id="f2788-120">-End</span></span>
<span data-ttu-id="f2788-121">Slutet av det efterfrågade tidsintervallet.</span><span class="sxs-lookup"><span data-stu-id="f2788-121">End of the queried time range.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2788-122">-ID</span><span class="sxs-lookup"><span data-stu-id="f2788-122">-Id</span></span>
<span data-ttu-id="f2788-123">Om ett ID anges hämtas Sök resultatet för detta ID med de ursprungliga frågeparametrarna.</span><span class="sxs-lookup"><span data-stu-id="f2788-123">If an id is given, the search results for that id will be retrieved using the original query parameters.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2788-124">-PostHighlight</span><span class="sxs-lookup"><span data-stu-id="f2788-124">-PostHighlight</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2788-125">-För markering</span><span class="sxs-lookup"><span data-stu-id="f2788-125">-PreHighlight</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2788-126">-Fråga</span><span class="sxs-lookup"><span data-stu-id="f2788-126">-Query</span></span>
<span data-ttu-id="f2788-127">Sök frågan som ska utföras.</span><span class="sxs-lookup"><span data-stu-id="f2788-127">The search query that will be executed.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2788-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2788-128">-ResourceGroupName</span></span>
<span data-ttu-id="f2788-129">Namnet på resurs gruppen som innehåller arbets ytan.</span><span class="sxs-lookup"><span data-stu-id="f2788-129">The name of the resource group that contains the workspace.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2788-130">-Start</span><span class="sxs-lookup"><span data-stu-id="f2788-130">-Start</span></span>
<span data-ttu-id="f2788-131">Början av det efterfrågade tidsintervallet.</span><span class="sxs-lookup"><span data-stu-id="f2788-131">Start of the queried time range.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2788-132">-Överst</span><span class="sxs-lookup"><span data-stu-id="f2788-132">-Top</span></span>
<span data-ttu-id="f2788-133">Maximalt antal resultat som ska returneras, begränsat till 5000.</span><span class="sxs-lookup"><span data-stu-id="f2788-133">The maximum number of results to be returned, limited to 5000.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: 10
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2788-134">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="f2788-134">-WorkspaceName</span></span>
<span data-ttu-id="f2788-135">Anger ett namn på en arbets yta.</span><span class="sxs-lookup"><span data-stu-id="f2788-135">Specifies a workspace name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2788-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2788-136">CommonParameters</span></span>
<span data-ttu-id="f2788-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f2788-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2788-138">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f2788-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2788-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f2788-139">INPUTS</span></span>

### <span data-ttu-id="f2788-140">Ingen</span><span class="sxs-lookup"><span data-stu-id="f2788-140">None</span></span>
<span data-ttu-id="f2788-141">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="f2788-141">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f2788-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f2788-142">OUTPUTS</span></span>

### <span data-ttu-id="f2788-143">PSSearchGetSearchResultsResponse</span><span class="sxs-lookup"><span data-stu-id="f2788-143">PSSearchGetSearchResultsResponse</span></span>
<span data-ttu-id="f2788-144">**PSSearchGetSearchResultsResponse** -objektet innehåller en värde-egenskap som innehåller de poster som returneras från sökning i JSON-format och ett metadataobjekt som innehåller information om Sök resultatet.</span><span class="sxs-lookup"><span data-stu-id="f2788-144">The **PSSearchGetSearchResultsResponse** object includes a Value property that includes the records returned from the search in JSON format and a metadata object that includes information about the results of the search.</span></span>

## <span data-ttu-id="f2788-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f2788-145">NOTES</span></span>

## <span data-ttu-id="f2788-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f2788-146">RELATED LINKS</span></span>

[<span data-ttu-id="f2788-147">Get-AzureRmOperationalInsightsSavedSearchResults</span><span class="sxs-lookup"><span data-stu-id="f2788-147">Get-AzureRmOperationalInsightsSavedSearchResults</span></span>](./Get-AzureRmOperationalInsightsSavedSearchResults.md)


