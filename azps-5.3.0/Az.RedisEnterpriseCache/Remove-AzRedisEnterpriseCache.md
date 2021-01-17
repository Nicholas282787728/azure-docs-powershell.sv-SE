---
external help file: ''
Module Name: Az.RedisEnterpriseCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.redisenterprisecache/remove-azredisenterprisecache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Remove-AzRedisEnterpriseCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Remove-AzRedisEnterpriseCache.md
ms.openlocfilehash: 22d0fed7c72aa5754b7393cdf06fb58a4bfc0db3
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98421168"
---
# <span data-ttu-id="4f0ad-101">Remove-AzRedisEnterpriseCache</span><span class="sxs-lookup"><span data-stu-id="4f0ad-101">Remove-AzRedisEnterpriseCache</span></span>

## <span data-ttu-id="4f0ad-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4f0ad-102">SYNOPSIS</span></span>
<span data-ttu-id="4f0ad-103">Tar bort ett RedisEnterprise.</span><span class="sxs-lookup"><span data-stu-id="4f0ad-103">Deletes a RedisEnterprise cache cluster.</span></span>

## <span data-ttu-id="4f0ad-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4f0ad-104">SYNTAX</span></span>

### <span data-ttu-id="4f0ad-105">Ta bort (standard)</span><span class="sxs-lookup"><span data-stu-id="4f0ad-105">Delete (Default)</span></span>
```
Remove-AzRedisEnterpriseCache -ClusterName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="4f0ad-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="4f0ad-106">DeleteViaIdentity</span></span>
```
Remove-AzRedisEnterpriseCache -InputObject <IRedisEnterpriseCacheIdentity> [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="4f0ad-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4f0ad-107">DESCRIPTION</span></span>
<span data-ttu-id="4f0ad-108">Tar bort ett RedisEnterprise.</span><span class="sxs-lookup"><span data-stu-id="4f0ad-108">Deletes a RedisEnterprise cache cluster.</span></span>

## <span data-ttu-id="4f0ad-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4f0ad-109">EXAMPLES</span></span>

### <span data-ttu-id="4f0ad-110">Exempel 1: ta bort en Redis företags-cache och returnera resultatet</span><span class="sxs-lookup"><span data-stu-id="4f0ad-110">Example 1: Remove a Redis Enterprise Cache and return the result</span></span>
```powershell
PS C:\> Remove-AzRedisEnterpriseCache -Name "MyCache" -ResourceGroupName "MyGroup" -PassThru
True
```

<span data-ttu-id="4f0ad-111">Det här kommandot tar bort en Redis företags-cache och visar om åtgärden lyckades.</span><span class="sxs-lookup"><span data-stu-id="4f0ad-111">This command removes a Redis Enterprise Cache and displays whether the operation is successful.</span></span>

### <span data-ttu-id="4f0ad-112">Exempel 2: ta bort en Redis företags-cache och Visa inte resultatet</span><span class="sxs-lookup"><span data-stu-id="4f0ad-112">Example 2: Remove a Redis Enterprise Cache and do not display the result</span></span>
```powershell
PS C:\> Remove-AzRedisEnterpriseCache -Name "MyCache" -ResourceGroupName "MyGroup"
```

<span data-ttu-id="4f0ad-113">Det här kommandot tar bort en Redis.</span><span class="sxs-lookup"><span data-stu-id="4f0ad-113">This command removes a Redis Enterprise Cache.</span></span>
<span data-ttu-id="4f0ad-114">Eftersom parametern PassThru inte anges visas inte resultatet av åtgärden.</span><span class="sxs-lookup"><span data-stu-id="4f0ad-114">Because the PassThru parameter is not specified, the result of the operation is not displayed.</span></span>

## <span data-ttu-id="4f0ad-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4f0ad-115">PARAMETERS</span></span>

### <span data-ttu-id="4f0ad-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4f0ad-116">-AsJob</span></span>
<span data-ttu-id="4f0ad-117">Köra kommandot som ett jobb</span><span class="sxs-lookup"><span data-stu-id="4f0ad-117">Run the command as a job</span></span>

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

### <span data-ttu-id="4f0ad-118">-Kluster namn</span><span class="sxs-lookup"><span data-stu-id="4f0ad-118">-ClusterName</span></span>
<span data-ttu-id="4f0ad-119">Namnet på RedisEnterprise-klustret.</span><span class="sxs-lookup"><span data-stu-id="4f0ad-119">The name of the RedisEnterprise cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f0ad-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f0ad-120">-DefaultProfile</span></span>
<span data-ttu-id="4f0ad-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4f0ad-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4f0ad-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4f0ad-122">-InputObject</span></span>
<span data-ttu-id="4f0ad-123">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="4f0ad-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.IRedisEnterpriseCacheIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4f0ad-124">-Nowait</span><span class="sxs-lookup"><span data-stu-id="4f0ad-124">-NoWait</span></span>
<span data-ttu-id="4f0ad-125">Kör kommandot asynkront</span><span class="sxs-lookup"><span data-stu-id="4f0ad-125">Run the command asynchronously</span></span>

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

### <span data-ttu-id="4f0ad-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4f0ad-126">-PassThru</span></span>
<span data-ttu-id="4f0ad-127">Returnerar true när kommandot lyckas</span><span class="sxs-lookup"><span data-stu-id="4f0ad-127">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="4f0ad-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4f0ad-128">-ResourceGroupName</span></span>
<span data-ttu-id="4f0ad-129">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="4f0ad-129">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f0ad-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4f0ad-130">-SubscriptionId</span></span>
<span data-ttu-id="4f0ad-131">Hämtar dina prenumerations uppgifter som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="4f0ad-131">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="4f0ad-132">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="4f0ad-132">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f0ad-133">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="4f0ad-133">-Confirm</span></span>
<span data-ttu-id="4f0ad-134">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="4f0ad-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4f0ad-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4f0ad-135">-WhatIf</span></span>
<span data-ttu-id="4f0ad-136">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="4f0ad-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4f0ad-137">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="4f0ad-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4f0ad-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f0ad-138">CommonParameters</span></span>
<span data-ttu-id="4f0ad-139">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4f0ad-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f0ad-140">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4f0ad-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f0ad-141">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4f0ad-141">INPUTS</span></span>

### <span data-ttu-id="4f0ad-142">Microsoft. Azure. PowerShell. cmdletar. RedisEnterpriseCache. Models. IRedisEnterpriseCacheIdentity</span><span class="sxs-lookup"><span data-stu-id="4f0ad-142">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.IRedisEnterpriseCacheIdentity</span></span>

## <span data-ttu-id="4f0ad-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4f0ad-143">OUTPUTS</span></span>

### <span data-ttu-id="4f0ad-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4f0ad-144">System.Boolean</span></span>

## <span data-ttu-id="4f0ad-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4f0ad-145">NOTES</span></span>

<span data-ttu-id="4f0ad-146">ALIAS</span><span class="sxs-lookup"><span data-stu-id="4f0ad-146">ALIASES</span></span>

<span data-ttu-id="4f0ad-147">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="4f0ad-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="4f0ad-148">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="4f0ad-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="4f0ad-149">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="4f0ad-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="4f0ad-150">INPUTOBJECT <IRedisEnterpriseCacheIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="4f0ad-150">INPUTOBJECT <IRedisEnterpriseCacheIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="4f0ad-151">`[ClusterName <String>]`: Namnet på RedisEnterprise-klustret.</span><span class="sxs-lookup"><span data-stu-id="4f0ad-151">`[ClusterName <String>]`: The name of the RedisEnterprise cluster.</span></span>
  - <span data-ttu-id="4f0ad-152">`[DatabaseName <String>]`: Namnet på databasen.</span><span class="sxs-lookup"><span data-stu-id="4f0ad-152">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="4f0ad-153">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="4f0ad-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="4f0ad-154">`[Location <String>]`: Regionen som operationen befinner sig i.</span><span class="sxs-lookup"><span data-stu-id="4f0ad-154">`[Location <String>]`: The region the operation is in.</span></span>
  - <span data-ttu-id="4f0ad-155">`[OperationId <String>]`: Åtgärdens unika identifierare.</span><span class="sxs-lookup"><span data-stu-id="4f0ad-155">`[OperationId <String>]`: The operation's unique identifier.</span></span>
  - <span data-ttu-id="4f0ad-156">`[PrivateEndpointConnectionName <String>]`: Namnet på den privata slut punkts anslutningen som är associerad med Azure-resursen</span><span class="sxs-lookup"><span data-stu-id="4f0ad-156">`[PrivateEndpointConnectionName <String>]`: The name of the private endpoint connection associated with the Azure resource</span></span>
  - <span data-ttu-id="4f0ad-157">`[ResourceGroupName <String>]`: Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="4f0ad-157">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="4f0ad-158">`[SubscriptionId <String>]`: Hämtar dina prenumerations uppgifter som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="4f0ad-158">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="4f0ad-159">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="4f0ad-159">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="4f0ad-160">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4f0ad-160">RELATED LINKS</span></span>

