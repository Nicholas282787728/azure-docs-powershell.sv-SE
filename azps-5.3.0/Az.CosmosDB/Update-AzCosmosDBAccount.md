---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBAccount.md
ms.openlocfilehash: e88deadc0a46aa5d89bd513a4aba1b93e22fbb5a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98524307"
---
# <span data-ttu-id="e95ef-101">Update-AzCosmosDBAccount</span><span class="sxs-lookup"><span data-stu-id="e95ef-101">Update-AzCosmosDBAccount</span></span>

## <span data-ttu-id="e95ef-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e95ef-102">SYNOPSIS</span></span>
<span data-ttu-id="e95ef-103">Uppdatera ett CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="e95ef-103">Update a CosmosDB account attributes.</span></span>

## <span data-ttu-id="e95ef-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e95ef-104">SYNTAX</span></span>

### <span data-ttu-id="e95ef-105">ByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="e95ef-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBAccount [-EnableAutomaticFailover <Boolean>] [-EnableMultipleWriteLocations <Boolean>]
 [-EnableVirtualNetwork <Boolean>] [-DisableKeyBasedMetadataWriteAccess <Boolean>] -ResourceGroupName <String>
 -Name <String> [-DefaultConsistencyLevel <String>] [-IpRule <String[]>]
 [-MaxStalenessIntervalInSeconds <Int32>] [-MaxStalenessPrefix <Int32>] [-Tag <Hashtable>]
 [-VirtualNetworkRule <String[]>] [-VirtualNetworkRuleObject <PSVirtualNetworkRule[]>]
 [-PublicNetworkAccess <String>] [-KeyVaultKeyUri <String>] [-EnableAnalyticalStorage <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e95ef-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e95ef-106">ByResourceIdParameterSet</span></span>
```
Update-AzCosmosDBAccount -ResourceId <String> [-EnableAutomaticFailover <Boolean>]
 [-EnableMultipleWriteLocations <Boolean>] [-EnableVirtualNetwork <Boolean>]
 [-DisableKeyBasedMetadataWriteAccess <Boolean>] [-DefaultConsistencyLevel <String>] [-IpRule <String[]>]
 [-MaxStalenessIntervalInSeconds <Int32>] [-MaxStalenessPrefix <Int32>] [-Tag <Hashtable>]
 [-VirtualNetworkRule <String[]>] [-VirtualNetworkRuleObject <PSVirtualNetworkRule[]>]
 [-PublicNetworkAccess <String>] [-KeyVaultKeyUri <String>] [-EnableAnalyticalStorage <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e95ef-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e95ef-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBAccount -InputObject <PSDatabaseAccountGetResults> [-EnableAutomaticFailover <Boolean>]
 [-EnableMultipleWriteLocations <Boolean>] [-EnableVirtualNetwork <Boolean>]
 [-DisableKeyBasedMetadataWriteAccess <Boolean>] [-DefaultConsistencyLevel <String>] [-IpRule <String[]>]
 [-MaxStalenessIntervalInSeconds <Int32>] [-MaxStalenessPrefix <Int32>] [-Tag <Hashtable>]
 [-VirtualNetworkRule <String[]>] [-VirtualNetworkRuleObject <PSVirtualNetworkRule[]>]
 [-PublicNetworkAccess <String>] [-KeyVaultKeyUri <String>] [-EnableAnalyticalStorage <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e95ef-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e95ef-108">DESCRIPTION</span></span>
<span data-ttu-id="e95ef-109">Uppdatera egenskaperna för ett CosmosDB-konto.</span><span class="sxs-lookup"><span data-stu-id="e95ef-109">Update the properties of a CosmosDB account.</span></span> <span data-ttu-id="e95ef-110">Det går inte att uppdatera konto områden simulataneously med andra egenskaper.</span><span class="sxs-lookup"><span data-stu-id="e95ef-110">Cannot update Account Regions simulataneously with other properties.</span></span>

## <span data-ttu-id="e95ef-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e95ef-111">EXAMPLES</span></span>

### <span data-ttu-id="e95ef-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="e95ef-112">Example 1</span></span>
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

<span data-ttu-id="e95ef-113">Uppdaterade DefaultConsistencyLevel till "Strong", aktiverat AutomaticFailover, aktiverat MultipleWriteLocations och aktiverat VirtualNetwork för CosmosDB-konto med namn accountName.</span><span class="sxs-lookup"><span data-stu-id="e95ef-113">Updated DefaultConsistencyLevel to "Strong", Enabled AutomaticFailover, Enabled MultipleWriteLocations and Enabled VirtualNetwork for CosmosDB Account with name accountName.</span></span> 

## <span data-ttu-id="e95ef-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e95ef-114">PARAMETERS</span></span>

### <span data-ttu-id="e95ef-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e95ef-115">-AsJob</span></span>
<span data-ttu-id="e95ef-116">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="e95ef-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e95ef-117">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="e95ef-117">-Confirm</span></span>
<span data-ttu-id="e95ef-118">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e95ef-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e95ef-119">-DefaultConsistencyLevel</span><span class="sxs-lookup"><span data-stu-id="e95ef-119">-DefaultConsistencyLevel</span></span>
<span data-ttu-id="e95ef-120">Standard konsekvens nivå för Cosmos DB-databasnamn.</span><span class="sxs-lookup"><span data-stu-id="e95ef-120">Default consistency level of the Cosmos DB database account.</span></span>
<span data-ttu-id="e95ef-121">Godkända värden: BoundedStaleness, ConsistentPrefix, nysession, Strong</span><span class="sxs-lookup"><span data-stu-id="e95ef-121">Accepted values: BoundedStaleness, ConsistentPrefix, Eventual, Session, Strong</span></span>

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

### <span data-ttu-id="e95ef-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e95ef-122">-DefaultProfile</span></span>
<span data-ttu-id="e95ef-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e95ef-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e95ef-124">-DisableKeyBasedMetadataWriteAccess</span><span class="sxs-lookup"><span data-stu-id="e95ef-124">-DisableKeyBasedMetadataWriteAccess</span></span>
<span data-ttu-id="e95ef-125">Inaktivera Skriv åtgärder för metadataegenskaper (databaser, behållare, genomflöde) via konto nycklar</span><span class="sxs-lookup"><span data-stu-id="e95ef-125">Disable write operations on metadata resources (databases, containers, throughput) via account keys</span></span>

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

### <span data-ttu-id="e95ef-126">-EnableAnalyticalStorage</span><span class="sxs-lookup"><span data-stu-id="e95ef-126">-EnableAnalyticalStorage</span></span>
<span data-ttu-id="e95ef-127">Bool för att ange om AnalyticalStorage är aktiverat för kontot.</span><span class="sxs-lookup"><span data-stu-id="e95ef-127">Bool to indicate if AnalyticalStorage is enabled on the account.</span></span>

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

### <span data-ttu-id="e95ef-128">-EnableAutomaticFailover</span><span class="sxs-lookup"><span data-stu-id="e95ef-128">-EnableAutomaticFailover</span></span>
<span data-ttu-id="e95ef-129">Aktiverar automatisk redundans av Skriv regionen i den sällsynta händelsen att regionen inte är tillgänglig på grund av ett avbrott.</span><span class="sxs-lookup"><span data-stu-id="e95ef-129">Enables automatic failover of the write region in the rare event that the region is unavailable due to an outage.</span></span>
<span data-ttu-id="e95ef-130">Automatisk redundans ger en ny Skriv region för kontot och väljs utifrån de prioriteter som kon figurer ATS för kontot.</span><span class="sxs-lookup"><span data-stu-id="e95ef-130">Automatic failover will result in a new write region for the account and is chosen based on the failover priorities configured for the account.</span></span>
<span data-ttu-id="e95ef-131">Godkända värden: falskt, sant</span><span class="sxs-lookup"><span data-stu-id="e95ef-131">Accepted values: false, true</span></span>

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

### <span data-ttu-id="e95ef-132">-EnableMultipleWriteLocations</span><span class="sxs-lookup"><span data-stu-id="e95ef-132">-EnableMultipleWriteLocations</span></span>
<span data-ttu-id="e95ef-133">Aktivera flera Skriv platser.</span><span class="sxs-lookup"><span data-stu-id="e95ef-133">Enable Multiple Write Locations.</span></span>
<span data-ttu-id="e95ef-134">Godkända värden: falskt, sant</span><span class="sxs-lookup"><span data-stu-id="e95ef-134">Accepted values: false, true</span></span>

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

### <span data-ttu-id="e95ef-135">-EnableVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="e95ef-135">-EnableVirtualNetwork</span></span>
<span data-ttu-id="e95ef-136">Aktiverar virtuellt nätverk på Cosmos DB Database-konto.</span><span class="sxs-lookup"><span data-stu-id="e95ef-136">Enables virtual network on the Cosmos DB database account.</span></span>
<span data-ttu-id="e95ef-137">Godkända värden: falskt, sant</span><span class="sxs-lookup"><span data-stu-id="e95ef-137">Accepted values: false, true</span></span>

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

### <span data-ttu-id="e95ef-138">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e95ef-138">-InputObject</span></span>
<span data-ttu-id="e95ef-139">CosmosDB</span><span class="sxs-lookup"><span data-stu-id="e95ef-139">CosmosDB Account object</span></span>

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

### <span data-ttu-id="e95ef-140">-IpRule</span><span class="sxs-lookup"><span data-stu-id="e95ef-140">-IpRule</span></span>
<span data-ttu-id="e95ef-141">Stöd för brand väggar.</span><span class="sxs-lookup"><span data-stu-id="e95ef-141">Firewall support.</span></span> <span data-ttu-id="e95ef-142">Anger uppsättningen IP-adresser eller IP-adressintervall i CIDR-format som ska tas med i listan över tillåtna klienter för ett visst databas konto.</span><span class="sxs-lookup"><span data-stu-id="e95ef-142">Specifies the set of IP addresses or IP address ranges in CIDR form to be included as the allowed list of client IPs for a given database account.</span></span>

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

### <span data-ttu-id="e95ef-143">-KeyVaultKeyUri</span><span class="sxs-lookup"><span data-stu-id="e95ef-143">-KeyVaultKeyUri</span></span>
<span data-ttu-id="e95ef-144">URI för ett valv</span><span class="sxs-lookup"><span data-stu-id="e95ef-144">URI of the KeyVault</span></span>

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

### <span data-ttu-id="e95ef-145">-MaxStalenessIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="e95ef-145">-MaxStalenessIntervalInSeconds</span></span>
<span data-ttu-id="e95ef-146">När det här värdet används med utgångs punkt som är bundet till inaktivitet representerar det tids mängd inaktuellt (i TimeSpan) som tolereras.</span><span class="sxs-lookup"><span data-stu-id="e95ef-146">When used with Bounded Staleness consistency, this value represents the time amount of staleness (in timespan) tolerated.</span></span>
<span data-ttu-id="e95ef-147">Det tillåtna intervallet för det här värdet är 5-86400.</span><span class="sxs-lookup"><span data-stu-id="e95ef-147">Accepted range for this value is 5-86400.</span></span>

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

### <span data-ttu-id="e95ef-148">-MaxStalenessPrefix</span><span class="sxs-lookup"><span data-stu-id="e95ef-148">-MaxStalenessPrefix</span></span>
<span data-ttu-id="e95ef-149">När det används med avgränsad utgångs konsekvens representerar det här värdet antalet begärda föråldrade förfrågningar.</span><span class="sxs-lookup"><span data-stu-id="e95ef-149">When used with Bounded Staleness consistency, this value represents the number of stale requests tolerated.</span></span>
<span data-ttu-id="e95ef-150">Det tillåtna intervallet för det här värdet är 1-2 147 483 647.</span><span class="sxs-lookup"><span data-stu-id="e95ef-150">Accepted range for this value is 1 - 2,147,483,647.</span></span>

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

### <span data-ttu-id="e95ef-151">-Namn</span><span class="sxs-lookup"><span data-stu-id="e95ef-151">-Name</span></span>
<span data-ttu-id="e95ef-152">Namn på Cosmos DB-databas.</span><span class="sxs-lookup"><span data-stu-id="e95ef-152">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="e95ef-153">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="e95ef-153">-PublicNetworkAccess</span></span>
<span data-ttu-id="e95ef-154">Om åtkomst för offentlig slut punkt tillåts för den här servern.</span><span class="sxs-lookup"><span data-stu-id="e95ef-154">Whether or not public endpoint access is allowed for this server.</span></span> <span data-ttu-id="e95ef-155">Möjliga värden är: ' Enabled ', ' disabled '</span><span class="sxs-lookup"><span data-stu-id="e95ef-155">Possible values include: 'Enabled', 'Disabled'</span></span>

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

### <span data-ttu-id="e95ef-156">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e95ef-156">-ResourceGroupName</span></span>
<span data-ttu-id="e95ef-157">Namn på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="e95ef-157">Name of resource group.</span></span>

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

### <span data-ttu-id="e95ef-158">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e95ef-158">-ResourceId</span></span>
<span data-ttu-id="e95ef-159">ResourceId för resursen.</span><span class="sxs-lookup"><span data-stu-id="e95ef-159">ResourceId of the resource.</span></span>

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

### <span data-ttu-id="e95ef-160">-Tagg</span><span class="sxs-lookup"><span data-stu-id="e95ef-160">-Tag</span></span>
<span data-ttu-id="e95ef-161">En produkt kod med taggar som par med nyckelord-värde.</span><span class="sxs-lookup"><span data-stu-id="e95ef-161">Hashtable of tags as key-value pairs.</span></span>
<span data-ttu-id="e95ef-162">Använd en tom sträng för att ta bort en befintlig tagg.</span><span class="sxs-lookup"><span data-stu-id="e95ef-162">Use empty string to clear existing tag.</span></span>

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

### <span data-ttu-id="e95ef-163">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="e95ef-163">-VirtualNetworkRule</span></span>
<span data-ttu-id="e95ef-164">Matris med sträng värden för ACL för virtuella nätverk.</span><span class="sxs-lookup"><span data-stu-id="e95ef-164">Array of string values of ACL's for virtual network.</span></span>

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

### <span data-ttu-id="e95ef-165">-VirtualNetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="e95ef-165">-VirtualNetworkRuleObject</span></span>
<span data-ttu-id="e95ef-166">Matris med PSVirtualNetworkRuleObjects för virtuella nätverk.</span><span class="sxs-lookup"><span data-stu-id="e95ef-166">Array of PSVirtualNetworkRuleObjects for virtual network.</span></span>

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

### <span data-ttu-id="e95ef-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e95ef-167">-WhatIf</span></span>
<span data-ttu-id="e95ef-168">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="e95ef-168">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e95ef-169">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="e95ef-169">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e95ef-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e95ef-170">CommonParameters</span></span>
<span data-ttu-id="e95ef-171">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e95ef-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e95ef-172">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e95ef-172">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e95ef-173">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e95ef-173">INPUTS</span></span>

### <span data-ttu-id="e95ef-174">Microsoft. Azure. commands. CosmosDB. Models. PSCorsRule []</span><span class="sxs-lookup"><span data-stu-id="e95ef-174">Microsoft.Azure.Commands.CosmosDB.Models.PSCorsRule[]</span></span>

## <span data-ttu-id="e95ef-175">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e95ef-175">OUTPUTS</span></span>

### <span data-ttu-id="e95ef-176">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="e95ef-176">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="e95ef-177">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e95ef-177">NOTES</span></span>

## <span data-ttu-id="e95ef-178">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e95ef-178">RELATED LINKS</span></span>
