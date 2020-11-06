---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: 6234F211-6ED4-443F-9B83-DEB9AC51B763
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/set-azurermrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Set-AzureRmRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Set-AzureRmRedisCache.md
ms.openlocfilehash: 484c72dd77ada862536b064cb2bcaec07ef51bb8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93584003"
---
# <span data-ttu-id="b7f7a-101">Set-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="b7f7a-101">Set-AzureRmRedisCache</span></span>

## <span data-ttu-id="b7f7a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b7f7a-102">SYNOPSIS</span></span>
<span data-ttu-id="b7f7a-103">Ändrar en Redis-cache.</span><span class="sxs-lookup"><span data-stu-id="b7f7a-103">Modifies a Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b7f7a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b7f7a-104">SYNTAX</span></span>

```
Set-AzureRmRedisCache [-ResourceGroupName <String>] -Name <String> [-Size <String>] [-Sku <String>]
 [-RedisConfiguration <Hashtable>] [-EnableNonSslPort <Boolean>] [-TenantSettings <Hashtable>]
 [-ShardCount <Int32>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b7f7a-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b7f7a-105">DESCRIPTION</span></span>
<span data-ttu-id="b7f7a-106">Cmdleten **set-AzureRmRedisCache** ändrar ett Azure Redis-cacheminne.</span><span class="sxs-lookup"><span data-stu-id="b7f7a-106">The **Set-AzureRmRedisCache** cmdlet modifies an Azure Redis Cache.</span></span>

## <span data-ttu-id="b7f7a-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b7f7a-107">EXAMPLES</span></span>

### <span data-ttu-id="b7f7a-108">Exempel 1: ändra en Redis-cache</span><span class="sxs-lookup"><span data-stu-id="b7f7a-108">Example 1: Modify a Redis Cache</span></span>
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

<span data-ttu-id="b7f7a-109">Det här kommandot uppdaterar maxmemory-principen för Redis cachelagrade namn-cachen.</span><span class="sxs-lookup"><span data-stu-id="b7f7a-109">This command updates the maxmemory-policy for the Redis Cache named MyCache.</span></span>

## <span data-ttu-id="b7f7a-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b7f7a-110">PARAMETERS</span></span>

### <span data-ttu-id="b7f7a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7f7a-111">-DefaultProfile</span></span>
<span data-ttu-id="b7f7a-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b7f7a-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b7f7a-113">-EnableNonSslPort</span><span class="sxs-lookup"><span data-stu-id="b7f7a-113">-EnableNonSslPort</span></span>
<span data-ttu-id="b7f7a-114">Anger om icke-SSL-porten är aktive rad.</span><span class="sxs-lookup"><span data-stu-id="b7f7a-114">Indicates whether the non-SSL port is enabled.</span></span>
<span data-ttu-id="b7f7a-115">Standardvärdet är $False (icke-SSL-porten är inaktive rad).</span><span class="sxs-lookup"><span data-stu-id="b7f7a-115">The default value is $False (the non-SSL port is disabled).</span></span>

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

### <span data-ttu-id="b7f7a-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="b7f7a-116">-Name</span></span>
<span data-ttu-id="b7f7a-117">Anger namnet på den Redis-cache som ska uppdateras.</span><span class="sxs-lookup"><span data-stu-id="b7f7a-117">Specifies the name of the Redis Cache to update.</span></span>

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

### <span data-ttu-id="b7f7a-118">-RedisConfiguration</span><span class="sxs-lookup"><span data-stu-id="b7f7a-118">-RedisConfiguration</span></span>
<span data-ttu-id="b7f7a-119">Anger konfigurations inställningar för Redis.</span><span class="sxs-lookup"><span data-stu-id="b7f7a-119">Specifies Redis configuration settings.</span></span>
<span data-ttu-id="b7f7a-120">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="b7f7a-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="b7f7a-121">RDB – säkerhets kopiering aktive rad.</span><span class="sxs-lookup"><span data-stu-id="b7f7a-121">rdb-backup-enabled.</span></span>
<span data-ttu-id="b7f7a-122">Anger att Redis data persistence är aktiverat.</span><span class="sxs-lookup"><span data-stu-id="b7f7a-122">Specifies that Redis data persistence is enabled.</span></span>
<span data-ttu-id="b7f7a-123">Endast Premium-nivå.</span><span class="sxs-lookup"><span data-stu-id="b7f7a-123">Premium tier only.</span></span>
- <span data-ttu-id="b7f7a-124">RDB-lagring-anslutning-sträng.</span><span class="sxs-lookup"><span data-stu-id="b7f7a-124">rdb-storage-connection-string.</span></span>
<span data-ttu-id="b7f7a-125">Anger anslutnings strängen till lagrings konto för Redis data.</span><span class="sxs-lookup"><span data-stu-id="b7f7a-125">Specifies the connection string to the Storage account for Redis data persistence.</span></span>
<span data-ttu-id="b7f7a-126">Endast Premium-nivå.</span><span class="sxs-lookup"><span data-stu-id="b7f7a-126">Premium tier only.</span></span>
- <span data-ttu-id="b7f7a-127">RDB-säkerhets kopiering-frekvens.</span><span class="sxs-lookup"><span data-stu-id="b7f7a-127">rdb-backup-frequency.</span></span>
<span data-ttu-id="b7f7a-128">Anger säkerhets kopierings frekvensen för Redis data.</span><span class="sxs-lookup"><span data-stu-id="b7f7a-128">Specifies the backup frequency for Redis data persistence.</span></span>
<span data-ttu-id="b7f7a-129">Endast Premium-nivå.</span><span class="sxs-lookup"><span data-stu-id="b7f7a-129">Premium tier only.</span></span> 
- <span data-ttu-id="b7f7a-130">maxmemory-reserverad.</span><span class="sxs-lookup"><span data-stu-id="b7f7a-130">maxmemory-reserved.</span></span>
<span data-ttu-id="b7f7a-131">Konfigurerar minnet reserverat för icke-cachelagrade processer.</span><span class="sxs-lookup"><span data-stu-id="b7f7a-131">Configures the memory reserved for non-cache processes.</span></span>
<span data-ttu-id="b7f7a-132">Standard-och Premium-nivåer.</span><span class="sxs-lookup"><span data-stu-id="b7f7a-132">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="b7f7a-133">maxmemory-policy.</span><span class="sxs-lookup"><span data-stu-id="b7f7a-133">maxmemory-policy.</span></span>
<span data-ttu-id="b7f7a-134">Konfigurerar borttagnings principen för cacheminnet.</span><span class="sxs-lookup"><span data-stu-id="b7f7a-134">Configures the eviction policy for the cache.</span></span>
<span data-ttu-id="b7f7a-135">Alla pris nivåer.</span><span class="sxs-lookup"><span data-stu-id="b7f7a-135">All pricing tiers.</span></span> 
- <span data-ttu-id="b7f7a-136">meddelande – inloggnings händelser.</span><span class="sxs-lookup"><span data-stu-id="b7f7a-136">notify-keyspace-events.</span></span>
<span data-ttu-id="b7f7a-137">Konfigurerar indikeringar för meddelanden.</span><span class="sxs-lookup"><span data-stu-id="b7f7a-137">Configures keyspace notifications.</span></span>
<span data-ttu-id="b7f7a-138">Standard-och Premium-nivåer.</span><span class="sxs-lookup"><span data-stu-id="b7f7a-138">Standard and premium tiers.</span></span> 
- <span data-ttu-id="b7f7a-139">hash-Max-ziplist-poster.</span><span class="sxs-lookup"><span data-stu-id="b7f7a-139">hash-max-ziplist-entries.</span></span>
<span data-ttu-id="b7f7a-140">Konfigurerar minnes optimering för små aggregerade data typer.</span><span class="sxs-lookup"><span data-stu-id="b7f7a-140">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="b7f7a-141">Standard-och Premium-nivåer.</span><span class="sxs-lookup"><span data-stu-id="b7f7a-141">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="b7f7a-142">hash-Max-ziplist-värde.</span><span class="sxs-lookup"><span data-stu-id="b7f7a-142">hash-max-ziplist-value.</span></span>
<span data-ttu-id="b7f7a-143">Konfigurerar minnes optimering för små aggregerade data typer.</span><span class="sxs-lookup"><span data-stu-id="b7f7a-143">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="b7f7a-144">Standard-och Premium-nivåer.</span><span class="sxs-lookup"><span data-stu-id="b7f7a-144">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="b7f7a-145">set-Max intset-poster.</span><span class="sxs-lookup"><span data-stu-id="b7f7a-145">set-max-intset-entries.</span></span>
<span data-ttu-id="b7f7a-146">Konfigurerar minnes optimering för små aggregerade data typer.</span><span class="sxs-lookup"><span data-stu-id="b7f7a-146">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="b7f7a-147">Standard-och Premium-nivåer.</span><span class="sxs-lookup"><span data-stu-id="b7f7a-147">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="b7f7a-148">zset-Max ziplist-poster.</span><span class="sxs-lookup"><span data-stu-id="b7f7a-148">zset-max-ziplist-entries.</span></span>
<span data-ttu-id="b7f7a-149">Konfigurerar minnes optimering för små aggregerade data typer.</span><span class="sxs-lookup"><span data-stu-id="b7f7a-149">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="b7f7a-150">Standard-och Premium-nivåer.</span><span class="sxs-lookup"><span data-stu-id="b7f7a-150">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="b7f7a-151">zset-Max-ziplist-värde.</span><span class="sxs-lookup"><span data-stu-id="b7f7a-151">zset-max-ziplist-value.</span></span>
<span data-ttu-id="b7f7a-152">Konfigurerar minnes optimering för små aggregerade data typer.</span><span class="sxs-lookup"><span data-stu-id="b7f7a-152">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="b7f7a-153">Standard-och Premium-nivåer.</span><span class="sxs-lookup"><span data-stu-id="b7f7a-153">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="b7f7a-154">samling.</span><span class="sxs-lookup"><span data-stu-id="b7f7a-154">databases.</span></span>
<span data-ttu-id="b7f7a-155">Konfigurerar antalet databaser.</span><span class="sxs-lookup"><span data-stu-id="b7f7a-155">Configures the number of databases.</span></span>
<span data-ttu-id="b7f7a-156">Det går bara att konfigurera den här egenskapen när cacheminnet skapas.</span><span class="sxs-lookup"><span data-stu-id="b7f7a-156">This property can be configured only at cache creation.</span></span>
<span data-ttu-id="b7f7a-157">Standard-och Premium-nivåer.</span><span class="sxs-lookup"><span data-stu-id="b7f7a-157">Standard and Premium tiers.</span></span>
<span data-ttu-id="b7f7a-158">Mer information finns i Hantera Azure Redis cache med Azure PowerShell https://go.microsoft.com/fwlink/?LinkId=800051 ( https://go.microsoft.com/fwlink/?LinkId=800051) .</span><span class="sxs-lookup"><span data-stu-id="b7f7a-158">For more information, see Manage Azure Redis Cache with Azure PowerShellhttps://go.microsoft.com/fwlink/?LinkId=800051 (https://go.microsoft.com/fwlink/?LinkId=800051).</span></span>

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

### <span data-ttu-id="b7f7a-159">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7f7a-159">-ResourceGroupName</span></span>
<span data-ttu-id="b7f7a-160">Anger namnet på den resurs grupp som innehåller Redis-cachen.</span><span class="sxs-lookup"><span data-stu-id="b7f7a-160">Specifies the name of the resource group that contains the Redis Cache.</span></span>

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

### <span data-ttu-id="b7f7a-161">-ShardCount</span><span class="sxs-lookup"><span data-stu-id="b7f7a-161">-ShardCount</span></span>
<span data-ttu-id="b7f7a-162">Anger antalet Shards som ska skapas i ett Premium-kluster-cacheminne.</span><span class="sxs-lookup"><span data-stu-id="b7f7a-162">Specifies the number of shards to create on a Premium cluster cache.</span></span>

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

### <span data-ttu-id="b7f7a-163">-Storlek</span><span class="sxs-lookup"><span data-stu-id="b7f7a-163">-Size</span></span>
<span data-ttu-id="b7f7a-164">Anger storleken på Redis cache.</span><span class="sxs-lookup"><span data-stu-id="b7f7a-164">Specifies the size of the Redis Cache.</span></span>
<span data-ttu-id="b7f7a-165">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="b7f7a-165">Valid values are:</span></span> 
- <span data-ttu-id="b7f7a-166">P1</span><span class="sxs-lookup"><span data-stu-id="b7f7a-166">P1</span></span>
- <span data-ttu-id="b7f7a-167">P2</span><span class="sxs-lookup"><span data-stu-id="b7f7a-167">P2</span></span>
- <span data-ttu-id="b7f7a-168">P3</span><span class="sxs-lookup"><span data-stu-id="b7f7a-168">P3</span></span>
- <span data-ttu-id="b7f7a-169">P4</span><span class="sxs-lookup"><span data-stu-id="b7f7a-169">P4</span></span>
- <span data-ttu-id="b7f7a-170">C0</span><span class="sxs-lookup"><span data-stu-id="b7f7a-170">C0</span></span>
- <span data-ttu-id="b7f7a-171">C1</span><span class="sxs-lookup"><span data-stu-id="b7f7a-171">C1</span></span>
- <span data-ttu-id="b7f7a-172">C2</span><span class="sxs-lookup"><span data-stu-id="b7f7a-172">C2</span></span>
- <span data-ttu-id="b7f7a-173">C3</span><span class="sxs-lookup"><span data-stu-id="b7f7a-173">C3</span></span>
- <span data-ttu-id="b7f7a-174">C4</span><span class="sxs-lookup"><span data-stu-id="b7f7a-174">C4</span></span>
- <span data-ttu-id="b7f7a-175">C5</span><span class="sxs-lookup"><span data-stu-id="b7f7a-175">C5</span></span>
- <span data-ttu-id="b7f7a-176">C6</span><span class="sxs-lookup"><span data-stu-id="b7f7a-176">C6</span></span>
- <span data-ttu-id="b7f7a-177">250</span><span class="sxs-lookup"><span data-stu-id="b7f7a-177">250MB</span></span>
- <span data-ttu-id="b7f7a-178">MINNE</span><span class="sxs-lookup"><span data-stu-id="b7f7a-178">1GB</span></span>
- <span data-ttu-id="b7f7a-179">2,5 GB</span><span class="sxs-lookup"><span data-stu-id="b7f7a-179">2.5GB</span></span>
- <span data-ttu-id="b7f7a-180">6GB</span><span class="sxs-lookup"><span data-stu-id="b7f7a-180">6GB</span></span>
- <span data-ttu-id="b7f7a-181">13GB</span><span class="sxs-lookup"><span data-stu-id="b7f7a-181">13GB</span></span>
- <span data-ttu-id="b7f7a-182">26GB</span><span class="sxs-lookup"><span data-stu-id="b7f7a-182">26GB</span></span>
- <span data-ttu-id="b7f7a-183">53GB standardvärdet är 1 GB eller C1.</span><span class="sxs-lookup"><span data-stu-id="b7f7a-183">53GB The default value is 1GB or C1.</span></span>

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

### <span data-ttu-id="b7f7a-184">-SKU</span><span class="sxs-lookup"><span data-stu-id="b7f7a-184">-Sku</span></span>
<span data-ttu-id="b7f7a-185">Anger SKU för det Redis-cacheminne som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="b7f7a-185">Specifies the SKU of the Redis Cache to create.</span></span>
<span data-ttu-id="b7f7a-186">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="b7f7a-186">Valid values are:</span></span> 
- <span data-ttu-id="b7f7a-187">Basisk</span><span class="sxs-lookup"><span data-stu-id="b7f7a-187">Basic</span></span>
- <span data-ttu-id="b7f7a-188">Standar</span><span class="sxs-lookup"><span data-stu-id="b7f7a-188">Standard</span></span>
- <span data-ttu-id="b7f7a-189">Premium är standardvärdet standard.</span><span class="sxs-lookup"><span data-stu-id="b7f7a-189">Premium The default value is Standard.</span></span>

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

### <span data-ttu-id="b7f7a-190">-Tagg</span><span class="sxs-lookup"><span data-stu-id="b7f7a-190">-Tag</span></span>
<span data-ttu-id="b7f7a-191">En hash-tabell som representerar taggar.</span><span class="sxs-lookup"><span data-stu-id="b7f7a-191">A hash table which represents tags.</span></span>

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

### <span data-ttu-id="b7f7a-192">-TenantSettings</span><span class="sxs-lookup"><span data-stu-id="b7f7a-192">-TenantSettings</span></span>
<span data-ttu-id="b7f7a-193">Denna parameter är inaktuell.</span><span class="sxs-lookup"><span data-stu-id="b7f7a-193">This parameter has been deprecated.</span></span>

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

### <span data-ttu-id="b7f7a-194">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b7f7a-194">-Confirm</span></span>
<span data-ttu-id="b7f7a-195">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b7f7a-195">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b7f7a-196">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b7f7a-196">-WhatIf</span></span>
<span data-ttu-id="b7f7a-197">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b7f7a-197">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b7f7a-198">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b7f7a-198">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b7f7a-199">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7f7a-199">CommonParameters</span></span>
<span data-ttu-id="b7f7a-200">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b7f7a-200">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7f7a-201">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b7f7a-201">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7f7a-202">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b7f7a-202">INPUTS</span></span>

### <span data-ttu-id="b7f7a-203">System. String</span><span class="sxs-lookup"><span data-stu-id="b7f7a-203">System.String</span></span>

### <span data-ttu-id="b7f7a-204">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="b7f7a-204">System.Collections.Hashtable</span></span>

### <span data-ttu-id="b7f7a-205">System. Nullable ' 1 [[system. Boolean, mscorlib, version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="b7f7a-205">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="b7f7a-206">System. Nullable ' 1 [[system. Int32, mscorlib, version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="b7f7a-206">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="b7f7a-207">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b7f7a-207">OUTPUTS</span></span>

### <span data-ttu-id="b7f7a-208">Microsoft. Azure. commands. RedisCache. Models. RedisCacheAttributesWithAccessKeys</span><span class="sxs-lookup"><span data-stu-id="b7f7a-208">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributesWithAccessKeys</span></span>

## <span data-ttu-id="b7f7a-209">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b7f7a-209">NOTES</span></span>

## <span data-ttu-id="b7f7a-210">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b7f7a-210">RELATED LINKS</span></span>

[<span data-ttu-id="b7f7a-211">Get-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="b7f7a-211">Get-AzureRmRedisCache</span></span>](./Get-AzureRmRedisCache.md)

[<span data-ttu-id="b7f7a-212">New-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="b7f7a-212">New-AzureRmRedisCache</span></span>](./New-AzureRmRedisCache.md)

[<span data-ttu-id="b7f7a-213">Remove-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="b7f7a-213">Remove-AzureRmRedisCache</span></span>](./Remove-AzureRmRedisCache.md)


