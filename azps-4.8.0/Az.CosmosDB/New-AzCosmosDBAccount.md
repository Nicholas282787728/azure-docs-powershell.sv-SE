---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBAccount.md
ms.openlocfilehash: f082f9390dd5a00fa5984aa2e0df26e8c3b63636
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94102987"
---
# <span data-ttu-id="0afdf-101">New-AzCosmosDBAccount</span><span class="sxs-lookup"><span data-stu-id="0afdf-101">New-AzCosmosDBAccount</span></span>

## <span data-ttu-id="0afdf-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0afdf-102">SYNOPSIS</span></span>
<span data-ttu-id="0afdf-103">Skapa ett nytt CosmosDB-konto.</span><span class="sxs-lookup"><span data-stu-id="0afdf-103">Create a new CosmosDB Account.</span></span>

## <span data-ttu-id="0afdf-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0afdf-104">SYNTAX</span></span>

```
New-AzCosmosDBAccount [-EnableAutomaticFailover] [-EnableMultipleWriteLocations] [-EnableVirtualNetwork]
 [-ApiKind <String>] [-DisableKeyBasedMetadataWriteAccess] [-EnableFreeTier <Boolean>]
 [-ServerVersion <String>] [-Location <String[]>] [-LocationObject <PSLocation[]>] -ResourceGroupName <String>
 -Name <String> [-DefaultConsistencyLevel <String>] [-IpRule <String[]>]
 [-MaxStalenessIntervalInSeconds <Int32>] [-MaxStalenessPrefix <Int32>] [-Tag <Hashtable>]
 [-VirtualNetworkRule <String[]>] [-VirtualNetworkRuleObject <PSVirtualNetworkRule[]>]
 [-PublicNetworkAccess <String>] [-KeyVaultKeyUri <String>] [-EnableAnalyticalStorage <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0afdf-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0afdf-105">DESCRIPTION</span></span>
<span data-ttu-id="0afdf-106">Skapa ett nytt CosmosDB-konto i angiven ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="0afdf-106">Create a new CosmosDB Account in the given ResourceGroup.</span></span>

## <span data-ttu-id="0afdf-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0afdf-107">EXAMPLES</span></span>

### <span data-ttu-id="0afdf-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="0afdf-108">Example 1</span></span>
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

<span data-ttu-id="0afdf-109">Ett nytt CosmosDB-konto med namnet databaseAccountName skapas i ResourceGroup resourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="0afdf-109">A new CosmosDB Account with name databaseAccountName is created in the ResourceGroup resourceGroupName.</span></span>

## <span data-ttu-id="0afdf-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0afdf-110">PARAMETERS</span></span>

### <span data-ttu-id="0afdf-111">-ApiKind</span><span class="sxs-lookup"><span data-stu-id="0afdf-111">-ApiKind</span></span>
<span data-ttu-id="0afdf-112">Den typ av Cosmos DB-databas som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="0afdf-112">The type of Cosmos DB database account to create.</span></span>
<span data-ttu-id="0afdf-113">Godkända värden: GlobalDocumentDB, MongoDB, Gremlin, Table, Cassandra.</span><span class="sxs-lookup"><span data-stu-id="0afdf-113">Accepted values: GlobalDocumentDB, MongoDB, Gremlin, Table, Cassandra.</span></span>
<span data-ttu-id="0afdf-114">Standardvärde: GlobalDocumentDB</span><span class="sxs-lookup"><span data-stu-id="0afdf-114">Default value: GlobalDocumentDB</span></span>

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

### <span data-ttu-id="0afdf-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0afdf-115">-AsJob</span></span>
<span data-ttu-id="0afdf-116">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="0afdf-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0afdf-117">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="0afdf-117">-Confirm</span></span>
<span data-ttu-id="0afdf-118">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="0afdf-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0afdf-119">-DefaultConsistencyLevel</span><span class="sxs-lookup"><span data-stu-id="0afdf-119">-DefaultConsistencyLevel</span></span>
<span data-ttu-id="0afdf-120">Standard konsekvens nivå för Cosmos DB-databasnamn.</span><span class="sxs-lookup"><span data-stu-id="0afdf-120">Default consistency level of the Cosmos DB database account.</span></span>
<span data-ttu-id="0afdf-121">Godkända värden: BoundedStaleness, ConsistentPrefix, nysession, Strong</span><span class="sxs-lookup"><span data-stu-id="0afdf-121">Accepted values: BoundedStaleness, ConsistentPrefix, Eventual, Session, Strong</span></span>

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

### <span data-ttu-id="0afdf-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0afdf-122">-DefaultProfile</span></span>
<span data-ttu-id="0afdf-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0afdf-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0afdf-124">-DisableKeyBasedMetadataWriteAccess</span><span class="sxs-lookup"><span data-stu-id="0afdf-124">-DisableKeyBasedMetadataWriteAccess</span></span>
<span data-ttu-id="0afdf-125">Inaktivera Skriv åtgärder för metadataegenskaper (databaser, behållare, genomflöde) via konto nycklar</span><span class="sxs-lookup"><span data-stu-id="0afdf-125">Disable write operations on metadata resources (databases, containers, throughput) via account keys</span></span>

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

### <span data-ttu-id="0afdf-126">-EnableAnalyticalStorage</span><span class="sxs-lookup"><span data-stu-id="0afdf-126">-EnableAnalyticalStorage</span></span>
<span data-ttu-id="0afdf-127">Bool för att ange om AnalyticalStorage är aktiverat för kontot.</span><span class="sxs-lookup"><span data-stu-id="0afdf-127">Bool to indicate if AnalyticalStorage is enabled on the account.</span></span>

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

### <span data-ttu-id="0afdf-128">-EnableAutomaticFailover</span><span class="sxs-lookup"><span data-stu-id="0afdf-128">-EnableAutomaticFailover</span></span>
<span data-ttu-id="0afdf-129">Aktiverar automatisk redundans av Skriv regionen i den sällsynta händelsen att regionen inte är tillgänglig på grund av ett avbrott.</span><span class="sxs-lookup"><span data-stu-id="0afdf-129">Enables automatic failover of the write region in the rare event that the region is unavailable due to an outage.</span></span>
<span data-ttu-id="0afdf-130">Automatisk redundans ger en ny Skriv region för kontot och väljs utifrån de prioriteter som kon figurer ATS för kontot.</span><span class="sxs-lookup"><span data-stu-id="0afdf-130">Automatic failover will result in a new write region for the account and is chosen based on the failover priorities configured for the account.</span></span>
<span data-ttu-id="0afdf-131">Godkända värden: falskt, sant</span><span class="sxs-lookup"><span data-stu-id="0afdf-131">Accepted values: false, true</span></span>

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

### <span data-ttu-id="0afdf-132">-EnableFreeTier</span><span class="sxs-lookup"><span data-stu-id="0afdf-132">-EnableFreeTier</span></span>
<span data-ttu-id="0afdf-133">Bool för att ange om en nivå är aktive rad för kontot.</span><span class="sxs-lookup"><span data-stu-id="0afdf-133">Bool to indicate if FreeTier is enabled on the account.</span></span>

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

### <span data-ttu-id="0afdf-134">-EnableMultipleWriteLocations</span><span class="sxs-lookup"><span data-stu-id="0afdf-134">-EnableMultipleWriteLocations</span></span>
<span data-ttu-id="0afdf-135">Aktivera flera Skriv platser.</span><span class="sxs-lookup"><span data-stu-id="0afdf-135">Enable Multiple Write Locations.</span></span>
<span data-ttu-id="0afdf-136">Godkända värden: falskt, sant</span><span class="sxs-lookup"><span data-stu-id="0afdf-136">Accepted values: false, true</span></span>

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

### <span data-ttu-id="0afdf-137">-EnableVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="0afdf-137">-EnableVirtualNetwork</span></span>
<span data-ttu-id="0afdf-138">Aktiverar virtuellt nätverk på Cosmos DB Database-konto.</span><span class="sxs-lookup"><span data-stu-id="0afdf-138">Enables virtual network on the Cosmos DB database account.</span></span>
<span data-ttu-id="0afdf-139">Godkända värden: falskt, sant</span><span class="sxs-lookup"><span data-stu-id="0afdf-139">Accepted values: false, true</span></span>

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

### <span data-ttu-id="0afdf-140">-IpRule</span><span class="sxs-lookup"><span data-stu-id="0afdf-140">-IpRule</span></span>
<span data-ttu-id="0afdf-141">Stöd för brand väggar.</span><span class="sxs-lookup"><span data-stu-id="0afdf-141">Firewall support.</span></span> <span data-ttu-id="0afdf-142">Anger uppsättningen IP-adresser eller IP-adressintervall i CIDR-format som ska tas med i listan över tillåtna klienter för ett visst databas konto.</span><span class="sxs-lookup"><span data-stu-id="0afdf-142">Specifies the set of IP addresses or IP address ranges in CIDR form to be included as the allowed list of client IPs for a given database account.</span></span>

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

### <span data-ttu-id="0afdf-143">-KeyVaultKeyUri</span><span class="sxs-lookup"><span data-stu-id="0afdf-143">-KeyVaultKeyUri</span></span>
<span data-ttu-id="0afdf-144">URI för ett valv</span><span class="sxs-lookup"><span data-stu-id="0afdf-144">URI of the KeyVault</span></span>

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

### <span data-ttu-id="0afdf-145">-Plats</span><span class="sxs-lookup"><span data-stu-id="0afdf-145">-Location</span></span>
<span data-ttu-id="0afdf-146">Lägga till en plats i Cosmos DB-databasnamn.</span><span class="sxs-lookup"><span data-stu-id="0afdf-146">Add a location to the Cosmos DB database account.</span></span>
<span data-ttu-id="0afdf-147">Matris med strängar sorterade efter prioritet för växling vid fel.</span><span class="sxs-lookup"><span data-stu-id="0afdf-147">Array of strings, ordered by failover priority.</span></span>

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

### <span data-ttu-id="0afdf-148">-LocationObject</span><span class="sxs-lookup"><span data-stu-id="0afdf-148">-LocationObject</span></span>
<span data-ttu-id="0afdf-149">Lägga till en plats i Cosmos DB-databasnamn.</span><span class="sxs-lookup"><span data-stu-id="0afdf-149">Add a location to the Cosmos DB database account.</span></span> <span data-ttu-id="0afdf-150">Matris med PSLocation-objekt.</span><span class="sxs-lookup"><span data-stu-id="0afdf-150">Array of PSLocation objects.</span></span>

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

### <span data-ttu-id="0afdf-151">-MaxStalenessIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="0afdf-151">-MaxStalenessIntervalInSeconds</span></span>
<span data-ttu-id="0afdf-152">När det här värdet används med utgångs punkt som är bundet till inaktivitet representerar det tids mängd inaktuellt (i TimeSpan) som tolereras.</span><span class="sxs-lookup"><span data-stu-id="0afdf-152">When used with Bounded Staleness consistency, this value represents the time amount of staleness (in timespan) tolerated.</span></span>
<span data-ttu-id="0afdf-153">Det tillåtna intervallet för det här värdet är 5-86400.</span><span class="sxs-lookup"><span data-stu-id="0afdf-153">Accepted range for this value is 5-86400.</span></span>

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

### <span data-ttu-id="0afdf-154">-MaxStalenessPrefix</span><span class="sxs-lookup"><span data-stu-id="0afdf-154">-MaxStalenessPrefix</span></span>
<span data-ttu-id="0afdf-155">När det används med avgränsad utgångs konsekvens representerar det här värdet antalet begärda föråldrade förfrågningar.</span><span class="sxs-lookup"><span data-stu-id="0afdf-155">When used with Bounded Staleness consistency, this value represents the number of stale requests tolerated.</span></span>
<span data-ttu-id="0afdf-156">Det tillåtna intervallet för det här värdet är 1-2 147 483 647.</span><span class="sxs-lookup"><span data-stu-id="0afdf-156">Accepted range for this value is 1 - 2,147,483,647.</span></span>

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

### <span data-ttu-id="0afdf-157">-Namn</span><span class="sxs-lookup"><span data-stu-id="0afdf-157">-Name</span></span>
<span data-ttu-id="0afdf-158">Namn på Cosmos DB-databas.</span><span class="sxs-lookup"><span data-stu-id="0afdf-158">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="0afdf-159">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="0afdf-159">-PublicNetworkAccess</span></span>
<span data-ttu-id="0afdf-160">Om åtkomst för offentlig slut punkt tillåts för den här servern.</span><span class="sxs-lookup"><span data-stu-id="0afdf-160">Whether or not public endpoint access is allowed for this server.</span></span> <span data-ttu-id="0afdf-161">Möjliga värden är: ' Enabled ', ' disabled '</span><span class="sxs-lookup"><span data-stu-id="0afdf-161">Possible values include: 'Enabled', 'Disabled'</span></span>

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

### <span data-ttu-id="0afdf-162">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0afdf-162">-ResourceGroupName</span></span>
<span data-ttu-id="0afdf-163">Namn på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="0afdf-163">Name of resource group.</span></span>

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

### <span data-ttu-id="0afdf-164">-ServerVersion</span><span class="sxs-lookup"><span data-stu-id="0afdf-164">-ServerVersion</span></span>
<span data-ttu-id="0afdf-165">ServerVersion, giltigt endast i händelse av MongoDB-konton.</span><span class="sxs-lookup"><span data-stu-id="0afdf-165">ServerVersion, valid only in case of MongoDB Accounts.</span></span>

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

### <span data-ttu-id="0afdf-166">-Tagg</span><span class="sxs-lookup"><span data-stu-id="0afdf-166">-Tag</span></span>
<span data-ttu-id="0afdf-167">En produkt kod med taggar som par med nyckelord-värde.</span><span class="sxs-lookup"><span data-stu-id="0afdf-167">Hashtable of tags as key-value pairs.</span></span>
<span data-ttu-id="0afdf-168">Använd en tom sträng för att ta bort en befintlig tagg.</span><span class="sxs-lookup"><span data-stu-id="0afdf-168">Use empty string to clear existing tag.</span></span>

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

### <span data-ttu-id="0afdf-169">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="0afdf-169">-VirtualNetworkRule</span></span>
<span data-ttu-id="0afdf-170">Matris med sträng värden för ACL för virtuella nätverk.</span><span class="sxs-lookup"><span data-stu-id="0afdf-170">Array of string values of ACL's for virtual network.</span></span>

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

### <span data-ttu-id="0afdf-171">-VirtualNetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="0afdf-171">-VirtualNetworkRuleObject</span></span>
<span data-ttu-id="0afdf-172">Matris med PSVirtualNetworkRuleObjects för virtuella nätverk.</span><span class="sxs-lookup"><span data-stu-id="0afdf-172">Array of PSVirtualNetworkRuleObjects for virtual network.</span></span>

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

### <span data-ttu-id="0afdf-173">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0afdf-173">-WhatIf</span></span>
<span data-ttu-id="0afdf-174">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="0afdf-174">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0afdf-175">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="0afdf-175">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0afdf-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0afdf-176">CommonParameters</span></span>
<span data-ttu-id="0afdf-177">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0afdf-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0afdf-178">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0afdf-178">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0afdf-179">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0afdf-179">INPUTS</span></span>

### <span data-ttu-id="0afdf-180">Microsoft. Azure. commands. CosmosDB. Models. PSCorsRule []</span><span class="sxs-lookup"><span data-stu-id="0afdf-180">Microsoft.Azure.Commands.CosmosDB.Models.PSCorsRule[]</span></span>

## <span data-ttu-id="0afdf-181">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0afdf-181">OUTPUTS</span></span>

### <span data-ttu-id="0afdf-182">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="0afdf-182">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="0afdf-183">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0afdf-183">NOTES</span></span>

## <span data-ttu-id="0afdf-184">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0afdf-184">RELATED LINKS</span></span>
