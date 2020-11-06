---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: 6234F211-6ED4-443F-9B83-DEB9AC51B763
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Set-AzureRmRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Set-AzureRmRedisCache.md
ms.openlocfilehash: bac4176671f5583072142b5973d12bc62205a0a1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575879"
---
# <span data-ttu-id="6cc13-101">Set-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="6cc13-101">Set-AzureRmRedisCache</span></span>

## <span data-ttu-id="6cc13-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6cc13-102">SYNOPSIS</span></span>
<span data-ttu-id="6cc13-103">Ändrar en Redis-cache.</span><span class="sxs-lookup"><span data-stu-id="6cc13-103">Modifies a Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6cc13-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6cc13-104">SYNTAX</span></span>

```
Set-AzureRmRedisCache -ResourceGroupName <String> -Name <String> [-Size <String>] [-Sku <String>]
 [-MaxMemoryPolicy <String>] [-RedisConfiguration <Hashtable>] [-EnableNonSslPort <Boolean>]
 [-TenantSettings <Hashtable>] [-ShardCount <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6cc13-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6cc13-105">DESCRIPTION</span></span>
<span data-ttu-id="6cc13-106">Cmdleten **set-AzureRmRedisCache** ändrar ett Azure Redis-cacheminne.</span><span class="sxs-lookup"><span data-stu-id="6cc13-106">The **Set-AzureRmRedisCache** cmdlet modifies an Azure Redis Cache.</span></span>

## <span data-ttu-id="6cc13-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6cc13-107">EXAMPLES</span></span>

### <span data-ttu-id="6cc13-108">Exempel 1: ändra en Redis-cache</span><span class="sxs-lookup"><span data-stu-id="6cc13-108">Example 1: Modify a Redis Cache</span></span>
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
```

<span data-ttu-id="6cc13-109">Det här kommandot uppdaterar maxmemory-principen för Redis cachelagrade namn-cachen.</span><span class="sxs-lookup"><span data-stu-id="6cc13-109">This command updates the maxmemory-policy for the Redis Cache named MyCache.</span></span>

## <span data-ttu-id="6cc13-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6cc13-110">PARAMETERS</span></span>

### <span data-ttu-id="6cc13-111">-EnableNonSslPort</span><span class="sxs-lookup"><span data-stu-id="6cc13-111">-EnableNonSslPort</span></span>
<span data-ttu-id="6cc13-112">Anger om icke-SSL-porten är aktive rad.</span><span class="sxs-lookup"><span data-stu-id="6cc13-112">Indicates whether the non-SSL port is enabled.</span></span>
<span data-ttu-id="6cc13-113">Standardvärdet är $False (icke-SSL-porten är inaktive rad).</span><span class="sxs-lookup"><span data-stu-id="6cc13-113">The default value is $False (the non-SSL port is disabled).</span></span>

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

### <span data-ttu-id="6cc13-114">-MaxMemoryPolicy</span><span class="sxs-lookup"><span data-stu-id="6cc13-114">-MaxMemoryPolicy</span></span>
<span data-ttu-id="6cc13-115">Denna parameter är inaktuell.</span><span class="sxs-lookup"><span data-stu-id="6cc13-115">This parameter has been deprecated.</span></span>
<span data-ttu-id="6cc13-116">Använd parametern *RedisConfiguration* för att ange maxmemory policy.</span><span class="sxs-lookup"><span data-stu-id="6cc13-116">Use the *RedisConfiguration* parameter to set maxmemory-policy.</span></span>
<span data-ttu-id="6cc13-117">Till exempel:</span><span class="sxs-lookup"><span data-stu-id="6cc13-117">For example:</span></span> 

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

### <span data-ttu-id="6cc13-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="6cc13-118">-Name</span></span>
<span data-ttu-id="6cc13-119">Anger namnet på den Redis-cache som ska uppdateras.</span><span class="sxs-lookup"><span data-stu-id="6cc13-119">Specifies the name of the Redis Cache to update.</span></span>

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

### <span data-ttu-id="6cc13-120">-RedisConfiguration</span><span class="sxs-lookup"><span data-stu-id="6cc13-120">-RedisConfiguration</span></span>
<span data-ttu-id="6cc13-121">Anger konfigurations inställningar för Redis.</span><span class="sxs-lookup"><span data-stu-id="6cc13-121">Specifies Redis configuration settings.</span></span>
<span data-ttu-id="6cc13-122">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="6cc13-122">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="6cc13-123">RDB – säkerhets kopiering aktive rad.</span><span class="sxs-lookup"><span data-stu-id="6cc13-123">rdb-backup-enabled.</span></span>
<span data-ttu-id="6cc13-124">Anger att Redis data persistence är aktiverat.</span><span class="sxs-lookup"><span data-stu-id="6cc13-124">Specifies that Redis data persistence is enabled.</span></span>
<span data-ttu-id="6cc13-125">Endast Premium-nivå.</span><span class="sxs-lookup"><span data-stu-id="6cc13-125">Premium tier only.</span></span>
- <span data-ttu-id="6cc13-126">RDB-lagring-anslutning-sträng.</span><span class="sxs-lookup"><span data-stu-id="6cc13-126">rdb-storage-connection-string.</span></span>
<span data-ttu-id="6cc13-127">Anger anslutnings strängen till lagrings konto för Redis data.</span><span class="sxs-lookup"><span data-stu-id="6cc13-127">Specifies the connection string to the Storage account for Redis data persistence.</span></span>
<span data-ttu-id="6cc13-128">Endast Premium-nivå.</span><span class="sxs-lookup"><span data-stu-id="6cc13-128">Premium tier only.</span></span>
- <span data-ttu-id="6cc13-129">RDB-säkerhets kopiering-frekvens.</span><span class="sxs-lookup"><span data-stu-id="6cc13-129">rdb-backup-frequency.</span></span>
<span data-ttu-id="6cc13-130">Anger säkerhets kopierings frekvensen för Redis data.</span><span class="sxs-lookup"><span data-stu-id="6cc13-130">Specifies the backup frequency for Redis data persistence.</span></span>
<span data-ttu-id="6cc13-131">Endast Premium-nivå.</span><span class="sxs-lookup"><span data-stu-id="6cc13-131">Premium tier only.</span></span> 
- <span data-ttu-id="6cc13-132">maxmemory-reserverad.</span><span class="sxs-lookup"><span data-stu-id="6cc13-132">maxmemory-reserved.</span></span>
<span data-ttu-id="6cc13-133">Konfigurerar minnet reserverat för icke-cachelagrade processer.</span><span class="sxs-lookup"><span data-stu-id="6cc13-133">Configures the memory reserved for non-cache processes.</span></span>
<span data-ttu-id="6cc13-134">Standard-och Premium-nivåer.</span><span class="sxs-lookup"><span data-stu-id="6cc13-134">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="6cc13-135">maxmemory-policy.</span><span class="sxs-lookup"><span data-stu-id="6cc13-135">maxmemory-policy.</span></span>
<span data-ttu-id="6cc13-136">Konfigurerar borttagnings principen för cacheminnet.</span><span class="sxs-lookup"><span data-stu-id="6cc13-136">Configures the eviction policy for the cache.</span></span>
<span data-ttu-id="6cc13-137">Alla pris nivåer.</span><span class="sxs-lookup"><span data-stu-id="6cc13-137">All pricing tiers.</span></span> 
- <span data-ttu-id="6cc13-138">meddelande – inloggnings händelser.</span><span class="sxs-lookup"><span data-stu-id="6cc13-138">notify-keyspace-events.</span></span>
<span data-ttu-id="6cc13-139">Konfigurerar indikeringar för meddelanden.</span><span class="sxs-lookup"><span data-stu-id="6cc13-139">Configures keyspace notifications.</span></span>
<span data-ttu-id="6cc13-140">Standard-och Premium-nivåer.</span><span class="sxs-lookup"><span data-stu-id="6cc13-140">Standard and premium tiers.</span></span> 
- <span data-ttu-id="6cc13-141">hash-Max-ziplist-poster.</span><span class="sxs-lookup"><span data-stu-id="6cc13-141">hash-max-ziplist-entries.</span></span>
<span data-ttu-id="6cc13-142">Konfigurerar minnes optimering för små aggregerade data typer.</span><span class="sxs-lookup"><span data-stu-id="6cc13-142">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="6cc13-143">Standard-och Premium-nivåer.</span><span class="sxs-lookup"><span data-stu-id="6cc13-143">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="6cc13-144">hash-Max-ziplist-värde.</span><span class="sxs-lookup"><span data-stu-id="6cc13-144">hash-max-ziplist-value.</span></span>
<span data-ttu-id="6cc13-145">Konfigurerar minnes optimering för små aggregerade data typer.</span><span class="sxs-lookup"><span data-stu-id="6cc13-145">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="6cc13-146">Standard-och Premium-nivåer.</span><span class="sxs-lookup"><span data-stu-id="6cc13-146">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="6cc13-147">set-Max intset-poster.</span><span class="sxs-lookup"><span data-stu-id="6cc13-147">set-max-intset-entries.</span></span>
<span data-ttu-id="6cc13-148">Konfigurerar minnes optimering för små aggregerade data typer.</span><span class="sxs-lookup"><span data-stu-id="6cc13-148">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="6cc13-149">Standard-och Premium-nivåer.</span><span class="sxs-lookup"><span data-stu-id="6cc13-149">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="6cc13-150">zset-Max ziplist-poster.</span><span class="sxs-lookup"><span data-stu-id="6cc13-150">zset-max-ziplist-entries.</span></span>
<span data-ttu-id="6cc13-151">Konfigurerar minnes optimering för små aggregerade data typer.</span><span class="sxs-lookup"><span data-stu-id="6cc13-151">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="6cc13-152">Standard-och Premium-nivåer.</span><span class="sxs-lookup"><span data-stu-id="6cc13-152">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="6cc13-153">zset-Max-ziplist-värde.</span><span class="sxs-lookup"><span data-stu-id="6cc13-153">zset-max-ziplist-value.</span></span>
<span data-ttu-id="6cc13-154">Konfigurerar minnes optimering för små aggregerade data typer.</span><span class="sxs-lookup"><span data-stu-id="6cc13-154">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="6cc13-155">Standard-och Premium-nivåer.</span><span class="sxs-lookup"><span data-stu-id="6cc13-155">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="6cc13-156">samling.</span><span class="sxs-lookup"><span data-stu-id="6cc13-156">databases.</span></span>
<span data-ttu-id="6cc13-157">Konfigurerar antalet databaser.</span><span class="sxs-lookup"><span data-stu-id="6cc13-157">Configures the number of databases.</span></span>
<span data-ttu-id="6cc13-158">Det går bara att konfigurera den här egenskapen när cacheminnet skapas.</span><span class="sxs-lookup"><span data-stu-id="6cc13-158">This property can be configured only at cache creation.</span></span>
<span data-ttu-id="6cc13-159">Standard-och Premium-nivåer.</span><span class="sxs-lookup"><span data-stu-id="6cc13-159">Standard and Premium tiers.</span></span>

<span data-ttu-id="6cc13-160">Mer information finns i Hantera Azure Redis cache med Azure PowerShell https://go.microsoft.com/fwlink/?LinkId=800051 ( https://go.microsoft.com/fwlink/?LinkId=800051) .</span><span class="sxs-lookup"><span data-stu-id="6cc13-160">For more information, see Manage Azure Redis Cache with Azure PowerShellhttps://go.microsoft.com/fwlink/?LinkId=800051 (https://go.microsoft.com/fwlink/?LinkId=800051).</span></span>

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

### <span data-ttu-id="6cc13-161">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6cc13-161">-ResourceGroupName</span></span>
<span data-ttu-id="6cc13-162">Anger namnet på den resurs grupp som innehåller Redis-cachen.</span><span class="sxs-lookup"><span data-stu-id="6cc13-162">Specifies the name of the resource group that contains the Redis Cache.</span></span>

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

### <span data-ttu-id="6cc13-163">-ShardCount</span><span class="sxs-lookup"><span data-stu-id="6cc13-163">-ShardCount</span></span>
<span data-ttu-id="6cc13-164">Anger antalet Shards som ska skapas i ett Premium-kluster-cacheminne.</span><span class="sxs-lookup"><span data-stu-id="6cc13-164">Specifies the number of shards to create on a Premium cluster cache.</span></span>

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

### <span data-ttu-id="6cc13-165">-Storlek</span><span class="sxs-lookup"><span data-stu-id="6cc13-165">-Size</span></span>
<span data-ttu-id="6cc13-166">Anger storleken på Redis cache.</span><span class="sxs-lookup"><span data-stu-id="6cc13-166">Specifies the size of the Redis Cache.</span></span>
<span data-ttu-id="6cc13-167">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="6cc13-167">Valid values are:</span></span> 

- <span data-ttu-id="6cc13-168">P1</span><span class="sxs-lookup"><span data-stu-id="6cc13-168">P1</span></span>
- <span data-ttu-id="6cc13-169">P2</span><span class="sxs-lookup"><span data-stu-id="6cc13-169">P2</span></span>
- <span data-ttu-id="6cc13-170">P3</span><span class="sxs-lookup"><span data-stu-id="6cc13-170">P3</span></span>
- <span data-ttu-id="6cc13-171">P4</span><span class="sxs-lookup"><span data-stu-id="6cc13-171">P4</span></span>
- <span data-ttu-id="6cc13-172">C0</span><span class="sxs-lookup"><span data-stu-id="6cc13-172">C0</span></span>
- <span data-ttu-id="6cc13-173">C1</span><span class="sxs-lookup"><span data-stu-id="6cc13-173">C1</span></span>
- <span data-ttu-id="6cc13-174">C2</span><span class="sxs-lookup"><span data-stu-id="6cc13-174">C2</span></span>
- <span data-ttu-id="6cc13-175">C3</span><span class="sxs-lookup"><span data-stu-id="6cc13-175">C3</span></span>
- <span data-ttu-id="6cc13-176">C4</span><span class="sxs-lookup"><span data-stu-id="6cc13-176">C4</span></span>
- <span data-ttu-id="6cc13-177">C5</span><span class="sxs-lookup"><span data-stu-id="6cc13-177">C5</span></span>
- <span data-ttu-id="6cc13-178">C6</span><span class="sxs-lookup"><span data-stu-id="6cc13-178">C6</span></span>
- <span data-ttu-id="6cc13-179">250</span><span class="sxs-lookup"><span data-stu-id="6cc13-179">250MB</span></span>
- <span data-ttu-id="6cc13-180">MINNE</span><span class="sxs-lookup"><span data-stu-id="6cc13-180">1GB</span></span>
- <span data-ttu-id="6cc13-181">2,5 GB</span><span class="sxs-lookup"><span data-stu-id="6cc13-181">2.5GB</span></span>
- <span data-ttu-id="6cc13-182">6GB</span><span class="sxs-lookup"><span data-stu-id="6cc13-182">6GB</span></span>
- <span data-ttu-id="6cc13-183">13GB</span><span class="sxs-lookup"><span data-stu-id="6cc13-183">13GB</span></span>
- <span data-ttu-id="6cc13-184">26GB</span><span class="sxs-lookup"><span data-stu-id="6cc13-184">26GB</span></span>
- <span data-ttu-id="6cc13-185">53GB</span><span class="sxs-lookup"><span data-stu-id="6cc13-185">53GB</span></span>

<span data-ttu-id="6cc13-186">Standardvärdet är 1 GB eller C1.</span><span class="sxs-lookup"><span data-stu-id="6cc13-186">The default value is 1GB or C1.</span></span>

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

### <span data-ttu-id="6cc13-187">-SKU</span><span class="sxs-lookup"><span data-stu-id="6cc13-187">-Sku</span></span>
<span data-ttu-id="6cc13-188">Anger SKU för det Redis-cacheminne som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="6cc13-188">Specifies the SKU of the Redis Cache to create.</span></span>
<span data-ttu-id="6cc13-189">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="6cc13-189">Valid values are:</span></span> 

- <span data-ttu-id="6cc13-190">Basisk</span><span class="sxs-lookup"><span data-stu-id="6cc13-190">Basic</span></span>
- <span data-ttu-id="6cc13-191">Standar</span><span class="sxs-lookup"><span data-stu-id="6cc13-191">Standard</span></span>
- <span data-ttu-id="6cc13-192">Beta</span><span class="sxs-lookup"><span data-stu-id="6cc13-192">Premium</span></span>

<span data-ttu-id="6cc13-193">Standardvärdet är standard.</span><span class="sxs-lookup"><span data-stu-id="6cc13-193">The default value is Standard.</span></span>

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

### <span data-ttu-id="6cc13-194">-TenantSettings</span><span class="sxs-lookup"><span data-stu-id="6cc13-194">-TenantSettings</span></span>
<span data-ttu-id="6cc13-195">Denna parameter är inaktuell.</span><span class="sxs-lookup"><span data-stu-id="6cc13-195">This parameter has been deprecated.</span></span>

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

### <span data-ttu-id="6cc13-196">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6cc13-196">-DefaultProfile</span></span>
<span data-ttu-id="6cc13-197">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="6cc13-197">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6cc13-198">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6cc13-198">CommonParameters</span></span>
<span data-ttu-id="6cc13-199">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6cc13-199">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6cc13-200">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6cc13-200">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6cc13-201">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6cc13-201">INPUTS</span></span>

### <span data-ttu-id="6cc13-202">Ingen</span><span class="sxs-lookup"><span data-stu-id="6cc13-202">None</span></span>
<span data-ttu-id="6cc13-203">Du kan ange indata för denna cmdlet efter egenskaps namn, men inte efter värde.</span><span class="sxs-lookup"><span data-stu-id="6cc13-203">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="6cc13-204">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6cc13-204">OUTPUTS</span></span>

### <span data-ttu-id="6cc13-205">Microsoft. Azure. commands. RedisCache. Models. RedisCacheAttributesWithAccessKeys</span><span class="sxs-lookup"><span data-stu-id="6cc13-205">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributesWithAccessKeys</span></span>
<span data-ttu-id="6cc13-206">Returnerar alla attribut i en Redis-cache, inklusive primära och sekundära åtkomst nycklar.</span><span class="sxs-lookup"><span data-stu-id="6cc13-206">Returns all attributes of a Redis Cache, including primary and secondary access keys.</span></span>

## <span data-ttu-id="6cc13-207">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6cc13-207">NOTES</span></span>

## <span data-ttu-id="6cc13-208">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6cc13-208">RELATED LINKS</span></span>

[<span data-ttu-id="6cc13-209">Get-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="6cc13-209">Get-AzureRmRedisCache</span></span>](./Get-AzureRmRedisCache.md)

[<span data-ttu-id="6cc13-210">New-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="6cc13-210">New-AzureRmRedisCache</span></span>](./New-AzureRmRedisCache.md)

[<span data-ttu-id="6cc13-211">Remove-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="6cc13-211">Remove-AzureRmRedisCache</span></span>](./Remove-AzureRmRedisCache.md)


