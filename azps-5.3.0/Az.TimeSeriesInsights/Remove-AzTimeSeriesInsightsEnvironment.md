---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/remove-aztimeseriesinsightsenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Remove-AzTimeSeriesInsightsEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Remove-AzTimeSeriesInsightsEnvironment.md
ms.openlocfilehash: 8b56475d2510099b7873fa444a0dc78497aeb729
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98525272"
---
# <span data-ttu-id="75aaa-101">Remove-AzTimeSeriesInsightsEnvironment</span><span class="sxs-lookup"><span data-stu-id="75aaa-101">Remove-AzTimeSeriesInsightsEnvironment</span></span>

## <span data-ttu-id="75aaa-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="75aaa-102">SYNOPSIS</span></span>
<span data-ttu-id="75aaa-103">Tar bort miljön med det angivna namnet i den angivna abonnemangs-och resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="75aaa-103">Deletes the environment with the specified name in the specified subscription and resource group.</span></span>

## <span data-ttu-id="75aaa-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="75aaa-104">SYNTAX</span></span>

### <span data-ttu-id="75aaa-105">Ta bort (standard)</span><span class="sxs-lookup"><span data-stu-id="75aaa-105">Delete (Default)</span></span>
```
Remove-AzTimeSeriesInsightsEnvironment -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="75aaa-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="75aaa-106">DeleteViaIdentity</span></span>
```
Remove-AzTimeSeriesInsightsEnvironment -InputObject <ITimeSeriesInsightsIdentity> [-DefaultProfile <PSObject>]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="75aaa-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="75aaa-107">DESCRIPTION</span></span>
<span data-ttu-id="75aaa-108">Tar bort miljön med det angivna namnet i den angivna abonnemangs-och resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="75aaa-108">Deletes the environment with the specified name in the specified subscription and resource group.</span></span>

## <span data-ttu-id="75aaa-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="75aaa-109">EXAMPLES</span></span>

### <span data-ttu-id="75aaa-110">Exempel 1: ta bort en miljö syn miljöer utifrån namn</span><span class="sxs-lookup"><span data-stu-id="75aaa-110">Example 1: Remove a time series insights environment by name</span></span>
```powershell
PS C:\> Remove-AzTimeSeriesInsightsEnvironment -ResourceGroupName testgroup -Name tsill

```

<span data-ttu-id="75aaa-111">Det här kommandot tar bort en miljö med tids serier.</span><span class="sxs-lookup"><span data-stu-id="75aaa-111">This command removes a time series insights environment.</span></span>

### <span data-ttu-id="75aaa-112">Exempel 2: ta bort en miljö för tids serie Insights efter objekt</span><span class="sxs-lookup"><span data-stu-id="75aaa-112">Example 2: Remove a time series insights environment by object</span></span>
```powershell
PS C:\> $env = Get-AzTimeSeriesInsightsEnvironment -ResourceGroupName testgroup -Name tsill
PS C:\> Remove-AzTimeSeriesInsightsEnvironment -InputObject $env

```

<span data-ttu-id="75aaa-113">Det här kommandot tar bort en miljö med tids serier.</span><span class="sxs-lookup"><span data-stu-id="75aaa-113">This command removes a time series insights environment.</span></span>

## <span data-ttu-id="75aaa-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="75aaa-114">PARAMETERS</span></span>

### <span data-ttu-id="75aaa-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75aaa-115">-DefaultProfile</span></span>
<span data-ttu-id="75aaa-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="75aaa-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="75aaa-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="75aaa-117">-InputObject</span></span>
<span data-ttu-id="75aaa-118">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="75aaa-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="75aaa-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="75aaa-119">-Name</span></span>
<span data-ttu-id="75aaa-120">Namnet på den miljö för tids serie som är kopplad till den angivna resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="75aaa-120">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: EnvironmentName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75aaa-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="75aaa-121">-PassThru</span></span>
<span data-ttu-id="75aaa-122">Returnerar true när kommandot lyckas</span><span class="sxs-lookup"><span data-stu-id="75aaa-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="75aaa-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75aaa-123">-ResourceGroupName</span></span>
<span data-ttu-id="75aaa-124">Namn på en Azure-resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="75aaa-124">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="75aaa-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="75aaa-125">-SubscriptionId</span></span>
<span data-ttu-id="75aaa-126">ID för Azure-prenumeration.</span><span class="sxs-lookup"><span data-stu-id="75aaa-126">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="75aaa-127">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="75aaa-127">-Confirm</span></span>
<span data-ttu-id="75aaa-128">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="75aaa-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="75aaa-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="75aaa-129">-WhatIf</span></span>
<span data-ttu-id="75aaa-130">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="75aaa-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="75aaa-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="75aaa-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="75aaa-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75aaa-132">CommonParameters</span></span>
<span data-ttu-id="75aaa-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75aaa-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75aaa-134">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="75aaa-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75aaa-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="75aaa-135">INPUTS</span></span>

### <span data-ttu-id="75aaa-136">Microsoft. Azure. PowerShell. cmdletar. TimeSeriesInsights. Models. ITimeSeriesInsightsIdentity</span><span class="sxs-lookup"><span data-stu-id="75aaa-136">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="75aaa-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="75aaa-137">OUTPUTS</span></span>

### <span data-ttu-id="75aaa-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="75aaa-138">System.Boolean</span></span>

## <span data-ttu-id="75aaa-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="75aaa-139">NOTES</span></span>

<span data-ttu-id="75aaa-140">ALIAS</span><span class="sxs-lookup"><span data-stu-id="75aaa-140">ALIASES</span></span>

<span data-ttu-id="75aaa-141">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="75aaa-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="75aaa-142">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="75aaa-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="75aaa-143">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="75aaa-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="75aaa-144">INPUTOBJECT <ITimeSeriesInsightsIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="75aaa-144">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="75aaa-145">`[AccessPolicyName <String>]`: Åtkomst Principens namn.</span><span class="sxs-lookup"><span data-stu-id="75aaa-145">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="75aaa-146">`[EnvironmentName <String>]`: Miljö namnet</span><span class="sxs-lookup"><span data-stu-id="75aaa-146">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="75aaa-147">`[EventSourceName <String>]`: Namnet på den händelse källa för tids serier som är associerad med den angivna miljön.</span><span class="sxs-lookup"><span data-stu-id="75aaa-147">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="75aaa-148">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="75aaa-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="75aaa-149">`[ReferenceDataSetName <String>]`: Referens data uppsättningens namn.</span><span class="sxs-lookup"><span data-stu-id="75aaa-149">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="75aaa-150">`[ResourceGroupName <String>]`: Namnet på en Azure-resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="75aaa-150">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="75aaa-151">`[SubscriptionId <String>]`: ID för Azure-prenumeration.</span><span class="sxs-lookup"><span data-stu-id="75aaa-151">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="75aaa-152">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="75aaa-152">RELATED LINKS</span></span>

