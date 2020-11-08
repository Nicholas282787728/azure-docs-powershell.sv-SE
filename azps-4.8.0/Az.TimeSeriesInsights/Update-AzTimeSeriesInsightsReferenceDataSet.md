---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/update-aztimeseriesinsightsreferencedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Update-AzTimeSeriesInsightsReferenceDataSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Update-AzTimeSeriesInsightsReferenceDataSet.md
ms.openlocfilehash: 7dbced00ee2e39c536765bd16a19fbe7a66e291b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94258442"
---
# <span data-ttu-id="97428-101">Update-AzTimeSeriesInsightsReferenceDataSet</span><span class="sxs-lookup"><span data-stu-id="97428-101">Update-AzTimeSeriesInsightsReferenceDataSet</span></span>

## <span data-ttu-id="97428-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="97428-102">SYNOPSIS</span></span>
<span data-ttu-id="97428-103">Uppdaterar referens data uppsättningen med det angivna namnet i angiven prenumeration, resurs grupp och miljö.</span><span class="sxs-lookup"><span data-stu-id="97428-103">Updates the reference data set with the specified name in the specified subscription, resource group, and environment.</span></span>

## <span data-ttu-id="97428-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="97428-104">SYNTAX</span></span>

### <span data-ttu-id="97428-105">UpdateExpanded (standard)</span><span class="sxs-lookup"><span data-stu-id="97428-105">UpdateExpanded (Default)</span></span>
```
Update-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName <String> -Name <String>
 -ResourceGroupName <String> [-SubscriptionId <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="97428-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="97428-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzTimeSeriesInsightsReferenceDataSet -InputObject <ITimeSeriesInsightsIdentity> [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="97428-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="97428-107">DESCRIPTION</span></span>
<span data-ttu-id="97428-108">Uppdaterar referens data uppsättningen med det angivna namnet i angiven prenumeration, resurs grupp och miljö.</span><span class="sxs-lookup"><span data-stu-id="97428-108">Updates the reference data set with the specified name in the specified subscription, resource group, and environment.</span></span>

## <span data-ttu-id="97428-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="97428-109">EXAMPLES</span></span>

### <span data-ttu-id="97428-110">Exempel 1: uppdatera en angiven referens data uppsättning efter namn</span><span class="sxs-lookup"><span data-stu-id="97428-110">Example 1: Update a specified reference data set by name</span></span>
```powershell
PS C:\> Update-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName tsitest001 -Name dstest001 -ResourceGroupName testgroup -Tag @{"tstg"="lb001"}

Location Name      Type
-------- ----      ----
eastus   dstest001 Microsoft.TimeSeriesInsights/Environments/ReferenceDataSets
```

<span data-ttu-id="97428-111">Det här kommandot uppdaterar en angiven referens data uppsättning.</span><span class="sxs-lookup"><span data-stu-id="97428-111">This command updates a specified reference data set.</span></span>

### <span data-ttu-id="97428-112">Exempel 2: uppdatera en angiven referens data uppsättning efter objekt</span><span class="sxs-lookup"><span data-stu-id="97428-112">Example 2: Update a specified reference data set by object</span></span>
```powershell
PS C:\> $ds = Get-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName tsitest001 -ResourceGroupName testgroup -ReferenceDataSetName dstest001
PS C:\> Update-AzTimeSeriesInsightsReferenceDataSet -InputObject $ds -Tag @{"tstg"="lb001"}

Location Name      Type
-------- ----      ----
eastus   dstest001 Microsoft.TimeSeriesInsights/Environments/ReferenceDataSets
```

<span data-ttu-id="97428-113">Det här kommandot uppdaterar en angiven referens data uppsättning.</span><span class="sxs-lookup"><span data-stu-id="97428-113">This command updates a specified reference data set.</span></span>

## <span data-ttu-id="97428-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="97428-114">PARAMETERS</span></span>

### <span data-ttu-id="97428-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97428-115">-DefaultProfile</span></span>
<span data-ttu-id="97428-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="97428-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="97428-117">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="97428-117">-EnvironmentName</span></span>
<span data-ttu-id="97428-118">Namnet på den miljö för tids serie som är kopplad till den angivna resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="97428-118">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

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

### <span data-ttu-id="97428-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="97428-119">-InputObject</span></span>
<span data-ttu-id="97428-120">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="97428-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="97428-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="97428-121">-Name</span></span>
<span data-ttu-id="97428-122">Namnet på den referens data uppsättning som är kopplad till den angivna miljön.</span><span class="sxs-lookup"><span data-stu-id="97428-122">The name of the Time Series Insights reference data set associated with the specified environment.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: ReferenceDataSetName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97428-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="97428-123">-ResourceGroupName</span></span>
<span data-ttu-id="97428-124">Namn på en Azure-resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="97428-124">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="97428-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="97428-125">-SubscriptionId</span></span>
<span data-ttu-id="97428-126">ID för Azure-prenumeration.</span><span class="sxs-lookup"><span data-stu-id="97428-126">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="97428-127">-Tagg</span><span class="sxs-lookup"><span data-stu-id="97428-127">-Tag</span></span>
<span data-ttu-id="97428-128">Nyckelord med ytterligare egenskaper för referens data uppsättningen.</span><span class="sxs-lookup"><span data-stu-id="97428-128">Key-value pairs of additional properties for the reference data set.</span></span>

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

### <span data-ttu-id="97428-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="97428-129">-Confirm</span></span>
<span data-ttu-id="97428-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="97428-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="97428-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="97428-131">-WhatIf</span></span>
<span data-ttu-id="97428-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="97428-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="97428-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="97428-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="97428-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97428-134">CommonParameters</span></span>
<span data-ttu-id="97428-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="97428-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97428-136">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="97428-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97428-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="97428-137">INPUTS</span></span>

### <span data-ttu-id="97428-138">Microsoft. Azure. PowerShell. cmdletar. TimeSeriesInsights. Models. ITimeSeriesInsightsIdentity</span><span class="sxs-lookup"><span data-stu-id="97428-138">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="97428-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="97428-139">OUTPUTS</span></span>

### <span data-ttu-id="97428-140">Microsoft. Azure. PowerShell. cmdletar. TimeSeriesInsights. Models. Api20200515. IReferenceDataSetResource</span><span class="sxs-lookup"><span data-stu-id="97428-140">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IReferenceDataSetResource</span></span>

## <span data-ttu-id="97428-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="97428-141">NOTES</span></span>

<span data-ttu-id="97428-142">ALIAS</span><span class="sxs-lookup"><span data-stu-id="97428-142">ALIASES</span></span>

<span data-ttu-id="97428-143">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="97428-143">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="97428-144">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="97428-144">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="97428-145">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="97428-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="97428-146">INPUTOBJECT <ITimeSeriesInsightsIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="97428-146">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="97428-147">`[AccessPolicyName <String>]`: Åtkomst Principens namn.</span><span class="sxs-lookup"><span data-stu-id="97428-147">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="97428-148">`[EnvironmentName <String>]`: Miljö namnet</span><span class="sxs-lookup"><span data-stu-id="97428-148">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="97428-149">`[EventSourceName <String>]`: Namnet på den händelse källa för tids serier som är associerad med den angivna miljön.</span><span class="sxs-lookup"><span data-stu-id="97428-149">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="97428-150">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="97428-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="97428-151">`[ReferenceDataSetName <String>]`: Referens data uppsättningens namn.</span><span class="sxs-lookup"><span data-stu-id="97428-151">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="97428-152">`[ResourceGroupName <String>]`: Namnet på en Azure-resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="97428-152">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="97428-153">`[SubscriptionId <String>]`: ID för Azure-prenumeration.</span><span class="sxs-lookup"><span data-stu-id="97428-153">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="97428-154">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="97428-154">RELATED LINKS</span></span>

