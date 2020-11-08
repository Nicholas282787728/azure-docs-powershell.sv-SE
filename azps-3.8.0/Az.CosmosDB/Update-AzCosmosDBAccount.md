---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBAccount.md
ms.openlocfilehash: a31df71a1242f4f4e9eb01a37d31eb54ec874a99
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94088278"
---
# <span data-ttu-id="716c9-101">Update-AzCosmosDBAccount</span><span class="sxs-lookup"><span data-stu-id="716c9-101">Update-AzCosmosDBAccount</span></span>

## <span data-ttu-id="716c9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="716c9-102">SYNOPSIS</span></span>
<span data-ttu-id="716c9-103">Uppdatera ett CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="716c9-103">Update a CosmosDB account attributes.</span></span>

## <span data-ttu-id="716c9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="716c9-104">SYNTAX</span></span>

### <span data-ttu-id="716c9-105">ByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="716c9-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBAccount -ResourceGroupName <String> -Name <String> [-DefaultConsistencyLevel <String>]
 [-EnableAutomaticFailover <Boolean>] [-EnableMultipleWriteLocations <Boolean>]
 [-EnableVirtualNetwork <Boolean>] [-IpRangeFilter <String[]>] [-MaxStalenessIntervalInSeconds <Int32>]
 [-MaxStalenessPrefix <Int32>] [-Tag <Hashtable>] [-VirtualNetworkRule <String[]>]
 [-VirtualNetworkRuleObject <PSVirtualNetworkRule[]>] [-DisableKeyBasedMetadataWriteAccess <Boolean>]
 [-PublicNetworkAccess <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="716c9-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="716c9-106">ByResourceIdParameterSet</span></span>
```
Update-AzCosmosDBAccount -ResourceId <String> [-DefaultConsistencyLevel <String>]
 [-EnableAutomaticFailover <Boolean>] [-EnableMultipleWriteLocations <Boolean>]
 [-EnableVirtualNetwork <Boolean>] [-IpRangeFilter <String[]>] [-MaxStalenessIntervalInSeconds <Int32>]
 [-MaxStalenessPrefix <Int32>] [-Tag <Hashtable>] [-VirtualNetworkRule <String[]>]
 [-VirtualNetworkRuleObject <PSVirtualNetworkRule[]>] [-DisableKeyBasedMetadataWriteAccess <Boolean>]
 [-PublicNetworkAccess <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="716c9-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="716c9-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBAccount -InputObject <PSDatabaseAccount> [-DefaultConsistencyLevel <String>]
 [-EnableAutomaticFailover <Boolean>] [-EnableMultipleWriteLocations <Boolean>]
 [-EnableVirtualNetwork <Boolean>] [-IpRangeFilter <String[]>] [-MaxStalenessIntervalInSeconds <Int32>]
 [-MaxStalenessPrefix <Int32>] [-Tag <Hashtable>] [-VirtualNetworkRule <String[]>]
 [-VirtualNetworkRuleObject <PSVirtualNetworkRule[]>] [-DisableKeyBasedMetadataWriteAccess <Boolean>]
 [-PublicNetworkAccess <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="716c9-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="716c9-108">DESCRIPTION</span></span>
<span data-ttu-id="716c9-109">Uppdatera egenskaperna för ett CosmosDB-konto.</span><span class="sxs-lookup"><span data-stu-id="716c9-109">Update the properties of a CosmosDB account.</span></span> <span data-ttu-id="716c9-110">Det går inte att uppdatera konto områden simulataneously med andra egenskaper.</span><span class="sxs-lookup"><span data-stu-id="716c9-110">Cannot update Account Regions simulataneously with other properties.</span></span>

## <span data-ttu-id="716c9-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="716c9-111">EXAMPLES</span></span>

### <span data-ttu-id="716c9-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="716c9-112">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBAccount -ResourceGroupName resourceGroupName -Name accountName -DefaultConsistencyLevel "Strong" -EnableAutomaticFailover 1 -EnableMultipleWriteLocations 1 -EnableVirtualNetwork 1

Kind                          : GlobalDocumentDB
ProvisioningState             : Initializing
DocumentEndpoint              :
DatabaseAccountOfferType      : Standard
IpRangeFilter                 :
IsVirtualNetworkFilterEnabled : True
EnableAutomaticFailover       : True
ConsistencyPolicy             : Microsoft.Azure.Management.CosmosDB.Fluent.Models.ConsistencyPolicy
Capabilities                  : {}
WriteLocations                : {accountName-eastus}
ReadLocations                 : {accountName-eastus}
FailoverPolicies              : {accountName-eastus}
VirtualNetworkRules           : {}
EnableMultipleWriteLocations  : True
Location                      : East US
Tags                          : {}
Id                            : /subscriptions/{subscriptionid}/resourceGroups/resourceGroupName/providers/Microsoft.DocumentDB/databaseAccounts/accountName
Name                          : accountName
Type                          : Microsoft.DocumentDB/databaseAccounts
```

<span data-ttu-id="716c9-113">Uppdaterade DefaultConsistencyLevel till "Strong", aktiverat AutomaticFailover, aktiverat MultipleWriteLocations och aktiverat VirtualNetwork för CosmosDB-konto med namn accountName.</span><span class="sxs-lookup"><span data-stu-id="716c9-113">Updated DefaultConsistencyLevel to "Strong", Enabled AutomaticFailover, Enabled MultipleWriteLocations and Enabled VirtualNetwork for CosmosDB Account with name accountName.</span></span> 

## <span data-ttu-id="716c9-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="716c9-114">PARAMETERS</span></span>

### <span data-ttu-id="716c9-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="716c9-115">-AsJob</span></span>
<span data-ttu-id="716c9-116">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="716c9-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="716c9-117">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="716c9-117">-Confirm</span></span>
<span data-ttu-id="716c9-118">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="716c9-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="716c9-119">-DefaultConsistencyLevel</span><span class="sxs-lookup"><span data-stu-id="716c9-119">-DefaultConsistencyLevel</span></span>
<span data-ttu-id="716c9-120">Standard konsekvens nivå för Cosmos DB-databasnamn.</span><span class="sxs-lookup"><span data-stu-id="716c9-120">Default consistency level of the Cosmos DB database account.</span></span>
<span data-ttu-id="716c9-121">Godkända värden: BoundedStaleness, ConsistentPrefix, nysession, Strong</span><span class="sxs-lookup"><span data-stu-id="716c9-121">Accepted values: BoundedStaleness, ConsistentPrefix, Eventual, Session, Strong</span></span>

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

### <span data-ttu-id="716c9-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="716c9-122">-DefaultProfile</span></span>
<span data-ttu-id="716c9-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="716c9-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="716c9-124">-DisableKeyBasedMetadataWriteAccess</span><span class="sxs-lookup"><span data-stu-id="716c9-124">-DisableKeyBasedMetadataWriteAccess</span></span>
<span data-ttu-id="716c9-125">Inaktivera Skriv åtgärder för metadataegenskaper (databaser, behållare, genomflöde) via konto nycklar</span><span class="sxs-lookup"><span data-stu-id="716c9-125">Disable write operations on metadata resources (databases, containers, throughput) via account keys</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="716c9-126">-EnableAutomaticFailover</span><span class="sxs-lookup"><span data-stu-id="716c9-126">-EnableAutomaticFailover</span></span>
<span data-ttu-id="716c9-127">Aktiverar automatisk redundans av Skriv regionen i den sällsynta händelsen att regionen inte är tillgänglig på grund av ett avbrott.</span><span class="sxs-lookup"><span data-stu-id="716c9-127">Enables automatic failover of the write region in the rare event that the region is unavailable due to an outage.</span></span>
<span data-ttu-id="716c9-128">Automatisk redundans ger en ny Skriv region för kontot och väljs utifrån de prioriteter som kon figurer ATS för kontot.</span><span class="sxs-lookup"><span data-stu-id="716c9-128">Automatic failover will result in a new write region for the account and is chosen based on the failover priorities configured for the account.</span></span>
<span data-ttu-id="716c9-129">Godkända värden: falskt, sant</span><span class="sxs-lookup"><span data-stu-id="716c9-129">Accepted values: false, true</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="716c9-130">-EnableMultipleWriteLocations</span><span class="sxs-lookup"><span data-stu-id="716c9-130">-EnableMultipleWriteLocations</span></span>
<span data-ttu-id="716c9-131">Aktivera flera Skriv platser.</span><span class="sxs-lookup"><span data-stu-id="716c9-131">Enable Multiple Write Locations.</span></span>
<span data-ttu-id="716c9-132">Godkända värden: falskt, sant</span><span class="sxs-lookup"><span data-stu-id="716c9-132">Accepted values: false, true</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="716c9-133">-EnableVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="716c9-133">-EnableVirtualNetwork</span></span>
<span data-ttu-id="716c9-134">Aktiverar virtuellt nätverk på Cosmos DB Database-konto.</span><span class="sxs-lookup"><span data-stu-id="716c9-134">Enables virtual network on the Cosmos DB database account.</span></span>
<span data-ttu-id="716c9-135">Godkända värden: falskt, sant</span><span class="sxs-lookup"><span data-stu-id="716c9-135">Accepted values: false, true</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="716c9-136">-InputObject</span><span class="sxs-lookup"><span data-stu-id="716c9-136">-InputObject</span></span>
<span data-ttu-id="716c9-137">CosmosDB</span><span class="sxs-lookup"><span data-stu-id="716c9-137">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccount
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="716c9-138">-IpRangeFilter</span><span class="sxs-lookup"><span data-stu-id="716c9-138">-IpRangeFilter</span></span>
<span data-ttu-id="716c9-139">Stöd för brand väggar.</span><span class="sxs-lookup"><span data-stu-id="716c9-139">Firewall support.</span></span>
<span data-ttu-id="716c9-140">Anger uppsättningen IP-adresser eller IP-adressintervall i CIDR-format som ska ingå som tillåten lista över klient-IP för ett visst databas konto</span><span class="sxs-lookup"><span data-stu-id="716c9-140">Specifies the set of IP addresses or IP address ranges in CIDR form to be included as the allowed list of client IPs for a given database account</span></span>

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

### <span data-ttu-id="716c9-141">-MaxStalenessIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="716c9-141">-MaxStalenessIntervalInSeconds</span></span>
<span data-ttu-id="716c9-142">När det här värdet används med utgångs punkt som är bundet till inaktivitet representerar det tids mängd inaktuellt (i TimeSpan) som tolereras.</span><span class="sxs-lookup"><span data-stu-id="716c9-142">When used with Bounded Staleness consistency, this value represents the time amount of staleness (in timespan) tolerated.</span></span>
<span data-ttu-id="716c9-143">Det tillåtna intervallet för det här värdet är 5-86400.</span><span class="sxs-lookup"><span data-stu-id="716c9-143">Accepted range for this value is 5-86400.</span></span>

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

### <span data-ttu-id="716c9-144">-MaxStalenessPrefix</span><span class="sxs-lookup"><span data-stu-id="716c9-144">-MaxStalenessPrefix</span></span>
<span data-ttu-id="716c9-145">När det används med avgränsad utgångs konsekvens representerar det här värdet antalet begärda föråldrade förfrågningar.</span><span class="sxs-lookup"><span data-stu-id="716c9-145">When used with Bounded Staleness consistency, this value represents the number of stale requests tolerated.</span></span>
<span data-ttu-id="716c9-146">Det tillåtna intervallet för det här värdet är 1-2 147 483 647.</span><span class="sxs-lookup"><span data-stu-id="716c9-146">Accepted range for this value is 1 - 2,147,483,647.</span></span>

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

### <span data-ttu-id="716c9-147">-Namn</span><span class="sxs-lookup"><span data-stu-id="716c9-147">-Name</span></span>
<span data-ttu-id="716c9-148">Namn på Cosmos DB-databas.</span><span class="sxs-lookup"><span data-stu-id="716c9-148">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="716c9-149">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="716c9-149">-PublicNetworkAccess</span></span>
<span data-ttu-id="716c9-150">Om åtkomst för offentlig slut punkt tillåts för den här servern.</span><span class="sxs-lookup"><span data-stu-id="716c9-150">Whether or not public endpoint access is allowed for this server.</span></span> <span data-ttu-id="716c9-151">Möjliga värden är: ' Enabled ', ' disabled '</span><span class="sxs-lookup"><span data-stu-id="716c9-151">Possible values include: 'Enabled', 'Disabled'</span></span>

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

### <span data-ttu-id="716c9-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="716c9-152">-ResourceGroupName</span></span>
<span data-ttu-id="716c9-153">Namn på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="716c9-153">Name of resource group.</span></span>

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

### <span data-ttu-id="716c9-154">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="716c9-154">-ResourceId</span></span>
<span data-ttu-id="716c9-155">ResourceId för resursen.</span><span class="sxs-lookup"><span data-stu-id="716c9-155">ResourceId of the resource.</span></span>

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

### <span data-ttu-id="716c9-156">-Tagg</span><span class="sxs-lookup"><span data-stu-id="716c9-156">-Tag</span></span>
<span data-ttu-id="716c9-157">En produkt kod med taggar som par med nyckelord-värde.</span><span class="sxs-lookup"><span data-stu-id="716c9-157">Hashtable of tags as key-value pairs.</span></span>
<span data-ttu-id="716c9-158">Använd en tom sträng för att ta bort en befintlig tagg.</span><span class="sxs-lookup"><span data-stu-id="716c9-158">Use empty string to clear existing tag.</span></span>

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

### <span data-ttu-id="716c9-159">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="716c9-159">-VirtualNetworkRule</span></span>
<span data-ttu-id="716c9-160">Matris med sträng värden för ACL för virtuella nätverk.</span><span class="sxs-lookup"><span data-stu-id="716c9-160">Array of string values of ACL's for virtual network.</span></span>

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

### <span data-ttu-id="716c9-161">-VirtualNetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="716c9-161">-VirtualNetworkRuleObject</span></span>
<span data-ttu-id="716c9-162">Matris med PSVirtualNetworkRuleObjects för virtuella nätverk.</span><span class="sxs-lookup"><span data-stu-id="716c9-162">Array of PSVirtualNetworkRuleObjects for virtual network.</span></span>

```yaml
Type: PSVirtualNetworkRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="716c9-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="716c9-163">-WhatIf</span></span>
<span data-ttu-id="716c9-164">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="716c9-164">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="716c9-165">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="716c9-165">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="716c9-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="716c9-166">CommonParameters</span></span>
<span data-ttu-id="716c9-167">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="716c9-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="716c9-168">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="716c9-168">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="716c9-169">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="716c9-169">INPUTS</span></span>

### <span data-ttu-id="716c9-170">Microsoft. Azure. commands. CosmosDB. Models. PSCorsRule []</span><span class="sxs-lookup"><span data-stu-id="716c9-170">Microsoft.Azure.Commands.CosmosDB.Models.PSCorsRule[]</span></span>

## <span data-ttu-id="716c9-171">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="716c9-171">OUTPUTS</span></span>

### <span data-ttu-id="716c9-172">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="716c9-172">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="716c9-173">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="716c9-173">NOTES</span></span>

## <span data-ttu-id="716c9-174">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="716c9-174">RELATED LINKS</span></span>
