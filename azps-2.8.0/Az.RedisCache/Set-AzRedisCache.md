---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: 6234F211-6ED4-443F-9B83-DEB9AC51B763
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/set-azrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Set-AzRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Set-AzRedisCache.md
ms.openlocfilehash: aaec1ed3f165338c0aea6bf93e38dfaa8460cdf3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93919382"
---
# <span data-ttu-id="09e85-101">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="09e85-101">Set-AzRedisCache</span></span>

## <span data-ttu-id="09e85-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="09e85-102">SYNOPSIS</span></span>
<span data-ttu-id="09e85-103">Ändrar en Redis-cache.</span><span class="sxs-lookup"><span data-stu-id="09e85-103">Modifies a Redis Cache.</span></span>

## <span data-ttu-id="09e85-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="09e85-104">SYNTAX</span></span>

```
Set-AzRedisCache [-ResourceGroupName <String>] -Name <String> [-Size <String>] [-Sku <String>]
 [-RedisConfiguration <Hashtable>] [-EnableNonSslPort <Boolean>] [-TenantSettings <Hashtable>]
 [-ShardCount <Int32>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="09e85-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="09e85-105">DESCRIPTION</span></span>
<span data-ttu-id="09e85-106">Cmdleten **set-AzRedisCache** ändrar ett Azure Redis-cacheminne.</span><span class="sxs-lookup"><span data-stu-id="09e85-106">The **Set-AzRedisCache** cmdlet modifies an Azure Redis Cache.</span></span>

## <span data-ttu-id="09e85-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="09e85-107">EXAMPLES</span></span>

### <span data-ttu-id="09e85-108">Exempel 1: ändra en Redis-cache</span><span class="sxs-lookup"><span data-stu-id="09e85-108">Example 1: Modify a Redis Cache</span></span>
```
PS C:\>Set-AzRedisCache -ResourceGroupName "MyGroup" -Name "MyCache" -RedisConfiguration @{"maxmemory-policy" = "allkeys-random"}

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

<span data-ttu-id="09e85-109">Det här kommandot uppdaterar maxmemory-principen för Redis cachelagrade namn-cachen.</span><span class="sxs-lookup"><span data-stu-id="09e85-109">This command updates the maxmemory-policy for the Redis Cache named MyCache.</span></span>

## <span data-ttu-id="09e85-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="09e85-110">PARAMETERS</span></span>

### <span data-ttu-id="09e85-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09e85-111">-DefaultProfile</span></span>
<span data-ttu-id="09e85-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="09e85-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="09e85-113">-EnableNonSslPort</span><span class="sxs-lookup"><span data-stu-id="09e85-113">-EnableNonSslPort</span></span>
<span data-ttu-id="09e85-114">Anger om icke-SSL-porten är aktive rad.</span><span class="sxs-lookup"><span data-stu-id="09e85-114">Indicates whether the non-SSL port is enabled.</span></span>
<span data-ttu-id="09e85-115">Standardvärdet är $False (icke-SSL-porten är inaktive rad).</span><span class="sxs-lookup"><span data-stu-id="09e85-115">The default value is $False (the non-SSL port is disabled).</span></span>

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

### <span data-ttu-id="09e85-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="09e85-116">-Name</span></span>
<span data-ttu-id="09e85-117">Anger namnet på den Redis-cache som ska uppdateras.</span><span class="sxs-lookup"><span data-stu-id="09e85-117">Specifies the name of the Redis Cache to update.</span></span>

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

### <span data-ttu-id="09e85-118">-RedisConfiguration</span><span class="sxs-lookup"><span data-stu-id="09e85-118">-RedisConfiguration</span></span>
<span data-ttu-id="09e85-119">Anger konfigurations inställningar för Redis.</span><span class="sxs-lookup"><span data-stu-id="09e85-119">Specifies Redis configuration settings.</span></span>
<span data-ttu-id="09e85-120">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="09e85-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="09e85-121">RDB – säkerhets kopiering aktive rad.</span><span class="sxs-lookup"><span data-stu-id="09e85-121">rdb-backup-enabled.</span></span>
<span data-ttu-id="09e85-122">Anger att Redis data persistence är aktiverat.</span><span class="sxs-lookup"><span data-stu-id="09e85-122">Specifies that Redis data persistence is enabled.</span></span>
<span data-ttu-id="09e85-123">Endast Premium-nivå.</span><span class="sxs-lookup"><span data-stu-id="09e85-123">Premium tier only.</span></span>
- <span data-ttu-id="09e85-124">RDB-lagring-anslutning-sträng.</span><span class="sxs-lookup"><span data-stu-id="09e85-124">rdb-storage-connection-string.</span></span>
<span data-ttu-id="09e85-125">Anger anslutnings strängen till lagrings konto för Redis data.</span><span class="sxs-lookup"><span data-stu-id="09e85-125">Specifies the connection string to the Storage account for Redis data persistence.</span></span>
<span data-ttu-id="09e85-126">Endast Premium-nivå.</span><span class="sxs-lookup"><span data-stu-id="09e85-126">Premium tier only.</span></span>
- <span data-ttu-id="09e85-127">RDB-säkerhets kopiering-frekvens.</span><span class="sxs-lookup"><span data-stu-id="09e85-127">rdb-backup-frequency.</span></span>
<span data-ttu-id="09e85-128">Anger säkerhets kopierings frekvensen för Redis data.</span><span class="sxs-lookup"><span data-stu-id="09e85-128">Specifies the backup frequency for Redis data persistence.</span></span>
<span data-ttu-id="09e85-129">Endast Premium-nivå.</span><span class="sxs-lookup"><span data-stu-id="09e85-129">Premium tier only.</span></span> 
- <span data-ttu-id="09e85-130">maxmemory-reserverad.</span><span class="sxs-lookup"><span data-stu-id="09e85-130">maxmemory-reserved.</span></span>
<span data-ttu-id="09e85-131">Konfigurerar minnet reserverat för icke-cachelagrade processer.</span><span class="sxs-lookup"><span data-stu-id="09e85-131">Configures the memory reserved for non-cache processes.</span></span>
<span data-ttu-id="09e85-132">Standard-och Premium-nivåer.</span><span class="sxs-lookup"><span data-stu-id="09e85-132">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="09e85-133">maxmemory-policy.</span><span class="sxs-lookup"><span data-stu-id="09e85-133">maxmemory-policy.</span></span>
<span data-ttu-id="09e85-134">Konfigurerar borttagnings principen för cacheminnet.</span><span class="sxs-lookup"><span data-stu-id="09e85-134">Configures the eviction policy for the cache.</span></span>
<span data-ttu-id="09e85-135">Alla pris nivåer.</span><span class="sxs-lookup"><span data-stu-id="09e85-135">All pricing tiers.</span></span> 
- <span data-ttu-id="09e85-136">meddelande – inloggnings händelser.</span><span class="sxs-lookup"><span data-stu-id="09e85-136">notify-keyspace-events.</span></span>
<span data-ttu-id="09e85-137">Konfigurerar indikeringar för meddelanden.</span><span class="sxs-lookup"><span data-stu-id="09e85-137">Configures keyspace notifications.</span></span>
<span data-ttu-id="09e85-138">Standard-och Premium-nivåer.</span><span class="sxs-lookup"><span data-stu-id="09e85-138">Standard and premium tiers.</span></span> 
- <span data-ttu-id="09e85-139">hash-Max-ziplist-poster.</span><span class="sxs-lookup"><span data-stu-id="09e85-139">hash-max-ziplist-entries.</span></span>
<span data-ttu-id="09e85-140">Konfigurerar minnes optimering för små aggregerade data typer.</span><span class="sxs-lookup"><span data-stu-id="09e85-140">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="09e85-141">Standard-och Premium-nivåer.</span><span class="sxs-lookup"><span data-stu-id="09e85-141">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="09e85-142">hash-Max-ziplist-värde.</span><span class="sxs-lookup"><span data-stu-id="09e85-142">hash-max-ziplist-value.</span></span>
<span data-ttu-id="09e85-143">Konfigurerar minnes optimering för små aggregerade data typer.</span><span class="sxs-lookup"><span data-stu-id="09e85-143">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="09e85-144">Standard-och Premium-nivåer.</span><span class="sxs-lookup"><span data-stu-id="09e85-144">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="09e85-145">set-Max intset-poster.</span><span class="sxs-lookup"><span data-stu-id="09e85-145">set-max-intset-entries.</span></span>
<span data-ttu-id="09e85-146">Konfigurerar minnes optimering för små aggregerade data typer.</span><span class="sxs-lookup"><span data-stu-id="09e85-146">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="09e85-147">Standard-och Premium-nivåer.</span><span class="sxs-lookup"><span data-stu-id="09e85-147">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="09e85-148">zset-Max ziplist-poster.</span><span class="sxs-lookup"><span data-stu-id="09e85-148">zset-max-ziplist-entries.</span></span>
<span data-ttu-id="09e85-149">Konfigurerar minnes optimering för små aggregerade data typer.</span><span class="sxs-lookup"><span data-stu-id="09e85-149">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="09e85-150">Standard-och Premium-nivåer.</span><span class="sxs-lookup"><span data-stu-id="09e85-150">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="09e85-151">zset-Max-ziplist-värde.</span><span class="sxs-lookup"><span data-stu-id="09e85-151">zset-max-ziplist-value.</span></span>
<span data-ttu-id="09e85-152">Konfigurerar minnes optimering för små aggregerade data typer.</span><span class="sxs-lookup"><span data-stu-id="09e85-152">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="09e85-153">Standard-och Premium-nivåer.</span><span class="sxs-lookup"><span data-stu-id="09e85-153">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="09e85-154">samling.</span><span class="sxs-lookup"><span data-stu-id="09e85-154">databases.</span></span>
<span data-ttu-id="09e85-155">Konfigurerar antalet databaser.</span><span class="sxs-lookup"><span data-stu-id="09e85-155">Configures the number of databases.</span></span>
<span data-ttu-id="09e85-156">Det går bara att konfigurera den här egenskapen när cacheminnet skapas.</span><span class="sxs-lookup"><span data-stu-id="09e85-156">This property can be configured only at cache creation.</span></span>
<span data-ttu-id="09e85-157">Standard-och Premium-nivåer.</span><span class="sxs-lookup"><span data-stu-id="09e85-157">Standard and Premium tiers.</span></span>
<span data-ttu-id="09e85-158">Mer information finns i Hantera Azure Redis cache med Azure PowerShell https://go.microsoft.com/fwlink/?LinkId=800051 ( https://go.microsoft.com/fwlink/?LinkId=800051) .</span><span class="sxs-lookup"><span data-stu-id="09e85-158">For more information, see Manage Azure Redis Cache with Azure PowerShellhttps://go.microsoft.com/fwlink/?LinkId=800051 (https://go.microsoft.com/fwlink/?LinkId=800051).</span></span>

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

### <span data-ttu-id="09e85-159">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="09e85-159">-ResourceGroupName</span></span>
<span data-ttu-id="09e85-160">Anger namnet på den resurs grupp som innehåller Redis-cachen.</span><span class="sxs-lookup"><span data-stu-id="09e85-160">Specifies the name of the resource group that contains the Redis Cache.</span></span>

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

### <span data-ttu-id="09e85-161">-ShardCount</span><span class="sxs-lookup"><span data-stu-id="09e85-161">-ShardCount</span></span>
<span data-ttu-id="09e85-162">Anger antalet Shards som ska skapas i ett Premium-kluster-cacheminne.</span><span class="sxs-lookup"><span data-stu-id="09e85-162">Specifies the number of shards to create on a Premium cluster cache.</span></span>

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

### <span data-ttu-id="09e85-163">-Storlek</span><span class="sxs-lookup"><span data-stu-id="09e85-163">-Size</span></span>
<span data-ttu-id="09e85-164">Anger storleken på Redis cache.</span><span class="sxs-lookup"><span data-stu-id="09e85-164">Specifies the size of the Redis Cache.</span></span>
<span data-ttu-id="09e85-165">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="09e85-165">Valid values are:</span></span> 
- <span data-ttu-id="09e85-166">P1</span><span class="sxs-lookup"><span data-stu-id="09e85-166">P1</span></span>
- <span data-ttu-id="09e85-167">P2</span><span class="sxs-lookup"><span data-stu-id="09e85-167">P2</span></span>
- <span data-ttu-id="09e85-168">P3</span><span class="sxs-lookup"><span data-stu-id="09e85-168">P3</span></span>
- <span data-ttu-id="09e85-169">P4</span><span class="sxs-lookup"><span data-stu-id="09e85-169">P4</span></span>
- <span data-ttu-id="09e85-170">P5</span><span class="sxs-lookup"><span data-stu-id="09e85-170">P5</span></span>
- <span data-ttu-id="09e85-171">C0</span><span class="sxs-lookup"><span data-stu-id="09e85-171">C0</span></span>
- <span data-ttu-id="09e85-172">C1</span><span class="sxs-lookup"><span data-stu-id="09e85-172">C1</span></span>
- <span data-ttu-id="09e85-173">C2</span><span class="sxs-lookup"><span data-stu-id="09e85-173">C2</span></span>
- <span data-ttu-id="09e85-174">C3</span><span class="sxs-lookup"><span data-stu-id="09e85-174">C3</span></span>
- <span data-ttu-id="09e85-175">C4</span><span class="sxs-lookup"><span data-stu-id="09e85-175">C4</span></span>
- <span data-ttu-id="09e85-176">C5</span><span class="sxs-lookup"><span data-stu-id="09e85-176">C5</span></span>
- <span data-ttu-id="09e85-177">C6</span><span class="sxs-lookup"><span data-stu-id="09e85-177">C6</span></span>
- <span data-ttu-id="09e85-178">250</span><span class="sxs-lookup"><span data-stu-id="09e85-178">250MB</span></span>
- <span data-ttu-id="09e85-179">MINNE</span><span class="sxs-lookup"><span data-stu-id="09e85-179">1GB</span></span>
- <span data-ttu-id="09e85-180">2,5 GB</span><span class="sxs-lookup"><span data-stu-id="09e85-180">2.5GB</span></span>
- <span data-ttu-id="09e85-181">6GB</span><span class="sxs-lookup"><span data-stu-id="09e85-181">6GB</span></span>
- <span data-ttu-id="09e85-182">13GB</span><span class="sxs-lookup"><span data-stu-id="09e85-182">13GB</span></span>
- <span data-ttu-id="09e85-183">26GB</span><span class="sxs-lookup"><span data-stu-id="09e85-183">26GB</span></span>
- <span data-ttu-id="09e85-184">53GB</span><span class="sxs-lookup"><span data-stu-id="09e85-184">53GB</span></span>
- <span data-ttu-id="09e85-185">120 GB standardvärdet är 1 GB eller C1.</span><span class="sxs-lookup"><span data-stu-id="09e85-185">120GB The default value is 1GB or C1.</span></span>

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

### <span data-ttu-id="09e85-186">-SKU</span><span class="sxs-lookup"><span data-stu-id="09e85-186">-Sku</span></span>
<span data-ttu-id="09e85-187">Anger SKU för det Redis-cacheminne som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="09e85-187">Specifies the SKU of the Redis Cache to create.</span></span>
<span data-ttu-id="09e85-188">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="09e85-188">Valid values are:</span></span> 
- <span data-ttu-id="09e85-189">Basisk</span><span class="sxs-lookup"><span data-stu-id="09e85-189">Basic</span></span>
- <span data-ttu-id="09e85-190">Standar</span><span class="sxs-lookup"><span data-stu-id="09e85-190">Standard</span></span>
- <span data-ttu-id="09e85-191">Premium är standardvärdet standard.</span><span class="sxs-lookup"><span data-stu-id="09e85-191">Premium The default value is Standard.</span></span>

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

### <span data-ttu-id="09e85-192">-Tagg</span><span class="sxs-lookup"><span data-stu-id="09e85-192">-Tag</span></span>
<span data-ttu-id="09e85-193">En hash-tabell som representerar taggar.</span><span class="sxs-lookup"><span data-stu-id="09e85-193">A hash table which represents tags.</span></span>

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

### <span data-ttu-id="09e85-194">-TenantSettings</span><span class="sxs-lookup"><span data-stu-id="09e85-194">-TenantSettings</span></span>
<span data-ttu-id="09e85-195">Denna parameter är inaktuell.</span><span class="sxs-lookup"><span data-stu-id="09e85-195">This parameter has been deprecated.</span></span>

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

### <span data-ttu-id="09e85-196">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="09e85-196">-Confirm</span></span>
<span data-ttu-id="09e85-197">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="09e85-197">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="09e85-198">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="09e85-198">-WhatIf</span></span>
<span data-ttu-id="09e85-199">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="09e85-199">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="09e85-200">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="09e85-200">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="09e85-201">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09e85-201">CommonParameters</span></span>
<span data-ttu-id="09e85-202">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="09e85-202">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09e85-203">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="09e85-203">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09e85-204">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="09e85-204">INPUTS</span></span>

### <span data-ttu-id="09e85-205">System. String</span><span class="sxs-lookup"><span data-stu-id="09e85-205">System.String</span></span>

### <span data-ttu-id="09e85-206">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="09e85-206">System.Collections.Hashtable</span></span>

### <span data-ttu-id="09e85-207">System. Nullable ' 1 [[system. Boolean, system. privat. CoreLib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="09e85-207">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="09e85-208">System. Nullable ' 1 [[system. Int32, system. privat. CoreLib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="09e85-208">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="09e85-209">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="09e85-209">OUTPUTS</span></span>

### <span data-ttu-id="09e85-210">Microsoft. Azure. commands. RedisCache. Models. RedisCacheAttributesWithAccessKeys</span><span class="sxs-lookup"><span data-stu-id="09e85-210">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributesWithAccessKeys</span></span>

## <span data-ttu-id="09e85-211">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="09e85-211">NOTES</span></span>

## <span data-ttu-id="09e85-212">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="09e85-212">RELATED LINKS</span></span>

[<span data-ttu-id="09e85-213">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="09e85-213">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="09e85-214">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="09e85-214">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="09e85-215">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="09e85-215">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)


