---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: 81179AFE-6524-4F59-8BC2-3E152F51D1DD
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCache.md
ms.openlocfilehash: 493a8e7a4e356284b2ae14241715a7631d99839c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755650"
---
# <span data-ttu-id="b39c8-101">New-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="b39c8-101">New-AzureRmRedisCache</span></span>

## <span data-ttu-id="b39c8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b39c8-102">SYNOPSIS</span></span>
<span data-ttu-id="b39c8-103">Skapar en Redis cache.</span><span class="sxs-lookup"><span data-stu-id="b39c8-103">Creates a Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b39c8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b39c8-104">SYNTAX</span></span>

```
New-AzureRmRedisCache -ResourceGroupName <String> -Name <String> -Location <String> [-RedisVersion <String>]
 [-Size <String>] [-Sku <String>] [-MaxMemoryPolicy <String>] [-RedisConfiguration <Hashtable>]
 [-EnableNonSslPort <Boolean>] [-TenantSettings <Hashtable>] [-ShardCount <Int32>] [-VirtualNetwork <String>]
 [-Subnet <String>] [-SubnetId <String>] [-StaticIP <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b39c8-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b39c8-105">DESCRIPTION</span></span>
<span data-ttu-id="b39c8-106">Cmdleten **New-AzureRmRedisCache** skapar ett Azure Redis-cacheminne.</span><span class="sxs-lookup"><span data-stu-id="b39c8-106">The **New-AzureRmRedisCache** cmdlet creates an Azure Redis Cache.</span></span>

## <span data-ttu-id="b39c8-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b39c8-107">EXAMPLES</span></span>

### <span data-ttu-id="b39c8-108">Exempel 1: skapa en Redis-cache</span><span class="sxs-lookup"><span data-stu-id="b39c8-108">Example 1: Create a Redis Cache</span></span>
```
PS C:\>New-AzureRmRedisCache -ResourceGroupName "MyGroup" -Name "MyCache" -Location "North Central US"


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
```

<span data-ttu-id="b39c8-109">Det här kommandot skapar en Redis cache.</span><span class="sxs-lookup"><span data-stu-id="b39c8-109">This command creates a Redis Cache.</span></span>

### <span data-ttu-id="b39c8-110">Exempel 2: skapa en standard-SKU Redis cache</span><span class="sxs-lookup"><span data-stu-id="b39c8-110">Example 2: Create a Standard SKU Redis Cache</span></span>
```
PS C:\>New-AzureRmRedisCache -ResourceGroupName "MyGroup" -Name "MyCache" -Location "North Central US" -Size 250MB -Sku "Standard" -RedisConfiguration @{"maxmemory-policy" = "allkeys-random"} -Force


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
```

<span data-ttu-id="b39c8-111">Det här kommandot skapar en Redis cache eller uppdaterar Redis-cachen om den redan finns.</span><span class="sxs-lookup"><span data-stu-id="b39c8-111">This command creates a Redis Cache or updates the Redis Cache if it already exists.</span></span>

## <span data-ttu-id="b39c8-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b39c8-112">PARAMETERS</span></span>

### <span data-ttu-id="b39c8-113">-EnableNonSslPort</span><span class="sxs-lookup"><span data-stu-id="b39c8-113">-EnableNonSslPort</span></span>
<span data-ttu-id="b39c8-114">Anger om icke-SSL-porten är aktive rad.</span><span class="sxs-lookup"><span data-stu-id="b39c8-114">Indicates whether the non-SSL port is enabled.</span></span>
<span data-ttu-id="b39c8-115">Standardvärdet är $False (icke-SSL-porten är inaktive rad).</span><span class="sxs-lookup"><span data-stu-id="b39c8-115">The default value is $False (the non-SSL port is disabled).</span></span>

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

### <span data-ttu-id="b39c8-116">-Plats</span><span class="sxs-lookup"><span data-stu-id="b39c8-116">-Location</span></span>
<span data-ttu-id="b39c8-117">Anger den plats där du vill skapa en Redis cache.</span><span class="sxs-lookup"><span data-stu-id="b39c8-117">Specifies the location in which to create a Redis Cache.</span></span>
<span data-ttu-id="b39c8-118">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="b39c8-118">Valid values are:</span></span> 

- <span data-ttu-id="b39c8-119">Norra Central USA</span><span class="sxs-lookup"><span data-stu-id="b39c8-119">North Central US</span></span>
- <span data-ttu-id="b39c8-120">Södra centrala USA</span><span class="sxs-lookup"><span data-stu-id="b39c8-120">South Central US</span></span>
- <span data-ttu-id="b39c8-121">Central</span><span class="sxs-lookup"><span data-stu-id="b39c8-121">Central US</span></span>
- <span data-ttu-id="b39c8-122">Västeuropa</span><span class="sxs-lookup"><span data-stu-id="b39c8-122">West Europe</span></span>
- <span data-ttu-id="b39c8-123">Nord Europa</span><span class="sxs-lookup"><span data-stu-id="b39c8-123">North Europe</span></span>
- <span data-ttu-id="b39c8-124">Västra USA</span><span class="sxs-lookup"><span data-stu-id="b39c8-124">West US</span></span>
- <span data-ttu-id="b39c8-125">Östra USA</span><span class="sxs-lookup"><span data-stu-id="b39c8-125">East US</span></span>
- <span data-ttu-id="b39c8-126">Östra USA 2</span><span class="sxs-lookup"><span data-stu-id="b39c8-126">East US 2</span></span>
- <span data-ttu-id="b39c8-127">Östra Japan</span><span class="sxs-lookup"><span data-stu-id="b39c8-127">Japan East</span></span>
- <span data-ttu-id="b39c8-128">Västra Japan</span><span class="sxs-lookup"><span data-stu-id="b39c8-128">Japan West</span></span>
- <span data-ttu-id="b39c8-129">Brasilien, Syd</span><span class="sxs-lookup"><span data-stu-id="b39c8-129">Brazil South</span></span>
- <span data-ttu-id="b39c8-130">Sydostasien</span><span class="sxs-lookup"><span data-stu-id="b39c8-130">Southeast Asia</span></span>
- <span data-ttu-id="b39c8-131">Östasien</span><span class="sxs-lookup"><span data-stu-id="b39c8-131">East Asia</span></span>
- <span data-ttu-id="b39c8-132">Östra Australien</span><span class="sxs-lookup"><span data-stu-id="b39c8-132">Australia East</span></span>
- <span data-ttu-id="b39c8-133">Australien, sydöst</span><span class="sxs-lookup"><span data-stu-id="b39c8-133">Australia Southeast</span></span>

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

### <span data-ttu-id="b39c8-134">-MaxMemoryPolicy</span><span class="sxs-lookup"><span data-stu-id="b39c8-134">-MaxMemoryPolicy</span></span>
<span data-ttu-id="b39c8-135">Denna parameter är inaktuell.</span><span class="sxs-lookup"><span data-stu-id="b39c8-135">This parameter has been deprecated.</span></span>
<span data-ttu-id="b39c8-136">Använd parametern *RedisConfiguration* för att ange maxmemory policy.</span><span class="sxs-lookup"><span data-stu-id="b39c8-136">Use the *RedisConfiguration* parameter to set maxmemory-policy.</span></span>
<span data-ttu-id="b39c8-137">Till exempel:</span><span class="sxs-lookup"><span data-stu-id="b39c8-137">For example:</span></span> 

`-RedisConfiguration @{"maxmemory-policy" = "allkeys-lru"}`

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

### <span data-ttu-id="b39c8-138">-Namn</span><span class="sxs-lookup"><span data-stu-id="b39c8-138">-Name</span></span>
<span data-ttu-id="b39c8-139">Anger namnet på den Redis-cache som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="b39c8-139">Specifies the name of the Redis Cache to create.</span></span>

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

### <span data-ttu-id="b39c8-140">-RedisConfiguration</span><span class="sxs-lookup"><span data-stu-id="b39c8-140">-RedisConfiguration</span></span>
<span data-ttu-id="b39c8-141">Anger konfigurations inställningar för Redis.</span><span class="sxs-lookup"><span data-stu-id="b39c8-141">Specifies Redis configuration settings.</span></span>
<span data-ttu-id="b39c8-142">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="b39c8-142">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b39c8-143">RDB – säkerhets kopiering aktive rad.</span><span class="sxs-lookup"><span data-stu-id="b39c8-143">rdb-backup-enabled.</span></span>
<span data-ttu-id="b39c8-144">Anger att Redis data persistence är aktiverat.</span><span class="sxs-lookup"><span data-stu-id="b39c8-144">Specifies that Redis data persistence is enabled.</span></span>
<span data-ttu-id="b39c8-145">Endast Premium-nivå.</span><span class="sxs-lookup"><span data-stu-id="b39c8-145">Premium tier only.</span></span>
- <span data-ttu-id="b39c8-146">RDB-lagring-anslutning-sträng.</span><span class="sxs-lookup"><span data-stu-id="b39c8-146">rdb-storage-connection-string.</span></span>
<span data-ttu-id="b39c8-147">Anger anslutnings strängen till lagrings konto för Redis data.</span><span class="sxs-lookup"><span data-stu-id="b39c8-147">Specifies the connection string to the Storage account for Redis data persistence.</span></span>
<span data-ttu-id="b39c8-148">Endast Premium-nivå.</span><span class="sxs-lookup"><span data-stu-id="b39c8-148">Premium tier only.</span></span>
- <span data-ttu-id="b39c8-149">RDB-säkerhets kopiering-frekvens.</span><span class="sxs-lookup"><span data-stu-id="b39c8-149">rdb-backup-frequency.</span></span>
<span data-ttu-id="b39c8-150">Anger säkerhets kopierings frekvensen för Redis data.</span><span class="sxs-lookup"><span data-stu-id="b39c8-150">Specifies the backup frequency for Redis data persistence.</span></span>
<span data-ttu-id="b39c8-151">Endast Premium-nivå.</span><span class="sxs-lookup"><span data-stu-id="b39c8-151">Premium tier only.</span></span> 
- <span data-ttu-id="b39c8-152">maxmemory-reserverad.</span><span class="sxs-lookup"><span data-stu-id="b39c8-152">maxmemory-reserved.</span></span>
<span data-ttu-id="b39c8-153">Konfigurerar minnet reserverat för icke-cachelagrade processer.</span><span class="sxs-lookup"><span data-stu-id="b39c8-153">Configures the memory reserved for non-cache processes.</span></span>
<span data-ttu-id="b39c8-154">Standard-och Premium-nivåer.</span><span class="sxs-lookup"><span data-stu-id="b39c8-154">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="b39c8-155">maxmemory-policy.</span><span class="sxs-lookup"><span data-stu-id="b39c8-155">maxmemory-policy.</span></span>
<span data-ttu-id="b39c8-156">Konfigurerar borttagnings principen för cacheminnet.</span><span class="sxs-lookup"><span data-stu-id="b39c8-156">Configures the eviction policy for the cache.</span></span>
<span data-ttu-id="b39c8-157">Alla pris nivåer.</span><span class="sxs-lookup"><span data-stu-id="b39c8-157">All pricing tiers.</span></span> 
- <span data-ttu-id="b39c8-158">meddelande – inloggnings händelser.</span><span class="sxs-lookup"><span data-stu-id="b39c8-158">notify-keyspace-events.</span></span>
<span data-ttu-id="b39c8-159">Konfigurerar indikeringar för meddelanden.</span><span class="sxs-lookup"><span data-stu-id="b39c8-159">Configures keyspace notifications.</span></span>
<span data-ttu-id="b39c8-160">Standard-och Premium-nivåer.</span><span class="sxs-lookup"><span data-stu-id="b39c8-160">Standard and premium tiers.</span></span> 
- <span data-ttu-id="b39c8-161">hash-Max-ziplist-poster.</span><span class="sxs-lookup"><span data-stu-id="b39c8-161">hash-max-ziplist-entries.</span></span>
<span data-ttu-id="b39c8-162">Konfigurerar minnes optimering för små aggregerade data typer.</span><span class="sxs-lookup"><span data-stu-id="b39c8-162">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="b39c8-163">Standard-och Premium-nivåer.</span><span class="sxs-lookup"><span data-stu-id="b39c8-163">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="b39c8-164">hash-Max-ziplist-värde.</span><span class="sxs-lookup"><span data-stu-id="b39c8-164">hash-max-ziplist-value.</span></span>
<span data-ttu-id="b39c8-165">Konfigurerar minnes optimering för små aggregerade data typer.</span><span class="sxs-lookup"><span data-stu-id="b39c8-165">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="b39c8-166">Standard-och Premium-nivåer.</span><span class="sxs-lookup"><span data-stu-id="b39c8-166">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="b39c8-167">set-Max intset-poster.</span><span class="sxs-lookup"><span data-stu-id="b39c8-167">set-max-intset-entries.</span></span>
<span data-ttu-id="b39c8-168">Konfigurerar minnes optimering för små aggregerade data typer.</span><span class="sxs-lookup"><span data-stu-id="b39c8-168">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="b39c8-169">Standard-och Premium-nivåer.</span><span class="sxs-lookup"><span data-stu-id="b39c8-169">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="b39c8-170">zset-Max ziplist-poster.</span><span class="sxs-lookup"><span data-stu-id="b39c8-170">zset-max-ziplist-entries.</span></span>
<span data-ttu-id="b39c8-171">Konfigurerar minnes optimering för små aggregerade data typer.</span><span class="sxs-lookup"><span data-stu-id="b39c8-171">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="b39c8-172">Standard-och Premium-nivåer.</span><span class="sxs-lookup"><span data-stu-id="b39c8-172">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="b39c8-173">zset-Max-ziplist-värde.</span><span class="sxs-lookup"><span data-stu-id="b39c8-173">zset-max-ziplist-value.</span></span>
<span data-ttu-id="b39c8-174">Konfigurerar minnes optimering för små aggregerade data typer.</span><span class="sxs-lookup"><span data-stu-id="b39c8-174">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="b39c8-175">Standard-och Premium-nivåer.</span><span class="sxs-lookup"><span data-stu-id="b39c8-175">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="b39c8-176">samling.</span><span class="sxs-lookup"><span data-stu-id="b39c8-176">databases.</span></span>
<span data-ttu-id="b39c8-177">Konfigurerar antalet databaser.</span><span class="sxs-lookup"><span data-stu-id="b39c8-177">Configures the number of databases.</span></span>
<span data-ttu-id="b39c8-178">Det går bara att konfigurera den här egenskapen när cacheminnet skapas.</span><span class="sxs-lookup"><span data-stu-id="b39c8-178">This property can be configured only at cache creation.</span></span>
<span data-ttu-id="b39c8-179">Standard-och Premium-nivåer.</span><span class="sxs-lookup"><span data-stu-id="b39c8-179">Standard and Premium tiers.</span></span>

<span data-ttu-id="b39c8-180">Mer information finns i Hantera Azure Redis cache med Azure PowerShell https://go.microsoft.com/fwlink/?LinkId=800051 ( https://go.microsoft.com/fwlink/?LinkId=800051) .</span><span class="sxs-lookup"><span data-stu-id="b39c8-180">For more information, see Manage Azure Redis Cache with Azure PowerShellhttps://go.microsoft.com/fwlink/?LinkId=800051 (https://go.microsoft.com/fwlink/?LinkId=800051).</span></span>

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

### <span data-ttu-id="b39c8-181">-RedisVersion</span><span class="sxs-lookup"><span data-stu-id="b39c8-181">-RedisVersion</span></span>
<span data-ttu-id="b39c8-182">Denna parameter är föråldrad och kommer att tas bort från framtida versioner.</span><span class="sxs-lookup"><span data-stu-id="b39c8-182">This parameter is deprecated and will be removed from future releases.</span></span>

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

### <span data-ttu-id="b39c8-183">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b39c8-183">-ResourceGroupName</span></span>
<span data-ttu-id="b39c8-184">Anger namnet på den resurs grupp där Redis cache ska skapas.</span><span class="sxs-lookup"><span data-stu-id="b39c8-184">Specifies the name of the resource group in which to create the Redis Cache.</span></span>

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

### <span data-ttu-id="b39c8-185">-ShardCount</span><span class="sxs-lookup"><span data-stu-id="b39c8-185">-ShardCount</span></span>
<span data-ttu-id="b39c8-186">Anger antalet Shards som ska skapas i ett Premium-kluster-cacheminne.</span><span class="sxs-lookup"><span data-stu-id="b39c8-186">Specifies the number of shards to create on a Premium cluster cache.</span></span>
<span data-ttu-id="b39c8-187">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="b39c8-187">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b39c8-188">9.1</span><span class="sxs-lookup"><span data-stu-id="b39c8-188">1</span></span>
- <span data-ttu-id="b39c8-189">två</span><span class="sxs-lookup"><span data-stu-id="b39c8-189">2</span></span>
- <span data-ttu-id="b39c8-190">amp;3D</span><span class="sxs-lookup"><span data-stu-id="b39c8-190">3</span></span>
- <span data-ttu-id="b39c8-191">9.4</span><span class="sxs-lookup"><span data-stu-id="b39c8-191">4</span></span>
- <span data-ttu-id="b39c8-192">T5</span><span class="sxs-lookup"><span data-stu-id="b39c8-192">5</span></span>
- <span data-ttu-id="b39c8-193">18.6</span><span class="sxs-lookup"><span data-stu-id="b39c8-193">6</span></span>
- <span data-ttu-id="b39c8-194">borttagning</span><span class="sxs-lookup"><span data-stu-id="b39c8-194">7</span></span>
- <span data-ttu-id="b39c8-195">8.2</span><span class="sxs-lookup"><span data-stu-id="b39c8-195">8</span></span>
- <span data-ttu-id="b39c8-196">9</span><span class="sxs-lookup"><span data-stu-id="b39c8-196">9</span></span> 
- <span data-ttu-id="b39c8-197">10.3</span><span class="sxs-lookup"><span data-stu-id="b39c8-197">10</span></span>

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

### <span data-ttu-id="b39c8-198">-Storlek</span><span class="sxs-lookup"><span data-stu-id="b39c8-198">-Size</span></span>
<span data-ttu-id="b39c8-199">Anger storleken på Redis cache.</span><span class="sxs-lookup"><span data-stu-id="b39c8-199">Specifies the size of the Redis Cache.</span></span>
<span data-ttu-id="b39c8-200">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="b39c8-200">Valid values are:</span></span> 

- <span data-ttu-id="b39c8-201">P1</span><span class="sxs-lookup"><span data-stu-id="b39c8-201">P1</span></span>
- <span data-ttu-id="b39c8-202">P2</span><span class="sxs-lookup"><span data-stu-id="b39c8-202">P2</span></span>
- <span data-ttu-id="b39c8-203">P3</span><span class="sxs-lookup"><span data-stu-id="b39c8-203">P3</span></span>
- <span data-ttu-id="b39c8-204">P4</span><span class="sxs-lookup"><span data-stu-id="b39c8-204">P4</span></span>
- <span data-ttu-id="b39c8-205">C0</span><span class="sxs-lookup"><span data-stu-id="b39c8-205">C0</span></span>
- <span data-ttu-id="b39c8-206">C1</span><span class="sxs-lookup"><span data-stu-id="b39c8-206">C1</span></span>
- <span data-ttu-id="b39c8-207">C2</span><span class="sxs-lookup"><span data-stu-id="b39c8-207">C2</span></span>
- <span data-ttu-id="b39c8-208">C3</span><span class="sxs-lookup"><span data-stu-id="b39c8-208">C3</span></span>
- <span data-ttu-id="b39c8-209">C4</span><span class="sxs-lookup"><span data-stu-id="b39c8-209">C4</span></span>
- <span data-ttu-id="b39c8-210">C5</span><span class="sxs-lookup"><span data-stu-id="b39c8-210">C5</span></span>
- <span data-ttu-id="b39c8-211">C6</span><span class="sxs-lookup"><span data-stu-id="b39c8-211">C6</span></span>
- <span data-ttu-id="b39c8-212">250</span><span class="sxs-lookup"><span data-stu-id="b39c8-212">250MB</span></span>
- <span data-ttu-id="b39c8-213">MINNE</span><span class="sxs-lookup"><span data-stu-id="b39c8-213">1GB</span></span>
- <span data-ttu-id="b39c8-214">2,5 GB</span><span class="sxs-lookup"><span data-stu-id="b39c8-214">2.5GB</span></span>
- <span data-ttu-id="b39c8-215">6GB</span><span class="sxs-lookup"><span data-stu-id="b39c8-215">6GB</span></span>
- <span data-ttu-id="b39c8-216">13GB</span><span class="sxs-lookup"><span data-stu-id="b39c8-216">13GB</span></span>
- <span data-ttu-id="b39c8-217">26GB</span><span class="sxs-lookup"><span data-stu-id="b39c8-217">26GB</span></span>
- <span data-ttu-id="b39c8-218">53GB</span><span class="sxs-lookup"><span data-stu-id="b39c8-218">53GB</span></span>

<span data-ttu-id="b39c8-219">Standardvärdet är 1 GB eller C1.</span><span class="sxs-lookup"><span data-stu-id="b39c8-219">The default value is 1GB or C1.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: P1, P2, P3, P4, C0, C1, C2, C3, C4, C5, C6, 250MB, 1GB, 2.5GB, 6GB, 13GB, 26GB, 53GB

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b39c8-220">-SKU</span><span class="sxs-lookup"><span data-stu-id="b39c8-220">-Sku</span></span>
<span data-ttu-id="b39c8-221">Anger SKU för det Redis-cacheminne som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="b39c8-221">Specifies the SKU of the Redis Cache to create.</span></span>
<span data-ttu-id="b39c8-222">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="b39c8-222">Valid values are:</span></span> 

- <span data-ttu-id="b39c8-223">Basisk</span><span class="sxs-lookup"><span data-stu-id="b39c8-223">Basic</span></span>
- <span data-ttu-id="b39c8-224">Standar</span><span class="sxs-lookup"><span data-stu-id="b39c8-224">Standard</span></span>
- <span data-ttu-id="b39c8-225">Beta</span><span class="sxs-lookup"><span data-stu-id="b39c8-225">Premium</span></span>

<span data-ttu-id="b39c8-226">Standardvärdet är standard.</span><span class="sxs-lookup"><span data-stu-id="b39c8-226">The default value is Standard.</span></span>

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

### <span data-ttu-id="b39c8-227">-StaticIP</span><span class="sxs-lookup"><span data-stu-id="b39c8-227">-StaticIP</span></span>
<span data-ttu-id="b39c8-228">Anger en unik IP-adress i Redis-cachen.</span><span class="sxs-lookup"><span data-stu-id="b39c8-228">Specifies a unique IP address in the subnet for the Redis Cache.</span></span>

<span data-ttu-id="b39c8-229">Om du inte anger ett värde för den här parametern väljer denna cmdlet en IP-adress från under nätet.</span><span class="sxs-lookup"><span data-stu-id="b39c8-229">If you do not specify a value for this parameter, this cmdlet chooses an IP address from the subnet.</span></span>

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

### <span data-ttu-id="b39c8-230">-Undernät</span><span class="sxs-lookup"><span data-stu-id="b39c8-230">-Subnet</span></span>
<span data-ttu-id="b39c8-231">Anger namnet på det undernät där Redis-cachen ska distribueras.</span><span class="sxs-lookup"><span data-stu-id="b39c8-231">Specifies the name of the subnet in which to deploy the Redis Cache.</span></span>

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

### <span data-ttu-id="b39c8-232">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="b39c8-232">-SubnetId</span></span>
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

### <span data-ttu-id="b39c8-233">-TenantSettings</span><span class="sxs-lookup"><span data-stu-id="b39c8-233">-TenantSettings</span></span>
<span data-ttu-id="b39c8-234">Denna parameter är inaktuell.</span><span class="sxs-lookup"><span data-stu-id="b39c8-234">This parameter has been deprecated.</span></span>

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

### <span data-ttu-id="b39c8-235">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="b39c8-235">-VirtualNetwork</span></span>
<span data-ttu-id="b39c8-236">Anger resurs-ID för det virtuella nätverk där Redis-cachen ska distribueras.</span><span class="sxs-lookup"><span data-stu-id="b39c8-236">Specifies the resource ID of the virtual network in which to deploy the Redis Cache.</span></span>

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

### <span data-ttu-id="b39c8-237">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b39c8-237">-DefaultProfile</span></span>
<span data-ttu-id="b39c8-238">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b39c8-238">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b39c8-239">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b39c8-239">CommonParameters</span></span>
<span data-ttu-id="b39c8-240">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b39c8-240">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b39c8-241">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b39c8-241">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b39c8-242">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b39c8-242">INPUTS</span></span>

### <span data-ttu-id="b39c8-243">Ingen</span><span class="sxs-lookup"><span data-stu-id="b39c8-243">None</span></span>
<span data-ttu-id="b39c8-244">Du kan pipes in i denna cmdlet efter namn men inte efter värde.</span><span class="sxs-lookup"><span data-stu-id="b39c8-244">You can pipe input to this cmdlet by name, but not by value.</span></span>

## <span data-ttu-id="b39c8-245">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b39c8-245">OUTPUTS</span></span>

### <span data-ttu-id="b39c8-246">Microsoft. Azure. commands. RedisCache. Models. RedisCacheAttributesWithAccessKeys</span><span class="sxs-lookup"><span data-stu-id="b39c8-246">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributesWithAccessKeys</span></span>
<span data-ttu-id="b39c8-247">Denna cmdlet returnerar alla attribut i en Redis-cache inklusive primära och sekundära åtkomst nycklar.</span><span class="sxs-lookup"><span data-stu-id="b39c8-247">This cmdlet returns all attributes of a Redis Cache including primary and secondary access keys.</span></span>

## <span data-ttu-id="b39c8-248">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b39c8-248">NOTES</span></span>

## <span data-ttu-id="b39c8-249">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b39c8-249">RELATED LINKS</span></span>

[<span data-ttu-id="b39c8-250">Get-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="b39c8-250">Get-AzureRmRedisCache</span></span>](./Get-AzureRmRedisCache.md)

[<span data-ttu-id="b39c8-251">Remove-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="b39c8-251">Remove-AzureRmRedisCache</span></span>](./Remove-AzureRmRedisCache.md)

[<span data-ttu-id="b39c8-252">Set-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="b39c8-252">Set-AzureRmRedisCache</span></span>](./Set-AzureRmRedisCache.md)


