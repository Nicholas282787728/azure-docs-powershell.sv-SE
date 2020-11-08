---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/get-aztimeseriesinsightsenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Get-AzTimeSeriesInsightsEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Get-AzTimeSeriesInsightsEnvironment.md
ms.openlocfilehash: f4f42b257c5ce54085214c8cd9d2f79d9e8a6387
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94262399"
---
# <span data-ttu-id="623b1-101">Get-AzTimeSeriesInsightsEnvironment</span><span class="sxs-lookup"><span data-stu-id="623b1-101">Get-AzTimeSeriesInsightsEnvironment</span></span>

## <span data-ttu-id="623b1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="623b1-102">SYNOPSIS</span></span>
<span data-ttu-id="623b1-103">Hämtar miljön med det angivna namnet i den angivna abonnemangs-och resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="623b1-103">Gets the environment with the specified name in the specified subscription and resource group.</span></span>

## <span data-ttu-id="623b1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="623b1-104">SYNTAX</span></span>

### <span data-ttu-id="623b1-105">List1 (standard)</span><span class="sxs-lookup"><span data-stu-id="623b1-105">List1 (Default)</span></span>
```
Get-AzTimeSeriesInsightsEnvironment [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="623b1-106">Lära</span><span class="sxs-lookup"><span data-stu-id="623b1-106">Get</span></span>
```
Get-AzTimeSeriesInsightsEnvironment -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-Expand <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="623b1-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="623b1-107">GetViaIdentity</span></span>
```
Get-AzTimeSeriesInsightsEnvironment -InputObject <ITimeSeriesInsightsIdentity> [-Expand <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="623b1-108">Förteckning</span><span class="sxs-lookup"><span data-stu-id="623b1-108">List</span></span>
```
Get-AzTimeSeriesInsightsEnvironment -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="623b1-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="623b1-109">DESCRIPTION</span></span>
<span data-ttu-id="623b1-110">Hämtar miljön med det angivna namnet i den angivna abonnemangs-och resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="623b1-110">Gets the environment with the specified name in the specified subscription and resource group.</span></span>

## <span data-ttu-id="623b1-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="623b1-111">EXAMPLES</span></span>

### <span data-ttu-id="623b1-112">Exempel 1: skaffa en miljö för tids serier</span><span class="sxs-lookup"><span data-stu-id="623b1-112">Example 1: Get a time series insights environment</span></span>
```powershell
PS C:\> Get-AzTimeSeriesInsightsEnvironment -ResourceGroupName testgroup -Name tsitest001

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
SkuCapacity                  : 2
SkuName                      : S1
StateDetailCode              :
StateDetailCurrentCount      :
StateDetailMaxCount          :
StateDetailMessage           :
StorageLimitExceededBehavior : PurgeOldData
Tag                          : Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20180815Preview.TrackedResourceTags
Type                         : Microsoft.TimeSeriesInsights/Environments
```

<span data-ttu-id="623b1-113">Det här kommandot får en miljö för Time Series Insights.</span><span class="sxs-lookup"><span data-stu-id="623b1-113">This command gets a time series insights environment.</span></span>

### <span data-ttu-id="623b1-114">Exempel 2: lista alla miljöer med tids serier</span><span class="sxs-lookup"><span data-stu-id="623b1-114">Example 2: List all time series insights environments</span></span>
```powershell
PS C:\> Get-AzTimeSeriesInsightsEnvironment -ResourceGroupName testgroup

DataAccessFqdn                      : 3de1d1e1-4f9b-4bc6-aad3-a835597dcd86.env.timeseries.azure.com
DataAccessId                        : 3de1d1e1-4f9b-4bc6-aad3-a835597dcd86
Id                                  : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourcegroups/testgroup/providers/Microsoft.TimeSeriesInsights/environments/ 
                                      tsill
IngressState                        :
Kind                                : Gen2
Location                            : EastUs
Name                                : tsill
PropertyUsageState                  :
Sku                                 : Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20180815Preview.Sku
SkuCapacity                         : 1
SkuName                             : L1
StateDetailCode                     :
StateDetailCurrentCount             :
StateDetailMaxCount                 :
StateDetailMessage                  :
StorageConfigurationAccountName     : cdolauli
Tag                                 : Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20180815Preview.TrackedResourceTags
TimeSeriesIdProperty                : {ccc}
Type                                : Microsoft.TimeSeriesInsights/Environments
WarmStoreConfigurationDataRetention : 00:00:00

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
SkuCapacity                  : 2
SkuName                      : S1
StateDetailCode              :
StateDetailCurrentCount      :
StateDetailMaxCount          :
StateDetailMessage           :
StorageLimitExceededBehavior : PurgeOldData
Tag                          : Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20180815Preview.TrackedResourceTags
Type                         : Microsoft.TimeSeriesInsights/Environments
```

<span data-ttu-id="623b1-115">Det här kommandot visar alla miljöer med olika tids serier i en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="623b1-115">This command lists all time series insights environments in a resource group.</span></span>

### <span data-ttu-id="623b1-116">Exempel 3: skaffa en miljö med insikter för tids serier</span><span class="sxs-lookup"><span data-stu-id="623b1-116">Example 3: Get a time series insights environment by object</span></span>
```powershell
PS C:\> $env = Get-AzTimeSeriesInsightsEnvironment -ResourceGroupName tsi-test-i01k5l -Name tsi-envv8u56x 
PS C:\> Get-AzTimeSeriesInsightsEnvironment -InputObject $env

DataAccessFqdn               : d76a61f2-8a30-41a5-9587-f241eb9b48d9.env.timeseries.azure.com
DataAccessId                 : d76a61f2-8a30-41a5-9587-f241eb9b48d9
DataRetentionTime            : 1.01:25:00
Id                           : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/tsi-test-i01k5l/providers/Microsoft.TimeSeriesInsights/environments/tsi-envv8u56x
IngressState                 :
Kind                         : Gen1
Location                     : eastus2
Name                         : tsi-envv8u56x
PartitionKeyProperty         :
PropertyUsageState           :
Sku                          : Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20180815Preview.Sku
SkuCapacity                  : 1
SkuName                      : S1
StateDetailCode              :
StateDetailCurrentCount      :
StateDetailMaxCount          :
StateDetailMessage           :
StorageLimitExceededBehavior : PurgeOldData
Tag                          : Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20180815Preview.TrackedResourceTags
Type                         : Microsoft.TimeSeriesInsights/Environments
```

<span data-ttu-id="623b1-117">Det här kommandot får en serie miljöer med Time Series.</span><span class="sxs-lookup"><span data-stu-id="623b1-117">This command gets a time series insights environments.</span></span>

## <span data-ttu-id="623b1-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="623b1-118">PARAMETERS</span></span>

### <span data-ttu-id="623b1-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="623b1-119">-DefaultProfile</span></span>
<span data-ttu-id="623b1-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="623b1-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="623b1-121">-Expandera</span><span class="sxs-lookup"><span data-stu-id="623b1-121">-Expand</span></span>
<span data-ttu-id="623b1-122">Om du anger $expand = status tas statusen för de interna tjänsterna för miljön i tjänsten Time Series Insights.</span><span class="sxs-lookup"><span data-stu-id="623b1-122">Setting $expand=status will include the status of the internal services of the environment in the Time Series Insights service.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, GetViaIdentity
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="623b1-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="623b1-123">-InputObject</span></span>
<span data-ttu-id="623b1-124">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="623b1-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="623b1-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="623b1-125">-Name</span></span>
<span data-ttu-id="623b1-126">Namnet på den miljö för tids serie som är kopplad till den angivna resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="623b1-126">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: EnvironmentName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="623b1-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="623b1-127">-ResourceGroupName</span></span>
<span data-ttu-id="623b1-128">Namn på en Azure-resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="623b1-128">Name of an Azure Resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="623b1-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="623b1-129">-SubscriptionId</span></span>
<span data-ttu-id="623b1-130">ID för Azure-prenumeration.</span><span class="sxs-lookup"><span data-stu-id="623b1-130">Azure Subscription ID.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="623b1-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="623b1-131">CommonParameters</span></span>
<span data-ttu-id="623b1-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="623b1-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="623b1-133">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="623b1-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="623b1-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="623b1-134">INPUTS</span></span>

### <span data-ttu-id="623b1-135">Microsoft. Azure. PowerShell. cmdletar. TimeSeriesInsights. Models. ITimeSeriesInsightsIdentity</span><span class="sxs-lookup"><span data-stu-id="623b1-135">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="623b1-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="623b1-136">OUTPUTS</span></span>

### <span data-ttu-id="623b1-137">Microsoft. Azure. PowerShell. cmdletar. TimeSeriesInsights. Models. Api20200515. IEnvironmentResource</span><span class="sxs-lookup"><span data-stu-id="623b1-137">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IEnvironmentResource</span></span>

## <span data-ttu-id="623b1-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="623b1-138">NOTES</span></span>

<span data-ttu-id="623b1-139">ALIAS</span><span class="sxs-lookup"><span data-stu-id="623b1-139">ALIASES</span></span>

<span data-ttu-id="623b1-140">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="623b1-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="623b1-141">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="623b1-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="623b1-142">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="623b1-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="623b1-143">INPUTOBJECT <ITimeSeriesInsightsIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="623b1-143">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="623b1-144">`[AccessPolicyName <String>]`: Åtkomst Principens namn.</span><span class="sxs-lookup"><span data-stu-id="623b1-144">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="623b1-145">`[EnvironmentName <String>]`: Miljö namnet</span><span class="sxs-lookup"><span data-stu-id="623b1-145">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="623b1-146">`[EventSourceName <String>]`: Namnet på den händelse källa för tids serier som är associerad med den angivna miljön.</span><span class="sxs-lookup"><span data-stu-id="623b1-146">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="623b1-147">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="623b1-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="623b1-148">`[ReferenceDataSetName <String>]`: Referens data uppsättningens namn.</span><span class="sxs-lookup"><span data-stu-id="623b1-148">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="623b1-149">`[ResourceGroupName <String>]`: Namnet på en Azure-resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="623b1-149">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="623b1-150">`[SubscriptionId <String>]`: ID för Azure-prenumeration.</span><span class="sxs-lookup"><span data-stu-id="623b1-150">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="623b1-151">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="623b1-151">RELATED LINKS</span></span>

