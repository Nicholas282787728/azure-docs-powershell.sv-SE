---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: 6234F211-6ED4-443F-9B83-DEB9AC51B763
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/set-azurermrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Set-AzureRmRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Set-AzureRmRedisCache.md
ms.openlocfilehash: 951198c93918c08f69f28dc6db3c5fe605e6d3bc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576441"
---
# <span data-ttu-id="2810a-101">Set-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="2810a-101">Set-AzureRmRedisCache</span></span>

## <span data-ttu-id="2810a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2810a-102">SYNOPSIS</span></span>
<span data-ttu-id="2810a-103">Ändrar en Redis-cache.</span><span class="sxs-lookup"><span data-stu-id="2810a-103">Modifies a Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2810a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2810a-104">SYNTAX</span></span>

```
Set-AzureRmRedisCache [-ResourceGroupName <String>] -Name <String> [-Size <String>] [-Sku <String>]
 [-MaxMemoryPolicy <String>] [-RedisConfiguration <Hashtable>] [-EnableNonSslPort <Boolean>]
 [-TenantSettings <Hashtable>] [-ShardCount <Int32>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2810a-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2810a-105">DESCRIPTION</span></span>
<span data-ttu-id="2810a-106">Cmdleten **set-AzureRmRedisCache** ändrar ett Azure Redis-cacheminne.</span><span class="sxs-lookup"><span data-stu-id="2810a-106">The **Set-AzureRmRedisCache** cmdlet modifies an Azure Redis Cache.</span></span>

## <span data-ttu-id="2810a-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2810a-107">EXAMPLES</span></span>

### <span data-ttu-id="2810a-108">Exempel 1: ändra en Redis-cache</span><span class="sxs-lookup"><span data-stu-id="2810a-108">Example 1: Modify a Redis Cache</span></span>
```
PS C:\>Set-AzureRmRedisCache -ResourceGroupName "MyGroup" -Name "MyCache" -RedisConfiguration @{"maxmemory-policy" = "allkeys-random"}

          PrimaryKey         : pJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
          SecondaryKey       : sJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
          ResourceGroupName  : mygroup
          Id                 : /subscriptions/a559b6fd-3a84-40bb-a450-b0db5ed37dfe/resourceGroups/mygroup/providers/Microsoft.Cache/Redis/myCache
          Location           : North Central US
          Name               : MyCache
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

<span data-ttu-id="2810a-109">Det här kommandot uppdaterar maxmemory-principen för Redis cachelagrade namn-cachen.</span><span class="sxs-lookup"><span data-stu-id="2810a-109">This command updates the maxmemory-policy for the Redis Cache named MyCache.</span></span>

## <span data-ttu-id="2810a-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2810a-110">PARAMETERS</span></span>

### <span data-ttu-id="2810a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2810a-111">-DefaultProfile</span></span>
<span data-ttu-id="2810a-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2810a-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2810a-113">-EnableNonSslPort</span><span class="sxs-lookup"><span data-stu-id="2810a-113">-EnableNonSslPort</span></span>
<span data-ttu-id="2810a-114">Anger om icke-SSL-porten är aktive rad.</span><span class="sxs-lookup"><span data-stu-id="2810a-114">Indicates whether the non-SSL port is enabled.</span></span>
<span data-ttu-id="2810a-115">Standardvärdet är $False (icke-SSL-porten är inaktive rad).</span><span class="sxs-lookup"><span data-stu-id="2810a-115">The default value is $False (the non-SSL port is disabled).</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2810a-116">-MaxMemoryPolicy</span><span class="sxs-lookup"><span data-stu-id="2810a-116">-MaxMemoryPolicy</span></span>
<span data-ttu-id="2810a-117">Denna parameter är inaktuell.</span><span class="sxs-lookup"><span data-stu-id="2810a-117">This parameter has been deprecated.</span></span>
<span data-ttu-id="2810a-118">Använd parametern *RedisConfiguration* för att ange maxmemory policy.</span><span class="sxs-lookup"><span data-stu-id="2810a-118">Use the *RedisConfiguration* parameter to set maxmemory-policy.</span></span>
<span data-ttu-id="2810a-119">Till exempel:</span><span class="sxs-lookup"><span data-stu-id="2810a-119">For example:</span></span> 

`-RedisConfiguration @{"maxmemory-policy" = "allkeys-lru"}`

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2810a-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="2810a-120">-Name</span></span>
<span data-ttu-id="2810a-121">Anger namnet på den Redis-cache som ska uppdateras.</span><span class="sxs-lookup"><span data-stu-id="2810a-121">Specifies the name of the Redis Cache to update.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2810a-122">-RedisConfiguration</span><span class="sxs-lookup"><span data-stu-id="2810a-122">-RedisConfiguration</span></span>
<span data-ttu-id="2810a-123">Anger konfigurations inställningar för Redis.</span><span class="sxs-lookup"><span data-stu-id="2810a-123">Specifies Redis configuration settings.</span></span>
<span data-ttu-id="2810a-124">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="2810a-124">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="2810a-125">RDB – säkerhets kopiering aktive rad.</span><span class="sxs-lookup"><span data-stu-id="2810a-125">rdb-backup-enabled.</span></span>
<span data-ttu-id="2810a-126">Anger att Redis data persistence är aktiverat.</span><span class="sxs-lookup"><span data-stu-id="2810a-126">Specifies that Redis data persistence is enabled.</span></span>
<span data-ttu-id="2810a-127">Endast Premium-nivå.</span><span class="sxs-lookup"><span data-stu-id="2810a-127">Premium tier only.</span></span>
- <span data-ttu-id="2810a-128">RDB-lagring-anslutning-sträng.</span><span class="sxs-lookup"><span data-stu-id="2810a-128">rdb-storage-connection-string.</span></span>
<span data-ttu-id="2810a-129">Anger anslutnings strängen till lagrings konto för Redis data.</span><span class="sxs-lookup"><span data-stu-id="2810a-129">Specifies the connection string to the Storage account for Redis data persistence.</span></span>
<span data-ttu-id="2810a-130">Endast Premium-nivå.</span><span class="sxs-lookup"><span data-stu-id="2810a-130">Premium tier only.</span></span>
- <span data-ttu-id="2810a-131">RDB-säkerhets kopiering-frekvens.</span><span class="sxs-lookup"><span data-stu-id="2810a-131">rdb-backup-frequency.</span></span>
<span data-ttu-id="2810a-132">Anger säkerhets kopierings frekvensen för Redis data.</span><span class="sxs-lookup"><span data-stu-id="2810a-132">Specifies the backup frequency for Redis data persistence.</span></span>
<span data-ttu-id="2810a-133">Endast Premium-nivå.</span><span class="sxs-lookup"><span data-stu-id="2810a-133">Premium tier only.</span></span> 
- <span data-ttu-id="2810a-134">maxmemory-reserverad.</span><span class="sxs-lookup"><span data-stu-id="2810a-134">maxmemory-reserved.</span></span>
<span data-ttu-id="2810a-135">Konfigurerar minnet reserverat för icke-cachelagrade processer.</span><span class="sxs-lookup"><span data-stu-id="2810a-135">Configures the memory reserved for non-cache processes.</span></span>
<span data-ttu-id="2810a-136">Standard-och Premium-nivåer.</span><span class="sxs-lookup"><span data-stu-id="2810a-136">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="2810a-137">maxmemory-policy.</span><span class="sxs-lookup"><span data-stu-id="2810a-137">maxmemory-policy.</span></span>
<span data-ttu-id="2810a-138">Konfigurerar borttagnings principen för cacheminnet.</span><span class="sxs-lookup"><span data-stu-id="2810a-138">Configures the eviction policy for the cache.</span></span>
<span data-ttu-id="2810a-139">Alla pris nivåer.</span><span class="sxs-lookup"><span data-stu-id="2810a-139">All pricing tiers.</span></span> 
- <span data-ttu-id="2810a-140">meddelande – inloggnings händelser.</span><span class="sxs-lookup"><span data-stu-id="2810a-140">notify-keyspace-events.</span></span>
<span data-ttu-id="2810a-141">Konfigurerar indikeringar för meddelanden.</span><span class="sxs-lookup"><span data-stu-id="2810a-141">Configures keyspace notifications.</span></span>
<span data-ttu-id="2810a-142">Standard-och Premium-nivåer.</span><span class="sxs-lookup"><span data-stu-id="2810a-142">Standard and premium tiers.</span></span> 
- <span data-ttu-id="2810a-143">hash-Max-ziplist-poster.</span><span class="sxs-lookup"><span data-stu-id="2810a-143">hash-max-ziplist-entries.</span></span>
<span data-ttu-id="2810a-144">Konfigurerar minnes optimering för små aggregerade data typer.</span><span class="sxs-lookup"><span data-stu-id="2810a-144">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="2810a-145">Standard-och Premium-nivåer.</span><span class="sxs-lookup"><span data-stu-id="2810a-145">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="2810a-146">hash-Max-ziplist-värde.</span><span class="sxs-lookup"><span data-stu-id="2810a-146">hash-max-ziplist-value.</span></span>
<span data-ttu-id="2810a-147">Konfigurerar minnes optimering för små aggregerade data typer.</span><span class="sxs-lookup"><span data-stu-id="2810a-147">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="2810a-148">Standard-och Premium-nivåer.</span><span class="sxs-lookup"><span data-stu-id="2810a-148">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="2810a-149">set-Max intset-poster.</span><span class="sxs-lookup"><span data-stu-id="2810a-149">set-max-intset-entries.</span></span>
<span data-ttu-id="2810a-150">Konfigurerar minnes optimering för små aggregerade data typer.</span><span class="sxs-lookup"><span data-stu-id="2810a-150">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="2810a-151">Standard-och Premium-nivåer.</span><span class="sxs-lookup"><span data-stu-id="2810a-151">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="2810a-152">zset-Max ziplist-poster.</span><span class="sxs-lookup"><span data-stu-id="2810a-152">zset-max-ziplist-entries.</span></span>
<span data-ttu-id="2810a-153">Konfigurerar minnes optimering för små aggregerade data typer.</span><span class="sxs-lookup"><span data-stu-id="2810a-153">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="2810a-154">Standard-och Premium-nivåer.</span><span class="sxs-lookup"><span data-stu-id="2810a-154">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="2810a-155">zset-Max-ziplist-värde.</span><span class="sxs-lookup"><span data-stu-id="2810a-155">zset-max-ziplist-value.</span></span>
<span data-ttu-id="2810a-156">Konfigurerar minnes optimering för små aggregerade data typer.</span><span class="sxs-lookup"><span data-stu-id="2810a-156">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="2810a-157">Standard-och Premium-nivåer.</span><span class="sxs-lookup"><span data-stu-id="2810a-157">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="2810a-158">samling.</span><span class="sxs-lookup"><span data-stu-id="2810a-158">databases.</span></span>
<span data-ttu-id="2810a-159">Konfigurerar antalet databaser.</span><span class="sxs-lookup"><span data-stu-id="2810a-159">Configures the number of databases.</span></span>
<span data-ttu-id="2810a-160">Det går bara att konfigurera den här egenskapen när cacheminnet skapas.</span><span class="sxs-lookup"><span data-stu-id="2810a-160">This property can be configured only at cache creation.</span></span>
<span data-ttu-id="2810a-161">Standard-och Premium-nivåer.</span><span class="sxs-lookup"><span data-stu-id="2810a-161">Standard and Premium tiers.</span></span>

<span data-ttu-id="2810a-162">Mer information finns i Hantera Azure Redis cache med Azure PowerShell https://go.microsoft.com/fwlink/?LinkId=800051 ( https://go.microsoft.com/fwlink/?LinkId=800051) .</span><span class="sxs-lookup"><span data-stu-id="2810a-162">For more information, see Manage Azure Redis Cache with Azure PowerShellhttps://go.microsoft.com/fwlink/?LinkId=800051 (https://go.microsoft.com/fwlink/?LinkId=800051).</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2810a-163">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2810a-163">-ResourceGroupName</span></span>
<span data-ttu-id="2810a-164">Anger namnet på den resurs grupp som innehåller Redis-cachen.</span><span class="sxs-lookup"><span data-stu-id="2810a-164">Specifies the name of the resource group that contains the Redis Cache.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2810a-165">-ShardCount</span><span class="sxs-lookup"><span data-stu-id="2810a-165">-ShardCount</span></span>
<span data-ttu-id="2810a-166">Anger antalet Shards som ska skapas i ett Premium-kluster-cacheminne.</span><span class="sxs-lookup"><span data-stu-id="2810a-166">Specifies the number of shards to create on a Premium cluster cache.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2810a-167">-Storlek</span><span class="sxs-lookup"><span data-stu-id="2810a-167">-Size</span></span>
<span data-ttu-id="2810a-168">Anger storleken på Redis cache.</span><span class="sxs-lookup"><span data-stu-id="2810a-168">Specifies the size of the Redis Cache.</span></span>
<span data-ttu-id="2810a-169">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="2810a-169">Valid values are:</span></span> 

- <span data-ttu-id="2810a-170">P1</span><span class="sxs-lookup"><span data-stu-id="2810a-170">P1</span></span>
- <span data-ttu-id="2810a-171">P2</span><span class="sxs-lookup"><span data-stu-id="2810a-171">P2</span></span>
- <span data-ttu-id="2810a-172">P3</span><span class="sxs-lookup"><span data-stu-id="2810a-172">P3</span></span>
- <span data-ttu-id="2810a-173">P4</span><span class="sxs-lookup"><span data-stu-id="2810a-173">P4</span></span>
- <span data-ttu-id="2810a-174">C0</span><span class="sxs-lookup"><span data-stu-id="2810a-174">C0</span></span>
- <span data-ttu-id="2810a-175">C1</span><span class="sxs-lookup"><span data-stu-id="2810a-175">C1</span></span>
- <span data-ttu-id="2810a-176">C2</span><span class="sxs-lookup"><span data-stu-id="2810a-176">C2</span></span>
- <span data-ttu-id="2810a-177">C3</span><span class="sxs-lookup"><span data-stu-id="2810a-177">C3</span></span>
- <span data-ttu-id="2810a-178">C4</span><span class="sxs-lookup"><span data-stu-id="2810a-178">C4</span></span>
- <span data-ttu-id="2810a-179">C5</span><span class="sxs-lookup"><span data-stu-id="2810a-179">C5</span></span>
- <span data-ttu-id="2810a-180">C6</span><span class="sxs-lookup"><span data-stu-id="2810a-180">C6</span></span>
- <span data-ttu-id="2810a-181">250</span><span class="sxs-lookup"><span data-stu-id="2810a-181">250MB</span></span>
- <span data-ttu-id="2810a-182">MINNE</span><span class="sxs-lookup"><span data-stu-id="2810a-182">1GB</span></span>
- <span data-ttu-id="2810a-183">2,5 GB</span><span class="sxs-lookup"><span data-stu-id="2810a-183">2.5GB</span></span>
- <span data-ttu-id="2810a-184">6GB</span><span class="sxs-lookup"><span data-stu-id="2810a-184">6GB</span></span>
- <span data-ttu-id="2810a-185">13GB</span><span class="sxs-lookup"><span data-stu-id="2810a-185">13GB</span></span>
- <span data-ttu-id="2810a-186">26GB</span><span class="sxs-lookup"><span data-stu-id="2810a-186">26GB</span></span>
- <span data-ttu-id="2810a-187">53GB</span><span class="sxs-lookup"><span data-stu-id="2810a-187">53GB</span></span>

<span data-ttu-id="2810a-188">Standardvärdet är 1 GB eller C1.</span><span class="sxs-lookup"><span data-stu-id="2810a-188">The default value is 1GB or C1.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: P1, P2, P3, P4, C0, C1, C2, C3, C4, C5, C6, 250MB, 1GB, 2.5GB, 6GB, 13GB, 26GB, 53GB

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2810a-189">-SKU</span><span class="sxs-lookup"><span data-stu-id="2810a-189">-Sku</span></span>
<span data-ttu-id="2810a-190">Anger SKU för det Redis-cacheminne som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="2810a-190">Specifies the SKU of the Redis Cache to create.</span></span>
<span data-ttu-id="2810a-191">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="2810a-191">Valid values are:</span></span> 

- <span data-ttu-id="2810a-192">Basisk</span><span class="sxs-lookup"><span data-stu-id="2810a-192">Basic</span></span>
- <span data-ttu-id="2810a-193">Standar</span><span class="sxs-lookup"><span data-stu-id="2810a-193">Standard</span></span>
- <span data-ttu-id="2810a-194">Beta</span><span class="sxs-lookup"><span data-stu-id="2810a-194">Premium</span></span>

<span data-ttu-id="2810a-195">Standardvärdet är standard.</span><span class="sxs-lookup"><span data-stu-id="2810a-195">The default value is Standard.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Basic, Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2810a-196">-Tagg</span><span class="sxs-lookup"><span data-stu-id="2810a-196">-Tag</span></span>
<span data-ttu-id="2810a-197">En hash-tabell som representerar taggar.</span><span class="sxs-lookup"><span data-stu-id="2810a-197">A hash table which represents tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2810a-198">-TenantSettings</span><span class="sxs-lookup"><span data-stu-id="2810a-198">-TenantSettings</span></span>
<span data-ttu-id="2810a-199">Denna parameter är inaktuell.</span><span class="sxs-lookup"><span data-stu-id="2810a-199">This parameter has been deprecated.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2810a-200">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="2810a-200">-Confirm</span></span>
<span data-ttu-id="2810a-201">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="2810a-201">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2810a-202">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2810a-202">-WhatIf</span></span>
<span data-ttu-id="2810a-203">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="2810a-203">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2810a-204">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="2810a-204">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2810a-205">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2810a-205">CommonParameters</span></span>
<span data-ttu-id="2810a-206">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2810a-206">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2810a-207">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2810a-207">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2810a-208">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2810a-208">INPUTS</span></span>

### <span data-ttu-id="2810a-209">Ingen</span><span class="sxs-lookup"><span data-stu-id="2810a-209">None</span></span>
<span data-ttu-id="2810a-210">Du kan ange indata för denna cmdlet efter egenskaps namn, men inte efter värde.</span><span class="sxs-lookup"><span data-stu-id="2810a-210">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="2810a-211">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2810a-211">OUTPUTS</span></span>

### <span data-ttu-id="2810a-212">Microsoft. Azure. commands. RedisCache. Models. RedisCacheAttributesWithAccessKeys</span><span class="sxs-lookup"><span data-stu-id="2810a-212">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributesWithAccessKeys</span></span>
<span data-ttu-id="2810a-213">Returnerar alla attribut i en Redis-cache, inklusive primära och sekundära åtkomst nycklar.</span><span class="sxs-lookup"><span data-stu-id="2810a-213">Returns all attributes of a Redis Cache, including primary and secondary access keys.</span></span>

## <span data-ttu-id="2810a-214">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2810a-214">NOTES</span></span>

## <span data-ttu-id="2810a-215">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2810a-215">RELATED LINKS</span></span>

[<span data-ttu-id="2810a-216">Get-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="2810a-216">Get-AzureRmRedisCache</span></span>](./Get-AzureRmRedisCache.md)

[<span data-ttu-id="2810a-217">New-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="2810a-217">New-AzureRmRedisCache</span></span>](./New-AzureRmRedisCache.md)

[<span data-ttu-id="2810a-218">Remove-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="2810a-218">Remove-AzureRmRedisCache</span></span>](./Remove-AzureRmRedisCache.md)


