---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: 6234F211-6ED4-443F-9B83-DEB9AC51B763
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/set-azrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Set-AzRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Set-AzRedisCache.md
ms.openlocfilehash: 637a1e634b0f8b6f890519bf4865378f50774e39
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93747251"
---
# <span data-ttu-id="dad90-101">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="dad90-101">Set-AzRedisCache</span></span>

## <span data-ttu-id="dad90-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="dad90-102">SYNOPSIS</span></span>
<span data-ttu-id="dad90-103">Ändrar en Redis-cache.</span><span class="sxs-lookup"><span data-stu-id="dad90-103">Modifies a Redis Cache.</span></span>

## <span data-ttu-id="dad90-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="dad90-104">SYNTAX</span></span>

```
Set-AzRedisCache [-ResourceGroupName <String>] -Name <String> [-Size <String>] [-Sku <String>]
 [-RedisConfiguration <Hashtable>] [-EnableNonSslPort <Boolean>] [-TenantSettings <Hashtable>]
 [-ShardCount <Int32>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="dad90-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="dad90-105">DESCRIPTION</span></span>
<span data-ttu-id="dad90-106">Cmdleten **set-AzRedisCache** ändrar ett Azure Redis-cacheminne.</span><span class="sxs-lookup"><span data-stu-id="dad90-106">The **Set-AzRedisCache** cmdlet modifies an Azure Redis Cache.</span></span>

## <span data-ttu-id="dad90-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="dad90-107">EXAMPLES</span></span>

### <span data-ttu-id="dad90-108">Exempel 1: ändra en Redis-cache</span><span class="sxs-lookup"><span data-stu-id="dad90-108">Example 1: Modify a Redis Cache</span></span>
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

<span data-ttu-id="dad90-109">Det här kommandot uppdaterar maxmemory-principen för Redis cachelagrade namn-cachen.</span><span class="sxs-lookup"><span data-stu-id="dad90-109">This command updates the maxmemory-policy for the Redis Cache named MyCache.</span></span>

## <span data-ttu-id="dad90-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="dad90-110">PARAMETERS</span></span>

### <span data-ttu-id="dad90-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dad90-111">-DefaultProfile</span></span>
<span data-ttu-id="dad90-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="dad90-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dad90-113">-EnableNonSslPort</span><span class="sxs-lookup"><span data-stu-id="dad90-113">-EnableNonSslPort</span></span>
<span data-ttu-id="dad90-114">Anger om icke-SSL-porten är aktive rad.</span><span class="sxs-lookup"><span data-stu-id="dad90-114">Indicates whether the non-SSL port is enabled.</span></span>
<span data-ttu-id="dad90-115">Standardvärdet är $False (icke-SSL-porten är inaktive rad).</span><span class="sxs-lookup"><span data-stu-id="dad90-115">The default value is $False (the non-SSL port is disabled).</span></span>

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

### <span data-ttu-id="dad90-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="dad90-116">-Name</span></span>
<span data-ttu-id="dad90-117">Anger namnet på den Redis-cache som ska uppdateras.</span><span class="sxs-lookup"><span data-stu-id="dad90-117">Specifies the name of the Redis Cache to update.</span></span>

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

### <span data-ttu-id="dad90-118">-RedisConfiguration</span><span class="sxs-lookup"><span data-stu-id="dad90-118">-RedisConfiguration</span></span>
<span data-ttu-id="dad90-119">Anger konfigurations inställningar för Redis.</span><span class="sxs-lookup"><span data-stu-id="dad90-119">Specifies Redis configuration settings.</span></span>
<span data-ttu-id="dad90-120">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="dad90-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="dad90-121">RDB – säkerhets kopiering aktive rad.</span><span class="sxs-lookup"><span data-stu-id="dad90-121">rdb-backup-enabled.</span></span>
<span data-ttu-id="dad90-122">Anger att Redis data persistence är aktiverat.</span><span class="sxs-lookup"><span data-stu-id="dad90-122">Specifies that Redis data persistence is enabled.</span></span>
<span data-ttu-id="dad90-123">Endast Premium-nivå.</span><span class="sxs-lookup"><span data-stu-id="dad90-123">Premium tier only.</span></span>
- <span data-ttu-id="dad90-124">RDB-lagring-anslutning-sträng.</span><span class="sxs-lookup"><span data-stu-id="dad90-124">rdb-storage-connection-string.</span></span>
<span data-ttu-id="dad90-125">Anger anslutnings strängen till lagrings konto för Redis data.</span><span class="sxs-lookup"><span data-stu-id="dad90-125">Specifies the connection string to the Storage account for Redis data persistence.</span></span>
<span data-ttu-id="dad90-126">Endast Premium-nivå.</span><span class="sxs-lookup"><span data-stu-id="dad90-126">Premium tier only.</span></span>
- <span data-ttu-id="dad90-127">RDB-säkerhets kopiering-frekvens.</span><span class="sxs-lookup"><span data-stu-id="dad90-127">rdb-backup-frequency.</span></span>
<span data-ttu-id="dad90-128">Anger säkerhets kopierings frekvensen för Redis data.</span><span class="sxs-lookup"><span data-stu-id="dad90-128">Specifies the backup frequency for Redis data persistence.</span></span>
<span data-ttu-id="dad90-129">Endast Premium-nivå.</span><span class="sxs-lookup"><span data-stu-id="dad90-129">Premium tier only.</span></span> 
- <span data-ttu-id="dad90-130">maxmemory-reserverad.</span><span class="sxs-lookup"><span data-stu-id="dad90-130">maxmemory-reserved.</span></span>
<span data-ttu-id="dad90-131">Konfigurerar minnet reserverat för icke-cachelagrade processer.</span><span class="sxs-lookup"><span data-stu-id="dad90-131">Configures the memory reserved for non-cache processes.</span></span>
<span data-ttu-id="dad90-132">Standard-och Premium-nivåer.</span><span class="sxs-lookup"><span data-stu-id="dad90-132">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="dad90-133">maxmemory-policy.</span><span class="sxs-lookup"><span data-stu-id="dad90-133">maxmemory-policy.</span></span>
<span data-ttu-id="dad90-134">Konfigurerar borttagnings principen för cacheminnet.</span><span class="sxs-lookup"><span data-stu-id="dad90-134">Configures the eviction policy for the cache.</span></span>
<span data-ttu-id="dad90-135">Alla pris nivåer.</span><span class="sxs-lookup"><span data-stu-id="dad90-135">All pricing tiers.</span></span> 
- <span data-ttu-id="dad90-136">meddelande – inloggnings händelser.</span><span class="sxs-lookup"><span data-stu-id="dad90-136">notify-keyspace-events.</span></span>
<span data-ttu-id="dad90-137">Konfigurerar indikeringar för meddelanden.</span><span class="sxs-lookup"><span data-stu-id="dad90-137">Configures keyspace notifications.</span></span>
<span data-ttu-id="dad90-138">Standard-och Premium-nivåer.</span><span class="sxs-lookup"><span data-stu-id="dad90-138">Standard and premium tiers.</span></span> 
- <span data-ttu-id="dad90-139">hash-Max-ziplist-poster.</span><span class="sxs-lookup"><span data-stu-id="dad90-139">hash-max-ziplist-entries.</span></span>
<span data-ttu-id="dad90-140">Konfigurerar minnes optimering för små aggregerade data typer.</span><span class="sxs-lookup"><span data-stu-id="dad90-140">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="dad90-141">Standard-och Premium-nivåer.</span><span class="sxs-lookup"><span data-stu-id="dad90-141">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="dad90-142">hash-Max-ziplist-värde.</span><span class="sxs-lookup"><span data-stu-id="dad90-142">hash-max-ziplist-value.</span></span>
<span data-ttu-id="dad90-143">Konfigurerar minnes optimering för små aggregerade data typer.</span><span class="sxs-lookup"><span data-stu-id="dad90-143">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="dad90-144">Standard-och Premium-nivåer.</span><span class="sxs-lookup"><span data-stu-id="dad90-144">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="dad90-145">set-Max intset-poster.</span><span class="sxs-lookup"><span data-stu-id="dad90-145">set-max-intset-entries.</span></span>
<span data-ttu-id="dad90-146">Konfigurerar minnes optimering för små aggregerade data typer.</span><span class="sxs-lookup"><span data-stu-id="dad90-146">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="dad90-147">Standard-och Premium-nivåer.</span><span class="sxs-lookup"><span data-stu-id="dad90-147">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="dad90-148">zset-Max ziplist-poster.</span><span class="sxs-lookup"><span data-stu-id="dad90-148">zset-max-ziplist-entries.</span></span>
<span data-ttu-id="dad90-149">Konfigurerar minnes optimering för små aggregerade data typer.</span><span class="sxs-lookup"><span data-stu-id="dad90-149">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="dad90-150">Standard-och Premium-nivåer.</span><span class="sxs-lookup"><span data-stu-id="dad90-150">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="dad90-151">zset-Max-ziplist-värde.</span><span class="sxs-lookup"><span data-stu-id="dad90-151">zset-max-ziplist-value.</span></span>
<span data-ttu-id="dad90-152">Konfigurerar minnes optimering för små aggregerade data typer.</span><span class="sxs-lookup"><span data-stu-id="dad90-152">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="dad90-153">Standard-och Premium-nivåer.</span><span class="sxs-lookup"><span data-stu-id="dad90-153">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="dad90-154">samling.</span><span class="sxs-lookup"><span data-stu-id="dad90-154">databases.</span></span>
<span data-ttu-id="dad90-155">Konfigurerar antalet databaser.</span><span class="sxs-lookup"><span data-stu-id="dad90-155">Configures the number of databases.</span></span>
<span data-ttu-id="dad90-156">Det går bara att konfigurera den här egenskapen när cacheminnet skapas.</span><span class="sxs-lookup"><span data-stu-id="dad90-156">This property can be configured only at cache creation.</span></span>
<span data-ttu-id="dad90-157">Standard-och Premium-nivåer.</span><span class="sxs-lookup"><span data-stu-id="dad90-157">Standard and Premium tiers.</span></span>
<span data-ttu-id="dad90-158">Mer information finns i Hantera Azure Redis cache med Azure PowerShell https://go.microsoft.com/fwlink/?LinkId=800051 ( https://go.microsoft.com/fwlink/?LinkId=800051) .</span><span class="sxs-lookup"><span data-stu-id="dad90-158">For more information, see Manage Azure Redis Cache with Azure PowerShellhttps://go.microsoft.com/fwlink/?LinkId=800051 (https://go.microsoft.com/fwlink/?LinkId=800051).</span></span>

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

### <span data-ttu-id="dad90-159">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dad90-159">-ResourceGroupName</span></span>
<span data-ttu-id="dad90-160">Anger namnet på den resurs grupp som innehåller Redis-cachen.</span><span class="sxs-lookup"><span data-stu-id="dad90-160">Specifies the name of the resource group that contains the Redis Cache.</span></span>

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

### <span data-ttu-id="dad90-161">-ShardCount</span><span class="sxs-lookup"><span data-stu-id="dad90-161">-ShardCount</span></span>
<span data-ttu-id="dad90-162">Anger antalet Shards som ska skapas i ett Premium-kluster-cacheminne.</span><span class="sxs-lookup"><span data-stu-id="dad90-162">Specifies the number of shards to create on a Premium cluster cache.</span></span>

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

### <span data-ttu-id="dad90-163">-Storlek</span><span class="sxs-lookup"><span data-stu-id="dad90-163">-Size</span></span>
<span data-ttu-id="dad90-164">Anger storleken på Redis cache.</span><span class="sxs-lookup"><span data-stu-id="dad90-164">Specifies the size of the Redis Cache.</span></span>
<span data-ttu-id="dad90-165">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="dad90-165">Valid values are:</span></span> 
- <span data-ttu-id="dad90-166">P1</span><span class="sxs-lookup"><span data-stu-id="dad90-166">P1</span></span>
- <span data-ttu-id="dad90-167">P2</span><span class="sxs-lookup"><span data-stu-id="dad90-167">P2</span></span>
- <span data-ttu-id="dad90-168">P3</span><span class="sxs-lookup"><span data-stu-id="dad90-168">P3</span></span>
- <span data-ttu-id="dad90-169">P4</span><span class="sxs-lookup"><span data-stu-id="dad90-169">P4</span></span>
- <span data-ttu-id="dad90-170">C0</span><span class="sxs-lookup"><span data-stu-id="dad90-170">C0</span></span>
- <span data-ttu-id="dad90-171">C1</span><span class="sxs-lookup"><span data-stu-id="dad90-171">C1</span></span>
- <span data-ttu-id="dad90-172">C2</span><span class="sxs-lookup"><span data-stu-id="dad90-172">C2</span></span>
- <span data-ttu-id="dad90-173">C3</span><span class="sxs-lookup"><span data-stu-id="dad90-173">C3</span></span>
- <span data-ttu-id="dad90-174">C4</span><span class="sxs-lookup"><span data-stu-id="dad90-174">C4</span></span>
- <span data-ttu-id="dad90-175">C5</span><span class="sxs-lookup"><span data-stu-id="dad90-175">C5</span></span>
- <span data-ttu-id="dad90-176">C6</span><span class="sxs-lookup"><span data-stu-id="dad90-176">C6</span></span>
- <span data-ttu-id="dad90-177">250</span><span class="sxs-lookup"><span data-stu-id="dad90-177">250MB</span></span>
- <span data-ttu-id="dad90-178">MINNE</span><span class="sxs-lookup"><span data-stu-id="dad90-178">1GB</span></span>
- <span data-ttu-id="dad90-179">2,5 GB</span><span class="sxs-lookup"><span data-stu-id="dad90-179">2.5GB</span></span>
- <span data-ttu-id="dad90-180">6GB</span><span class="sxs-lookup"><span data-stu-id="dad90-180">6GB</span></span>
- <span data-ttu-id="dad90-181">13GB</span><span class="sxs-lookup"><span data-stu-id="dad90-181">13GB</span></span>
- <span data-ttu-id="dad90-182">26GB</span><span class="sxs-lookup"><span data-stu-id="dad90-182">26GB</span></span>
- <span data-ttu-id="dad90-183">53GB standardvärdet är 1 GB eller C1.</span><span class="sxs-lookup"><span data-stu-id="dad90-183">53GB The default value is 1GB or C1.</span></span>

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

### <span data-ttu-id="dad90-184">-SKU</span><span class="sxs-lookup"><span data-stu-id="dad90-184">-Sku</span></span>
<span data-ttu-id="dad90-185">Anger SKU för det Redis-cacheminne som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="dad90-185">Specifies the SKU of the Redis Cache to create.</span></span>
<span data-ttu-id="dad90-186">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="dad90-186">Valid values are:</span></span> 
- <span data-ttu-id="dad90-187">Basisk</span><span class="sxs-lookup"><span data-stu-id="dad90-187">Basic</span></span>
- <span data-ttu-id="dad90-188">Standar</span><span class="sxs-lookup"><span data-stu-id="dad90-188">Standard</span></span>
- <span data-ttu-id="dad90-189">Premium är standardvärdet standard.</span><span class="sxs-lookup"><span data-stu-id="dad90-189">Premium The default value is Standard.</span></span>

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

### <span data-ttu-id="dad90-190">-Tagg</span><span class="sxs-lookup"><span data-stu-id="dad90-190">-Tag</span></span>
<span data-ttu-id="dad90-191">En hash-tabell som representerar taggar.</span><span class="sxs-lookup"><span data-stu-id="dad90-191">A hash table which represents tags.</span></span>

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

### <span data-ttu-id="dad90-192">-TenantSettings</span><span class="sxs-lookup"><span data-stu-id="dad90-192">-TenantSettings</span></span>
<span data-ttu-id="dad90-193">Denna parameter är inaktuell.</span><span class="sxs-lookup"><span data-stu-id="dad90-193">This parameter has been deprecated.</span></span>

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

### <span data-ttu-id="dad90-194">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="dad90-194">-Confirm</span></span>
<span data-ttu-id="dad90-195">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="dad90-195">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dad90-196">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dad90-196">-WhatIf</span></span>
<span data-ttu-id="dad90-197">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="dad90-197">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="dad90-198">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="dad90-198">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dad90-199">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dad90-199">CommonParameters</span></span>
<span data-ttu-id="dad90-200">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dad90-200">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dad90-201">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dad90-201">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dad90-202">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="dad90-202">INPUTS</span></span>

### <span data-ttu-id="dad90-203">System. String</span><span class="sxs-lookup"><span data-stu-id="dad90-203">System.String</span></span>

### <span data-ttu-id="dad90-204">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="dad90-204">System.Collections.Hashtable</span></span>

### <span data-ttu-id="dad90-205">System. Nullable ' 1 [[system. Boolean, system. privat. CoreLib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="dad90-205">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="dad90-206">System. Nullable ' 1 [[system. Int32, system. privat. CoreLib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="dad90-206">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="dad90-207">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="dad90-207">OUTPUTS</span></span>

### <span data-ttu-id="dad90-208">Microsoft. Azure. commands. RedisCache. Models. RedisCacheAttributesWithAccessKeys</span><span class="sxs-lookup"><span data-stu-id="dad90-208">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributesWithAccessKeys</span></span>

## <span data-ttu-id="dad90-209">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="dad90-209">NOTES</span></span>

## <span data-ttu-id="dad90-210">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="dad90-210">RELATED LINKS</span></span>

[<span data-ttu-id="dad90-211">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="dad90-211">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="dad90-212">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="dad90-212">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="dad90-213">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="dad90-213">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)


