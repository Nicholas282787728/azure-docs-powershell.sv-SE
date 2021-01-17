---
external help file: ''
Module Name: Az.RedisEnterpriseCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.redisenterprisecache/update-azredisenterprisecache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Update-AzRedisEnterpriseCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Update-AzRedisEnterpriseCache.md
ms.openlocfilehash: ef1ef3d45594b0e290a014fb3aa98d670e5681a2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98421160"
---
# <span data-ttu-id="cd717-101">Update-AzRedisEnterpriseCache</span><span class="sxs-lookup"><span data-stu-id="cd717-101">Update-AzRedisEnterpriseCache</span></span>

## <span data-ttu-id="cd717-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="cd717-102">SYNOPSIS</span></span>
<span data-ttu-id="cd717-103">Uppdaterar ett befintligt RedisEnterprise-kluster</span><span class="sxs-lookup"><span data-stu-id="cd717-103">Updates an existing RedisEnterprise cluster</span></span>

## <span data-ttu-id="cd717-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="cd717-104">SYNTAX</span></span>

### <span data-ttu-id="cd717-105">UpdateExpanded (standard)</span><span class="sxs-lookup"><span data-stu-id="cd717-105">UpdateExpanded (Default)</span></span>
```
Update-AzRedisEnterpriseCache -ClusterName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Capacity <Int32>] [-MinimumTlsVersion <String>] [-Sku <SkuName>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="cd717-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="cd717-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzRedisEnterpriseCache -InputObject <IRedisEnterpriseCacheIdentity> [-Capacity <Int32>]
 [-MinimumTlsVersion <String>] [-Sku <SkuName>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="cd717-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="cd717-107">DESCRIPTION</span></span>
<span data-ttu-id="cd717-108">Uppdaterar ett befintligt RedisEnterprise-kluster</span><span class="sxs-lookup"><span data-stu-id="cd717-108">Updates an existing RedisEnterprise cluster</span></span>

## <span data-ttu-id="cd717-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="cd717-109">EXAMPLES</span></span>

### <span data-ttu-id="cd717-110">Exempel 1: uppdatera Redis företags-cache</span><span class="sxs-lookup"><span data-stu-id="cd717-110">Example 1: Update Redis Enterprise Cache</span></span>
```powershell
PS C:\> Update-AzRedisEnterpriseCache -Name "MyCache" -ResourceGroupName "MyGroup" -MinimumTlsVersion "1.2" -Tag @{"tag" = "value"}

Location Name    Type                            Zone Database
-------- ----    ----                            ---- --------
West US  MyCache Microsoft.Cache/redisEnterprise      {default}

```

<span data-ttu-id="cd717-111">Det här kommandot uppdaterar den minsta TLS-versionen och lägger till en tagg i Redis företags-cache med namnet mina cacheminne.</span><span class="sxs-lookup"><span data-stu-id="cd717-111">This command updates the minimum TLS version and adds a tag to the Redis Enterprise Cache named MyCache.</span></span>

## <span data-ttu-id="cd717-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="cd717-112">PARAMETERS</span></span>

### <span data-ttu-id="cd717-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cd717-113">-AsJob</span></span>
<span data-ttu-id="cd717-114">Köra kommandot som ett jobb</span><span class="sxs-lookup"><span data-stu-id="cd717-114">Run the command as a job</span></span>

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

### <span data-ttu-id="cd717-115">-Kapacitet</span><span class="sxs-lookup"><span data-stu-id="cd717-115">-Capacity</span></span>
<span data-ttu-id="cd717-116">Storleken på RedisEnterprise-klustret.</span><span class="sxs-lookup"><span data-stu-id="cd717-116">The size of the RedisEnterprise cluster.</span></span>
<span data-ttu-id="cd717-117">Standardvärdet är 2 eller 3 beroende på SKU.</span><span class="sxs-lookup"><span data-stu-id="cd717-117">Defaults to 2 or 3 depending on SKU.</span></span>
<span data-ttu-id="cd717-118">Giltiga värden är (2, 4, 6,...) för företags lager enheter och (3, 9, 15,...) för Flash-SKU: er.</span><span class="sxs-lookup"><span data-stu-id="cd717-118">Valid values are (2, 4, 6, ...) for Enterprise SKUs and (3, 9, 15, ...) for Flash SKUs.</span></span>

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

### <span data-ttu-id="cd717-119">-Kluster namn</span><span class="sxs-lookup"><span data-stu-id="cd717-119">-ClusterName</span></span>
<span data-ttu-id="cd717-120">Namnet på RedisEnterprise-klustret.</span><span class="sxs-lookup"><span data-stu-id="cd717-120">The name of the RedisEnterprise cluster.</span></span>

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

### <span data-ttu-id="cd717-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd717-121">-DefaultProfile</span></span>
<span data-ttu-id="cd717-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="cd717-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cd717-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cd717-123">-InputObject</span></span>
<span data-ttu-id="cd717-124">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="cd717-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="cd717-125">-MinimumTlsVersion</span><span class="sxs-lookup"><span data-stu-id="cd717-125">-MinimumTlsVersion</span></span>
<span data-ttu-id="cd717-126">Den minsta TLS-versionen för klustret som stöds, till exempel "1,2"</span><span class="sxs-lookup"><span data-stu-id="cd717-126">The minimum TLS version for the cluster to support, e.g. '1.2'</span></span>

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

### <span data-ttu-id="cd717-127">-Nowait</span><span class="sxs-lookup"><span data-stu-id="cd717-127">-NoWait</span></span>
<span data-ttu-id="cd717-128">Kör kommandot asynkront</span><span class="sxs-lookup"><span data-stu-id="cd717-128">Run the command asynchronously</span></span>

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

### <span data-ttu-id="cd717-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd717-129">-ResourceGroupName</span></span>
<span data-ttu-id="cd717-130">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="cd717-130">The name of the resource group.</span></span>

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

### <span data-ttu-id="cd717-131">-SKU</span><span class="sxs-lookup"><span data-stu-id="cd717-131">-Sku</span></span>
<span data-ttu-id="cd717-132">Den typ av RedisEnterprise-kluster som ska distribueras.</span><span class="sxs-lookup"><span data-stu-id="cd717-132">The type of RedisEnterprise cluster to deploy.</span></span>
<span data-ttu-id="cd717-133">Möjliga värden: (Enterprise_E10 EnterpriseFlash_F300 etc.)</span><span class="sxs-lookup"><span data-stu-id="cd717-133">Possible values: (Enterprise_E10, EnterpriseFlash_F300 etc.)</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Support.SkuName
Parameter Sets: (All)
Aliases: SkuName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd717-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="cd717-134">-SubscriptionId</span></span>
<span data-ttu-id="cd717-135">Hämtar dina prenumerations uppgifter som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="cd717-135">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="cd717-136">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="cd717-136">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="cd717-137">-Tagg</span><span class="sxs-lookup"><span data-stu-id="cd717-137">-Tag</span></span>
<span data-ttu-id="cd717-138">Resource-taggar.</span><span class="sxs-lookup"><span data-stu-id="cd717-138">Resource tags.</span></span>

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

### <span data-ttu-id="cd717-139">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="cd717-139">-Confirm</span></span>
<span data-ttu-id="cd717-140">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="cd717-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cd717-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd717-141">-WhatIf</span></span>
<span data-ttu-id="cd717-142">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="cd717-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cd717-143">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="cd717-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cd717-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd717-144">CommonParameters</span></span>
<span data-ttu-id="cd717-145">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd717-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd717-146">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cd717-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd717-147">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="cd717-147">INPUTS</span></span>

### <span data-ttu-id="cd717-148">Microsoft. Azure. PowerShell. cmdletar. RedisEnterpriseCache. Models. IRedisEnterpriseCacheIdentity</span><span class="sxs-lookup"><span data-stu-id="cd717-148">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.IRedisEnterpriseCacheIdentity</span></span>

## <span data-ttu-id="cd717-149">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="cd717-149">OUTPUTS</span></span>

### <span data-ttu-id="cd717-150">Microsoft. Azure. PowerShell. cmdletar. RedisEnterpriseCache. Models. Api20201001Preview. ICluster</span><span class="sxs-lookup"><span data-stu-id="cd717-150">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.Api20201001Preview.ICluster</span></span>

## <span data-ttu-id="cd717-151">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="cd717-151">NOTES</span></span>

<span data-ttu-id="cd717-152">ALIAS</span><span class="sxs-lookup"><span data-stu-id="cd717-152">ALIASES</span></span>

<span data-ttu-id="cd717-153">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="cd717-153">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="cd717-154">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="cd717-154">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="cd717-155">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="cd717-155">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="cd717-156">INPUTOBJECT <IRedisEnterpriseCacheIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="cd717-156">INPUTOBJECT <IRedisEnterpriseCacheIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="cd717-157">`[ClusterName <String>]`: Namnet på RedisEnterprise-klustret.</span><span class="sxs-lookup"><span data-stu-id="cd717-157">`[ClusterName <String>]`: The name of the RedisEnterprise cluster.</span></span>
  - <span data-ttu-id="cd717-158">`[DatabaseName <String>]`: Namnet på databasen.</span><span class="sxs-lookup"><span data-stu-id="cd717-158">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="cd717-159">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="cd717-159">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="cd717-160">`[Location <String>]`: Regionen som operationen befinner sig i.</span><span class="sxs-lookup"><span data-stu-id="cd717-160">`[Location <String>]`: The region the operation is in.</span></span>
  - <span data-ttu-id="cd717-161">`[OperationId <String>]`: Åtgärdens unika identifierare.</span><span class="sxs-lookup"><span data-stu-id="cd717-161">`[OperationId <String>]`: The operation's unique identifier.</span></span>
  - <span data-ttu-id="cd717-162">`[PrivateEndpointConnectionName <String>]`: Namnet på den privata slut punkts anslutningen som är associerad med Azure-resursen</span><span class="sxs-lookup"><span data-stu-id="cd717-162">`[PrivateEndpointConnectionName <String>]`: The name of the private endpoint connection associated with the Azure resource</span></span>
  - <span data-ttu-id="cd717-163">`[ResourceGroupName <String>]`: Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="cd717-163">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="cd717-164">`[SubscriptionId <String>]`: Hämtar dina prenumerations uppgifter som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="cd717-164">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="cd717-165">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="cd717-165">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="cd717-166">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="cd717-166">RELATED LINKS</span></span>

