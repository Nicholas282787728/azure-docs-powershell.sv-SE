---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: 81179AFE-6524-4F59-8BC2-3E152F51D1DD
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/new-azrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCache.md
ms.openlocfilehash: 2c11e12fa398c7a76fa10f1129bc5cf3696ae68c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94100907"
---
# <span data-ttu-id="a24c3-101">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="a24c3-101">New-AzRedisCache</span></span>

## <span data-ttu-id="a24c3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a24c3-102">SYNOPSIS</span></span>
<span data-ttu-id="a24c3-103">Skapar en Redis cache.</span><span class="sxs-lookup"><span data-stu-id="a24c3-103">Creates a Redis Cache.</span></span>

## <span data-ttu-id="a24c3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a24c3-104">SYNTAX</span></span>

```
New-AzRedisCache -ResourceGroupName <String> -Name <String> -Location <String> [-Size <String>] [-Sku <String>]
 [-RedisConfiguration <Hashtable>] [-EnableNonSslPort <Boolean>] [-TenantSettings <Hashtable>]
 [-ShardCount <Int32>] [-MinimumTlsVersion <String>] [-SubnetId <String>] [-StaticIP <String>]
 [-Tag <Hashtable>] [-Zone <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a24c3-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a24c3-105">DESCRIPTION</span></span>
<span data-ttu-id="a24c3-106">Cmdleten **New-AzRedisCache** skapar ett Azure Redis-cacheminne.</span><span class="sxs-lookup"><span data-stu-id="a24c3-106">The **New-AzRedisCache** cmdlet creates an Azure Redis Cache.</span></span>

## <span data-ttu-id="a24c3-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a24c3-107">EXAMPLES</span></span>

### <span data-ttu-id="a24c3-108">Exempel 1: skapa en Redis-cache</span><span class="sxs-lookup"><span data-stu-id="a24c3-108">Example 1: Create a Redis Cache</span></span>
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

<span data-ttu-id="a24c3-109">Det här kommandot skapar en Redis cache.</span><span class="sxs-lookup"><span data-stu-id="a24c3-109">This command creates a Redis Cache.</span></span>

### <span data-ttu-id="a24c3-110">Exempel 2: skapa en standard-SKU Redis cache</span><span class="sxs-lookup"><span data-stu-id="a24c3-110">Example 2: Create a Standard SKU Redis Cache</span></span>
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

<span data-ttu-id="a24c3-111">Det här kommandot skapar en Redis cache.</span><span class="sxs-lookup"><span data-stu-id="a24c3-111">This command creates a Redis Cache.</span></span>

## <span data-ttu-id="a24c3-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a24c3-112">PARAMETERS</span></span>

### <span data-ttu-id="a24c3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a24c3-113">-DefaultProfile</span></span>
<span data-ttu-id="a24c3-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a24c3-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a24c3-115">-EnableNonSslPort</span><span class="sxs-lookup"><span data-stu-id="a24c3-115">-EnableNonSslPort</span></span>
<span data-ttu-id="a24c3-116">Anger om icke-SSL-porten är aktive rad.</span><span class="sxs-lookup"><span data-stu-id="a24c3-116">Indicates whether the non-SSL port is enabled.</span></span>
<span data-ttu-id="a24c3-117">Standardvärdet är $False (icke-SSL-porten är inaktive rad).</span><span class="sxs-lookup"><span data-stu-id="a24c3-117">The default value is $False (the non-SSL port is disabled).</span></span>

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

### <span data-ttu-id="a24c3-118">-Plats</span><span class="sxs-lookup"><span data-stu-id="a24c3-118">-Location</span></span>
<span data-ttu-id="a24c3-119">Anger den plats där du vill skapa en Redis cache.</span><span class="sxs-lookup"><span data-stu-id="a24c3-119">Specifies the location in which to create a Redis Cache.</span></span>
<span data-ttu-id="a24c3-120">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="a24c3-120">Valid values are:</span></span> 
- <span data-ttu-id="a24c3-121">Norra Central USA</span><span class="sxs-lookup"><span data-stu-id="a24c3-121">North Central US</span></span>
- <span data-ttu-id="a24c3-122">Södra centrala USA</span><span class="sxs-lookup"><span data-stu-id="a24c3-122">South Central US</span></span>
- <span data-ttu-id="a24c3-123">Central</span><span class="sxs-lookup"><span data-stu-id="a24c3-123">Central US</span></span>
- <span data-ttu-id="a24c3-124">Västeuropa</span><span class="sxs-lookup"><span data-stu-id="a24c3-124">West Europe</span></span>
- <span data-ttu-id="a24c3-125">Nord Europa</span><span class="sxs-lookup"><span data-stu-id="a24c3-125">North Europe</span></span>
- <span data-ttu-id="a24c3-126">Västra USA</span><span class="sxs-lookup"><span data-stu-id="a24c3-126">West US</span></span>
- <span data-ttu-id="a24c3-127">Östra USA</span><span class="sxs-lookup"><span data-stu-id="a24c3-127">East US</span></span>
- <span data-ttu-id="a24c3-128">Östra USA 2</span><span class="sxs-lookup"><span data-stu-id="a24c3-128">East US 2</span></span>
- <span data-ttu-id="a24c3-129">Östra Japan</span><span class="sxs-lookup"><span data-stu-id="a24c3-129">Japan East</span></span>
- <span data-ttu-id="a24c3-130">Västra Japan</span><span class="sxs-lookup"><span data-stu-id="a24c3-130">Japan West</span></span>
- <span data-ttu-id="a24c3-131">Brasilien, Syd</span><span class="sxs-lookup"><span data-stu-id="a24c3-131">Brazil South</span></span>
- <span data-ttu-id="a24c3-132">Sydostasien</span><span class="sxs-lookup"><span data-stu-id="a24c3-132">Southeast Asia</span></span>
- <span data-ttu-id="a24c3-133">Östasien</span><span class="sxs-lookup"><span data-stu-id="a24c3-133">East Asia</span></span>
- <span data-ttu-id="a24c3-134">Östra Australien</span><span class="sxs-lookup"><span data-stu-id="a24c3-134">Australia East</span></span>
- <span data-ttu-id="a24c3-135">Australien, sydöst</span><span class="sxs-lookup"><span data-stu-id="a24c3-135">Australia Southeast</span></span>

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

### <span data-ttu-id="a24c3-136">-MinimumTlsVersion</span><span class="sxs-lookup"><span data-stu-id="a24c3-136">-MinimumTlsVersion</span></span>
<span data-ttu-id="a24c3-137">Ange den TLS-version som krävs för att klienterna ska kunna ansluta till cacheminnet.</span><span class="sxs-lookup"><span data-stu-id="a24c3-137">Specify the TLS version required by clients to connect to cache.</span></span>

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

### <span data-ttu-id="a24c3-138">-Namn</span><span class="sxs-lookup"><span data-stu-id="a24c3-138">-Name</span></span>
<span data-ttu-id="a24c3-139">Anger namnet på den Redis-cache som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="a24c3-139">Specifies the name of the Redis Cache to create.</span></span>

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

### <span data-ttu-id="a24c3-140">-RedisConfiguration</span><span class="sxs-lookup"><span data-stu-id="a24c3-140">-RedisConfiguration</span></span>
<span data-ttu-id="a24c3-141">Anger konfigurations inställningar för Redis.</span><span class="sxs-lookup"><span data-stu-id="a24c3-141">Specifies Redis configuration settings.</span></span>
<span data-ttu-id="a24c3-142">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="a24c3-142">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="a24c3-143">RDB – säkerhets kopiering aktive rad.</span><span class="sxs-lookup"><span data-stu-id="a24c3-143">rdb-backup-enabled.</span></span>
<span data-ttu-id="a24c3-144">Anger att Redis data persistence är aktiverat.</span><span class="sxs-lookup"><span data-stu-id="a24c3-144">Specifies that Redis data persistence is enabled.</span></span>
<span data-ttu-id="a24c3-145">Endast Premium-nivå.</span><span class="sxs-lookup"><span data-stu-id="a24c3-145">Premium tier only.</span></span>
- <span data-ttu-id="a24c3-146">RDB-lagring-anslutning-sträng.</span><span class="sxs-lookup"><span data-stu-id="a24c3-146">rdb-storage-connection-string.</span></span>
<span data-ttu-id="a24c3-147">Anger anslutnings strängen till lagrings konto för Redis data.</span><span class="sxs-lookup"><span data-stu-id="a24c3-147">Specifies the connection string to the Storage account for Redis data persistence.</span></span>
<span data-ttu-id="a24c3-148">Endast Premium-nivå.</span><span class="sxs-lookup"><span data-stu-id="a24c3-148">Premium tier only.</span></span>
- <span data-ttu-id="a24c3-149">RDB-säkerhets kopiering-frekvens.</span><span class="sxs-lookup"><span data-stu-id="a24c3-149">rdb-backup-frequency.</span></span>
<span data-ttu-id="a24c3-150">Anger säkerhets kopierings frekvensen för Redis data.</span><span class="sxs-lookup"><span data-stu-id="a24c3-150">Specifies the backup frequency for Redis data persistence.</span></span>
<span data-ttu-id="a24c3-151">Endast Premium-nivå.</span><span class="sxs-lookup"><span data-stu-id="a24c3-151">Premium tier only.</span></span> 
- <span data-ttu-id="a24c3-152">maxmemory-reserverad.</span><span class="sxs-lookup"><span data-stu-id="a24c3-152">maxmemory-reserved.</span></span>
<span data-ttu-id="a24c3-153">Konfigurerar minnet reserverat för icke-cachelagrade processer.</span><span class="sxs-lookup"><span data-stu-id="a24c3-153">Configures the memory reserved for non-cache processes.</span></span>
<span data-ttu-id="a24c3-154">Standard-och Premium-nivåer.</span><span class="sxs-lookup"><span data-stu-id="a24c3-154">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="a24c3-155">maxmemory-policy.</span><span class="sxs-lookup"><span data-stu-id="a24c3-155">maxmemory-policy.</span></span>
<span data-ttu-id="a24c3-156">Konfigurerar borttagnings principen för cacheminnet.</span><span class="sxs-lookup"><span data-stu-id="a24c3-156">Configures the eviction policy for the cache.</span></span>
<span data-ttu-id="a24c3-157">Alla pris nivåer.</span><span class="sxs-lookup"><span data-stu-id="a24c3-157">All pricing tiers.</span></span> 
- <span data-ttu-id="a24c3-158">meddelande – inloggnings händelser.</span><span class="sxs-lookup"><span data-stu-id="a24c3-158">notify-keyspace-events.</span></span>
<span data-ttu-id="a24c3-159">Konfigurerar indikeringar för meddelanden.</span><span class="sxs-lookup"><span data-stu-id="a24c3-159">Configures keyspace notifications.</span></span>
<span data-ttu-id="a24c3-160">Standard-och Premium-nivåer.</span><span class="sxs-lookup"><span data-stu-id="a24c3-160">Standard and premium tiers.</span></span> 
- <span data-ttu-id="a24c3-161">hash-Max-ziplist-poster.</span><span class="sxs-lookup"><span data-stu-id="a24c3-161">hash-max-ziplist-entries.</span></span>
<span data-ttu-id="a24c3-162">Konfigurerar minnes optimering för små aggregerade data typer.</span><span class="sxs-lookup"><span data-stu-id="a24c3-162">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="a24c3-163">Standard-och Premium-nivåer.</span><span class="sxs-lookup"><span data-stu-id="a24c3-163">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="a24c3-164">hash-Max-ziplist-värde.</span><span class="sxs-lookup"><span data-stu-id="a24c3-164">hash-max-ziplist-value.</span></span>
<span data-ttu-id="a24c3-165">Konfigurerar minnes optimering för små aggregerade data typer.</span><span class="sxs-lookup"><span data-stu-id="a24c3-165">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="a24c3-166">Standard-och Premium-nivåer.</span><span class="sxs-lookup"><span data-stu-id="a24c3-166">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="a24c3-167">set-Max intset-poster.</span><span class="sxs-lookup"><span data-stu-id="a24c3-167">set-max-intset-entries.</span></span>
<span data-ttu-id="a24c3-168">Konfigurerar minnes optimering för små aggregerade data typer.</span><span class="sxs-lookup"><span data-stu-id="a24c3-168">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="a24c3-169">Standard-och Premium-nivåer.</span><span class="sxs-lookup"><span data-stu-id="a24c3-169">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="a24c3-170">zset-Max ziplist-poster.</span><span class="sxs-lookup"><span data-stu-id="a24c3-170">zset-max-ziplist-entries.</span></span>
<span data-ttu-id="a24c3-171">Konfigurerar minnes optimering för små aggregerade data typer.</span><span class="sxs-lookup"><span data-stu-id="a24c3-171">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="a24c3-172">Standard-och Premium-nivåer.</span><span class="sxs-lookup"><span data-stu-id="a24c3-172">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="a24c3-173">zset-Max-ziplist-värde.</span><span class="sxs-lookup"><span data-stu-id="a24c3-173">zset-max-ziplist-value.</span></span>
<span data-ttu-id="a24c3-174">Konfigurerar minnes optimering för små aggregerade data typer.</span><span class="sxs-lookup"><span data-stu-id="a24c3-174">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="a24c3-175">Standard-och Premium-nivåer.</span><span class="sxs-lookup"><span data-stu-id="a24c3-175">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="a24c3-176">samling.</span><span class="sxs-lookup"><span data-stu-id="a24c3-176">databases.</span></span>
<span data-ttu-id="a24c3-177">Konfigurerar antalet databaser.</span><span class="sxs-lookup"><span data-stu-id="a24c3-177">Configures the number of databases.</span></span>
<span data-ttu-id="a24c3-178">Det går bara att konfigurera den här egenskapen när cacheminnet skapas.</span><span class="sxs-lookup"><span data-stu-id="a24c3-178">This property can be configured only at cache creation.</span></span>
<span data-ttu-id="a24c3-179">Standard-och Premium-nivåer.</span><span class="sxs-lookup"><span data-stu-id="a24c3-179">Standard and Premium tiers.</span></span>
<span data-ttu-id="a24c3-180">Mer information finns i Hantera Azure Redis cache med Azure PowerShell http://go.microsoft.com/fwlink/?LinkId=800051 ( http://go.microsoft.com/fwlink/?LinkId=800051) .</span><span class="sxs-lookup"><span data-stu-id="a24c3-180">For more information, see Manage Azure Redis Cache with Azure PowerShellhttp://go.microsoft.com/fwlink/?LinkId=800051 (http://go.microsoft.com/fwlink/?LinkId=800051).</span></span>

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

### <span data-ttu-id="a24c3-181">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a24c3-181">-ResourceGroupName</span></span>
<span data-ttu-id="a24c3-182">Anger namnet på den resurs grupp där Redis cache ska skapas.</span><span class="sxs-lookup"><span data-stu-id="a24c3-182">Specifies the name of the resource group in which to create the Redis Cache.</span></span>

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

### <span data-ttu-id="a24c3-183">-ShardCount</span><span class="sxs-lookup"><span data-stu-id="a24c3-183">-ShardCount</span></span>
<span data-ttu-id="a24c3-184">Anger antalet Shards som ska skapas i ett Premium-kluster-cacheminne.</span><span class="sxs-lookup"><span data-stu-id="a24c3-184">Specifies the number of shards to create on a Premium cluster cache.</span></span>
<span data-ttu-id="a24c3-185">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="a24c3-185">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="a24c3-186">9.1</span><span class="sxs-lookup"><span data-stu-id="a24c3-186">1</span></span>
- <span data-ttu-id="a24c3-187">två</span><span class="sxs-lookup"><span data-stu-id="a24c3-187">2</span></span>
- <span data-ttu-id="a24c3-188">amp;3D</span><span class="sxs-lookup"><span data-stu-id="a24c3-188">3</span></span>
- <span data-ttu-id="a24c3-189">9.4</span><span class="sxs-lookup"><span data-stu-id="a24c3-189">4</span></span>
- <span data-ttu-id="a24c3-190">T5</span><span class="sxs-lookup"><span data-stu-id="a24c3-190">5</span></span>
- <span data-ttu-id="a24c3-191">18.6</span><span class="sxs-lookup"><span data-stu-id="a24c3-191">6</span></span>
- <span data-ttu-id="a24c3-192">borttagning</span><span class="sxs-lookup"><span data-stu-id="a24c3-192">7</span></span>
- <span data-ttu-id="a24c3-193">8.2</span><span class="sxs-lookup"><span data-stu-id="a24c3-193">8</span></span>
- <span data-ttu-id="a24c3-194">9</span><span class="sxs-lookup"><span data-stu-id="a24c3-194">9</span></span> 
- <span data-ttu-id="a24c3-195">10.3</span><span class="sxs-lookup"><span data-stu-id="a24c3-195">10</span></span>

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

### <span data-ttu-id="a24c3-196">-Storlek</span><span class="sxs-lookup"><span data-stu-id="a24c3-196">-Size</span></span>
<span data-ttu-id="a24c3-197">Anger storleken på Redis cache.</span><span class="sxs-lookup"><span data-stu-id="a24c3-197">Specifies the size of the Redis Cache.</span></span>
<span data-ttu-id="a24c3-198">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="a24c3-198">Valid values are:</span></span> 
- <span data-ttu-id="a24c3-199">P1</span><span class="sxs-lookup"><span data-stu-id="a24c3-199">P1</span></span>
- <span data-ttu-id="a24c3-200">P2</span><span class="sxs-lookup"><span data-stu-id="a24c3-200">P2</span></span>
- <span data-ttu-id="a24c3-201">P3</span><span class="sxs-lookup"><span data-stu-id="a24c3-201">P3</span></span>
- <span data-ttu-id="a24c3-202">P4</span><span class="sxs-lookup"><span data-stu-id="a24c3-202">P4</span></span>
- <span data-ttu-id="a24c3-203">P5</span><span class="sxs-lookup"><span data-stu-id="a24c3-203">P5</span></span>
- <span data-ttu-id="a24c3-204">C0</span><span class="sxs-lookup"><span data-stu-id="a24c3-204">C0</span></span>
- <span data-ttu-id="a24c3-205">C1</span><span class="sxs-lookup"><span data-stu-id="a24c3-205">C1</span></span>
- <span data-ttu-id="a24c3-206">C2</span><span class="sxs-lookup"><span data-stu-id="a24c3-206">C2</span></span>
- <span data-ttu-id="a24c3-207">C3</span><span class="sxs-lookup"><span data-stu-id="a24c3-207">C3</span></span>
- <span data-ttu-id="a24c3-208">C4</span><span class="sxs-lookup"><span data-stu-id="a24c3-208">C4</span></span>
- <span data-ttu-id="a24c3-209">C5</span><span class="sxs-lookup"><span data-stu-id="a24c3-209">C5</span></span>
- <span data-ttu-id="a24c3-210">C6</span><span class="sxs-lookup"><span data-stu-id="a24c3-210">C6</span></span>
- <span data-ttu-id="a24c3-211">250</span><span class="sxs-lookup"><span data-stu-id="a24c3-211">250MB</span></span>
- <span data-ttu-id="a24c3-212">MINNE</span><span class="sxs-lookup"><span data-stu-id="a24c3-212">1GB</span></span>
- <span data-ttu-id="a24c3-213">2,5 GB</span><span class="sxs-lookup"><span data-stu-id="a24c3-213">2.5GB</span></span>
- <span data-ttu-id="a24c3-214">6GB</span><span class="sxs-lookup"><span data-stu-id="a24c3-214">6GB</span></span>
- <span data-ttu-id="a24c3-215">13GB</span><span class="sxs-lookup"><span data-stu-id="a24c3-215">13GB</span></span>
- <span data-ttu-id="a24c3-216">26GB</span><span class="sxs-lookup"><span data-stu-id="a24c3-216">26GB</span></span>
- <span data-ttu-id="a24c3-217">53GB standardvärdet är 1 GB eller C1.</span><span class="sxs-lookup"><span data-stu-id="a24c3-217">53GB The default value is 1GB or C1.</span></span>

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

### <span data-ttu-id="a24c3-218">-SKU</span><span class="sxs-lookup"><span data-stu-id="a24c3-218">-Sku</span></span>
<span data-ttu-id="a24c3-219">Anger SKU för det Redis-cacheminne som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="a24c3-219">Specifies the SKU of the Redis Cache to create.</span></span>
<span data-ttu-id="a24c3-220">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="a24c3-220">Valid values are:</span></span> 
- <span data-ttu-id="a24c3-221">Basisk</span><span class="sxs-lookup"><span data-stu-id="a24c3-221">Basic</span></span>
- <span data-ttu-id="a24c3-222">Standar</span><span class="sxs-lookup"><span data-stu-id="a24c3-222">Standard</span></span>
- <span data-ttu-id="a24c3-223">Premium är standardvärdet standard.</span><span class="sxs-lookup"><span data-stu-id="a24c3-223">Premium The default value is Standard.</span></span>

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

### <span data-ttu-id="a24c3-224">-StaticIP</span><span class="sxs-lookup"><span data-stu-id="a24c3-224">-StaticIP</span></span>
<span data-ttu-id="a24c3-225">Anger en unik IP-adress i Redis-cachen.</span><span class="sxs-lookup"><span data-stu-id="a24c3-225">Specifies a unique IP address in the subnet for the Redis Cache.</span></span>
<span data-ttu-id="a24c3-226">Om du inte anger ett värde för den här parametern väljer denna cmdlet en IP-adress från under nätet.</span><span class="sxs-lookup"><span data-stu-id="a24c3-226">If you do not specify a value for this parameter, this cmdlet chooses an IP address from the subnet.</span></span>

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

### <span data-ttu-id="a24c3-227">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="a24c3-227">-SubnetId</span></span>
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

### <span data-ttu-id="a24c3-228">-Tagg</span><span class="sxs-lookup"><span data-stu-id="a24c3-228">-Tag</span></span>
<span data-ttu-id="a24c3-229">En hash-tabell som representerar taggar.</span><span class="sxs-lookup"><span data-stu-id="a24c3-229">A hash table which represents tags.</span></span>

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

### <span data-ttu-id="a24c3-230">-TenantSettings</span><span class="sxs-lookup"><span data-stu-id="a24c3-230">-TenantSettings</span></span>
<span data-ttu-id="a24c3-231">Denna parameter är inaktuell.</span><span class="sxs-lookup"><span data-stu-id="a24c3-231">This parameter has been deprecated.</span></span>

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

### <span data-ttu-id="a24c3-232">-Zone</span><span class="sxs-lookup"><span data-stu-id="a24c3-232">-Zone</span></span>
<span data-ttu-id="a24c3-233">Lista över zoner.</span><span class="sxs-lookup"><span data-stu-id="a24c3-233">List of zones.</span></span>

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

### <span data-ttu-id="a24c3-234">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a24c3-234">-Confirm</span></span>
<span data-ttu-id="a24c3-235">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a24c3-235">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a24c3-236">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a24c3-236">-WhatIf</span></span>
<span data-ttu-id="a24c3-237">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a24c3-237">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a24c3-238">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a24c3-238">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a24c3-239">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a24c3-239">CommonParameters</span></span>
<span data-ttu-id="a24c3-240">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a24c3-240">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a24c3-241">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a24c3-241">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a24c3-242">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a24c3-242">INPUTS</span></span>

### <span data-ttu-id="a24c3-243">System. String</span><span class="sxs-lookup"><span data-stu-id="a24c3-243">System.String</span></span>

### <span data-ttu-id="a24c3-244">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="a24c3-244">System.Collections.Hashtable</span></span>

### <span data-ttu-id="a24c3-245">System. Nullable ' 1 [[system. Boolean, system. privat. CoreLib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="a24c3-245">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="a24c3-246">System. Nullable ' 1 [[system. Int32, system. privat. CoreLib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="a24c3-246">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="a24c3-247">System. string []</span><span class="sxs-lookup"><span data-stu-id="a24c3-247">System.String[]</span></span>

## <span data-ttu-id="a24c3-248">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a24c3-248">OUTPUTS</span></span>

### <span data-ttu-id="a24c3-249">Microsoft. Azure. commands. RedisCache. Models. RedisCacheAttributesWithAccessKeys</span><span class="sxs-lookup"><span data-stu-id="a24c3-249">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributesWithAccessKeys</span></span>

## <span data-ttu-id="a24c3-250">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a24c3-250">NOTES</span></span>

## <span data-ttu-id="a24c3-251">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a24c3-251">RELATED LINKS</span></span>

[<span data-ttu-id="a24c3-252">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="a24c3-252">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="a24c3-253">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="a24c3-253">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="a24c3-254">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="a24c3-254">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)


