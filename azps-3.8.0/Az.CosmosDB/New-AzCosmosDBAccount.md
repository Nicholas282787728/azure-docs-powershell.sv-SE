---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBAccount.md
ms.openlocfilehash: 76df37703882e799eb42542cd08d105f62787419
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94090291"
---
# <span data-ttu-id="0fc67-101">New-AzCosmosDBAccount</span><span class="sxs-lookup"><span data-stu-id="0fc67-101">New-AzCosmosDBAccount</span></span>

## <span data-ttu-id="0fc67-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0fc67-102">SYNOPSIS</span></span>
<span data-ttu-id="0fc67-103">Skapa ett nytt CosmosDB-konto.</span><span class="sxs-lookup"><span data-stu-id="0fc67-103">Create a new CosmosDB Account.</span></span>

## <span data-ttu-id="0fc67-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0fc67-104">SYNTAX</span></span>

```
New-AzCosmosDBAccount -ResourceGroupName <String> -Name <String> [-DefaultConsistencyLevel <String>]
 [-EnableAutomaticFailover] [-EnableMultipleWriteLocations] [-EnableVirtualNetwork] [-IpRangeFilter <String[]>]
 [-Location <String[]>] [-LocationObject <PSLocation[]>] [-MaxStalenessIntervalInSeconds <Int32>]
 [-MaxStalenessPrefix <Int32>] [-Tag <Hashtable>] [-VirtualNetworkRule <String[]>]
 [-VirtualNetworkRuleObject <PSVirtualNetworkRule[]>] [-ApiKind <String>] [-PublicNetworkAccess <String>]
 [-DisableKeyBasedMetadataWriteAccess] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0fc67-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0fc67-105">DESCRIPTION</span></span>
<span data-ttu-id="0fc67-106">Skapa ett nytt CosmosDB-konto i angiven ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="0fc67-106">Create a new CosmosDB Account in the given ResourceGroup.</span></span>

## <span data-ttu-id="0fc67-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0fc67-107">EXAMPLES</span></span>

### <span data-ttu-id="0fc67-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="0fc67-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBAccount -ResourceGroupName resourceGroupName -Name databaseAccountName  -Location "East US"

Kind                          : GlobalDocumentDB
ProvisioningState             : Initializing
DocumentEndpoint              :
DatabaseAccountOfferType      : Standard
IpRangeFilter                 :
IsVirtualNetworkFilterEnabled : False
EnableAutomaticFailover       : False
ConsistencyPolicy             : Microsoft.Azure.Management.CosmosDB.Models.ConsistencyPolicy
Capabilities                  : {}
WriteLocations                : {databaseAccountName-eastus}
ReadLocations                 : {databaseAccountName-eastus}
FailoverPolicies              : {databaseAccountName-eastus}
VirtualNetworkRules           : {}
EnableMultipleWriteLocations  : False
Location                      : East US
Tags                          : {}
Id                            : /subscriptions/{subscriptionid}/resourceGroups/resourceGroupName/providers/Microsoft.DocumentDB/databaseAccounts/databaseAccountName
Name                          : databaseAccountName
Type                          : Microsoft.DocumentDB/databaseAccounts
```

<span data-ttu-id="0fc67-109">Ett nytt CosmosDB-konto med namnet databaseAccountName skapas i ResourceGroup resourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="0fc67-109">A new CosmosDB Account with name databaseAccountName is created in the ResourceGroup resourceGroupName.</span></span>

## <span data-ttu-id="0fc67-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0fc67-110">PARAMETERS</span></span>

### <span data-ttu-id="0fc67-111">-ApiKind</span><span class="sxs-lookup"><span data-stu-id="0fc67-111">-ApiKind</span></span>
<span data-ttu-id="0fc67-112">Den typ av Cosmos DB-databas som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="0fc67-112">The type of Cosmos DB database account to create.</span></span>
<span data-ttu-id="0fc67-113">Godkända värden: GlobalDocumentDB, MongoDB, Gremlin, Table, Cassandra.</span><span class="sxs-lookup"><span data-stu-id="0fc67-113">Accepted values: GlobalDocumentDB, MongoDB, Gremlin, Table, Cassandra.</span></span>
<span data-ttu-id="0fc67-114">Standardvärde: GlobalDocumentDB</span><span class="sxs-lookup"><span data-stu-id="0fc67-114">Default value: GlobalDocumentDB</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0fc67-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0fc67-115">-AsJob</span></span>
<span data-ttu-id="0fc67-116">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="0fc67-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0fc67-117">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="0fc67-117">-Confirm</span></span>
<span data-ttu-id="0fc67-118">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="0fc67-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0fc67-119">-DefaultConsistencyLevel</span><span class="sxs-lookup"><span data-stu-id="0fc67-119">-DefaultConsistencyLevel</span></span>
<span data-ttu-id="0fc67-120">Standard konsekvens nivå för Cosmos DB-databasnamn.</span><span class="sxs-lookup"><span data-stu-id="0fc67-120">Default consistency level of the Cosmos DB database account.</span></span>
<span data-ttu-id="0fc67-121">Godkända värden: BoundedStaleness, ConsistentPrefix, nysession, Strong</span><span class="sxs-lookup"><span data-stu-id="0fc67-121">Accepted values: BoundedStaleness, ConsistentPrefix, Eventual, Session, Strong</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0fc67-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0fc67-122">-DefaultProfile</span></span>
<span data-ttu-id="0fc67-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0fc67-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0fc67-124">-DisableKeyBasedMetadataWriteAccess</span><span class="sxs-lookup"><span data-stu-id="0fc67-124">-DisableKeyBasedMetadataWriteAccess</span></span>
<span data-ttu-id="0fc67-125">Inaktivera Skriv åtgärder för metadataegenskaper (databaser, behållare, genomflöde) via konto nycklar</span><span class="sxs-lookup"><span data-stu-id="0fc67-125">Disable write operations on metadata resources (databases, containers, throughput) via account keys</span></span>

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

### <span data-ttu-id="0fc67-126">-EnableAutomaticFailover</span><span class="sxs-lookup"><span data-stu-id="0fc67-126">-EnableAutomaticFailover</span></span>
<span data-ttu-id="0fc67-127">Aktiverar automatisk redundans av Skriv regionen i den sällsynta händelsen att regionen inte är tillgänglig på grund av ett avbrott.</span><span class="sxs-lookup"><span data-stu-id="0fc67-127">Enables automatic failover of the write region in the rare event that the region is unavailable due to an outage.</span></span>
<span data-ttu-id="0fc67-128">Automatisk redundans ger en ny Skriv region för kontot och väljs utifrån de prioriteter som kon figurer ATS för kontot.</span><span class="sxs-lookup"><span data-stu-id="0fc67-128">Automatic failover will result in a new write region for the account and is chosen based on the failover priorities configured for the account.</span></span>
<span data-ttu-id="0fc67-129">Godkända värden: falskt, sant</span><span class="sxs-lookup"><span data-stu-id="0fc67-129">Accepted values: false, true</span></span>

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

### <span data-ttu-id="0fc67-130">-EnableMultipleWriteLocations</span><span class="sxs-lookup"><span data-stu-id="0fc67-130">-EnableMultipleWriteLocations</span></span>
<span data-ttu-id="0fc67-131">Aktivera flera Skriv platser.</span><span class="sxs-lookup"><span data-stu-id="0fc67-131">Enable Multiple Write Locations.</span></span>
<span data-ttu-id="0fc67-132">Godkända värden: falskt, sant</span><span class="sxs-lookup"><span data-stu-id="0fc67-132">Accepted values: false, true</span></span>

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

### <span data-ttu-id="0fc67-133">-EnableVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="0fc67-133">-EnableVirtualNetwork</span></span>
<span data-ttu-id="0fc67-134">Aktiverar virtuellt nätverk på Cosmos DB Database-konto.</span><span class="sxs-lookup"><span data-stu-id="0fc67-134">Enables virtual network on the Cosmos DB database account.</span></span>
<span data-ttu-id="0fc67-135">Godkända värden: falskt, sant</span><span class="sxs-lookup"><span data-stu-id="0fc67-135">Accepted values: false, true</span></span>

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

### <span data-ttu-id="0fc67-136">-IpRangeFilter</span><span class="sxs-lookup"><span data-stu-id="0fc67-136">-IpRangeFilter</span></span>
<span data-ttu-id="0fc67-137">Stöd för brand väggar.</span><span class="sxs-lookup"><span data-stu-id="0fc67-137">Firewall support.</span></span>
<span data-ttu-id="0fc67-138">Anger uppsättningen IP-adresser eller IP-adressintervall i CIDR-format som ska ingå som tillåten lista över klient-IP för ett visst databas konto</span><span class="sxs-lookup"><span data-stu-id="0fc67-138">Specifies the set of IP addresses or IP address ranges in CIDR form to be included as the allowed list of client IPs for a given database account</span></span>

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

### <span data-ttu-id="0fc67-139">-Plats</span><span class="sxs-lookup"><span data-stu-id="0fc67-139">-Location</span></span>
<span data-ttu-id="0fc67-140">Lägga till en plats i Cosmos DB-databasnamn.</span><span class="sxs-lookup"><span data-stu-id="0fc67-140">Add a location to the Cosmos DB database account.</span></span>
<span data-ttu-id="0fc67-141">Matris med strängar sorterade efter prioritet för växling vid fel.</span><span class="sxs-lookup"><span data-stu-id="0fc67-141">Array of strings, ordered by failover priority.</span></span>

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

### <span data-ttu-id="0fc67-142">-LocationObject</span><span class="sxs-lookup"><span data-stu-id="0fc67-142">-LocationObject</span></span>
<span data-ttu-id="0fc67-143">Lägga till en plats i Cosmos DB-databasnamn.</span><span class="sxs-lookup"><span data-stu-id="0fc67-143">Add a location to the Cosmos DB database account.</span></span> <span data-ttu-id="0fc67-144">Matris med PSLocation-objekt.</span><span class="sxs-lookup"><span data-stu-id="0fc67-144">Array of PSLocation objects.</span></span>

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

### <span data-ttu-id="0fc67-145">-MaxStalenessIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="0fc67-145">-MaxStalenessIntervalInSeconds</span></span>
<span data-ttu-id="0fc67-146">När det här värdet används med utgångs punkt som är bundet till inaktivitet representerar det tids mängd inaktuellt (i TimeSpan) som tolereras.</span><span class="sxs-lookup"><span data-stu-id="0fc67-146">When used with Bounded Staleness consistency, this value represents the time amount of staleness (in timespan) tolerated.</span></span>
<span data-ttu-id="0fc67-147">Det tillåtna intervallet för det här värdet är 5-86400.</span><span class="sxs-lookup"><span data-stu-id="0fc67-147">Accepted range for this value is 5-86400.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0fc67-148">-MaxStalenessPrefix</span><span class="sxs-lookup"><span data-stu-id="0fc67-148">-MaxStalenessPrefix</span></span>
<span data-ttu-id="0fc67-149">När det används med avgränsad utgångs konsekvens representerar det här värdet antalet begärda föråldrade förfrågningar.</span><span class="sxs-lookup"><span data-stu-id="0fc67-149">When used with Bounded Staleness consistency, this value represents the number of stale requests tolerated.</span></span>
<span data-ttu-id="0fc67-150">Det tillåtna intervallet för det här värdet är 1-2 147 483 647.</span><span class="sxs-lookup"><span data-stu-id="0fc67-150">Accepted range for this value is 1 - 2,147,483,647.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0fc67-151">-Namn</span><span class="sxs-lookup"><span data-stu-id="0fc67-151">-Name</span></span>
<span data-ttu-id="0fc67-152">Namn på Cosmos DB-databas.</span><span class="sxs-lookup"><span data-stu-id="0fc67-152">Name of the Cosmos DB database account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0fc67-153">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="0fc67-153">-PublicNetworkAccess</span></span>
<span data-ttu-id="0fc67-154">Om åtkomst för offentlig slut punkt tillåts för den här servern.</span><span class="sxs-lookup"><span data-stu-id="0fc67-154">Whether or not public endpoint access is allowed for this server.</span></span> <span data-ttu-id="0fc67-155">Möjliga värden är: ' Enabled ', ' disabled '</span><span class="sxs-lookup"><span data-stu-id="0fc67-155">Possible values include: 'Enabled', 'Disabled'</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0fc67-156">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0fc67-156">-ResourceGroupName</span></span>
<span data-ttu-id="0fc67-157">Namn på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="0fc67-157">Name of resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0fc67-158">-Tagg</span><span class="sxs-lookup"><span data-stu-id="0fc67-158">-Tag</span></span>
<span data-ttu-id="0fc67-159">En produkt kod med taggar som par med nyckelord-värde.</span><span class="sxs-lookup"><span data-stu-id="0fc67-159">Hashtable of tags as key-value pairs.</span></span>
<span data-ttu-id="0fc67-160">Använd en tom sträng för att ta bort en befintlig tagg.</span><span class="sxs-lookup"><span data-stu-id="0fc67-160">Use empty string to clear existing tag.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0fc67-161">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="0fc67-161">-VirtualNetworkRule</span></span>
<span data-ttu-id="0fc67-162">Matris med sträng värden för ACL för virtuella nätverk.</span><span class="sxs-lookup"><span data-stu-id="0fc67-162">Array of string values of ACL's for virtual network.</span></span>

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

### <span data-ttu-id="0fc67-163">-VirtualNetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="0fc67-163">-VirtualNetworkRuleObject</span></span>
<span data-ttu-id="0fc67-164">Matris med PSVirtualNetworkRuleObjects för virtuella nätverk.</span><span class="sxs-lookup"><span data-stu-id="0fc67-164">Array of PSVirtualNetworkRuleObjects for virtual network.</span></span>

```yaml
Type: PSVirtualNetworkRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0fc67-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0fc67-165">-WhatIf</span></span>
<span data-ttu-id="0fc67-166">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="0fc67-166">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0fc67-167">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="0fc67-167">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0fc67-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0fc67-168">CommonParameters</span></span>
<span data-ttu-id="0fc67-169">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0fc67-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0fc67-170">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0fc67-170">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0fc67-171">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0fc67-171">INPUTS</span></span>

### <span data-ttu-id="0fc67-172">Microsoft. Azure. commands. CosmosDB. Models. PSCorsRule []</span><span class="sxs-lookup"><span data-stu-id="0fc67-172">Microsoft.Azure.Commands.CosmosDB.Models.PSCorsRule[]</span></span>

## <span data-ttu-id="0fc67-173">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0fc67-173">OUTPUTS</span></span>

### <span data-ttu-id="0fc67-174">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="0fc67-174">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="0fc67-175">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0fc67-175">NOTES</span></span>

## <span data-ttu-id="0fc67-176">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0fc67-176">RELATED LINKS</span></span>
