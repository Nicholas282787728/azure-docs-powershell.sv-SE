---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/remove-aztimeseriesinsightsreferencedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Remove-AzTimeSeriesInsightsReferenceDataSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Remove-AzTimeSeriesInsightsReferenceDataSet.md
ms.openlocfilehash: 56173c8ca384c817912395a536583fb26e9dfa76
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98522155"
---
# <span data-ttu-id="4b90a-101">Remove-AzTimeSeriesInsightsReferenceDataSet</span><span class="sxs-lookup"><span data-stu-id="4b90a-101">Remove-AzTimeSeriesInsightsReferenceDataSet</span></span>

## <span data-ttu-id="4b90a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4b90a-102">SYNOPSIS</span></span>
<span data-ttu-id="4b90a-103">Tar bort referens data uppsättningen med det angivna namnet i angiven prenumeration, resurs grupp och miljö</span><span class="sxs-lookup"><span data-stu-id="4b90a-103">Deletes the reference data set with the specified name in the specified subscription, resource group, and environment</span></span>

## <span data-ttu-id="4b90a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4b90a-104">SYNTAX</span></span>

### <span data-ttu-id="4b90a-105">Ta bort (standard)</span><span class="sxs-lookup"><span data-stu-id="4b90a-105">Delete (Default)</span></span>
```
Remove-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName <String> -Name <String>
 -ResourceGroupName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="4b90a-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="4b90a-106">DeleteViaIdentity</span></span>
```
Remove-AzTimeSeriesInsightsReferenceDataSet -InputObject <ITimeSeriesInsightsIdentity>
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="4b90a-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4b90a-107">DESCRIPTION</span></span>
<span data-ttu-id="4b90a-108">Tar bort referens data uppsättningen med det angivna namnet i angiven prenumeration, resurs grupp och miljö</span><span class="sxs-lookup"><span data-stu-id="4b90a-108">Deletes the reference data set with the specified name in the specified subscription, resource group, and environment</span></span>

## <span data-ttu-id="4b90a-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4b90a-109">EXAMPLES</span></span>

### <span data-ttu-id="4b90a-110">Exempel 1: ta bort en angiven referens data uppsättning efter namn</span><span class="sxs-lookup"><span data-stu-id="4b90a-110">Example 1: Remove a specified reference data set by name</span></span>
```powershell
PS C:\> Remove-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName tsitest001 -Name dstest001 -ResourceGroupName testgroup

```

<span data-ttu-id="4b90a-111">Det här kommandot tar bort en angiven referens data uppsättning.</span><span class="sxs-lookup"><span data-stu-id="4b90a-111">This command removes a specified reference data set.</span></span>

### <span data-ttu-id="4b90a-112">Exempel 2: ta bort en angiven referens data uppsättning utifrån objekt</span><span class="sxs-lookup"><span data-stu-id="4b90a-112">Example 2: Remove a specified reference data set by object</span></span>
```powershell
PS C:\> $ds = Get-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName tsitest001 -Name dstest001 -ResourceGroupName testgroup
PS C:\> Remove-AzTimeSeriesInsightsReferenceDataSet -InputObject $ds

```

<span data-ttu-id="4b90a-113">Det här kommandot tar bort en angiven referens data uppsättning.</span><span class="sxs-lookup"><span data-stu-id="4b90a-113">This command removes a specified reference data set.</span></span>

## <span data-ttu-id="4b90a-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4b90a-114">PARAMETERS</span></span>

### <span data-ttu-id="4b90a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b90a-115">-DefaultProfile</span></span>
<span data-ttu-id="4b90a-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4b90a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4b90a-117">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="4b90a-117">-EnvironmentName</span></span>
<span data-ttu-id="4b90a-118">Namnet på den miljö för tids serie som är kopplad till den angivna resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="4b90a-118">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

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

### <span data-ttu-id="4b90a-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4b90a-119">-InputObject</span></span>
<span data-ttu-id="4b90a-120">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="4b90a-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4b90a-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="4b90a-121">-Name</span></span>
<span data-ttu-id="4b90a-122">Namnet på den referens data uppsättning som är kopplad till den angivna miljön.</span><span class="sxs-lookup"><span data-stu-id="4b90a-122">The name of the Time Series Insights reference data set associated with the specified environment.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: ReferenceDataSetName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b90a-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4b90a-123">-PassThru</span></span>
<span data-ttu-id="4b90a-124">Returnerar true när kommandot lyckas</span><span class="sxs-lookup"><span data-stu-id="4b90a-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="4b90a-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4b90a-125">-ResourceGroupName</span></span>
<span data-ttu-id="4b90a-126">Namn på en Azure-resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="4b90a-126">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="4b90a-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4b90a-127">-SubscriptionId</span></span>
<span data-ttu-id="4b90a-128">ID för Azure-prenumeration.</span><span class="sxs-lookup"><span data-stu-id="4b90a-128">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="4b90a-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="4b90a-129">-Confirm</span></span>
<span data-ttu-id="4b90a-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="4b90a-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4b90a-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4b90a-131">-WhatIf</span></span>
<span data-ttu-id="4b90a-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="4b90a-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4b90a-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="4b90a-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4b90a-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b90a-134">CommonParameters</span></span>
<span data-ttu-id="4b90a-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4b90a-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b90a-136">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4b90a-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b90a-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4b90a-137">INPUTS</span></span>

### <span data-ttu-id="4b90a-138">Microsoft. Azure. PowerShell. cmdletar. TimeSeriesInsights. Models. ITimeSeriesInsightsIdentity</span><span class="sxs-lookup"><span data-stu-id="4b90a-138">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="4b90a-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4b90a-139">OUTPUTS</span></span>

### <span data-ttu-id="4b90a-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4b90a-140">System.Boolean</span></span>

## <span data-ttu-id="4b90a-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4b90a-141">NOTES</span></span>

<span data-ttu-id="4b90a-142">ALIAS</span><span class="sxs-lookup"><span data-stu-id="4b90a-142">ALIASES</span></span>

<span data-ttu-id="4b90a-143">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="4b90a-143">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="4b90a-144">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="4b90a-144">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="4b90a-145">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="4b90a-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="4b90a-146">INPUTOBJECT <ITimeSeriesInsightsIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="4b90a-146">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="4b90a-147">`[AccessPolicyName <String>]`: Åtkomst Principens namn.</span><span class="sxs-lookup"><span data-stu-id="4b90a-147">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="4b90a-148">`[EnvironmentName <String>]`: Miljö namnet</span><span class="sxs-lookup"><span data-stu-id="4b90a-148">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="4b90a-149">`[EventSourceName <String>]`: Namnet på den händelse källa för tids serier som är associerad med den angivna miljön.</span><span class="sxs-lookup"><span data-stu-id="4b90a-149">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="4b90a-150">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="4b90a-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="4b90a-151">`[ReferenceDataSetName <String>]`: Referens data uppsättningens namn.</span><span class="sxs-lookup"><span data-stu-id="4b90a-151">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="4b90a-152">`[ResourceGroupName <String>]`: Namnet på en Azure-resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="4b90a-152">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="4b90a-153">`[SubscriptionId <String>]`: ID för Azure-prenumeration.</span><span class="sxs-lookup"><span data-stu-id="4b90a-153">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="4b90a-154">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4b90a-154">RELATED LINKS</span></span>

