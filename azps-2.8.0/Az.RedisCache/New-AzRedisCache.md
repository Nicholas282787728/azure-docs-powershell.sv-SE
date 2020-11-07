---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: 81179AFE-6524-4F59-8BC2-3E152F51D1DD
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/new-azrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCache.md
ms.openlocfilehash: ab0b84578339568e48458de8a89daccd83092e65
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93919677"
---
# <span data-ttu-id="96c85-101">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="96c85-101">New-AzRedisCache</span></span>

## <span data-ttu-id="96c85-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="96c85-102">SYNOPSIS</span></span>
<span data-ttu-id="96c85-103">Skapar en Redis cache.</span><span class="sxs-lookup"><span data-stu-id="96c85-103">Creates a Redis Cache.</span></span>

## <span data-ttu-id="96c85-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="96c85-104">SYNTAX</span></span>

```
New-AzRedisCache -ResourceGroupName <String> -Name <String> -Location <String> [-Size <String>] [-Sku <String>]
 [-RedisConfiguration <Hashtable>] [-EnableNonSslPort <Boolean>] [-TenantSettings <Hashtable>]
 [-ShardCount <Int32>] [-SubnetId <String>] [-StaticIP <String>] [-Tag <Hashtable>] [-Zone <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="96c85-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="96c85-105">DESCRIPTION</span></span>
<span data-ttu-id="96c85-106">Cmdleten **New-AzRedisCache** skapar ett Azure Redis-cacheminne.</span><span class="sxs-lookup"><span data-stu-id="96c85-106">The **New-AzRedisCache** cmdlet creates an Azure Redis Cache.</span></span>

## <span data-ttu-id="96c85-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="96c85-107">EXAMPLES</span></span>

### <span data-ttu-id="96c85-108">Exempel 1: skapa en Redis-cache</span><span class="sxs-lookup"><span data-stu-id="96c85-108">Example 1: Create a Redis Cache</span></span>
```
PS C:\>New-AzRedisCache -ResourceGroupName "MyGroup" -Name "MyCache" -Location "North Central US"

          PrimaryKey         : pJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
          SecondaryKey       : sJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
          ResourceGroupName  : MyGroup
          Id                 : /subscriptions/a559b6fd-3a84-40bb-a450-b0db5ed37dfe/resourceGroups/mygroup/providers/Microsoft.Cache/Redis/mycache
          Location           : North Central US
          Name               : MyCache
          Type               : Microsoft.Cache/Redis
          HostName           : mycache.redis.cache.windows.net 
          Port               : 6379
          ProvisioningState  : creating
          SslPort            : 6380
          RedisConfiguration : {}
          EnableNonSslPort   : False
          RedisVersion       : 2.8
          Size               : 1GB
          Sku                : Standard
          Tag                : {}
          Zone               : []
```

<span data-ttu-id="96c85-109">Det här kommandot skapar en Redis cache.</span><span class="sxs-lookup"><span data-stu-id="96c85-109">This command creates a Redis Cache.</span></span>

### <span data-ttu-id="96c85-110">Exempel 2: skapa en standard-SKU Redis cache</span><span class="sxs-lookup"><span data-stu-id="96c85-110">Example 2: Create a Standard SKU Redis Cache</span></span>
```
PS C:\>New-AzRedisCache -ResourceGroupName "MyGroup" -Name "MyCache" -Location "North Central US" -Size 250MB -Sku "Standard" -RedisConfiguration @{"maxmemory-policy" = "allkeys-random"} -Force

          PrimaryKey         : pJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
          SecondaryKey       : sJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
          ResourceGroupName  : MyGroup
          Id                 : /subscriptions/a559b6fd-3a84-40bb-a450-b0db5ed37dfe/resourceGroups/mygroup/providers/Microsoft.Cache/Redis/MyCache
          Location           : North Central US
          Name               : mycache
          Type               : Microsoft.Cache/Redis
          HostName           : mycache.redis.cache.windows.net
          Port               : 6379
          ProvisioningState  : creating
          SslPort            : 6380
          RedisConfiguration : {[maxmemory-policy, allkeys-random]} 
          EnableNonSslPort   : False
          RedisVersion       : 2.8
          Size               : 250MB
          Sku                : Standard
          Tag                : {}
          Zone               : []
```

<span data-ttu-id="96c85-111">Det här kommandot skapar en Redis cache.</span><span class="sxs-lookup"><span data-stu-id="96c85-111">This command creates a Redis Cache.</span></span>

## <span data-ttu-id="96c85-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="96c85-112">PARAMETERS</span></span>

### <span data-ttu-id="96c85-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96c85-113">-DefaultProfile</span></span>
<span data-ttu-id="96c85-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="96c85-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="96c85-115">-EnableNonSslPort</span><span class="sxs-lookup"><span data-stu-id="96c85-115">-EnableNonSslPort</span></span>
<span data-ttu-id="96c85-116">Anger om icke-SSL-porten är aktive rad.</span><span class="sxs-lookup"><span data-stu-id="96c85-116">Indicates whether the non-SSL port is enabled.</span></span>
<span data-ttu-id="96c85-117">Standardvärdet är $False (icke-SSL-porten är inaktive rad).</span><span class="sxs-lookup"><span data-stu-id="96c85-117">The default value is $False (the non-SSL port is disabled).</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="96c85-118">-Plats</span><span class="sxs-lookup"><span data-stu-id="96c85-118">-Location</span></span>
<span data-ttu-id="96c85-119">Anger den plats där du vill skapa en Redis cache.</span><span class="sxs-lookup"><span data-stu-id="96c85-119">Specifies the location in which to create a Redis Cache.</span></span>
<span data-ttu-id="96c85-120">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="96c85-120">Valid values are:</span></span> 
- <span data-ttu-id="96c85-121">Norra Central USA</span><span class="sxs-lookup"><span data-stu-id="96c85-121">North Central US</span></span>
- <span data-ttu-id="96c85-122">Södra centrala USA</span><span class="sxs-lookup"><span data-stu-id="96c85-122">South Central US</span></span>
- <span data-ttu-id="96c85-123">Central</span><span class="sxs-lookup"><span data-stu-id="96c85-123">Central US</span></span>
- <span data-ttu-id="96c85-124">Västeuropa</span><span class="sxs-lookup"><span data-stu-id="96c85-124">West Europe</span></span>
- <span data-ttu-id="96c85-125">Nord Europa</span><span class="sxs-lookup"><span data-stu-id="96c85-125">North Europe</span></span>
- <span data-ttu-id="96c85-126">Västra USA</span><span class="sxs-lookup"><span data-stu-id="96c85-126">West US</span></span>
- <span data-ttu-id="96c85-127">Östra USA</span><span class="sxs-lookup"><span data-stu-id="96c85-127">East US</span></span>
- <span data-ttu-id="96c85-128">Östra USA 2</span><span class="sxs-lookup"><span data-stu-id="96c85-128">East US 2</span></span>
- <span data-ttu-id="96c85-129">Östra Japan</span><span class="sxs-lookup"><span data-stu-id="96c85-129">Japan East</span></span>
- <span data-ttu-id="96c85-130">Västra Japan</span><span class="sxs-lookup"><span data-stu-id="96c85-130">Japan West</span></span>
- <span data-ttu-id="96c85-131">Brasilien, Syd</span><span class="sxs-lookup"><span data-stu-id="96c85-131">Brazil South</span></span>
- <span data-ttu-id="96c85-132">Sydostasien</span><span class="sxs-lookup"><span data-stu-id="96c85-132">Southeast Asia</span></span>
- <span data-ttu-id="96c85-133">Östasien</span><span class="sxs-lookup"><span data-stu-id="96c85-133">East Asia</span></span>
- <span data-ttu-id="96c85-134">Östra Australien</span><span class="sxs-lookup"><span data-stu-id="96c85-134">Australia East</span></span>
- <span data-ttu-id="96c85-135">Australien, sydöst</span><span class="sxs-lookup"><span data-stu-id="96c85-135">Australia Southeast</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="96c85-136">-Namn</span><span class="sxs-lookup"><span data-stu-id="96c85-136">-Name</span></span>
<span data-ttu-id="96c85-137">Anger namnet på den Redis-cache som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="96c85-137">Specifies the name of the Redis Cache to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="96c85-138">-RedisConfiguration</span><span class="sxs-lookup"><span data-stu-id="96c85-138">-RedisConfiguration</span></span>
<span data-ttu-id="96c85-139">Anger konfigurations inställningar för Redis.</span><span class="sxs-lookup"><span data-stu-id="96c85-139">Specifies Redis configuration settings.</span></span>
<span data-ttu-id="96c85-140">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="96c85-140">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="96c85-141">RDB – säkerhets kopiering aktive rad.</span><span class="sxs-lookup"><span data-stu-id="96c85-141">rdb-backup-enabled.</span></span>
<span data-ttu-id="96c85-142">Anger att Redis data persistence är aktiverat.</span><span class="sxs-lookup"><span data-stu-id="96c85-142">Specifies that Redis data persistence is enabled.</span></span>
<span data-ttu-id="96c85-143">Endast Premium-nivå.</span><span class="sxs-lookup"><span data-stu-id="96c85-143">Premium tier only.</span></span>
- <span data-ttu-id="96c85-144">RDB-lagring-anslutning-sträng.</span><span class="sxs-lookup"><span data-stu-id="96c85-144">rdb-storage-connection-string.</span></span>
<span data-ttu-id="96c85-145">Anger anslutnings strängen till lagrings konto för Redis data.</span><span class="sxs-lookup"><span data-stu-id="96c85-145">Specifies the connection string to the Storage account for Redis data persistence.</span></span>
<span data-ttu-id="96c85-146">Endast Premium-nivå.</span><span class="sxs-lookup"><span data-stu-id="96c85-146">Premium tier only.</span></span>
- <span data-ttu-id="96c85-147">RDB-säkerhets kopiering-frekvens.</span><span class="sxs-lookup"><span data-stu-id="96c85-147">rdb-backup-frequency.</span></span>
<span data-ttu-id="96c85-148">Anger säkerhets kopierings frekvensen för Redis data.</span><span class="sxs-lookup"><span data-stu-id="96c85-148">Specifies the backup frequency for Redis data persistence.</span></span>
<span data-ttu-id="96c85-149">Endast Premium-nivå.</span><span class="sxs-lookup"><span data-stu-id="96c85-149">Premium tier only.</span></span> 
- <span data-ttu-id="96c85-150">maxmemory-reserverad.</span><span class="sxs-lookup"><span data-stu-id="96c85-150">maxmemory-reserved.</span></span>
<span data-ttu-id="96c85-151">Konfigurerar minnet reserverat för icke-cachelagrade processer.</span><span class="sxs-lookup"><span data-stu-id="96c85-151">Configures the memory reserved for non-cache processes.</span></span>
<span data-ttu-id="96c85-152">Standard-och Premium-nivåer.</span><span class="sxs-lookup"><span data-stu-id="96c85-152">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="96c85-153">maxmemory-policy.</span><span class="sxs-lookup"><span data-stu-id="96c85-153">maxmemory-policy.</span></span>
<span data-ttu-id="96c85-154">Konfigurerar borttagnings principen för cacheminnet.</span><span class="sxs-lookup"><span data-stu-id="96c85-154">Configures the eviction policy for the cache.</span></span>
<span data-ttu-id="96c85-155">Alla pris nivåer.</span><span class="sxs-lookup"><span data-stu-id="96c85-155">All pricing tiers.</span></span> 
- <span data-ttu-id="96c85-156">meddelande – inloggnings händelser.</span><span class="sxs-lookup"><span data-stu-id="96c85-156">notify-keyspace-events.</span></span>
<span data-ttu-id="96c85-157">Konfigurerar indikeringar för meddelanden.</span><span class="sxs-lookup"><span data-stu-id="96c85-157">Configures keyspace notifications.</span></span>
<span data-ttu-id="96c85-158">Standard-och Premium-nivåer.</span><span class="sxs-lookup"><span data-stu-id="96c85-158">Standard and premium tiers.</span></span> 
- <span data-ttu-id="96c85-159">hash-Max-ziplist-poster.</span><span class="sxs-lookup"><span data-stu-id="96c85-159">hash-max-ziplist-entries.</span></span>
<span data-ttu-id="96c85-160">Konfigurerar minnes optimering för små aggregerade data typer.</span><span class="sxs-lookup"><span data-stu-id="96c85-160">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="96c85-161">Standard-och Premium-nivåer.</span><span class="sxs-lookup"><span data-stu-id="96c85-161">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="96c85-162">hash-Max-ziplist-värde.</span><span class="sxs-lookup"><span data-stu-id="96c85-162">hash-max-ziplist-value.</span></span>
<span data-ttu-id="96c85-163">Konfigurerar minnes optimering för små aggregerade data typer.</span><span class="sxs-lookup"><span data-stu-id="96c85-163">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="96c85-164">Standard-och Premium-nivåer.</span><span class="sxs-lookup"><span data-stu-id="96c85-164">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="96c85-165">set-Max intset-poster.</span><span class="sxs-lookup"><span data-stu-id="96c85-165">set-max-intset-entries.</span></span>
<span data-ttu-id="96c85-166">Konfigurerar minnes optimering för små aggregerade data typer.</span><span class="sxs-lookup"><span data-stu-id="96c85-166">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="96c85-167">Standard-och Premium-nivåer.</span><span class="sxs-lookup"><span data-stu-id="96c85-167">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="96c85-168">zset-Max ziplist-poster.</span><span class="sxs-lookup"><span data-stu-id="96c85-168">zset-max-ziplist-entries.</span></span>
<span data-ttu-id="96c85-169">Konfigurerar minnes optimering för små aggregerade data typer.</span><span class="sxs-lookup"><span data-stu-id="96c85-169">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="96c85-170">Standard-och Premium-nivåer.</span><span class="sxs-lookup"><span data-stu-id="96c85-170">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="96c85-171">zset-Max-ziplist-värde.</span><span class="sxs-lookup"><span data-stu-id="96c85-171">zset-max-ziplist-value.</span></span>
<span data-ttu-id="96c85-172">Konfigurerar minnes optimering för små aggregerade data typer.</span><span class="sxs-lookup"><span data-stu-id="96c85-172">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="96c85-173">Standard-och Premium-nivåer.</span><span class="sxs-lookup"><span data-stu-id="96c85-173">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="96c85-174">samling.</span><span class="sxs-lookup"><span data-stu-id="96c85-174">databases.</span></span>
<span data-ttu-id="96c85-175">Konfigurerar antalet databaser.</span><span class="sxs-lookup"><span data-stu-id="96c85-175">Configures the number of databases.</span></span>
<span data-ttu-id="96c85-176">Det går bara att konfigurera den här egenskapen när cacheminnet skapas.</span><span class="sxs-lookup"><span data-stu-id="96c85-176">This property can be configured only at cache creation.</span></span>
<span data-ttu-id="96c85-177">Standard-och Premium-nivåer.</span><span class="sxs-lookup"><span data-stu-id="96c85-177">Standard and Premium tiers.</span></span>
<span data-ttu-id="96c85-178">Mer information finns i Hantera Azure Redis cache med Azure PowerShell https://go.microsoft.com/fwlink/?LinkId=800051 ( https://go.microsoft.com/fwlink/?LinkId=800051) .</span><span class="sxs-lookup"><span data-stu-id="96c85-178">For more information, see Manage Azure Redis Cache with Azure PowerShellhttps://go.microsoft.com/fwlink/?LinkId=800051 (https://go.microsoft.com/fwlink/?LinkId=800051).</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="96c85-179">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="96c85-179">-ResourceGroupName</span></span>
<span data-ttu-id="96c85-180">Anger namnet på den resurs grupp där Redis cache ska skapas.</span><span class="sxs-lookup"><span data-stu-id="96c85-180">Specifies the name of the resource group in which to create the Redis Cache.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="96c85-181">-ShardCount</span><span class="sxs-lookup"><span data-stu-id="96c85-181">-ShardCount</span></span>
<span data-ttu-id="96c85-182">Anger antalet Shards som ska skapas i ett Premium-kluster-cacheminne.</span><span class="sxs-lookup"><span data-stu-id="96c85-182">Specifies the number of shards to create on a Premium cluster cache.</span></span>
<span data-ttu-id="96c85-183">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="96c85-183">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="96c85-184">9.1</span><span class="sxs-lookup"><span data-stu-id="96c85-184">1</span></span>
- <span data-ttu-id="96c85-185">två</span><span class="sxs-lookup"><span data-stu-id="96c85-185">2</span></span>
- <span data-ttu-id="96c85-186">amp;3D</span><span class="sxs-lookup"><span data-stu-id="96c85-186">3</span></span>
- <span data-ttu-id="96c85-187">9.4</span><span class="sxs-lookup"><span data-stu-id="96c85-187">4</span></span>
- <span data-ttu-id="96c85-188">T5</span><span class="sxs-lookup"><span data-stu-id="96c85-188">5</span></span>
- <span data-ttu-id="96c85-189">18.6</span><span class="sxs-lookup"><span data-stu-id="96c85-189">6</span></span>
- <span data-ttu-id="96c85-190">borttagning</span><span class="sxs-lookup"><span data-stu-id="96c85-190">7</span></span>
- <span data-ttu-id="96c85-191">8.2</span><span class="sxs-lookup"><span data-stu-id="96c85-191">8</span></span>
- <span data-ttu-id="96c85-192">9</span><span class="sxs-lookup"><span data-stu-id="96c85-192">9</span></span> 
- <span data-ttu-id="96c85-193">10.3</span><span class="sxs-lookup"><span data-stu-id="96c85-193">10</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="96c85-194">-Storlek</span><span class="sxs-lookup"><span data-stu-id="96c85-194">-Size</span></span>
<span data-ttu-id="96c85-195">Anger storleken på Redis cache.</span><span class="sxs-lookup"><span data-stu-id="96c85-195">Specifies the size of the Redis Cache.</span></span>
<span data-ttu-id="96c85-196">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="96c85-196">Valid values are:</span></span> 
- <span data-ttu-id="96c85-197">P1</span><span class="sxs-lookup"><span data-stu-id="96c85-197">P1</span></span>
- <span data-ttu-id="96c85-198">P2</span><span class="sxs-lookup"><span data-stu-id="96c85-198">P2</span></span>
- <span data-ttu-id="96c85-199">P3</span><span class="sxs-lookup"><span data-stu-id="96c85-199">P3</span></span>
- <span data-ttu-id="96c85-200">P4</span><span class="sxs-lookup"><span data-stu-id="96c85-200">P4</span></span>
- <span data-ttu-id="96c85-201">C0</span><span class="sxs-lookup"><span data-stu-id="96c85-201">C0</span></span>
- <span data-ttu-id="96c85-202">C1</span><span class="sxs-lookup"><span data-stu-id="96c85-202">C1</span></span>
- <span data-ttu-id="96c85-203">C2</span><span class="sxs-lookup"><span data-stu-id="96c85-203">C2</span></span>
- <span data-ttu-id="96c85-204">C3</span><span class="sxs-lookup"><span data-stu-id="96c85-204">C3</span></span>
- <span data-ttu-id="96c85-205">C4</span><span class="sxs-lookup"><span data-stu-id="96c85-205">C4</span></span>
- <span data-ttu-id="96c85-206">C5</span><span class="sxs-lookup"><span data-stu-id="96c85-206">C5</span></span>
- <span data-ttu-id="96c85-207">C6</span><span class="sxs-lookup"><span data-stu-id="96c85-207">C6</span></span>
- <span data-ttu-id="96c85-208">250</span><span class="sxs-lookup"><span data-stu-id="96c85-208">250MB</span></span>
- <span data-ttu-id="96c85-209">MINNE</span><span class="sxs-lookup"><span data-stu-id="96c85-209">1GB</span></span>
- <span data-ttu-id="96c85-210">2,5 GB</span><span class="sxs-lookup"><span data-stu-id="96c85-210">2.5GB</span></span>
- <span data-ttu-id="96c85-211">6GB</span><span class="sxs-lookup"><span data-stu-id="96c85-211">6GB</span></span>
- <span data-ttu-id="96c85-212">13GB</span><span class="sxs-lookup"><span data-stu-id="96c85-212">13GB</span></span>
- <span data-ttu-id="96c85-213">26GB</span><span class="sxs-lookup"><span data-stu-id="96c85-213">26GB</span></span>
- <span data-ttu-id="96c85-214">53GB standardvärdet är 1 GB eller C1.</span><span class="sxs-lookup"><span data-stu-id="96c85-214">53GB The default value is 1GB or C1.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="96c85-215">-SKU</span><span class="sxs-lookup"><span data-stu-id="96c85-215">-Sku</span></span>
<span data-ttu-id="96c85-216">Anger SKU för det Redis-cacheminne som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="96c85-216">Specifies the SKU of the Redis Cache to create.</span></span>
<span data-ttu-id="96c85-217">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="96c85-217">Valid values are:</span></span> 
- <span data-ttu-id="96c85-218">Basisk</span><span class="sxs-lookup"><span data-stu-id="96c85-218">Basic</span></span>
- <span data-ttu-id="96c85-219">Standar</span><span class="sxs-lookup"><span data-stu-id="96c85-219">Standard</span></span>
- <span data-ttu-id="96c85-220">Premium är standardvärdet standard.</span><span class="sxs-lookup"><span data-stu-id="96c85-220">Premium The default value is Standard.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Basic, Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="96c85-221">-StaticIP</span><span class="sxs-lookup"><span data-stu-id="96c85-221">-StaticIP</span></span>
<span data-ttu-id="96c85-222">Anger en unik IP-adress i Redis-cachen.</span><span class="sxs-lookup"><span data-stu-id="96c85-222">Specifies a unique IP address in the subnet for the Redis Cache.</span></span>
<span data-ttu-id="96c85-223">Om du inte anger ett värde för den här parametern väljer denna cmdlet en IP-adress från under nätet.</span><span class="sxs-lookup"><span data-stu-id="96c85-223">If you do not specify a value for this parameter, this cmdlet chooses an IP address from the subnet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="96c85-224">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="96c85-224">-SubnetId</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="96c85-225">-Tagg</span><span class="sxs-lookup"><span data-stu-id="96c85-225">-Tag</span></span>
<span data-ttu-id="96c85-226">En hash-tabell som representerar taggar.</span><span class="sxs-lookup"><span data-stu-id="96c85-226">A hash table which represents tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="96c85-227">-TenantSettings</span><span class="sxs-lookup"><span data-stu-id="96c85-227">-TenantSettings</span></span>
<span data-ttu-id="96c85-228">Denna parameter är inaktuell.</span><span class="sxs-lookup"><span data-stu-id="96c85-228">This parameter has been deprecated.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="96c85-229">-Zone</span><span class="sxs-lookup"><span data-stu-id="96c85-229">-Zone</span></span>
<span data-ttu-id="96c85-230">Lista över zoner.</span><span class="sxs-lookup"><span data-stu-id="96c85-230">List of zones.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="96c85-231">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="96c85-231">-Confirm</span></span>
<span data-ttu-id="96c85-232">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="96c85-232">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96c85-233">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="96c85-233">-WhatIf</span></span>
<span data-ttu-id="96c85-234">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="96c85-234">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="96c85-235">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="96c85-235">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96c85-236">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96c85-236">CommonParameters</span></span>
<span data-ttu-id="96c85-237">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="96c85-237">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96c85-238">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="96c85-238">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96c85-239">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="96c85-239">INPUTS</span></span>

### <span data-ttu-id="96c85-240">System. String</span><span class="sxs-lookup"><span data-stu-id="96c85-240">System.String</span></span>

### <span data-ttu-id="96c85-241">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="96c85-241">System.Collections.Hashtable</span></span>

### <span data-ttu-id="96c85-242">System. Nullable ' 1 [[system. Boolean, system. privat. CoreLib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="96c85-242">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="96c85-243">System. Nullable ' 1 [[system. Int32, system. privat. CoreLib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="96c85-243">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="96c85-244">System. string []</span><span class="sxs-lookup"><span data-stu-id="96c85-244">System.String[]</span></span>

## <span data-ttu-id="96c85-245">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="96c85-245">OUTPUTS</span></span>

### <span data-ttu-id="96c85-246">Microsoft. Azure. commands. RedisCache. Models. RedisCacheAttributesWithAccessKeys</span><span class="sxs-lookup"><span data-stu-id="96c85-246">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributesWithAccessKeys</span></span>

## <span data-ttu-id="96c85-247">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="96c85-247">NOTES</span></span>

## <span data-ttu-id="96c85-248">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="96c85-248">RELATED LINKS</span></span>

[<span data-ttu-id="96c85-249">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="96c85-249">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="96c85-250">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="96c85-250">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="96c85-251">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="96c85-251">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)


