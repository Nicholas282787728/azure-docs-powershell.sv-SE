---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbaccountregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBAccountRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBAccountRegion.md
ms.openlocfilehash: bfbbc0b4d5fbaac1dc6ad5f18af2cb201e5124c8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94260100"
---
# <span data-ttu-id="318f2-101">Update-AzCosmosDBAccountRegion</span><span class="sxs-lookup"><span data-stu-id="318f2-101">Update-AzCosmosDBAccountRegion</span></span>

## <span data-ttu-id="318f2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="318f2-102">SYNOPSIS</span></span>
<span data-ttu-id="318f2-103">Uppdatera regioner i ett CosmosDB-konto.</span><span class="sxs-lookup"><span data-stu-id="318f2-103">Update Regions of a CosmosDB Account.</span></span>

## <span data-ttu-id="318f2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="318f2-104">SYNTAX</span></span>

### <span data-ttu-id="318f2-105">ByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="318f2-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBAccountRegion -ResourceGroupName <String> -Name <String> [-Location <String[]>]
 [-LocationObject <PSLocation[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="318f2-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="318f2-106">ByResourceIdParameterSet</span></span>
```
Update-AzCosmosDBAccountRegion [-Location <String[]>] [-LocationObject <PSLocation[]>] -ResourceId <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="318f2-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="318f2-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBAccountRegion [-Location <String[]>] [-LocationObject <PSLocation[]>]
 -InputObject <PSDatabaseAccountGetResults> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="318f2-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="318f2-108">DESCRIPTION</span></span>
<span data-ttu-id="318f2-109">Uppdatera regioner i ett CosmosDB-konto.</span><span class="sxs-lookup"><span data-stu-id="318f2-109">Update Regions of a CosmosDB Account.</span></span> <span data-ttu-id="318f2-110">Platsen kan tillhandahållas antingen som ett objekt av typen PSLocation eller som strängar med plats namnet ordnade efter prioritet för redundans.</span><span class="sxs-lookup"><span data-stu-id="318f2-110">Location can be provided either as an object of type PSLocation or as strings of Location Name ordered by failover priority.</span></span>
<span data-ttu-id="318f2-111">LocationObject parameter förväntar sig att listan med aktuella platser (failover prioritiies) läggs till av de nya LocationObjects som motsvarar nya platser som ska läggas till.</span><span class="sxs-lookup"><span data-stu-id="318f2-111">LocationObject parameter expects the list of current locations (failover prioritiies included) appended by the new LocationObjects corresponding to new locations to be added.</span></span>
<span data-ttu-id="318f2-112">Parametern location förväntar sig en lista över aktuell plats (ordnad efter prioritet för redundans) och de nya platserna.</span><span class="sxs-lookup"><span data-stu-id="318f2-112">Location parameter expects the list of current location(ordered by failover priority) and the new locations.</span></span> <span data-ttu-id="318f2-113">Observera att vi inte har stöd för att lägga till regioner.</span><span class="sxs-lookup"><span data-stu-id="318f2-113">Please note, we only support Addition of Regions.</span></span> <span data-ttu-id="318f2-114">Ange plats eller LocationObject.</span><span class="sxs-lookup"><span data-stu-id="318f2-114">Please provide either Location or LocationObject.</span></span>

## <span data-ttu-id="318f2-115">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="318f2-115">EXAMPLES</span></span>

### <span data-ttu-id="318f2-116">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="318f2-116">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBAccountRegion -ResourceGroupName rg1 -Name dbname -Location "location1, location2"

Kind                          : GlobalDocumentDB
ProvisioningState             : Succeeded
DocumentEndpoint              : https://dbname.documents.azure.com:443/
DatabaseAccountOfferType      : Standard
IpRangeFilter                 :
IsVirtualNetworkFilterEnabled : False
EnableAutomaticFailover       : False
ConsistencyPolicy             : Microsoft.Azure.Management.CosmosDB.Fluent.Models.ConsistencyPolicy
Capabilities                  : {}
WriteLocations                : {dbname-location1}
ReadLocations                 : {dbname-location2}
FailoverPolicies              : {dbname-location1, dbname-location2}
VirtualNetworkRules           : {}
EnableMultipleWriteLocations  : False
Location                      : location1
Tags                          : {}
Id                            : /subscriptions/{subscriptionid}/resourceGroups/rg1/providers/Microsoft.DocumentDB/databaseAccounts/dbname
Name                          : dbname
Type                          : Microsoft.DocumentDB/databaseAccounts
```

## <span data-ttu-id="318f2-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="318f2-117">PARAMETERS</span></span>

### <span data-ttu-id="318f2-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="318f2-118">-AsJob</span></span>
<span data-ttu-id="318f2-119">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="318f2-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="318f2-120">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="318f2-120">-Confirm</span></span>
<span data-ttu-id="318f2-121">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="318f2-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="318f2-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="318f2-122">-DefaultProfile</span></span>
<span data-ttu-id="318f2-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="318f2-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="318f2-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="318f2-124">-InputObject</span></span>
<span data-ttu-id="318f2-125">ResourceId för resursen.</span><span class="sxs-lookup"><span data-stu-id="318f2-125">ResourceId of the resource.</span></span>

```yaml
Type: PSDatabaseAccountGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="318f2-126">-Plats</span><span class="sxs-lookup"><span data-stu-id="318f2-126">-Location</span></span>
<span data-ttu-id="318f2-127">Namn på platsen som ska läggas till.</span><span class="sxs-lookup"><span data-stu-id="318f2-127">Name of the location to be added.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="318f2-128">-LocationObject</span><span class="sxs-lookup"><span data-stu-id="318f2-128">-LocationObject</span></span>
<span data-ttu-id="318f2-129">Lägga till en plats i Cosmos DB-databasnamn.</span><span class="sxs-lookup"><span data-stu-id="318f2-129">Add a location to the Cosmos DB database account.</span></span> <span data-ttu-id="318f2-130">Matris med PSLocation-objekt.</span><span class="sxs-lookup"><span data-stu-id="318f2-130">Array of PSLocation objects.</span></span>

```yaml
Type: PSLocation[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="318f2-131">-Namn</span><span class="sxs-lookup"><span data-stu-id="318f2-131">-Name</span></span>
<span data-ttu-id="318f2-132">Namn på Cosmos DB-databas.</span><span class="sxs-lookup"><span data-stu-id="318f2-132">Name of the Cosmos DB database account.</span></span>

```yaml
Type: String
Parameter Sets: ByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="318f2-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="318f2-133">-ResourceGroupName</span></span>
<span data-ttu-id="318f2-134">Namn på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="318f2-134">Name of resource group.</span></span>

```yaml
Type: String
Parameter Sets: ByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="318f2-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="318f2-135">-ResourceId</span></span>
<span data-ttu-id="318f2-136">ResourceId för resursen.</span><span class="sxs-lookup"><span data-stu-id="318f2-136">ResourceId of the resource.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="318f2-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="318f2-137">-WhatIf</span></span>
<span data-ttu-id="318f2-138">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="318f2-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="318f2-139">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="318f2-139">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="318f2-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="318f2-140">CommonParameters</span></span>
<span data-ttu-id="318f2-141">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="318f2-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="318f2-142">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="318f2-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="318f2-143">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="318f2-143">INPUTS</span></span>

### <span data-ttu-id="318f2-144">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="318f2-144">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="318f2-145">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="318f2-145">OUTPUTS</span></span>

### <span data-ttu-id="318f2-146">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="318f2-146">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="318f2-147">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="318f2-147">NOTES</span></span>

## <span data-ttu-id="318f2-148">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="318f2-148">RELATED LINKS</span></span>
