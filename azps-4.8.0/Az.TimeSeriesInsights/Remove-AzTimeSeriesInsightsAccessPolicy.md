---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/remove-aztimeseriesinsightsaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Remove-AzTimeSeriesInsightsAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Remove-AzTimeSeriesInsightsAccessPolicy.md
ms.openlocfilehash: 2a6c58729d08c5bd060434c7a21720f87a3f7de3
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94260873"
---
# <span data-ttu-id="1398c-101">Remove-AzTimeSeriesInsightsAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="1398c-101">Remove-AzTimeSeriesInsightsAccessPolicy</span></span>

## <span data-ttu-id="1398c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1398c-102">SYNOPSIS</span></span>
<span data-ttu-id="1398c-103">Tar bort åtkomst principen med angivet namn i angiven prenumeration, resurs grupp och miljö</span><span class="sxs-lookup"><span data-stu-id="1398c-103">Deletes the access policy with the specified name in the specified subscription, resource group, and environment</span></span>

## <span data-ttu-id="1398c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1398c-104">SYNTAX</span></span>

### <span data-ttu-id="1398c-105">Ta bort (standard)</span><span class="sxs-lookup"><span data-stu-id="1398c-105">Delete (Default)</span></span>
```
Remove-AzTimeSeriesInsightsAccessPolicy -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="1398c-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="1398c-106">DeleteViaIdentity</span></span>
```
Remove-AzTimeSeriesInsightsAccessPolicy -InputObject <ITimeSeriesInsightsIdentity>
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="1398c-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1398c-107">DESCRIPTION</span></span>
<span data-ttu-id="1398c-108">Tar bort åtkomst principen med angivet namn i angiven prenumeration, resurs grupp och miljö</span><span class="sxs-lookup"><span data-stu-id="1398c-108">Deletes the access policy with the specified name in the specified subscription, resource group, and environment</span></span>

## <span data-ttu-id="1398c-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1398c-109">EXAMPLES</span></span>

### <span data-ttu-id="1398c-110">Exempel 1: ta bort en angiven åtkomst princip utifrån namn</span><span class="sxs-lookup"><span data-stu-id="1398c-110">Example 1: Remove a specified access policy by name</span></span>
```powershell
PS C:\> Remove-AzTimeSeriesInsightsAccessPolicy -EnvironmentName tsitest001 -Name policy001 -ResourceGroupName testgroup

```

<span data-ttu-id="1398c-111">Det här kommandot tar bort en angiven åtkomst princip.</span><span class="sxs-lookup"><span data-stu-id="1398c-111">This command removes a specified access policy.</span></span>

### <span data-ttu-id="1398c-112">Exempel 2: ta bort en specifik åtkomst princip efter objekt</span><span class="sxs-lookup"><span data-stu-id="1398c-112">Example 2: Remove a specified access policy by object</span></span>
```powershell
PS C:\> $policy = Get-AzTimeSeriesInsightsAccessPolicy -EnvironmentName tsitest001 -Name policy001 -ResourceGroupName testgroup
PS C:\> Remove-AzTimeSeriesInsightsAccessPolicy -InputObject $policy

```

<span data-ttu-id="1398c-113">Det här kommandot tar bort en angiven åtkomst princip.</span><span class="sxs-lookup"><span data-stu-id="1398c-113">This command removes a specified access policy.</span></span>

## <span data-ttu-id="1398c-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1398c-114">PARAMETERS</span></span>

### <span data-ttu-id="1398c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1398c-115">-DefaultProfile</span></span>
<span data-ttu-id="1398c-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1398c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1398c-117">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="1398c-117">-EnvironmentName</span></span>
<span data-ttu-id="1398c-118">Namnet på den miljö för tids serie som är kopplad till den angivna resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="1398c-118">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

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

### <span data-ttu-id="1398c-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1398c-119">-InputObject</span></span>
<span data-ttu-id="1398c-120">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="1398c-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="1398c-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="1398c-121">-Name</span></span>
<span data-ttu-id="1398c-122">Namnet på den åtkomst policyn för tids serier som är associerad med den angivna miljön.</span><span class="sxs-lookup"><span data-stu-id="1398c-122">The name of the Time Series Insights access policy associated with the specified environment.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: AccessPolicyName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1398c-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1398c-123">-PassThru</span></span>
<span data-ttu-id="1398c-124">Returnerar true när kommandot lyckas</span><span class="sxs-lookup"><span data-stu-id="1398c-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="1398c-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1398c-125">-ResourceGroupName</span></span>
<span data-ttu-id="1398c-126">Namn på en Azure-resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="1398c-126">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="1398c-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1398c-127">-SubscriptionId</span></span>
<span data-ttu-id="1398c-128">ID för Azure-prenumeration.</span><span class="sxs-lookup"><span data-stu-id="1398c-128">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="1398c-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="1398c-129">-Confirm</span></span>
<span data-ttu-id="1398c-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="1398c-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1398c-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1398c-131">-WhatIf</span></span>
<span data-ttu-id="1398c-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="1398c-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1398c-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="1398c-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1398c-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1398c-134">CommonParameters</span></span>
<span data-ttu-id="1398c-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1398c-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1398c-136">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1398c-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1398c-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1398c-137">INPUTS</span></span>

### <span data-ttu-id="1398c-138">Microsoft. Azure. PowerShell. cmdletar. TimeSeriesInsights. Models. ITimeSeriesInsightsIdentity</span><span class="sxs-lookup"><span data-stu-id="1398c-138">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="1398c-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1398c-139">OUTPUTS</span></span>

### <span data-ttu-id="1398c-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1398c-140">System.Boolean</span></span>

## <span data-ttu-id="1398c-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1398c-141">NOTES</span></span>

<span data-ttu-id="1398c-142">ALIAS</span><span class="sxs-lookup"><span data-stu-id="1398c-142">ALIASES</span></span>

<span data-ttu-id="1398c-143">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="1398c-143">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="1398c-144">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="1398c-144">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="1398c-145">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="1398c-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="1398c-146">INPUTOBJECT <ITimeSeriesInsightsIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="1398c-146">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="1398c-147">`[AccessPolicyName <String>]`: Åtkomst Principens namn.</span><span class="sxs-lookup"><span data-stu-id="1398c-147">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="1398c-148">`[EnvironmentName <String>]`: Miljö namnet</span><span class="sxs-lookup"><span data-stu-id="1398c-148">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="1398c-149">`[EventSourceName <String>]`: Namnet på den händelse källa för tids serier som är associerad med den angivna miljön.</span><span class="sxs-lookup"><span data-stu-id="1398c-149">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="1398c-150">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="1398c-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="1398c-151">`[ReferenceDataSetName <String>]`: Referens data uppsättningens namn.</span><span class="sxs-lookup"><span data-stu-id="1398c-151">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="1398c-152">`[ResourceGroupName <String>]`: Namnet på en Azure-resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="1398c-152">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="1398c-153">`[SubscriptionId <String>]`: ID för Azure-prenumeration.</span><span class="sxs-lookup"><span data-stu-id="1398c-153">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="1398c-154">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1398c-154">RELATED LINKS</span></span>

