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
ms.locfileid: "93747273"
---
# <span data-ttu-id="cf09b-101">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="cf09b-101">New-AzRedisCache</span></span>

## <span data-ttu-id="cf09b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="cf09b-102">SYNOPSIS</span></span>
<span data-ttu-id="cf09b-103">Skapar en Redis cache.</span><span class="sxs-lookup"><span data-stu-id="cf09b-103">Creates a Redis Cache.</span></span>

## <span data-ttu-id="cf09b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="cf09b-104">SYNTAX</span></span>

```
New-AzRedisCache -ResourceGroupName <String> -Name <String> -Location <String> [-Size <String>] [-Sku <String>]
 [-RedisConfiguration <Hashtable>] [-EnableNonSslPort <Boolean>] [-TenantSettings <Hashtable>]
 [-ShardCount <Int32>] [-SubnetId <String>] [-StaticIP <String>] [-Tag <Hashtable>] [-Zone <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cf09b-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="cf09b-105">DESCRIPTION</span></span>
<span data-ttu-id="cf09b-106">Cmdleten **New-AzRedisCache** skapar ett Azure Redis-cacheminne.</span><span class="sxs-lookup"><span data-stu-id="cf09b-106">The **New-AzRedisCache** cmdlet creates an Azure Redis Cache.</span></span>

## <span data-ttu-id="cf09b-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="cf09b-107">EXAMPLES</span></span>

### <span data-ttu-id="cf09b-108">Exempel 1: skapa en Redis-cache</span><span class="sxs-lookup"><span data-stu-id="cf09b-108">Example 1: Create a Redis Cache</span></span>
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

<span data-ttu-id="cf09b-109">Det här kommandot skapar en Redis cache.</span><span class="sxs-lookup"><span data-stu-id="cf09b-109">This command creates a Redis Cache.</span></span>

### <span data-ttu-id="cf09b-110">Exempel 2: skapa en standard-SKU Redis cache</span><span class="sxs-lookup"><span data-stu-id="cf09b-110">Example 2: Create a Standard SKU Redis Cache</span></span>
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

<span data-ttu-id="cf09b-111">Det här kommandot skapar en Redis cache.</span><span class="sxs-lookup"><span data-stu-id="cf09b-111">This command creates a Redis Cache.</span></span>

## <span data-ttu-id="cf09b-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="cf09b-112">PARAMETERS</span></span>

### <span data-ttu-id="cf09b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf09b-113">-DefaultProfile</span></span>
<span data-ttu-id="cf09b-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="cf09b-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cf09b-115">-EnableNonSslPort</span><span class="sxs-lookup"><span data-stu-id="cf09b-115">-EnableNonSslPort</span></span>
<span data-ttu-id="cf09b-116">Anger om icke-SSL-porten är aktive rad.</span><span class="sxs-lookup"><span data-stu-id="cf09b-116">Indicates whether the non-SSL port is enabled.</span></span>
<span data-ttu-id="cf09b-117">Standardvärdet är $False (icke-SSL-porten är inaktive rad).</span><span class="sxs-lookup"><span data-stu-id="cf09b-117">The default value is $False (the non-SSL port is disabled).</span></span>

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

### <span data-ttu-id="cf09b-118">-Plats</span><span class="sxs-lookup"><span data-stu-id="cf09b-118">-Location</span></span>
<span data-ttu-id="cf09b-119">Anger den plats där du vill skapa en Redis cache.</span><span class="sxs-lookup"><span data-stu-id="cf09b-119">Specifies the location in which to create a Redis Cache.</span></span>
<span data-ttu-id="cf09b-120">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="cf09b-120">Valid values are:</span></span> 
- <span data-ttu-id="cf09b-121">Norra Central USA</span><span class="sxs-lookup"><span data-stu-id="cf09b-121">North Central US</span></span>
- <span data-ttu-id="cf09b-122">Södra centrala USA</span><span class="sxs-lookup"><span data-stu-id="cf09b-122">South Central US</span></span>
- <span data-ttu-id="cf09b-123">Central</span><span class="sxs-lookup"><span data-stu-id="cf09b-123">Central US</span></span>
- <span data-ttu-id="cf09b-124">Västeuropa</span><span class="sxs-lookup"><span data-stu-id="cf09b-124">West Europe</span></span>
- <span data-ttu-id="cf09b-125">Nord Europa</span><span class="sxs-lookup"><span data-stu-id="cf09b-125">North Europe</span></span>
- <span data-ttu-id="cf09b-126">Västra USA</span><span class="sxs-lookup"><span data-stu-id="cf09b-126">West US</span></span>
- <span data-ttu-id="cf09b-127">Östra USA</span><span class="sxs-lookup"><span data-stu-id="cf09b-127">East US</span></span>
- <span data-ttu-id="cf09b-128">Östra USA 2</span><span class="sxs-lookup"><span data-stu-id="cf09b-128">East US 2</span></span>
- <span data-ttu-id="cf09b-129">Östra Japan</span><span class="sxs-lookup"><span data-stu-id="cf09b-129">Japan East</span></span>
- <span data-ttu-id="cf09b-130">Västra Japan</span><span class="sxs-lookup"><span data-stu-id="cf09b-130">Japan West</span></span>
- <span data-ttu-id="cf09b-131">Brasilien, Syd</span><span class="sxs-lookup"><span data-stu-id="cf09b-131">Brazil South</span></span>
- <span data-ttu-id="cf09b-132">Sydostasien</span><span class="sxs-lookup"><span data-stu-id="cf09b-132">Southeast Asia</span></span>
- <span data-ttu-id="cf09b-133">Östasien</span><span class="sxs-lookup"><span data-stu-id="cf09b-133">East Asia</span></span>
- <span data-ttu-id="cf09b-134">Östra Australien</span><span class="sxs-lookup"><span data-stu-id="cf09b-134">Australia East</span></span>
- <span data-ttu-id="cf09b-135">Australien, sydöst</span><span class="sxs-lookup"><span data-stu-id="cf09b-135">Australia Southeast</span></span>

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

### <span data-ttu-id="cf09b-136">-Namn</span><span class="sxs-lookup"><span data-stu-id="cf09b-136">-Name</span></span>
<span data-ttu-id="cf09b-137">Anger namnet på den Redis-cache som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="cf09b-137">Specifies the name of the Redis Cache to create.</span></span>

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

### <span data-ttu-id="cf09b-138">-RedisConfiguration</span><span class="sxs-lookup"><span data-stu-id="cf09b-138">-RedisConfiguration</span></span>
<span data-ttu-id="cf09b-139">Anger konfigurations inställningar för Redis.</span><span class="sxs-lookup"><span data-stu-id="cf09b-139">Specifies Redis configuration settings.</span></span>
<span data-ttu-id="cf09b-140">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="cf09b-140">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="cf09b-141">RDB – säkerhets kopiering aktive rad.</span><span class="sxs-lookup"><span data-stu-id="cf09b-141">rdb-backup-enabled.</span></span>
<span data-ttu-id="cf09b-142">Anger att Redis data persistence är aktiverat.</span><span class="sxs-lookup"><span data-stu-id="cf09b-142">Specifies that Redis data persistence is enabled.</span></span>
<span data-ttu-id="cf09b-143">Endast Premium-nivå.</span><span class="sxs-lookup"><span data-stu-id="cf09b-143">Premium tier only.</span></span>
- <span data-ttu-id="cf09b-144">RDB-lagring-anslutning-sträng.</span><span class="sxs-lookup"><span data-stu-id="cf09b-144">rdb-storage-connection-string.</span></span>
<span data-ttu-id="cf09b-145">Anger anslutnings strängen till lagrings konto för Redis data.</span><span class="sxs-lookup"><span data-stu-id="cf09b-145">Specifies the connection string to the Storage account for Redis data persistence.</span></span>
<span data-ttu-id="cf09b-146">Endast Premium-nivå.</span><span class="sxs-lookup"><span data-stu-id="cf09b-146">Premium tier only.</span></span>
- <span data-ttu-id="cf09b-147">RDB-säkerhets kopiering-frekvens.</span><span class="sxs-lookup"><span data-stu-id="cf09b-147">rdb-backup-frequency.</span></span>
<span data-ttu-id="cf09b-148">Anger säkerhets kopierings frekvensen för Redis data.</span><span class="sxs-lookup"><span data-stu-id="cf09b-148">Specifies the backup frequency for Redis data persistence.</span></span>
<span data-ttu-id="cf09b-149">Endast Premium-nivå.</span><span class="sxs-lookup"><span data-stu-id="cf09b-149">Premium tier only.</span></span> 
- <span data-ttu-id="cf09b-150">maxmemory-reserverad.</span><span class="sxs-lookup"><span data-stu-id="cf09b-150">maxmemory-reserved.</span></span>
<span data-ttu-id="cf09b-151">Konfigurerar minnet reserverat för icke-cachelagrade processer.</span><span class="sxs-lookup"><span data-stu-id="cf09b-151">Configures the memory reserved for non-cache processes.</span></span>
<span data-ttu-id="cf09b-152">Standard-och Premium-nivåer.</span><span class="sxs-lookup"><span data-stu-id="cf09b-152">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="cf09b-153">maxmemory-policy.</span><span class="sxs-lookup"><span data-stu-id="cf09b-153">maxmemory-policy.</span></span>
<span data-ttu-id="cf09b-154">Konfigurerar borttagnings principen för cacheminnet.</span><span class="sxs-lookup"><span data-stu-id="cf09b-154">Configures the eviction policy for the cache.</span></span>
<span data-ttu-id="cf09b-155">Alla pris nivåer.</span><span class="sxs-lookup"><span data-stu-id="cf09b-155">All pricing tiers.</span></span> 
- <span data-ttu-id="cf09b-156">meddelande – inloggnings händelser.</span><span class="sxs-lookup"><span data-stu-id="cf09b-156">notify-keyspace-events.</span></span>
<span data-ttu-id="cf09b-157">Konfigurerar indikeringar för meddelanden.</span><span class="sxs-lookup"><span data-stu-id="cf09b-157">Configures keyspace notifications.</span></span>
<span data-ttu-id="cf09b-158">Standard-och Premium-nivåer.</span><span class="sxs-lookup"><span data-stu-id="cf09b-158">Standard and premium tiers.</span></span> 
- <span data-ttu-id="cf09b-159">hash-Max-ziplist-poster.</span><span class="sxs-lookup"><span data-stu-id="cf09b-159">hash-max-ziplist-entries.</span></span>
<span data-ttu-id="cf09b-160">Konfigurerar minnes optimering för små aggregerade data typer.</span><span class="sxs-lookup"><span data-stu-id="cf09b-160">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="cf09b-161">Standard-och Premium-nivåer.</span><span class="sxs-lookup"><span data-stu-id="cf09b-161">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="cf09b-162">hash-Max-ziplist-värde.</span><span class="sxs-lookup"><span data-stu-id="cf09b-162">hash-max-ziplist-value.</span></span>
<span data-ttu-id="cf09b-163">Konfigurerar minnes optimering för små aggregerade data typer.</span><span class="sxs-lookup"><span data-stu-id="cf09b-163">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="cf09b-164">Standard-och Premium-nivåer.</span><span class="sxs-lookup"><span data-stu-id="cf09b-164">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="cf09b-165">set-Max intset-poster.</span><span class="sxs-lookup"><span data-stu-id="cf09b-165">set-max-intset-entries.</span></span>
<span data-ttu-id="cf09b-166">Konfigurerar minnes optimering för små aggregerade data typer.</span><span class="sxs-lookup"><span data-stu-id="cf09b-166">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="cf09b-167">Standard-och Premium-nivåer.</span><span class="sxs-lookup"><span data-stu-id="cf09b-167">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="cf09b-168">zset-Max ziplist-poster.</span><span class="sxs-lookup"><span data-stu-id="cf09b-168">zset-max-ziplist-entries.</span></span>
<span data-ttu-id="cf09b-169">Konfigurerar minnes optimering för små aggregerade data typer.</span><span class="sxs-lookup"><span data-stu-id="cf09b-169">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="cf09b-170">Standard-och Premium-nivåer.</span><span class="sxs-lookup"><span data-stu-id="cf09b-170">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="cf09b-171">zset-Max-ziplist-värde.</span><span class="sxs-lookup"><span data-stu-id="cf09b-171">zset-max-ziplist-value.</span></span>
<span data-ttu-id="cf09b-172">Konfigurerar minnes optimering för små aggregerade data typer.</span><span class="sxs-lookup"><span data-stu-id="cf09b-172">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="cf09b-173">Standard-och Premium-nivåer.</span><span class="sxs-lookup"><span data-stu-id="cf09b-173">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="cf09b-174">samling.</span><span class="sxs-lookup"><span data-stu-id="cf09b-174">databases.</span></span>
<span data-ttu-id="cf09b-175">Konfigurerar antalet databaser.</span><span class="sxs-lookup"><span data-stu-id="cf09b-175">Configures the number of databases.</span></span>
<span data-ttu-id="cf09b-176">Det går bara att konfigurera den här egenskapen när cacheminnet skapas.</span><span class="sxs-lookup"><span data-stu-id="cf09b-176">This property can be configured only at cache creation.</span></span>
<span data-ttu-id="cf09b-177">Standard-och Premium-nivåer.</span><span class="sxs-lookup"><span data-stu-id="cf09b-177">Standard and Premium tiers.</span></span>
<span data-ttu-id="cf09b-178">Mer information finns i Hantera Azure Redis cache med Azure PowerShell https://go.microsoft.com/fwlink/?LinkId=800051 ( https://go.microsoft.com/fwlink/?LinkId=800051) .</span><span class="sxs-lookup"><span data-stu-id="cf09b-178">For more information, see Manage Azure Redis Cache with Azure PowerShellhttps://go.microsoft.com/fwlink/?LinkId=800051 (https://go.microsoft.com/fwlink/?LinkId=800051).</span></span>

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

### <span data-ttu-id="cf09b-179">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cf09b-179">-ResourceGroupName</span></span>
<span data-ttu-id="cf09b-180">Anger namnet på den resurs grupp där Redis cache ska skapas.</span><span class="sxs-lookup"><span data-stu-id="cf09b-180">Specifies the name of the resource group in which to create the Redis Cache.</span></span>

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

### <span data-ttu-id="cf09b-181">-ShardCount</span><span class="sxs-lookup"><span data-stu-id="cf09b-181">-ShardCount</span></span>
<span data-ttu-id="cf09b-182">Anger antalet Shards som ska skapas i ett Premium-kluster-cacheminne.</span><span class="sxs-lookup"><span data-stu-id="cf09b-182">Specifies the number of shards to create on a Premium cluster cache.</span></span>
<span data-ttu-id="cf09b-183">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="cf09b-183">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="cf09b-184">9.1</span><span class="sxs-lookup"><span data-stu-id="cf09b-184">1</span></span>
- <span data-ttu-id="cf09b-185">två</span><span class="sxs-lookup"><span data-stu-id="cf09b-185">2</span></span>
- <span data-ttu-id="cf09b-186">amp;3D</span><span class="sxs-lookup"><span data-stu-id="cf09b-186">3</span></span>
- <span data-ttu-id="cf09b-187">9.4</span><span class="sxs-lookup"><span data-stu-id="cf09b-187">4</span></span>
- <span data-ttu-id="cf09b-188">T5</span><span class="sxs-lookup"><span data-stu-id="cf09b-188">5</span></span>
- <span data-ttu-id="cf09b-189">18.6</span><span class="sxs-lookup"><span data-stu-id="cf09b-189">6</span></span>
- <span data-ttu-id="cf09b-190">borttagning</span><span class="sxs-lookup"><span data-stu-id="cf09b-190">7</span></span>
- <span data-ttu-id="cf09b-191">8.2</span><span class="sxs-lookup"><span data-stu-id="cf09b-191">8</span></span>
- <span data-ttu-id="cf09b-192">9</span><span class="sxs-lookup"><span data-stu-id="cf09b-192">9</span></span> 
- <span data-ttu-id="cf09b-193">10.3</span><span class="sxs-lookup"><span data-stu-id="cf09b-193">10</span></span>

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

### <span data-ttu-id="cf09b-194">-Storlek</span><span class="sxs-lookup"><span data-stu-id="cf09b-194">-Size</span></span>
<span data-ttu-id="cf09b-195">Anger storleken på Redis cache.</span><span class="sxs-lookup"><span data-stu-id="cf09b-195">Specifies the size of the Redis Cache.</span></span>
<span data-ttu-id="cf09b-196">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="cf09b-196">Valid values are:</span></span> 
- <span data-ttu-id="cf09b-197">P1</span><span class="sxs-lookup"><span data-stu-id="cf09b-197">P1</span></span>
- <span data-ttu-id="cf09b-198">P2</span><span class="sxs-lookup"><span data-stu-id="cf09b-198">P2</span></span>
- <span data-ttu-id="cf09b-199">P3</span><span class="sxs-lookup"><span data-stu-id="cf09b-199">P3</span></span>
- <span data-ttu-id="cf09b-200">P4</span><span class="sxs-lookup"><span data-stu-id="cf09b-200">P4</span></span>
- <span data-ttu-id="cf09b-201">C0</span><span class="sxs-lookup"><span data-stu-id="cf09b-201">C0</span></span>
- <span data-ttu-id="cf09b-202">C1</span><span class="sxs-lookup"><span data-stu-id="cf09b-202">C1</span></span>
- <span data-ttu-id="cf09b-203">C2</span><span class="sxs-lookup"><span data-stu-id="cf09b-203">C2</span></span>
- <span data-ttu-id="cf09b-204">C3</span><span class="sxs-lookup"><span data-stu-id="cf09b-204">C3</span></span>
- <span data-ttu-id="cf09b-205">C4</span><span class="sxs-lookup"><span data-stu-id="cf09b-205">C4</span></span>
- <span data-ttu-id="cf09b-206">C5</span><span class="sxs-lookup"><span data-stu-id="cf09b-206">C5</span></span>
- <span data-ttu-id="cf09b-207">C6</span><span class="sxs-lookup"><span data-stu-id="cf09b-207">C6</span></span>
- <span data-ttu-id="cf09b-208">250</span><span class="sxs-lookup"><span data-stu-id="cf09b-208">250MB</span></span>
- <span data-ttu-id="cf09b-209">MINNE</span><span class="sxs-lookup"><span data-stu-id="cf09b-209">1GB</span></span>
- <span data-ttu-id="cf09b-210">2,5 GB</span><span class="sxs-lookup"><span data-stu-id="cf09b-210">2.5GB</span></span>
- <span data-ttu-id="cf09b-211">6GB</span><span class="sxs-lookup"><span data-stu-id="cf09b-211">6GB</span></span>
- <span data-ttu-id="cf09b-212">13GB</span><span class="sxs-lookup"><span data-stu-id="cf09b-212">13GB</span></span>
- <span data-ttu-id="cf09b-213">26GB</span><span class="sxs-lookup"><span data-stu-id="cf09b-213">26GB</span></span>
- <span data-ttu-id="cf09b-214">53GB standardvärdet är 1 GB eller C1.</span><span class="sxs-lookup"><span data-stu-id="cf09b-214">53GB The default value is 1GB or C1.</span></span>

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

### <span data-ttu-id="cf09b-215">-SKU</span><span class="sxs-lookup"><span data-stu-id="cf09b-215">-Sku</span></span>
<span data-ttu-id="cf09b-216">Anger SKU för det Redis-cacheminne som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="cf09b-216">Specifies the SKU of the Redis Cache to create.</span></span>
<span data-ttu-id="cf09b-217">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="cf09b-217">Valid values are:</span></span> 
- <span data-ttu-id="cf09b-218">Basisk</span><span class="sxs-lookup"><span data-stu-id="cf09b-218">Basic</span></span>
- <span data-ttu-id="cf09b-219">Standar</span><span class="sxs-lookup"><span data-stu-id="cf09b-219">Standard</span></span>
- <span data-ttu-id="cf09b-220">Premium är standardvärdet standard.</span><span class="sxs-lookup"><span data-stu-id="cf09b-220">Premium The default value is Standard.</span></span>

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

### <span data-ttu-id="cf09b-221">-StaticIP</span><span class="sxs-lookup"><span data-stu-id="cf09b-221">-StaticIP</span></span>
<span data-ttu-id="cf09b-222">Anger en unik IP-adress i Redis-cachen.</span><span class="sxs-lookup"><span data-stu-id="cf09b-222">Specifies a unique IP address in the subnet for the Redis Cache.</span></span>
<span data-ttu-id="cf09b-223">Om du inte anger ett värde för den här parametern väljer denna cmdlet en IP-adress från under nätet.</span><span class="sxs-lookup"><span data-stu-id="cf09b-223">If you do not specify a value for this parameter, this cmdlet chooses an IP address from the subnet.</span></span>

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

### <span data-ttu-id="cf09b-224">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="cf09b-224">-SubnetId</span></span>
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

### <span data-ttu-id="cf09b-225">-Tagg</span><span class="sxs-lookup"><span data-stu-id="cf09b-225">-Tag</span></span>
<span data-ttu-id="cf09b-226">En hash-tabell som representerar taggar.</span><span class="sxs-lookup"><span data-stu-id="cf09b-226">A hash table which represents tags.</span></span>

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

### <span data-ttu-id="cf09b-227">-TenantSettings</span><span class="sxs-lookup"><span data-stu-id="cf09b-227">-TenantSettings</span></span>
<span data-ttu-id="cf09b-228">Denna parameter är inaktuell.</span><span class="sxs-lookup"><span data-stu-id="cf09b-228">This parameter has been deprecated.</span></span>

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

### <span data-ttu-id="cf09b-229">-Zone</span><span class="sxs-lookup"><span data-stu-id="cf09b-229">-Zone</span></span>
<span data-ttu-id="cf09b-230">Lista över zoner.</span><span class="sxs-lookup"><span data-stu-id="cf09b-230">List of zones.</span></span>

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

### <span data-ttu-id="cf09b-231">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="cf09b-231">-Confirm</span></span>
<span data-ttu-id="cf09b-232">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="cf09b-232">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cf09b-233">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cf09b-233">-WhatIf</span></span>
<span data-ttu-id="cf09b-234">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="cf09b-234">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cf09b-235">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="cf09b-235">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cf09b-236">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf09b-236">CommonParameters</span></span>
<span data-ttu-id="cf09b-237">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cf09b-237">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf09b-238">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cf09b-238">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf09b-239">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="cf09b-239">INPUTS</span></span>

### <span data-ttu-id="cf09b-240">System. String</span><span class="sxs-lookup"><span data-stu-id="cf09b-240">System.String</span></span>

### <span data-ttu-id="cf09b-241">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="cf09b-241">System.Collections.Hashtable</span></span>

### <span data-ttu-id="cf09b-242">System. Nullable ' 1 [[system. Boolean, system. privat. CoreLib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="cf09b-242">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="cf09b-243">System. Nullable ' 1 [[system. Int32, system. privat. CoreLib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="cf09b-243">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="cf09b-244">System. string []</span><span class="sxs-lookup"><span data-stu-id="cf09b-244">System.String[]</span></span>

## <span data-ttu-id="cf09b-245">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="cf09b-245">OUTPUTS</span></span>

### <span data-ttu-id="cf09b-246">Microsoft. Azure. commands. RedisCache. Models. RedisCacheAttributesWithAccessKeys</span><span class="sxs-lookup"><span data-stu-id="cf09b-246">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributesWithAccessKeys</span></span>

## <span data-ttu-id="cf09b-247">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="cf09b-247">NOTES</span></span>

## <span data-ttu-id="cf09b-248">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="cf09b-248">RELATED LINKS</span></span>

[<span data-ttu-id="cf09b-249">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="cf09b-249">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="cf09b-250">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="cf09b-250">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="cf09b-251">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="cf09b-251">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)

