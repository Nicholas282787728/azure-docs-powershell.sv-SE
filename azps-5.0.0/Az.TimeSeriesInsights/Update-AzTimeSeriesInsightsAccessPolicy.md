---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/update-aztimeseriesinsightsaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Update-AzTimeSeriesInsightsAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Update-AzTimeSeriesInsightsAccessPolicy.md
ms.openlocfilehash: e776b0e11fedd0b2903135b9b640c3b704706027
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94269225"
---
# <span data-ttu-id="b7bc4-101">Update-AzTimeSeriesInsightsAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="b7bc4-101">Update-AzTimeSeriesInsightsAccessPolicy</span></span>

## <span data-ttu-id="b7bc4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b7bc4-102">SYNOPSIS</span></span>
<span data-ttu-id="b7bc4-103">Uppdaterar åtkomst principen med angivet namn i angiven prenumeration, resurs grupp och miljö.</span><span class="sxs-lookup"><span data-stu-id="b7bc4-103">Updates the access policy with the specified name in the specified subscription, resource group, and environment.</span></span>

## <span data-ttu-id="b7bc4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b7bc4-104">SYNTAX</span></span>

### <span data-ttu-id="b7bc4-105">UpdateExpanded (standard)</span><span class="sxs-lookup"><span data-stu-id="b7bc4-105">UpdateExpanded (Default)</span></span>
```
Update-AzTimeSeriesInsightsAccessPolicy -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Description <String>] [-Role <AccessPolicyRole[]>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="b7bc4-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="b7bc4-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzTimeSeriesInsightsAccessPolicy -InputObject <ITimeSeriesInsightsIdentity> [-Description <String>]
 [-Role <AccessPolicyRole[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="b7bc4-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b7bc4-107">DESCRIPTION</span></span>
<span data-ttu-id="b7bc4-108">Uppdaterar åtkomst principen med angivet namn i angiven prenumeration, resurs grupp och miljö.</span><span class="sxs-lookup"><span data-stu-id="b7bc4-108">Updates the access policy with the specified name in the specified subscription, resource group, and environment.</span></span>

## <span data-ttu-id="b7bc4-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b7bc4-109">EXAMPLES</span></span>

### <span data-ttu-id="b7bc4-110">Exempel 1: uppdatera en angiven åtkomst princip utifrån namn</span><span class="sxs-lookup"><span data-stu-id="b7bc4-110">Example 1: Update a specified access policy by name</span></span>
```powershell
PS C:\> Update-AzTimeSeriesInsightsAccessPolicy -EnvironmentName tsitest001 -Name policy001 -ResourceGroupName testgroup -Role Contributor,Reader

Name      Type
----      ----
policy001 Microsoft.TimeSeriesInsights/Environments/AccessPolicies
```

<span data-ttu-id="b7bc4-111">Det här kommandot uppdaterar en angiven åtkomst princip.</span><span class="sxs-lookup"><span data-stu-id="b7bc4-111">This command updates a specified access policy.</span></span>

### <span data-ttu-id="b7bc4-112">Exempel 2: uppdatera en angiven åtkomst princip efter objekt</span><span class="sxs-lookup"><span data-stu-id="b7bc4-112">Example 2: Update a specified access policy by object</span></span>
```powershell
PS C:\> $policy = Get-AzTimeSeriesInsightsAccessPolicy -EnvironmentName tsitest001 -ResourceGroupName testgroup -Name policy001
PS C:\> Update-AzTimeSeriesInsightsAccessPolicy -InputObject $policy -Role Contributor

Name      Type
----      ----
policy001 Microsoft.TimeSeriesInsights/Environments/AccessPolicies
```

<span data-ttu-id="b7bc4-113">Det här kommandot uppdaterar en angiven åtkomst princip.</span><span class="sxs-lookup"><span data-stu-id="b7bc4-113">This command updates a specified access policy.</span></span>

## <span data-ttu-id="b7bc4-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b7bc4-114">PARAMETERS</span></span>

### <span data-ttu-id="b7bc4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7bc4-115">-DefaultProfile</span></span>
<span data-ttu-id="b7bc4-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b7bc4-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b7bc4-117">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="b7bc4-117">-Description</span></span>
<span data-ttu-id="b7bc4-118">En beskrivning av åtkomst principen.</span><span class="sxs-lookup"><span data-stu-id="b7bc4-118">An description of the access policy.</span></span>

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

### <span data-ttu-id="b7bc4-119">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="b7bc4-119">-EnvironmentName</span></span>
<span data-ttu-id="b7bc4-120">Namnet på den miljö för tids serie som är kopplad till den angivna resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="b7bc4-120">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

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

### <span data-ttu-id="b7bc4-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b7bc4-121">-InputObject</span></span>
<span data-ttu-id="b7bc4-122">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="b7bc4-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="b7bc4-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="b7bc4-123">-Name</span></span>
<span data-ttu-id="b7bc4-124">Namnet på den åtkomst policyn för tids serier som är associerad med den angivna miljön.</span><span class="sxs-lookup"><span data-stu-id="b7bc4-124">The name of the Time Series Insights access policy associated with the specified environment.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: AccessPolicyName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7bc4-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7bc4-125">-ResourceGroupName</span></span>
<span data-ttu-id="b7bc4-126">Namn på en Azure-resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="b7bc4-126">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="b7bc4-127">-Roll</span><span class="sxs-lookup"><span data-stu-id="b7bc4-127">-Role</span></span>
<span data-ttu-id="b7bc4-128">Listan med roller som huvud kontot har tilldelats i miljön.</span><span class="sxs-lookup"><span data-stu-id="b7bc4-128">The list of roles the principal is assigned on the environment.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Support.AccessPolicyRole[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7bc4-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b7bc4-129">-SubscriptionId</span></span>
<span data-ttu-id="b7bc4-130">ID för Azure-prenumeration.</span><span class="sxs-lookup"><span data-stu-id="b7bc4-130">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="b7bc4-131">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b7bc4-131">-Confirm</span></span>
<span data-ttu-id="b7bc4-132">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b7bc4-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b7bc4-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b7bc4-133">-WhatIf</span></span>
<span data-ttu-id="b7bc4-134">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b7bc4-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b7bc4-135">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b7bc4-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b7bc4-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7bc4-136">CommonParameters</span></span>
<span data-ttu-id="b7bc4-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b7bc4-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7bc4-138">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b7bc4-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7bc4-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b7bc4-139">INPUTS</span></span>

### <span data-ttu-id="b7bc4-140">Microsoft. Azure. PowerShell. cmdletar. TimeSeriesInsights. Models. ITimeSeriesInsightsIdentity</span><span class="sxs-lookup"><span data-stu-id="b7bc4-140">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="b7bc4-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b7bc4-141">OUTPUTS</span></span>

### <span data-ttu-id="b7bc4-142">Microsoft. Azure. PowerShell. cmdletar. TimeSeriesInsights. Models. Api20200515. IAccessPolicyResource</span><span class="sxs-lookup"><span data-stu-id="b7bc4-142">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IAccessPolicyResource</span></span>

## <span data-ttu-id="b7bc4-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b7bc4-143">NOTES</span></span>

<span data-ttu-id="b7bc4-144">ALIAS</span><span class="sxs-lookup"><span data-stu-id="b7bc4-144">ALIASES</span></span>

<span data-ttu-id="b7bc4-145">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="b7bc4-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b7bc4-146">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="b7bc4-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b7bc4-147">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="b7bc4-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b7bc4-148">INPUTOBJECT <ITimeSeriesInsightsIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="b7bc4-148">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b7bc4-149">`[AccessPolicyName <String>]`: Åtkomst Principens namn.</span><span class="sxs-lookup"><span data-stu-id="b7bc4-149">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="b7bc4-150">`[EnvironmentName <String>]`: Miljö namnet</span><span class="sxs-lookup"><span data-stu-id="b7bc4-150">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="b7bc4-151">`[EventSourceName <String>]`: Namnet på den händelse källa för tids serier som är associerad med den angivna miljön.</span><span class="sxs-lookup"><span data-stu-id="b7bc4-151">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="b7bc4-152">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="b7bc4-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b7bc4-153">`[ReferenceDataSetName <String>]`: Referens data uppsättningens namn.</span><span class="sxs-lookup"><span data-stu-id="b7bc4-153">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="b7bc4-154">`[ResourceGroupName <String>]`: Namnet på en Azure-resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="b7bc4-154">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="b7bc4-155">`[SubscriptionId <String>]`: ID för Azure-prenumeration.</span><span class="sxs-lookup"><span data-stu-id="b7bc4-155">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="b7bc4-156">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b7bc4-156">RELATED LINKS</span></span>
