---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: 6234F211-6ED4-443F-9B83-DEB9AC51B763
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/set-azrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Set-AzRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Set-AzRedisCache.md
ms.openlocfilehash: 5cb3723e95acbc05b5fffce55a1f768c8a3b7fba
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93927502"
---
# <span data-ttu-id="4945e-101">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="4945e-101">Set-AzRedisCache</span></span>

## <span data-ttu-id="4945e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4945e-102">SYNOPSIS</span></span>
<span data-ttu-id="4945e-103">Ändrar en Redis-cache.</span><span class="sxs-lookup"><span data-stu-id="4945e-103">Modifies a Redis Cache.</span></span>

## <span data-ttu-id="4945e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4945e-104">SYNTAX</span></span>

```
Set-AzRedisCache [-ResourceGroupName <String>] -Name <String> [-Size <String>] [-Sku <String>]
 [-RedisConfiguration <Hashtable>] [-EnableNonSslPort <Boolean>] [-TenantSettings <Hashtable>]
 [-ShardCount <Int32>] [-MinimumTlsVersion <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4945e-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4945e-105">DESCRIPTION</span></span>
<span data-ttu-id="4945e-106">Cmdleten **set-AzRedisCache** ändrar ett Azure Redis-cacheminne.</span><span class="sxs-lookup"><span data-stu-id="4945e-106">The **Set-AzRedisCache** cmdlet modifies an Azure Redis Cache.</span></span>

## <span data-ttu-id="4945e-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4945e-107">EXAMPLES</span></span>

### <span data-ttu-id="4945e-108">Exempel 1: ändra en Redis-cache</span><span class="sxs-lookup"><span data-stu-id="4945e-108">Example 1: Modify a Redis Cache</span></span>
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

<span data-ttu-id="4945e-109">Det här kommandot uppdaterar maxmemory-principen för Redis cachelagrade namn-cachen.</span><span class="sxs-lookup"><span data-stu-id="4945e-109">This command updates the maxmemory-policy for the Redis Cache named MyCache.</span></span>

## <span data-ttu-id="4945e-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4945e-110">PARAMETERS</span></span>

### <span data-ttu-id="4945e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4945e-111">-DefaultProfile</span></span>
<span data-ttu-id="4945e-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4945e-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4945e-113">-EnableNonSslPort</span><span class="sxs-lookup"><span data-stu-id="4945e-113">-EnableNonSslPort</span></span>
<span data-ttu-id="4945e-114">Anger om icke-SSL-porten är aktive rad.</span><span class="sxs-lookup"><span data-stu-id="4945e-114">Indicates whether the non-SSL port is enabled.</span></span>
<span data-ttu-id="4945e-115">Standardvärdet är $False (icke-SSL-porten är inaktive rad).</span><span class="sxs-lookup"><span data-stu-id="4945e-115">The default value is $False (the non-SSL port is disabled).</span></span>

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

### <span data-ttu-id="4945e-116">-MinimumTlsVersion</span><span class="sxs-lookup"><span data-stu-id="4945e-116">-MinimumTlsVersion</span></span>
<span data-ttu-id="4945e-117">Ange den TLS-version som krävs för att klienterna ska kunna ansluta till cacheminnet.</span><span class="sxs-lookup"><span data-stu-id="4945e-117">Specify the TLS version required by clients to connect to cache.</span></span>

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

### <span data-ttu-id="4945e-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="4945e-118">-Name</span></span>
<span data-ttu-id="4945e-119">Anger namnet på den Redis-cache som ska uppdateras.</span><span class="sxs-lookup"><span data-stu-id="4945e-119">Specifies the name of the Redis Cache to update.</span></span>

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

### <span data-ttu-id="4945e-120">-RedisConfiguration</span><span class="sxs-lookup"><span data-stu-id="4945e-120">-RedisConfiguration</span></span>
<span data-ttu-id="4945e-121">Anger konfigurations inställningar för Redis.</span><span class="sxs-lookup"><span data-stu-id="4945e-121">Specifies Redis configuration settings.</span></span>
<span data-ttu-id="4945e-122">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="4945e-122">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="4945e-123">RDB – säkerhets kopiering aktive rad.</span><span class="sxs-lookup"><span data-stu-id="4945e-123">rdb-backup-enabled.</span></span>
<span data-ttu-id="4945e-124">Anger att Redis data persistence är aktiverat.</span><span class="sxs-lookup"><span data-stu-id="4945e-124">Specifies that Redis data persistence is enabled.</span></span>
<span data-ttu-id="4945e-125">Endast Premium-nivå.</span><span class="sxs-lookup"><span data-stu-id="4945e-125">Premium tier only.</span></span>
- <span data-ttu-id="4945e-126">RDB-lagring-anslutning-sträng.</span><span class="sxs-lookup"><span data-stu-id="4945e-126">rdb-storage-connection-string.</span></span>
<span data-ttu-id="4945e-127">Anger anslutnings strängen till lagrings konto för Redis data.</span><span class="sxs-lookup"><span data-stu-id="4945e-127">Specifies the connection string to the Storage account for Redis data persistence.</span></span>
<span data-ttu-id="4945e-128">Endast Premium-nivå.</span><span class="sxs-lookup"><span data-stu-id="4945e-128">Premium tier only.</span></span>
- <span data-ttu-id="4945e-129">RDB-säkerhets kopiering-frekvens.</span><span class="sxs-lookup"><span data-stu-id="4945e-129">rdb-backup-frequency.</span></span>
<span data-ttu-id="4945e-130">Anger säkerhets kopierings frekvensen för Redis data.</span><span class="sxs-lookup"><span data-stu-id="4945e-130">Specifies the backup frequency for Redis data persistence.</span></span>
<span data-ttu-id="4945e-131">Endast Premium-nivå.</span><span class="sxs-lookup"><span data-stu-id="4945e-131">Premium tier only.</span></span> 
- <span data-ttu-id="4945e-132">maxmemory-reserverad.</span><span class="sxs-lookup"><span data-stu-id="4945e-132">maxmemory-reserved.</span></span>
<span data-ttu-id="4945e-133">Konfigurerar minnet reserverat för icke-cachelagrade processer.</span><span class="sxs-lookup"><span data-stu-id="4945e-133">Configures the memory reserved for non-cache processes.</span></span>
<span data-ttu-id="4945e-134">Standard-och Premium-nivåer.</span><span class="sxs-lookup"><span data-stu-id="4945e-134">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="4945e-135">maxmemory-policy.</span><span class="sxs-lookup"><span data-stu-id="4945e-135">maxmemory-policy.</span></span>
<span data-ttu-id="4945e-136">Konfigurerar borttagnings principen för cacheminnet.</span><span class="sxs-lookup"><span data-stu-id="4945e-136">Configures the eviction policy for the cache.</span></span>
<span data-ttu-id="4945e-137">Alla pris nivåer.</span><span class="sxs-lookup"><span data-stu-id="4945e-137">All pricing tiers.</span></span> 
- <span data-ttu-id="4945e-138">meddelande – inloggnings händelser.</span><span class="sxs-lookup"><span data-stu-id="4945e-138">notify-keyspace-events.</span></span>
<span data-ttu-id="4945e-139">Konfigurerar indikeringar för meddelanden.</span><span class="sxs-lookup"><span data-stu-id="4945e-139">Configures keyspace notifications.</span></span>
<span data-ttu-id="4945e-140">Standard-och Premium-nivåer.</span><span class="sxs-lookup"><span data-stu-id="4945e-140">Standard and premium tiers.</span></span> 
- <span data-ttu-id="4945e-141">hash-Max-ziplist-poster.</span><span class="sxs-lookup"><span data-stu-id="4945e-141">hash-max-ziplist-entries.</span></span>
<span data-ttu-id="4945e-142">Konfigurerar minnes optimering för små aggregerade data typer.</span><span class="sxs-lookup"><span data-stu-id="4945e-142">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="4945e-143">Standard-och Premium-nivåer.</span><span class="sxs-lookup"><span data-stu-id="4945e-143">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="4945e-144">hash-Max-ziplist-värde.</span><span class="sxs-lookup"><span data-stu-id="4945e-144">hash-max-ziplist-value.</span></span>
<span data-ttu-id="4945e-145">Konfigurerar minnes optimering för små aggregerade data typer.</span><span class="sxs-lookup"><span data-stu-id="4945e-145">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="4945e-146">Standard-och Premium-nivåer.</span><span class="sxs-lookup"><span data-stu-id="4945e-146">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="4945e-147">set-Max intset-poster.</span><span class="sxs-lookup"><span data-stu-id="4945e-147">set-max-intset-entries.</span></span>
<span data-ttu-id="4945e-148">Konfigurerar minnes optimering för små aggregerade data typer.</span><span class="sxs-lookup"><span data-stu-id="4945e-148">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="4945e-149">Standard-och Premium-nivåer.</span><span class="sxs-lookup"><span data-stu-id="4945e-149">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="4945e-150">zset-Max ziplist-poster.</span><span class="sxs-lookup"><span data-stu-id="4945e-150">zset-max-ziplist-entries.</span></span>
<span data-ttu-id="4945e-151">Konfigurerar minnes optimering för små aggregerade data typer.</span><span class="sxs-lookup"><span data-stu-id="4945e-151">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="4945e-152">Standard-och Premium-nivåer.</span><span class="sxs-lookup"><span data-stu-id="4945e-152">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="4945e-153">zset-Max-ziplist-värde.</span><span class="sxs-lookup"><span data-stu-id="4945e-153">zset-max-ziplist-value.</span></span>
<span data-ttu-id="4945e-154">Konfigurerar minnes optimering för små aggregerade data typer.</span><span class="sxs-lookup"><span data-stu-id="4945e-154">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="4945e-155">Standard-och Premium-nivåer.</span><span class="sxs-lookup"><span data-stu-id="4945e-155">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="4945e-156">samling.</span><span class="sxs-lookup"><span data-stu-id="4945e-156">databases.</span></span>
<span data-ttu-id="4945e-157">Konfigurerar antalet databaser.</span><span class="sxs-lookup"><span data-stu-id="4945e-157">Configures the number of databases.</span></span>
<span data-ttu-id="4945e-158">Det går bara att konfigurera den här egenskapen när cacheminnet skapas.</span><span class="sxs-lookup"><span data-stu-id="4945e-158">This property can be configured only at cache creation.</span></span>
<span data-ttu-id="4945e-159">Standard-och Premium-nivåer.</span><span class="sxs-lookup"><span data-stu-id="4945e-159">Standard and Premium tiers.</span></span>
<span data-ttu-id="4945e-160">Mer information finns i Hantera Azure Redis cache med Azure PowerShell http://go.microsoft.com/fwlink/?LinkId=800051 ( http://go.microsoft.com/fwlink/?LinkId=800051) .</span><span class="sxs-lookup"><span data-stu-id="4945e-160">For more information, see Manage Azure Redis Cache with Azure PowerShellhttp://go.microsoft.com/fwlink/?LinkId=800051 (http://go.microsoft.com/fwlink/?LinkId=800051).</span></span>

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

### <span data-ttu-id="4945e-161">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4945e-161">-ResourceGroupName</span></span>
<span data-ttu-id="4945e-162">Anger namnet på den resurs grupp som innehåller Redis-cachen.</span><span class="sxs-lookup"><span data-stu-id="4945e-162">Specifies the name of the resource group that contains the Redis Cache.</span></span>

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

### <span data-ttu-id="4945e-163">-ShardCount</span><span class="sxs-lookup"><span data-stu-id="4945e-163">-ShardCount</span></span>
<span data-ttu-id="4945e-164">Anger antalet Shards som ska skapas i ett Premium-kluster-cacheminne.</span><span class="sxs-lookup"><span data-stu-id="4945e-164">Specifies the number of shards to create on a Premium cluster cache.</span></span>

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

### <span data-ttu-id="4945e-165">-Storlek</span><span class="sxs-lookup"><span data-stu-id="4945e-165">-Size</span></span>
<span data-ttu-id="4945e-166">Anger storleken på Redis cache.</span><span class="sxs-lookup"><span data-stu-id="4945e-166">Specifies the size of the Redis Cache.</span></span>
<span data-ttu-id="4945e-167">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="4945e-167">Valid values are:</span></span> 
- <span data-ttu-id="4945e-168">P1</span><span class="sxs-lookup"><span data-stu-id="4945e-168">P1</span></span>
- <span data-ttu-id="4945e-169">P2</span><span class="sxs-lookup"><span data-stu-id="4945e-169">P2</span></span>
- <span data-ttu-id="4945e-170">P3</span><span class="sxs-lookup"><span data-stu-id="4945e-170">P3</span></span>
- <span data-ttu-id="4945e-171">P4</span><span class="sxs-lookup"><span data-stu-id="4945e-171">P4</span></span>
- <span data-ttu-id="4945e-172">P5</span><span class="sxs-lookup"><span data-stu-id="4945e-172">P5</span></span>
- <span data-ttu-id="4945e-173">C0</span><span class="sxs-lookup"><span data-stu-id="4945e-173">C0</span></span>
- <span data-ttu-id="4945e-174">C1</span><span class="sxs-lookup"><span data-stu-id="4945e-174">C1</span></span>
- <span data-ttu-id="4945e-175">C2</span><span class="sxs-lookup"><span data-stu-id="4945e-175">C2</span></span>
- <span data-ttu-id="4945e-176">C3</span><span class="sxs-lookup"><span data-stu-id="4945e-176">C3</span></span>
- <span data-ttu-id="4945e-177">C4</span><span class="sxs-lookup"><span data-stu-id="4945e-177">C4</span></span>
- <span data-ttu-id="4945e-178">C5</span><span class="sxs-lookup"><span data-stu-id="4945e-178">C5</span></span>
- <span data-ttu-id="4945e-179">C6</span><span class="sxs-lookup"><span data-stu-id="4945e-179">C6</span></span>
- <span data-ttu-id="4945e-180">250</span><span class="sxs-lookup"><span data-stu-id="4945e-180">250MB</span></span>
- <span data-ttu-id="4945e-181">MINNE</span><span class="sxs-lookup"><span data-stu-id="4945e-181">1GB</span></span>
- <span data-ttu-id="4945e-182">2,5 GB</span><span class="sxs-lookup"><span data-stu-id="4945e-182">2.5GB</span></span>
- <span data-ttu-id="4945e-183">6GB</span><span class="sxs-lookup"><span data-stu-id="4945e-183">6GB</span></span>
- <span data-ttu-id="4945e-184">13GB</span><span class="sxs-lookup"><span data-stu-id="4945e-184">13GB</span></span>
- <span data-ttu-id="4945e-185">26GB</span><span class="sxs-lookup"><span data-stu-id="4945e-185">26GB</span></span>
- <span data-ttu-id="4945e-186">53GB</span><span class="sxs-lookup"><span data-stu-id="4945e-186">53GB</span></span>
- <span data-ttu-id="4945e-187">120 GB standardvärdet är 1 GB eller C1.</span><span class="sxs-lookup"><span data-stu-id="4945e-187">120GB The default value is 1GB or C1.</span></span>

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

### <span data-ttu-id="4945e-188">-SKU</span><span class="sxs-lookup"><span data-stu-id="4945e-188">-Sku</span></span>
<span data-ttu-id="4945e-189">Anger SKU för det Redis-cacheminne som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="4945e-189">Specifies the SKU of the Redis Cache to create.</span></span>
<span data-ttu-id="4945e-190">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="4945e-190">Valid values are:</span></span> 
- <span data-ttu-id="4945e-191">Basisk</span><span class="sxs-lookup"><span data-stu-id="4945e-191">Basic</span></span>
- <span data-ttu-id="4945e-192">Standar</span><span class="sxs-lookup"><span data-stu-id="4945e-192">Standard</span></span>
- <span data-ttu-id="4945e-193">Premium är standardvärdet standard.</span><span class="sxs-lookup"><span data-stu-id="4945e-193">Premium The default value is Standard.</span></span>

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

### <span data-ttu-id="4945e-194">-Tagg</span><span class="sxs-lookup"><span data-stu-id="4945e-194">-Tag</span></span>
<span data-ttu-id="4945e-195">En hash-tabell som representerar taggar.</span><span class="sxs-lookup"><span data-stu-id="4945e-195">A hash table which represents tags.</span></span>

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

### <span data-ttu-id="4945e-196">-TenantSettings</span><span class="sxs-lookup"><span data-stu-id="4945e-196">-TenantSettings</span></span>
<span data-ttu-id="4945e-197">Denna parameter är inaktuell.</span><span class="sxs-lookup"><span data-stu-id="4945e-197">This parameter has been deprecated.</span></span>

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

### <span data-ttu-id="4945e-198">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="4945e-198">-Confirm</span></span>
<span data-ttu-id="4945e-199">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="4945e-199">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4945e-200">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4945e-200">-WhatIf</span></span>
<span data-ttu-id="4945e-201">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="4945e-201">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4945e-202">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="4945e-202">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4945e-203">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4945e-203">CommonParameters</span></span>
<span data-ttu-id="4945e-204">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4945e-204">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4945e-205">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4945e-205">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4945e-206">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4945e-206">INPUTS</span></span>

### <span data-ttu-id="4945e-207">System. String</span><span class="sxs-lookup"><span data-stu-id="4945e-207">System.String</span></span>

### <span data-ttu-id="4945e-208">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="4945e-208">System.Collections.Hashtable</span></span>

### <span data-ttu-id="4945e-209">System. Nullable ' 1 [[system. Boolean, system. privat. CoreLib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="4945e-209">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="4945e-210">System. Nullable ' 1 [[system. Int32, system. privat. CoreLib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="4945e-210">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="4945e-211">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4945e-211">OUTPUTS</span></span>

### <span data-ttu-id="4945e-212">Microsoft. Azure. commands. RedisCache. Models. RedisCacheAttributesWithAccessKeys</span><span class="sxs-lookup"><span data-stu-id="4945e-212">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributesWithAccessKeys</span></span>

## <span data-ttu-id="4945e-213">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4945e-213">NOTES</span></span>

## <span data-ttu-id="4945e-214">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4945e-214">RELATED LINKS</span></span>

[<span data-ttu-id="4945e-215">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="4945e-215">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="4945e-216">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="4945e-216">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="4945e-217">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="4945e-217">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)


