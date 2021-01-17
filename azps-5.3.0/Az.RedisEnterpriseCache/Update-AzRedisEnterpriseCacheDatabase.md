---
external help file: ''
Module Name: Az.RedisEnterpriseCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.redisenterprisecache/update-azredisenterprisecachedatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Update-AzRedisEnterpriseCacheDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Update-AzRedisEnterpriseCacheDatabase.md
ms.openlocfilehash: 9b41dbeaa10b77ed86567a51ec5fb106648e8ebd
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98421152"
---
# <span data-ttu-id="9e7ee-101">Update-AzRedisEnterpriseCacheDatabase</span><span class="sxs-lookup"><span data-stu-id="9e7ee-101">Update-AzRedisEnterpriseCacheDatabase</span></span>

## <span data-ttu-id="9e7ee-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9e7ee-102">SYNOPSIS</span></span>
<span data-ttu-id="9e7ee-103">Uppdaterar en databas</span><span class="sxs-lookup"><span data-stu-id="9e7ee-103">Updates a database</span></span>

## <span data-ttu-id="9e7ee-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9e7ee-104">SYNTAX</span></span>

### <span data-ttu-id="9e7ee-105">UpdateExpanded (standard)</span><span class="sxs-lookup"><span data-stu-id="9e7ee-105">UpdateExpanded (Default)</span></span>
```
Update-AzRedisEnterpriseCacheDatabase -ClusterName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-ClientProtocol <Protocol>] [-ClusteringPolicy <ClusteringPolicy>]
 [-EvictionPolicy <EvictionPolicy>] [-Module <IModule[]>] [-Port <Int32>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="9e7ee-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="9e7ee-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzRedisEnterpriseCacheDatabase -InputObject <IRedisEnterpriseCacheIdentity>
 [-ClientProtocol <Protocol>] [-ClusteringPolicy <ClusteringPolicy>] [-EvictionPolicy <EvictionPolicy>]
 [-Module <IModule[]>] [-Port <Int32>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="9e7ee-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9e7ee-107">DESCRIPTION</span></span>
<span data-ttu-id="9e7ee-108">Uppdaterar en databas</span><span class="sxs-lookup"><span data-stu-id="9e7ee-108">Updates a database</span></span>

## <span data-ttu-id="9e7ee-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9e7ee-109">EXAMPLES</span></span>

### <span data-ttu-id="9e7ee-110">Exempel 1: uppdatera klient protokoll</span><span class="sxs-lookup"><span data-stu-id="9e7ee-110">Example 1: Update client protocol</span></span>
```powershell
PS C:\> Update-AzRedisEnterpriseCacheDatabase -Name "MyCache" -ResourceGroupName "MyGroup" -ClientProtocol "Plaintext"

Name    Type
----    ----
default Microsoft.Cache/redisEnterprise/databases

```

<span data-ttu-id="9e7ee-111">Det här kommandot uppdaterar klient protokollet för databasen för Redis företags-cache med namnet mina cacheminne.</span><span class="sxs-lookup"><span data-stu-id="9e7ee-111">This command updates the client protocol of the database for the Redis Enterprise Cache named MyCache.</span></span>

### <span data-ttu-id="9e7ee-112">Exempel 2: uppdatera klient protokoll och avlägsning princip</span><span class="sxs-lookup"><span data-stu-id="9e7ee-112">Example 2: Update client protocol and eviction policy</span></span>
```powershell
PS C:\> Update-AzRedisEnterpriseCacheDatabase -Name "MyCache" -ResourceGroupName "MyGroup" -ClientProtocol "Encrypted" -EvictionPolicy "NoEviction"

Name    Type
----    ----
default Microsoft.Cache/redisEnterprise/databases

```

<span data-ttu-id="9e7ee-113">Det här kommandot uppdaterar klient protokoll och borttagnings princip för databasen för Redis företags-cache med namnet noncache.</span><span class="sxs-lookup"><span data-stu-id="9e7ee-113">This command updates the client protocol and eviction policy of the database for the Redis Enterprise Cache named MyCache.</span></span>

## <span data-ttu-id="9e7ee-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9e7ee-114">PARAMETERS</span></span>

### <span data-ttu-id="9e7ee-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9e7ee-115">-AsJob</span></span>
<span data-ttu-id="9e7ee-116">Köra kommandot som ett jobb</span><span class="sxs-lookup"><span data-stu-id="9e7ee-116">Run the command as a job</span></span>

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

### <span data-ttu-id="9e7ee-117">-ClientProtocol</span><span class="sxs-lookup"><span data-stu-id="9e7ee-117">-ClientProtocol</span></span>
<span data-ttu-id="9e7ee-118">Anger om Redis-klienter kan ansluta via TLS-krypterade eller Redis-protokoll.</span><span class="sxs-lookup"><span data-stu-id="9e7ee-118">Specifies whether redis clients can connect using TLS-encrypted or plaintext redis protocols.</span></span>
<span data-ttu-id="9e7ee-119">Standard är TLS-krypterat.</span><span class="sxs-lookup"><span data-stu-id="9e7ee-119">Default is TLS-encrypted.</span></span>

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

### <span data-ttu-id="9e7ee-120">-ClusteringPolicy</span><span class="sxs-lookup"><span data-stu-id="9e7ee-120">-ClusteringPolicy</span></span>
<span data-ttu-id="9e7ee-121">Kluster princip-standard är OSSCluster.</span><span class="sxs-lookup"><span data-stu-id="9e7ee-121">Clustering policy - default is OSSCluster.</span></span>
<span data-ttu-id="9e7ee-122">Anges vid skapande tillfället.</span><span class="sxs-lookup"><span data-stu-id="9e7ee-122">Specified at create time.</span></span>

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

### <span data-ttu-id="9e7ee-123">-Kluster namn</span><span class="sxs-lookup"><span data-stu-id="9e7ee-123">-ClusterName</span></span>
<span data-ttu-id="9e7ee-124">Namnet på RedisEnterprise-klustret.</span><span class="sxs-lookup"><span data-stu-id="9e7ee-124">The name of the RedisEnterprise cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e7ee-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e7ee-125">-DefaultProfile</span></span>
<span data-ttu-id="9e7ee-126">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9e7ee-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9e7ee-127">-EvictionPolicy</span><span class="sxs-lookup"><span data-stu-id="9e7ee-127">-EvictionPolicy</span></span>
<span data-ttu-id="9e7ee-128">Redis-standard är VolatileLRU</span><span class="sxs-lookup"><span data-stu-id="9e7ee-128">Redis eviction policy - default is VolatileLRU</span></span>

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

### <span data-ttu-id="9e7ee-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9e7ee-129">-InputObject</span></span>
<span data-ttu-id="9e7ee-130">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="9e7ee-130">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.IRedisEnterpriseCacheIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9e7ee-131">-Modul</span><span class="sxs-lookup"><span data-stu-id="9e7ee-131">-Module</span></span>
<span data-ttu-id="9e7ee-132">Valfri uppsättning Redis-moduler som ska aktive ras i den här databasen – moduler kan bara läggas till när du skapar.</span><span class="sxs-lookup"><span data-stu-id="9e7ee-132">Optional set of redis modules to enable in this database - modules can only be added at creation time.</span></span>
<span data-ttu-id="9e7ee-133">För att konstruera kan du läsa avsnittet anteckningar för modul egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="9e7ee-133">To construct, see NOTES section for MODULE properties and create a hash table.</span></span>

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

### <span data-ttu-id="9e7ee-134">-Nowait</span><span class="sxs-lookup"><span data-stu-id="9e7ee-134">-NoWait</span></span>
<span data-ttu-id="9e7ee-135">Kör kommandot asynkront</span><span class="sxs-lookup"><span data-stu-id="9e7ee-135">Run the command asynchronously</span></span>

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

### <span data-ttu-id="9e7ee-136">-Port</span><span class="sxs-lookup"><span data-stu-id="9e7ee-136">-Port</span></span>
<span data-ttu-id="9e7ee-137">TCP-port för databasens slut punkt.</span><span class="sxs-lookup"><span data-stu-id="9e7ee-137">TCP port of the database endpoint.</span></span>
<span data-ttu-id="9e7ee-138">Anges vid skapande tillfället.</span><span class="sxs-lookup"><span data-stu-id="9e7ee-138">Specified at create time.</span></span>
<span data-ttu-id="9e7ee-139">Standard porten är tillgänglig.</span><span class="sxs-lookup"><span data-stu-id="9e7ee-139">Defaults to an available port.</span></span>

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

### <span data-ttu-id="9e7ee-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9e7ee-140">-ResourceGroupName</span></span>
<span data-ttu-id="9e7ee-141">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="9e7ee-141">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e7ee-142">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9e7ee-142">-SubscriptionId</span></span>
<span data-ttu-id="9e7ee-143">Hämtar dina prenumerations uppgifter som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="9e7ee-143">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="9e7ee-144">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="9e7ee-144">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e7ee-145">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="9e7ee-145">-Confirm</span></span>
<span data-ttu-id="9e7ee-146">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="9e7ee-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9e7ee-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9e7ee-147">-WhatIf</span></span>
<span data-ttu-id="9e7ee-148">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="9e7ee-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9e7ee-149">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="9e7ee-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9e7ee-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e7ee-150">CommonParameters</span></span>
<span data-ttu-id="9e7ee-151">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e7ee-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e7ee-152">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9e7ee-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e7ee-153">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9e7ee-153">INPUTS</span></span>

### <span data-ttu-id="9e7ee-154">Microsoft. Azure. PowerShell. cmdletar. RedisEnterpriseCache. Models. IRedisEnterpriseCacheIdentity</span><span class="sxs-lookup"><span data-stu-id="9e7ee-154">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.IRedisEnterpriseCacheIdentity</span></span>

## <span data-ttu-id="9e7ee-155">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9e7ee-155">OUTPUTS</span></span>

### <span data-ttu-id="9e7ee-156">Microsoft. Azure. PowerShell. cmdletar. RedisEnterpriseCache. Models. Api20201001Preview. IDatabase</span><span class="sxs-lookup"><span data-stu-id="9e7ee-156">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.Api20201001Preview.IDatabase</span></span>

## <span data-ttu-id="9e7ee-157">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9e7ee-157">NOTES</span></span>

<span data-ttu-id="9e7ee-158">ALIAS</span><span class="sxs-lookup"><span data-stu-id="9e7ee-158">ALIASES</span></span>

<span data-ttu-id="9e7ee-159">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="9e7ee-159">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="9e7ee-160">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="9e7ee-160">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="9e7ee-161">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="9e7ee-161">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="9e7ee-162">INPUTOBJECT <IRedisEnterpriseCacheIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="9e7ee-162">INPUTOBJECT <IRedisEnterpriseCacheIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="9e7ee-163">`[ClusterName <String>]`: Namnet på RedisEnterprise-klustret.</span><span class="sxs-lookup"><span data-stu-id="9e7ee-163">`[ClusterName <String>]`: The name of the RedisEnterprise cluster.</span></span>
  - <span data-ttu-id="9e7ee-164">`[DatabaseName <String>]`: Namnet på databasen.</span><span class="sxs-lookup"><span data-stu-id="9e7ee-164">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="9e7ee-165">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="9e7ee-165">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="9e7ee-166">`[Location <String>]`: Regionen som operationen befinner sig i.</span><span class="sxs-lookup"><span data-stu-id="9e7ee-166">`[Location <String>]`: The region the operation is in.</span></span>
  - <span data-ttu-id="9e7ee-167">`[OperationId <String>]`: Åtgärdens unika identifierare.</span><span class="sxs-lookup"><span data-stu-id="9e7ee-167">`[OperationId <String>]`: The operation's unique identifier.</span></span>
  - <span data-ttu-id="9e7ee-168">`[PrivateEndpointConnectionName <String>]`: Namnet på den privata slut punkts anslutningen som är associerad med Azure-resursen</span><span class="sxs-lookup"><span data-stu-id="9e7ee-168">`[PrivateEndpointConnectionName <String>]`: The name of the private endpoint connection associated with the Azure resource</span></span>
  - <span data-ttu-id="9e7ee-169">`[ResourceGroupName <String>]`: Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="9e7ee-169">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="9e7ee-170">`[SubscriptionId <String>]`: Hämtar dina prenumerations uppgifter som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="9e7ee-170">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="9e7ee-171">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="9e7ee-171">The subscription ID forms part of the URI for every service call.</span></span>

<span data-ttu-id="9e7ee-172">MODUL <IModule [] >: valfri uppsättning Redis-moduler som ska aktive ras i den här databasen – moduler kan bara läggas till när du skapar.</span><span class="sxs-lookup"><span data-stu-id="9e7ee-172">MODULE <IModule[]>: Optional set of redis modules to enable in this database - modules can only be added at creation time.</span></span>
  - <span data-ttu-id="9e7ee-173">`Name <String>`: Namnet på modulen, till exempel "RedisBloom", "RediSearch", "RedisTimeSeries"</span><span class="sxs-lookup"><span data-stu-id="9e7ee-173">`Name <String>`: The name of the module, e.g. 'RedisBloom', 'RediSearch', 'RedisTimeSeries'</span></span>
  - <span data-ttu-id="9e7ee-174">`[Arg <String>]`: Konfigurations alternativ för modulen, till exempel "ERROR_RATE 0,00 INITIAL_SIZE 400".</span><span class="sxs-lookup"><span data-stu-id="9e7ee-174">`[Arg <String>]`: Configuration options for the module, e.g. 'ERROR_RATE 0.00 INITIAL_SIZE 400'.</span></span>

## <span data-ttu-id="9e7ee-175">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9e7ee-175">RELATED LINKS</span></span>

