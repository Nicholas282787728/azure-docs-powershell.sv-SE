---
external help file: ''
Module Name: Az.RedisEnterpriseCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.redisenterprisecache/new-azredisenterprisecache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/New-AzRedisEnterpriseCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/New-AzRedisEnterpriseCache.md
ms.openlocfilehash: f2f996bc212772b3b44202796e270ec345898a11
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98421192"
---
# <span data-ttu-id="59a12-101">New-AzRedisEnterpriseCache</span><span class="sxs-lookup"><span data-stu-id="59a12-101">New-AzRedisEnterpriseCache</span></span>

## <span data-ttu-id="59a12-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="59a12-102">SYNOPSIS</span></span>
<span data-ttu-id="59a12-103">Skapar ett Redis Enterpise-kluster och en associerad databas</span><span class="sxs-lookup"><span data-stu-id="59a12-103">Creates a Redis Enterpise cache cluster and an associated database</span></span>

## <span data-ttu-id="59a12-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="59a12-104">SYNTAX</span></span>

```
New-AzRedisEnterpriseCache -ClusterName <String> -ResourceGroupName <String> -Location <String> -Sku <SkuName>
 [-SubscriptionId <String>] [-Capacity <Int32>] [-ClientProtocol <Protocol>]
 [-ClusteringPolicy <ClusteringPolicy>] [-EvictionPolicy <EvictionPolicy>] [-MinimumTlsVersion <String>]
 [-Module <IModule[]>] [-Port <Int32>] [-Tag <Hashtable>] [-Zone <String[]>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="59a12-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="59a12-105">DESCRIPTION</span></span>
<span data-ttu-id="59a12-106">Skapar eller uppdaterar ett befintligt (överskrivnings-och återskapande, med möjligt nertid) cache-kluster och en associerad databas med namnet "standard"</span><span class="sxs-lookup"><span data-stu-id="59a12-106">Creates or updates an existing (overwrite/recreate, with potential downtime) cache cluster and an associated database named 'default'</span></span>

## <span data-ttu-id="59a12-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="59a12-107">EXAMPLES</span></span>

### <span data-ttu-id="59a12-108">Exempel 1: skapa en Redis företags-cache</span><span class="sxs-lookup"><span data-stu-id="59a12-108">Example 1: Create a Redis Enterprise Cache</span></span>
```powershell
PS C:\> New-AzRedisEnterpriseCache -Name "MyCache" -ResourceGroupName "MyGroup" -Location "West US" -Sku "Enterprise_E10"

Location Name    Type                            Zone Database
-------- ----    ----                            ---- --------
West US  MyCache Microsoft.Cache/redisEnterprise      {default}

```

<span data-ttu-id="59a12-109">Det här kommandot skapar en Redis företags-cache med namnetin cache.</span><span class="sxs-lookup"><span data-stu-id="59a12-109">This command creates a Redis Enterprise Cache named MyCache.</span></span>

### <span data-ttu-id="59a12-110">Exempel 2: skapa en Redis företags-cache med några valfria parametrar</span><span class="sxs-lookup"><span data-stu-id="59a12-110">Example 2: Create a Redis Enterprise Cache using some optional parameters</span></span>
```powershell
PS C:\> New-AzRedisEnterpriseCache -Name "MyCache" -ResourceGroupName "MyGroup" -Location "East US" -Sku "Enterprise_E20" -Capacity 4 -Zone "1","2","3" -Module "{name:RedisBloom, args:`"ERROR_RATE 0.00 INITIAL_SIZE 400`"}","{name:RedisTimeSeries, args:`"RETENTION_POLICY 20`"}","{name:RediSearch}" -ClientProtocol "Plaintext" -EvictionPolicy "NoEviction" -ClusteringPolicy "EnterpriseCluster" -Tag @{"tag" = "value"}

Location Name    Type                            Zone      Database
-------- ----    ----                            ----      --------
East US  MyCache Microsoft.Cache/redisEnterprise {1, 2, 3} {default}

```

<span data-ttu-id="59a12-111">Det här kommandot skapar en Redis företags-cache som heterin med vissa valfria parametrar.</span><span class="sxs-lookup"><span data-stu-id="59a12-111">This command creates a Redis Enterprise Cache named MyCache using some optional parameters.</span></span>

## <span data-ttu-id="59a12-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="59a12-112">PARAMETERS</span></span>

### <span data-ttu-id="59a12-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="59a12-113">-AsJob</span></span>
<span data-ttu-id="59a12-114">Köra kommandot som ett jobb</span><span class="sxs-lookup"><span data-stu-id="59a12-114">Run the command as a job</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59a12-115">-Kapacitet</span><span class="sxs-lookup"><span data-stu-id="59a12-115">-Capacity</span></span>
<span data-ttu-id="59a12-116">Storleken på RedisEnterprise-klustret.</span><span class="sxs-lookup"><span data-stu-id="59a12-116">The size of the RedisEnterprise cluster.</span></span>
<span data-ttu-id="59a12-117">Standardvärdet är 2 eller 3 beroende på SKU.</span><span class="sxs-lookup"><span data-stu-id="59a12-117">Defaults to 2 or 3 depending on SKU.</span></span>
<span data-ttu-id="59a12-118">Giltiga värden är (2, 4, 6,...) för företags lager enheter och (3, 9, 15,...) för Flash-SKU: er.</span><span class="sxs-lookup"><span data-stu-id="59a12-118">Valid values are (2, 4, 6, ...) for Enterprise SKUs and (3, 9, 15, ...) for Flash SKUs.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: SkuCapacity

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59a12-119">-ClientProtocol</span><span class="sxs-lookup"><span data-stu-id="59a12-119">-ClientProtocol</span></span>
<span data-ttu-id="59a12-120">Anger om Redis-klienter kan ansluta via TLS-krypterade eller Redis-protokoll.</span><span class="sxs-lookup"><span data-stu-id="59a12-120">Specifies whether redis clients can connect using TLS-encrypted or plaintext redis protocols.</span></span>
<span data-ttu-id="59a12-121">Standard är TLS-krypterat.</span><span class="sxs-lookup"><span data-stu-id="59a12-121">Default is TLS-encrypted.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Support.Protocol
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59a12-122">-ClusteringPolicy</span><span class="sxs-lookup"><span data-stu-id="59a12-122">-ClusteringPolicy</span></span>
<span data-ttu-id="59a12-123">Kluster princip-standard är OSSCluster.</span><span class="sxs-lookup"><span data-stu-id="59a12-123">Clustering policy - default is OSSCluster.</span></span>
<span data-ttu-id="59a12-124">Anges vid skapande tillfället.</span><span class="sxs-lookup"><span data-stu-id="59a12-124">Specified at create time.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Support.ClusteringPolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59a12-125">-Kluster namn</span><span class="sxs-lookup"><span data-stu-id="59a12-125">-ClusterName</span></span>
<span data-ttu-id="59a12-126">Namnet på RedisEnterprise-klustret.</span><span class="sxs-lookup"><span data-stu-id="59a12-126">The name of the RedisEnterprise cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59a12-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59a12-127">-DefaultProfile</span></span>
<span data-ttu-id="59a12-128">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="59a12-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59a12-129">-EvictionPolicy</span><span class="sxs-lookup"><span data-stu-id="59a12-129">-EvictionPolicy</span></span>
<span data-ttu-id="59a12-130">Redis-standard är VolatileLRU.</span><span class="sxs-lookup"><span data-stu-id="59a12-130">Redis eviction policy - default is VolatileLRU.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Support.EvictionPolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59a12-131">-Plats</span><span class="sxs-lookup"><span data-stu-id="59a12-131">-Location</span></span>
<span data-ttu-id="59a12-132">Den Geo-plats där resursen bor</span><span class="sxs-lookup"><span data-stu-id="59a12-132">The geo-location where the resource lives</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59a12-133">-MinimumTlsVersion</span><span class="sxs-lookup"><span data-stu-id="59a12-133">-MinimumTlsVersion</span></span>
<span data-ttu-id="59a12-134">Den minsta TLS-versionen för klustret som stöds, till exempel 1,2</span><span class="sxs-lookup"><span data-stu-id="59a12-134">The minimum TLS version for the cluster to support, e.g. 1.2</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59a12-135">-Modul</span><span class="sxs-lookup"><span data-stu-id="59a12-135">-Module</span></span>
<span data-ttu-id="59a12-136">Valfri uppsättning Redis-moduler som ska aktive ras i den här databasen – moduler kan bara läggas till när du skapar.</span><span class="sxs-lookup"><span data-stu-id="59a12-136">Optional set of redis modules to enable in this database - modules can only be added at creation time.</span></span>
<span data-ttu-id="59a12-137">För att konstruera kan du läsa avsnittet anteckningar för modul egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="59a12-137">To construct, see NOTES section for MODULE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.Api20201001Preview.IModule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59a12-138">-Nowait</span><span class="sxs-lookup"><span data-stu-id="59a12-138">-NoWait</span></span>
<span data-ttu-id="59a12-139">Kör kommandot asynkront</span><span class="sxs-lookup"><span data-stu-id="59a12-139">Run the command asynchronously</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59a12-140">-Port</span><span class="sxs-lookup"><span data-stu-id="59a12-140">-Port</span></span>
<span data-ttu-id="59a12-141">TCP-port för databasens slut punkt.</span><span class="sxs-lookup"><span data-stu-id="59a12-141">TCP port of the database endpoint.</span></span>
<span data-ttu-id="59a12-142">Anges vid skapande tillfället.</span><span class="sxs-lookup"><span data-stu-id="59a12-142">Specified at create time.</span></span>
<span data-ttu-id="59a12-143">Standard porten är tillgänglig.</span><span class="sxs-lookup"><span data-stu-id="59a12-143">Defaults to an available port.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59a12-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="59a12-144">-ResourceGroupName</span></span>
<span data-ttu-id="59a12-145">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="59a12-145">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59a12-146">-SKU</span><span class="sxs-lookup"><span data-stu-id="59a12-146">-Sku</span></span>
<span data-ttu-id="59a12-147">Den typ av RedisEnterprise-kluster som ska distribueras.</span><span class="sxs-lookup"><span data-stu-id="59a12-147">The type of RedisEnterprise cluster to deploy.</span></span>
<span data-ttu-id="59a12-148">Möjliga värden: (Enterprise_E10 EnterpriseFlash_F300 etc.)</span><span class="sxs-lookup"><span data-stu-id="59a12-148">Possible values: (Enterprise_E10, EnterpriseFlash_F300 etc.)</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Support.SkuName
Parameter Sets: (All)
Aliases: SkuName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59a12-149">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="59a12-149">-SubscriptionId</span></span>
<span data-ttu-id="59a12-150">Hämtar dina prenumerations uppgifter som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="59a12-150">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="59a12-151">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="59a12-151">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59a12-152">-Tagg</span><span class="sxs-lookup"><span data-stu-id="59a12-152">-Tag</span></span>
<span data-ttu-id="59a12-153">Resource-taggar.</span><span class="sxs-lookup"><span data-stu-id="59a12-153">Resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59a12-154">-Zone</span><span class="sxs-lookup"><span data-stu-id="59a12-154">-Zone</span></span>
<span data-ttu-id="59a12-155">Zonerna där klustret ska distribueras.</span><span class="sxs-lookup"><span data-stu-id="59a12-155">The zones where this cluster will be deployed.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59a12-156">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="59a12-156">-Confirm</span></span>
<span data-ttu-id="59a12-157">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="59a12-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="59a12-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="59a12-158">-WhatIf</span></span>
<span data-ttu-id="59a12-159">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="59a12-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="59a12-160">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="59a12-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="59a12-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59a12-161">CommonParameters</span></span>
<span data-ttu-id="59a12-162">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="59a12-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59a12-163">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="59a12-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59a12-164">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="59a12-164">INPUTS</span></span>

## <span data-ttu-id="59a12-165">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="59a12-165">OUTPUTS</span></span>

### <span data-ttu-id="59a12-166">Microsoft. Azure. PowerShell. cmdletar. RedisEnterpriseCache. Models. Api20201001Preview. ICluster</span><span class="sxs-lookup"><span data-stu-id="59a12-166">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.Api20201001Preview.ICluster</span></span>

## <span data-ttu-id="59a12-167">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="59a12-167">NOTES</span></span>

<span data-ttu-id="59a12-168">ALIAS</span><span class="sxs-lookup"><span data-stu-id="59a12-168">ALIASES</span></span>

<span data-ttu-id="59a12-169">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="59a12-169">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="59a12-170">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="59a12-170">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="59a12-171">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="59a12-171">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="59a12-172">MODUL <IModule [] >: valfri uppsättning Redis-moduler som ska aktive ras i den här databasen – moduler kan bara läggas till när du skapar.</span><span class="sxs-lookup"><span data-stu-id="59a12-172">MODULE <IModule[]>: Optional set of redis modules to enable in this database - modules can only be added at creation time.</span></span>
  - <span data-ttu-id="59a12-173">`Name <String>`: Namnet på modulen, till exempel "RedisBloom", "RediSearch", "RedisTimeSeries"</span><span class="sxs-lookup"><span data-stu-id="59a12-173">`Name <String>`: The name of the module, e.g. 'RedisBloom', 'RediSearch', 'RedisTimeSeries'</span></span>
  - <span data-ttu-id="59a12-174">`[Arg <String>]`: Konfigurations alternativ för modulen, till exempel "ERROR_RATE 0,00 INITIAL_SIZE 400".</span><span class="sxs-lookup"><span data-stu-id="59a12-174">`[Arg <String>]`: Configuration options for the module, e.g. 'ERROR_RATE 0.00 INITIAL_SIZE 400'.</span></span>

## <span data-ttu-id="59a12-175">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="59a12-175">RELATED LINKS</span></span>

