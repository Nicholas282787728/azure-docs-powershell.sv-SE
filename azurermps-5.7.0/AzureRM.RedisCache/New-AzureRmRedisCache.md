---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: 81179AFE-6524-4F59-8BC2-3E152F51D1DD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/new-azurermrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCache.md
ms.openlocfilehash: bbba6372be7176b8ac1aec553a9abbbf83c7da31
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575553"
---
# <span data-ttu-id="0c660-101">New-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="0c660-101">New-AzureRmRedisCache</span></span>

## <span data-ttu-id="0c660-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0c660-102">SYNOPSIS</span></span>
<span data-ttu-id="0c660-103">Skapar en Redis cache.</span><span class="sxs-lookup"><span data-stu-id="0c660-103">Creates a Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0c660-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0c660-104">SYNTAX</span></span>

```
New-AzureRmRedisCache -ResourceGroupName <String> -Name <String> -Location <String> [-RedisVersion <String>]
 [-Size <String>] [-Sku <String>] [-MaxMemoryPolicy <String>] [-RedisConfiguration <Hashtable>]
 [-EnableNonSslPort <Boolean>] [-TenantSettings <Hashtable>] [-ShardCount <Int32>] [-VirtualNetwork <String>]
 [-Subnet <String>] [-SubnetId <String>] [-StaticIP <String>] [-Tag <Hashtable>] [-Zone <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0c660-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0c660-105">DESCRIPTION</span></span>
<span data-ttu-id="0c660-106">Cmdleten **New-AzureRmRedisCache** skapar ett Azure Redis-cacheminne.</span><span class="sxs-lookup"><span data-stu-id="0c660-106">The **New-AzureRmRedisCache** cmdlet creates an Azure Redis Cache.</span></span>

## <span data-ttu-id="0c660-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0c660-107">EXAMPLES</span></span>

### <span data-ttu-id="0c660-108">Exempel 1: skapa en Redis-cache</span><span class="sxs-lookup"><span data-stu-id="0c660-108">Example 1: Create a Redis Cache</span></span>
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
          Tag                : {}
          Zone               : []
```

<span data-ttu-id="0c660-109">Det här kommandot skapar en Redis cache.</span><span class="sxs-lookup"><span data-stu-id="0c660-109">This command creates a Redis Cache.</span></span>

### <span data-ttu-id="0c660-110">Exempel 2: skapa en standard-SKU Redis cache</span><span class="sxs-lookup"><span data-stu-id="0c660-110">Example 2: Create a Standard SKU Redis Cache</span></span>
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
          Tag                : {}
          Zone               : []
```

<span data-ttu-id="0c660-111">Det här kommandot skapar en Redis cache.</span><span class="sxs-lookup"><span data-stu-id="0c660-111">This command creates a Redis Cache.</span></span>

## <span data-ttu-id="0c660-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0c660-112">PARAMETERS</span></span>

### <span data-ttu-id="0c660-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c660-113">-DefaultProfile</span></span>
<span data-ttu-id="0c660-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0c660-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0c660-115">-EnableNonSslPort</span><span class="sxs-lookup"><span data-stu-id="0c660-115">-EnableNonSslPort</span></span>
<span data-ttu-id="0c660-116">Anger om icke-SSL-porten är aktive rad.</span><span class="sxs-lookup"><span data-stu-id="0c660-116">Indicates whether the non-SSL port is enabled.</span></span>
<span data-ttu-id="0c660-117">Standardvärdet är $False (icke-SSL-porten är inaktive rad).</span><span class="sxs-lookup"><span data-stu-id="0c660-117">The default value is $False (the non-SSL port is disabled).</span></span>

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

### <span data-ttu-id="0c660-118">-Plats</span><span class="sxs-lookup"><span data-stu-id="0c660-118">-Location</span></span>
<span data-ttu-id="0c660-119">Anger den plats där du vill skapa en Redis cache.</span><span class="sxs-lookup"><span data-stu-id="0c660-119">Specifies the location in which to create a Redis Cache.</span></span>
<span data-ttu-id="0c660-120">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="0c660-120">Valid values are:</span></span> 

- <span data-ttu-id="0c660-121">Norra Central USA</span><span class="sxs-lookup"><span data-stu-id="0c660-121">North Central US</span></span>
- <span data-ttu-id="0c660-122">Södra centrala USA</span><span class="sxs-lookup"><span data-stu-id="0c660-122">South Central US</span></span>
- <span data-ttu-id="0c660-123">Central</span><span class="sxs-lookup"><span data-stu-id="0c660-123">Central US</span></span>
- <span data-ttu-id="0c660-124">Västeuropa</span><span class="sxs-lookup"><span data-stu-id="0c660-124">West Europe</span></span>
- <span data-ttu-id="0c660-125">Nord Europa</span><span class="sxs-lookup"><span data-stu-id="0c660-125">North Europe</span></span>
- <span data-ttu-id="0c660-126">Västra USA</span><span class="sxs-lookup"><span data-stu-id="0c660-126">West US</span></span>
- <span data-ttu-id="0c660-127">Östra USA</span><span class="sxs-lookup"><span data-stu-id="0c660-127">East US</span></span>
- <span data-ttu-id="0c660-128">Östra USA 2</span><span class="sxs-lookup"><span data-stu-id="0c660-128">East US 2</span></span>
- <span data-ttu-id="0c660-129">Östra Japan</span><span class="sxs-lookup"><span data-stu-id="0c660-129">Japan East</span></span>
- <span data-ttu-id="0c660-130">Västra Japan</span><span class="sxs-lookup"><span data-stu-id="0c660-130">Japan West</span></span>
- <span data-ttu-id="0c660-131">Brasilien, Syd</span><span class="sxs-lookup"><span data-stu-id="0c660-131">Brazil South</span></span>
- <span data-ttu-id="0c660-132">Sydostasien</span><span class="sxs-lookup"><span data-stu-id="0c660-132">Southeast Asia</span></span>
- <span data-ttu-id="0c660-133">Östasien</span><span class="sxs-lookup"><span data-stu-id="0c660-133">East Asia</span></span>
- <span data-ttu-id="0c660-134">Östra Australien</span><span class="sxs-lookup"><span data-stu-id="0c660-134">Australia East</span></span>
- <span data-ttu-id="0c660-135">Australien, sydöst</span><span class="sxs-lookup"><span data-stu-id="0c660-135">Australia Southeast</span></span>

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

### <span data-ttu-id="0c660-136">-MaxMemoryPolicy</span><span class="sxs-lookup"><span data-stu-id="0c660-136">-MaxMemoryPolicy</span></span>
<span data-ttu-id="0c660-137">Denna parameter är inaktuell.</span><span class="sxs-lookup"><span data-stu-id="0c660-137">This parameter has been deprecated.</span></span>
<span data-ttu-id="0c660-138">Använd parametern *RedisConfiguration* för att ange maxmemory policy.</span><span class="sxs-lookup"><span data-stu-id="0c660-138">Use the *RedisConfiguration* parameter to set maxmemory-policy.</span></span>
<span data-ttu-id="0c660-139">Till exempel:</span><span class="sxs-lookup"><span data-stu-id="0c660-139">For example:</span></span> 

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

### <span data-ttu-id="0c660-140">-Namn</span><span class="sxs-lookup"><span data-stu-id="0c660-140">-Name</span></span>
<span data-ttu-id="0c660-141">Anger namnet på den Redis-cache som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="0c660-141">Specifies the name of the Redis Cache to create.</span></span>

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

### <span data-ttu-id="0c660-142">-RedisConfiguration</span><span class="sxs-lookup"><span data-stu-id="0c660-142">-RedisConfiguration</span></span>
<span data-ttu-id="0c660-143">Anger konfigurations inställningar för Redis.</span><span class="sxs-lookup"><span data-stu-id="0c660-143">Specifies Redis configuration settings.</span></span>
<span data-ttu-id="0c660-144">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="0c660-144">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="0c660-145">RDB – säkerhets kopiering aktive rad.</span><span class="sxs-lookup"><span data-stu-id="0c660-145">rdb-backup-enabled.</span></span>
<span data-ttu-id="0c660-146">Anger att Redis data persistence är aktiverat.</span><span class="sxs-lookup"><span data-stu-id="0c660-146">Specifies that Redis data persistence is enabled.</span></span>
<span data-ttu-id="0c660-147">Endast Premium-nivå.</span><span class="sxs-lookup"><span data-stu-id="0c660-147">Premium tier only.</span></span>
- <span data-ttu-id="0c660-148">RDB-lagring-anslutning-sträng.</span><span class="sxs-lookup"><span data-stu-id="0c660-148">rdb-storage-connection-string.</span></span>
<span data-ttu-id="0c660-149">Anger anslutnings strängen till lagrings konto för Redis data.</span><span class="sxs-lookup"><span data-stu-id="0c660-149">Specifies the connection string to the Storage account for Redis data persistence.</span></span>
<span data-ttu-id="0c660-150">Endast Premium-nivå.</span><span class="sxs-lookup"><span data-stu-id="0c660-150">Premium tier only.</span></span>
- <span data-ttu-id="0c660-151">RDB-säkerhets kopiering-frekvens.</span><span class="sxs-lookup"><span data-stu-id="0c660-151">rdb-backup-frequency.</span></span>
<span data-ttu-id="0c660-152">Anger säkerhets kopierings frekvensen för Redis data.</span><span class="sxs-lookup"><span data-stu-id="0c660-152">Specifies the backup frequency for Redis data persistence.</span></span>
<span data-ttu-id="0c660-153">Endast Premium-nivå.</span><span class="sxs-lookup"><span data-stu-id="0c660-153">Premium tier only.</span></span> 
- <span data-ttu-id="0c660-154">maxmemory-reserverad.</span><span class="sxs-lookup"><span data-stu-id="0c660-154">maxmemory-reserved.</span></span>
<span data-ttu-id="0c660-155">Konfigurerar minnet reserverat för icke-cachelagrade processer.</span><span class="sxs-lookup"><span data-stu-id="0c660-155">Configures the memory reserved for non-cache processes.</span></span>
<span data-ttu-id="0c660-156">Standard-och Premium-nivåer.</span><span class="sxs-lookup"><span data-stu-id="0c660-156">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="0c660-157">maxmemory-policy.</span><span class="sxs-lookup"><span data-stu-id="0c660-157">maxmemory-policy.</span></span>
<span data-ttu-id="0c660-158">Konfigurerar borttagnings principen för cacheminnet.</span><span class="sxs-lookup"><span data-stu-id="0c660-158">Configures the eviction policy for the cache.</span></span>
<span data-ttu-id="0c660-159">Alla pris nivåer.</span><span class="sxs-lookup"><span data-stu-id="0c660-159">All pricing tiers.</span></span> 
- <span data-ttu-id="0c660-160">meddelande – inloggnings händelser.</span><span class="sxs-lookup"><span data-stu-id="0c660-160">notify-keyspace-events.</span></span>
<span data-ttu-id="0c660-161">Konfigurerar indikeringar för meddelanden.</span><span class="sxs-lookup"><span data-stu-id="0c660-161">Configures keyspace notifications.</span></span>
<span data-ttu-id="0c660-162">Standard-och Premium-nivåer.</span><span class="sxs-lookup"><span data-stu-id="0c660-162">Standard and premium tiers.</span></span> 
- <span data-ttu-id="0c660-163">hash-Max-ziplist-poster.</span><span class="sxs-lookup"><span data-stu-id="0c660-163">hash-max-ziplist-entries.</span></span>
<span data-ttu-id="0c660-164">Konfigurerar minnes optimering för små aggregerade data typer.</span><span class="sxs-lookup"><span data-stu-id="0c660-164">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="0c660-165">Standard-och Premium-nivåer.</span><span class="sxs-lookup"><span data-stu-id="0c660-165">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="0c660-166">hash-Max-ziplist-värde.</span><span class="sxs-lookup"><span data-stu-id="0c660-166">hash-max-ziplist-value.</span></span>
<span data-ttu-id="0c660-167">Konfigurerar minnes optimering för små aggregerade data typer.</span><span class="sxs-lookup"><span data-stu-id="0c660-167">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="0c660-168">Standard-och Premium-nivåer.</span><span class="sxs-lookup"><span data-stu-id="0c660-168">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="0c660-169">set-Max intset-poster.</span><span class="sxs-lookup"><span data-stu-id="0c660-169">set-max-intset-entries.</span></span>
<span data-ttu-id="0c660-170">Konfigurerar minnes optimering för små aggregerade data typer.</span><span class="sxs-lookup"><span data-stu-id="0c660-170">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="0c660-171">Standard-och Premium-nivåer.</span><span class="sxs-lookup"><span data-stu-id="0c660-171">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="0c660-172">zset-Max ziplist-poster.</span><span class="sxs-lookup"><span data-stu-id="0c660-172">zset-max-ziplist-entries.</span></span>
<span data-ttu-id="0c660-173">Konfigurerar minnes optimering för små aggregerade data typer.</span><span class="sxs-lookup"><span data-stu-id="0c660-173">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="0c660-174">Standard-och Premium-nivåer.</span><span class="sxs-lookup"><span data-stu-id="0c660-174">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="0c660-175">zset-Max-ziplist-värde.</span><span class="sxs-lookup"><span data-stu-id="0c660-175">zset-max-ziplist-value.</span></span>
<span data-ttu-id="0c660-176">Konfigurerar minnes optimering för små aggregerade data typer.</span><span class="sxs-lookup"><span data-stu-id="0c660-176">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="0c660-177">Standard-och Premium-nivåer.</span><span class="sxs-lookup"><span data-stu-id="0c660-177">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="0c660-178">samling.</span><span class="sxs-lookup"><span data-stu-id="0c660-178">databases.</span></span>
<span data-ttu-id="0c660-179">Konfigurerar antalet databaser.</span><span class="sxs-lookup"><span data-stu-id="0c660-179">Configures the number of databases.</span></span>
<span data-ttu-id="0c660-180">Det går bara att konfigurera den här egenskapen när cacheminnet skapas.</span><span class="sxs-lookup"><span data-stu-id="0c660-180">This property can be configured only at cache creation.</span></span>
<span data-ttu-id="0c660-181">Standard-och Premium-nivåer.</span><span class="sxs-lookup"><span data-stu-id="0c660-181">Standard and Premium tiers.</span></span>

<span data-ttu-id="0c660-182">Mer information finns i Hantera Azure Redis cache med Azure PowerShell https://go.microsoft.com/fwlink/?LinkId=800051 ( https://go.microsoft.com/fwlink/?LinkId=800051) .</span><span class="sxs-lookup"><span data-stu-id="0c660-182">For more information, see Manage Azure Redis Cache with Azure PowerShellhttps://go.microsoft.com/fwlink/?LinkId=800051 (https://go.microsoft.com/fwlink/?LinkId=800051).</span></span>

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

### <span data-ttu-id="0c660-183">-RedisVersion</span><span class="sxs-lookup"><span data-stu-id="0c660-183">-RedisVersion</span></span>
<span data-ttu-id="0c660-184">Denna parameter är föråldrad och kommer att tas bort från framtida versioner.</span><span class="sxs-lookup"><span data-stu-id="0c660-184">This parameter is deprecated and will be removed from future releases.</span></span>

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

### <span data-ttu-id="0c660-185">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0c660-185">-ResourceGroupName</span></span>
<span data-ttu-id="0c660-186">Anger namnet på den resurs grupp där Redis cache ska skapas.</span><span class="sxs-lookup"><span data-stu-id="0c660-186">Specifies the name of the resource group in which to create the Redis Cache.</span></span>

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

### <span data-ttu-id="0c660-187">-ShardCount</span><span class="sxs-lookup"><span data-stu-id="0c660-187">-ShardCount</span></span>
<span data-ttu-id="0c660-188">Anger antalet Shards som ska skapas i ett Premium-kluster-cacheminne.</span><span class="sxs-lookup"><span data-stu-id="0c660-188">Specifies the number of shards to create on a Premium cluster cache.</span></span>
<span data-ttu-id="0c660-189">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="0c660-189">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="0c660-190">9.1</span><span class="sxs-lookup"><span data-stu-id="0c660-190">1</span></span>
- <span data-ttu-id="0c660-191">två</span><span class="sxs-lookup"><span data-stu-id="0c660-191">2</span></span>
- <span data-ttu-id="0c660-192">amp;3D</span><span class="sxs-lookup"><span data-stu-id="0c660-192">3</span></span>
- <span data-ttu-id="0c660-193">9.4</span><span class="sxs-lookup"><span data-stu-id="0c660-193">4</span></span>
- <span data-ttu-id="0c660-194">T5</span><span class="sxs-lookup"><span data-stu-id="0c660-194">5</span></span>
- <span data-ttu-id="0c660-195">18.6</span><span class="sxs-lookup"><span data-stu-id="0c660-195">6</span></span>
- <span data-ttu-id="0c660-196">borttagning</span><span class="sxs-lookup"><span data-stu-id="0c660-196">7</span></span>
- <span data-ttu-id="0c660-197">8.2</span><span class="sxs-lookup"><span data-stu-id="0c660-197">8</span></span>
- <span data-ttu-id="0c660-198">9</span><span class="sxs-lookup"><span data-stu-id="0c660-198">9</span></span> 
- <span data-ttu-id="0c660-199">10.3</span><span class="sxs-lookup"><span data-stu-id="0c660-199">10</span></span>

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

### <span data-ttu-id="0c660-200">-Storlek</span><span class="sxs-lookup"><span data-stu-id="0c660-200">-Size</span></span>
<span data-ttu-id="0c660-201">Anger storleken på Redis cache.</span><span class="sxs-lookup"><span data-stu-id="0c660-201">Specifies the size of the Redis Cache.</span></span>
<span data-ttu-id="0c660-202">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="0c660-202">Valid values are:</span></span> 

- <span data-ttu-id="0c660-203">P1</span><span class="sxs-lookup"><span data-stu-id="0c660-203">P1</span></span>
- <span data-ttu-id="0c660-204">P2</span><span class="sxs-lookup"><span data-stu-id="0c660-204">P2</span></span>
- <span data-ttu-id="0c660-205">P3</span><span class="sxs-lookup"><span data-stu-id="0c660-205">P3</span></span>
- <span data-ttu-id="0c660-206">P4</span><span class="sxs-lookup"><span data-stu-id="0c660-206">P4</span></span>
- <span data-ttu-id="0c660-207">C0</span><span class="sxs-lookup"><span data-stu-id="0c660-207">C0</span></span>
- <span data-ttu-id="0c660-208">C1</span><span class="sxs-lookup"><span data-stu-id="0c660-208">C1</span></span>
- <span data-ttu-id="0c660-209">C2</span><span class="sxs-lookup"><span data-stu-id="0c660-209">C2</span></span>
- <span data-ttu-id="0c660-210">C3</span><span class="sxs-lookup"><span data-stu-id="0c660-210">C3</span></span>
- <span data-ttu-id="0c660-211">C4</span><span class="sxs-lookup"><span data-stu-id="0c660-211">C4</span></span>
- <span data-ttu-id="0c660-212">C5</span><span class="sxs-lookup"><span data-stu-id="0c660-212">C5</span></span>
- <span data-ttu-id="0c660-213">C6</span><span class="sxs-lookup"><span data-stu-id="0c660-213">C6</span></span>
- <span data-ttu-id="0c660-214">250</span><span class="sxs-lookup"><span data-stu-id="0c660-214">250MB</span></span>
- <span data-ttu-id="0c660-215">MINNE</span><span class="sxs-lookup"><span data-stu-id="0c660-215">1GB</span></span>
- <span data-ttu-id="0c660-216">2,5 GB</span><span class="sxs-lookup"><span data-stu-id="0c660-216">2.5GB</span></span>
- <span data-ttu-id="0c660-217">6GB</span><span class="sxs-lookup"><span data-stu-id="0c660-217">6GB</span></span>
- <span data-ttu-id="0c660-218">13GB</span><span class="sxs-lookup"><span data-stu-id="0c660-218">13GB</span></span>
- <span data-ttu-id="0c660-219">26GB</span><span class="sxs-lookup"><span data-stu-id="0c660-219">26GB</span></span>
- <span data-ttu-id="0c660-220">53GB</span><span class="sxs-lookup"><span data-stu-id="0c660-220">53GB</span></span>

<span data-ttu-id="0c660-221">Standardvärdet är 1 GB eller C1.</span><span class="sxs-lookup"><span data-stu-id="0c660-221">The default value is 1GB or C1.</span></span>

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

### <span data-ttu-id="0c660-222">-SKU</span><span class="sxs-lookup"><span data-stu-id="0c660-222">-Sku</span></span>
<span data-ttu-id="0c660-223">Anger SKU för det Redis-cacheminne som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="0c660-223">Specifies the SKU of the Redis Cache to create.</span></span>
<span data-ttu-id="0c660-224">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="0c660-224">Valid values are:</span></span> 

- <span data-ttu-id="0c660-225">Basisk</span><span class="sxs-lookup"><span data-stu-id="0c660-225">Basic</span></span>
- <span data-ttu-id="0c660-226">Standar</span><span class="sxs-lookup"><span data-stu-id="0c660-226">Standard</span></span>
- <span data-ttu-id="0c660-227">Beta</span><span class="sxs-lookup"><span data-stu-id="0c660-227">Premium</span></span>

<span data-ttu-id="0c660-228">Standardvärdet är standard.</span><span class="sxs-lookup"><span data-stu-id="0c660-228">The default value is Standard.</span></span>

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

### <span data-ttu-id="0c660-229">-StaticIP</span><span class="sxs-lookup"><span data-stu-id="0c660-229">-StaticIP</span></span>
<span data-ttu-id="0c660-230">Anger en unik IP-adress i Redis-cachen.</span><span class="sxs-lookup"><span data-stu-id="0c660-230">Specifies a unique IP address in the subnet for the Redis Cache.</span></span>

<span data-ttu-id="0c660-231">Om du inte anger ett värde för den här parametern väljer denna cmdlet en IP-adress från under nätet.</span><span class="sxs-lookup"><span data-stu-id="0c660-231">If you do not specify a value for this parameter, this cmdlet chooses an IP address from the subnet.</span></span>

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

### <span data-ttu-id="0c660-232">-Undernät</span><span class="sxs-lookup"><span data-stu-id="0c660-232">-Subnet</span></span>
<span data-ttu-id="0c660-233">Anger namnet på det undernät där Redis-cachen ska distribueras.</span><span class="sxs-lookup"><span data-stu-id="0c660-233">Specifies the name of the subnet in which to deploy the Redis Cache.</span></span>

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

### <span data-ttu-id="0c660-234">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="0c660-234">-SubnetId</span></span>
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

### <span data-ttu-id="0c660-235">-Tagg</span><span class="sxs-lookup"><span data-stu-id="0c660-235">-Tag</span></span>
<span data-ttu-id="0c660-236">En hash-tabell som representerar taggar.</span><span class="sxs-lookup"><span data-stu-id="0c660-236">A hash table which represents tags.</span></span>

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

### <span data-ttu-id="0c660-237">-TenantSettings</span><span class="sxs-lookup"><span data-stu-id="0c660-237">-TenantSettings</span></span>
<span data-ttu-id="0c660-238">Denna parameter är inaktuell.</span><span class="sxs-lookup"><span data-stu-id="0c660-238">This parameter has been deprecated.</span></span>

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

### <span data-ttu-id="0c660-239">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="0c660-239">-VirtualNetwork</span></span>
<span data-ttu-id="0c660-240">Anger resurs-ID för det virtuella nätverk där Redis-cachen ska distribueras.</span><span class="sxs-lookup"><span data-stu-id="0c660-240">Specifies the resource ID of the virtual network in which to deploy the Redis Cache.</span></span>

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

### <span data-ttu-id="0c660-241">-Zone</span><span class="sxs-lookup"><span data-stu-id="0c660-241">-Zone</span></span>
<span data-ttu-id="0c660-242">Lista över zoner.</span><span class="sxs-lookup"><span data-stu-id="0c660-242">List of zones.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c660-243">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="0c660-243">-Confirm</span></span>
<span data-ttu-id="0c660-244">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="0c660-244">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0c660-245">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0c660-245">-WhatIf</span></span>
<span data-ttu-id="0c660-246">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="0c660-246">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0c660-247">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="0c660-247">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0c660-248">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c660-248">CommonParameters</span></span>
<span data-ttu-id="0c660-249">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0c660-249">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c660-250">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0c660-250">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c660-251">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0c660-251">INPUTS</span></span>

### <span data-ttu-id="0c660-252">Ingen</span><span class="sxs-lookup"><span data-stu-id="0c660-252">None</span></span>
<span data-ttu-id="0c660-253">Du kan pipes in i denna cmdlet efter namn men inte efter värde.</span><span class="sxs-lookup"><span data-stu-id="0c660-253">You can pipe input to this cmdlet by name, but not by value.</span></span>

## <span data-ttu-id="0c660-254">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0c660-254">OUTPUTS</span></span>

### <span data-ttu-id="0c660-255">Microsoft. Azure. commands. RedisCache. Models. RedisCacheAttributesWithAccessKeys</span><span class="sxs-lookup"><span data-stu-id="0c660-255">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributesWithAccessKeys</span></span>
<span data-ttu-id="0c660-256">Denna cmdlet returnerar alla attribut i en Redis-cache inklusive primära och sekundära åtkomst nycklar.</span><span class="sxs-lookup"><span data-stu-id="0c660-256">This cmdlet returns all attributes of a Redis Cache including primary and secondary access keys.</span></span>

## <span data-ttu-id="0c660-257">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0c660-257">NOTES</span></span>

## <span data-ttu-id="0c660-258">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0c660-258">RELATED LINKS</span></span>

[<span data-ttu-id="0c660-259">Get-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="0c660-259">Get-AzureRmRedisCache</span></span>](./Get-AzureRmRedisCache.md)

[<span data-ttu-id="0c660-260">Remove-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="0c660-260">Remove-AzureRmRedisCache</span></span>](./Remove-AzureRmRedisCache.md)

[<span data-ttu-id="0c660-261">Set-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="0c660-261">Set-AzureRmRedisCache</span></span>](./Set-AzureRmRedisCache.md)


