---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/update-aztimeseriesinsightsenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Update-AzTimeSeriesInsightsEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Update-AzTimeSeriesInsightsEnvironment.md
ms.openlocfilehash: e2b7fa000251a12e09dfd7cd345f54f967962839
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98423944"
---
# <span data-ttu-id="23d57-101">Update-AzTimeSeriesInsightsEnvironment</span><span class="sxs-lookup"><span data-stu-id="23d57-101">Update-AzTimeSeriesInsightsEnvironment</span></span>

## <span data-ttu-id="23d57-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="23d57-102">SYNOPSIS</span></span>
<span data-ttu-id="23d57-103">Uppdaterar miljön med det angivna namnet i den angivna abonnemangs-och resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="23d57-103">Updates the environment with the specified name in the specified subscription and resource group.</span></span>

## <span data-ttu-id="23d57-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="23d57-104">SYNTAX</span></span>

### <span data-ttu-id="23d57-105">UpdateExpanded (standard)</span><span class="sxs-lookup"><span data-stu-id="23d57-105">UpdateExpanded (Default)</span></span>
```
Update-AzTimeSeriesInsightsEnvironment -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="23d57-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="23d57-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzTimeSeriesInsightsEnvironment -InputObject <ITimeSeriesInsightsIdentity> [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="23d57-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="23d57-107">DESCRIPTION</span></span>
<span data-ttu-id="23d57-108">Uppdaterar miljön med det angivna namnet i den angivna abonnemangs-och resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="23d57-108">Updates the environment with the specified name in the specified subscription and resource group.</span></span>

## <span data-ttu-id="23d57-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="23d57-109">EXAMPLES</span></span>

### <span data-ttu-id="23d57-110">Exempel 1: uppdatera en gen1-miljö med Time Series</span><span class="sxs-lookup"><span data-stu-id="23d57-110">Example 1: Update a Gen1 time series insights environment</span></span>
```powershell
PS C:\> Update-AzTimeSeriesInsightsEnvironment -ResourceGroupName testgroup -Name tsitest001 -Tag @{'key1'='val1'}

DataAccessFqdn               : b6d113a4-0865-405f-b09e-ad4355b5d046.env.timeseries.azure.com
DataAccessId                 : b6d113a4-0865-405f-b09e-ad4355b5d046
DataRetentionTime            : 1.01:25:00
Id                           : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/testgroup/providers/Microsoft.TimeSeriesInsights/environments/tsitest 
                               001
IngressState                 :
Kind                         : Gen1
Location                     : eastus
Name                         : tsitest001
PartitionKeyProperty         :
PropertyUsageState           :
Sku                          : Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20180815Preview.Sku
SkuCapacity                  : 5
SkuName                      : S1
StateDetailCode              :
StateDetailCurrentCount      :
StateDetailMaxCount          :
StateDetailMessage           :
StorageLimitExceededBehavior : PurgeOldData
Tag                          : Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20180815Preview.TrackedResourceTags
Type                         : Microsoft.TimeSeriesInsights/Environments
```

<span data-ttu-id="23d57-111">Det här kommandot uppdaterar en gen1 tids serie miljö.</span><span class="sxs-lookup"><span data-stu-id="23d57-111">This command updates a Gen1 time series insights environment.</span></span>

### <span data-ttu-id="23d57-112">Exempel 2: uppdatera en gen1-miljö med Time Series</span><span class="sxs-lookup"><span data-stu-id="23d57-112">Example 2:  Update a Gen1 time series insights environment</span></span>
```powershell
PS C:\> $env = Get-AzTimeSeriesInsightsEnvironment -ResourceGroupName testgroup -Name tsitest001
PS C:\> Update-AzTimeSeriesInsightsEnvironment -InputObject $env -Tag @{'key2'='val2'}

DataAccessFqdn               : b6d113a4-0865-405f-b09e-ad4355b5d046.env.timeseries.azure.com
DataAccessId                 : b6d113a4-0865-405f-b09e-ad4355b5d046
DataRetentionTime            : 1.01:25:00
Id                           : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/testgroup/providers/Microsoft.TimeSeriesInsights/environments/tsitest 
                               001
IngressState                 :
Kind                         : Gen1
Location                     : eastus
Name                         : tsitest001
PartitionKeyProperty         :
PropertyUsageState           :
Sku                          : Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20180815Preview.Sku
SkuCapacity                  : 5
SkuName                      : S1
StateDetailCode              :
StateDetailCurrentCount      :
StateDetailMaxCount          :
StateDetailMessage           :
StorageLimitExceededBehavior : PurgeOldData
Tag                          : Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20180815Preview.TrackedResourceTags
Type                         : Microsoft.TimeSeriesInsights/Environments
```

<span data-ttu-id="23d57-113">Det här kommandot uppdaterar en gen1 tids serie miljö.</span><span class="sxs-lookup"><span data-stu-id="23d57-113">This command updates a Gen1 time series insights environment.</span></span>

## <span data-ttu-id="23d57-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="23d57-114">PARAMETERS</span></span>

### <span data-ttu-id="23d57-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="23d57-115">-AsJob</span></span>
<span data-ttu-id="23d57-116">Köra kommandot som ett jobb</span><span class="sxs-lookup"><span data-stu-id="23d57-116">Run the command as a job</span></span>

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

### <span data-ttu-id="23d57-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23d57-117">-DefaultProfile</span></span>
<span data-ttu-id="23d57-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="23d57-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="23d57-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="23d57-119">-InputObject</span></span>
<span data-ttu-id="23d57-120">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="23d57-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="23d57-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="23d57-121">-Name</span></span>
<span data-ttu-id="23d57-122">Namnet på den miljö för tids serie som är kopplad till den angivna resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="23d57-122">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: EnvironmentName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23d57-123">-Nowait</span><span class="sxs-lookup"><span data-stu-id="23d57-123">-NoWait</span></span>
<span data-ttu-id="23d57-124">Kör kommandot asynkront</span><span class="sxs-lookup"><span data-stu-id="23d57-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="23d57-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="23d57-125">-ResourceGroupName</span></span>
<span data-ttu-id="23d57-126">Namn på en Azure-resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="23d57-126">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="23d57-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="23d57-127">-SubscriptionId</span></span>
<span data-ttu-id="23d57-128">ID för Azure-prenumeration.</span><span class="sxs-lookup"><span data-stu-id="23d57-128">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="23d57-129">-Tagg</span><span class="sxs-lookup"><span data-stu-id="23d57-129">-Tag</span></span>
<span data-ttu-id="23d57-130">Nyckeltal för fler egenskaper för miljön.</span><span class="sxs-lookup"><span data-stu-id="23d57-130">Key-value pairs of additional properties for the environment.</span></span>

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

### <span data-ttu-id="23d57-131">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="23d57-131">-Confirm</span></span>
<span data-ttu-id="23d57-132">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="23d57-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="23d57-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="23d57-133">-WhatIf</span></span>
<span data-ttu-id="23d57-134">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="23d57-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="23d57-135">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="23d57-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="23d57-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23d57-136">CommonParameters</span></span>
<span data-ttu-id="23d57-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="23d57-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23d57-138">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="23d57-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23d57-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="23d57-139">INPUTS</span></span>

### <span data-ttu-id="23d57-140">Microsoft. Azure. PowerShell. cmdletar. TimeSeriesInsights. Models. ITimeSeriesInsightsIdentity</span><span class="sxs-lookup"><span data-stu-id="23d57-140">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="23d57-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="23d57-141">OUTPUTS</span></span>

### <span data-ttu-id="23d57-142">Microsoft. Azure. PowerShell. cmdletar. TimeSeriesInsights. Models. Api20200515. IEnvironmentResource</span><span class="sxs-lookup"><span data-stu-id="23d57-142">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IEnvironmentResource</span></span>

## <span data-ttu-id="23d57-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="23d57-143">NOTES</span></span>

<span data-ttu-id="23d57-144">ALIAS</span><span class="sxs-lookup"><span data-stu-id="23d57-144">ALIASES</span></span>

<span data-ttu-id="23d57-145">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="23d57-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="23d57-146">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="23d57-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="23d57-147">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="23d57-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="23d57-148">INPUTOBJECT <ITimeSeriesInsightsIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="23d57-148">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="23d57-149">`[AccessPolicyName <String>]`: Åtkomst Principens namn.</span><span class="sxs-lookup"><span data-stu-id="23d57-149">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="23d57-150">`[EnvironmentName <String>]`: Miljö namnet</span><span class="sxs-lookup"><span data-stu-id="23d57-150">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="23d57-151">`[EventSourceName <String>]`: Namnet på den händelse källa för tids serier som är associerad med den angivna miljön.</span><span class="sxs-lookup"><span data-stu-id="23d57-151">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="23d57-152">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="23d57-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="23d57-153">`[ReferenceDataSetName <String>]`: Referens data uppsättningens namn.</span><span class="sxs-lookup"><span data-stu-id="23d57-153">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="23d57-154">`[ResourceGroupName <String>]`: Namnet på en Azure-resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="23d57-154">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="23d57-155">`[SubscriptionId <String>]`: ID för Azure-prenumeration.</span><span class="sxs-lookup"><span data-stu-id="23d57-155">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="23d57-156">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="23d57-156">RELATED LINKS</span></span>

