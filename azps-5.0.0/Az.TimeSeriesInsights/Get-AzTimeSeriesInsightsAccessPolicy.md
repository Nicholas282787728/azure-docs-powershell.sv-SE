---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/get-aztimeseriesinsightsaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Get-AzTimeSeriesInsightsAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Get-AzTimeSeriesInsightsAccessPolicy.md
ms.openlocfilehash: c7d8f46f42b1b42e4831540f5c68706c61ff78cf
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94269826"
---
# <span data-ttu-id="7d09e-101">Get-AzTimeSeriesInsightsAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="7d09e-101">Get-AzTimeSeriesInsightsAccessPolicy</span></span>

## <span data-ttu-id="7d09e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7d09e-102">SYNOPSIS</span></span>
<span data-ttu-id="7d09e-103">Hämtar åtkomst principen med det angivna namnet i den angivna miljön.</span><span class="sxs-lookup"><span data-stu-id="7d09e-103">Gets the access policy with the specified name in the specified environment.</span></span>

## <span data-ttu-id="7d09e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7d09e-104">SYNTAX</span></span>

### <span data-ttu-id="7d09e-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="7d09e-105">List (Default)</span></span>
```
Get-AzTimeSeriesInsightsAccessPolicy -EnvironmentName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="7d09e-106">Lära</span><span class="sxs-lookup"><span data-stu-id="7d09e-106">Get</span></span>
```
Get-AzTimeSeriesInsightsAccessPolicy -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="7d09e-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="7d09e-107">GetViaIdentity</span></span>
```
Get-AzTimeSeriesInsightsAccessPolicy -InputObject <ITimeSeriesInsightsIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="7d09e-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7d09e-108">DESCRIPTION</span></span>
<span data-ttu-id="7d09e-109">Hämtar åtkomst principen med det angivna namnet i den angivna miljön.</span><span class="sxs-lookup"><span data-stu-id="7d09e-109">Gets the access policy with the specified name in the specified environment.</span></span>

## <span data-ttu-id="7d09e-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7d09e-110">EXAMPLES</span></span>

### <span data-ttu-id="7d09e-111">Exempel 1: lista alla åtkomst principer under en angiven miljö</span><span class="sxs-lookup"><span data-stu-id="7d09e-111">Example 1: List all access policies under a specified environment</span></span>
```powershell
PS C:\> Get-AzTimeSeriesInsightsAccessPolicy -EnvironmentName tsitest001 -ResourceGroupName testgroup

Name      Type
----      ----
policy001 Microsoft.TimeSeriesInsights/Environments/AccessPolicies
policy002 Microsoft.TimeSeriesInsights/Environments/AccessPolicies
```

<span data-ttu-id="7d09e-112">Det här kommandot visar alla åtkomst principer under en angiven miljö.</span><span class="sxs-lookup"><span data-stu-id="7d09e-112">This command lists all access policies under a specified environment.</span></span>

### <span data-ttu-id="7d09e-113">Exempel 2: Hämta en angiven åtkomst princip med namn</span><span class="sxs-lookup"><span data-stu-id="7d09e-113">Example 2: Get a specified access policy by name</span></span>
```powershell
PS C:\> Get-AzTimeSeriesInsightsAccessPolicy -EnvironmentName tsitest001 -ResourceGroupName testgroup -Name policy001

Name      Type
----      ----
policy001 Microsoft.TimeSeriesInsights/Environments/AccessPolicies
```

<span data-ttu-id="7d09e-114">Det här kommandot får en angiven åtkomst policy.</span><span class="sxs-lookup"><span data-stu-id="7d09e-114">This command gets a specified access policy.</span></span>

### <span data-ttu-id="7d09e-115">Exempel 3: Hämta en angiven åtkomst princip efter objekt</span><span class="sxs-lookup"><span data-stu-id="7d09e-115">Example 3: Get a specified access policy by object</span></span>
```powershell
PS C:\>$ap = Get-AzTimeSeriesInsightsAccessPolicy -EnvironmentName tsi-envv8u56x -ResourceGroupName tsi-test-i01k5l -Name tsi-apilgj5y 
PS C:\>Get-AzTimeSeriesInsightsAccessPolicy -InputObject $ap

Name      Type
----      ----
policy001 Microsoft.TimeSeriesInsights/Environments/AccessPolicies
```

<span data-ttu-id="7d09e-116">Det här kommandot får en angiven åtkomst policy.</span><span class="sxs-lookup"><span data-stu-id="7d09e-116">This command gets a specified access policy.</span></span>

## <span data-ttu-id="7d09e-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7d09e-117">PARAMETERS</span></span>

### <span data-ttu-id="7d09e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d09e-118">-DefaultProfile</span></span>
<span data-ttu-id="7d09e-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7d09e-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7d09e-120">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="7d09e-120">-EnvironmentName</span></span>
<span data-ttu-id="7d09e-121">Namnet på den miljö för tids serie som är kopplad till den angivna resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="7d09e-121">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

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

### <span data-ttu-id="7d09e-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7d09e-122">-InputObject</span></span>
<span data-ttu-id="7d09e-123">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="7d09e-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="7d09e-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="7d09e-124">-Name</span></span>
<span data-ttu-id="7d09e-125">Namnet på den åtkomst policyn för tids serier som är associerad med den angivna miljön.</span><span class="sxs-lookup"><span data-stu-id="7d09e-125">The name of the Time Series Insights access policy associated with the specified environment.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: AccessPolicyName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d09e-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d09e-126">-ResourceGroupName</span></span>
<span data-ttu-id="7d09e-127">Namn på en Azure-resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="7d09e-127">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="7d09e-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7d09e-128">-SubscriptionId</span></span>
<span data-ttu-id="7d09e-129">ID för Azure-prenumeration.</span><span class="sxs-lookup"><span data-stu-id="7d09e-129">Azure Subscription ID.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d09e-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d09e-130">CommonParameters</span></span>
<span data-ttu-id="7d09e-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7d09e-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d09e-132">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7d09e-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d09e-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7d09e-133">INPUTS</span></span>

### <span data-ttu-id="7d09e-134">Microsoft. Azure. PowerShell. cmdletar. TimeSeriesInsights. Models. ITimeSeriesInsightsIdentity</span><span class="sxs-lookup"><span data-stu-id="7d09e-134">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="7d09e-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7d09e-135">OUTPUTS</span></span>

### <span data-ttu-id="7d09e-136">Microsoft. Azure. PowerShell. cmdletar. TimeSeriesInsights. Models. Api20200515. IAccessPolicyResource</span><span class="sxs-lookup"><span data-stu-id="7d09e-136">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IAccessPolicyResource</span></span>

## <span data-ttu-id="7d09e-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7d09e-137">NOTES</span></span>

<span data-ttu-id="7d09e-138">ALIAS</span><span class="sxs-lookup"><span data-stu-id="7d09e-138">ALIASES</span></span>

<span data-ttu-id="7d09e-139">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="7d09e-139">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="7d09e-140">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="7d09e-140">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="7d09e-141">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="7d09e-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="7d09e-142">INPUTOBJECT <ITimeSeriesInsightsIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="7d09e-142">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="7d09e-143">`[AccessPolicyName <String>]`: Åtkomst Principens namn.</span><span class="sxs-lookup"><span data-stu-id="7d09e-143">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="7d09e-144">`[EnvironmentName <String>]`: Miljö namnet</span><span class="sxs-lookup"><span data-stu-id="7d09e-144">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="7d09e-145">`[EventSourceName <String>]`: Namnet på den händelse källa för tids serier som är associerad med den angivna miljön.</span><span class="sxs-lookup"><span data-stu-id="7d09e-145">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="7d09e-146">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="7d09e-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="7d09e-147">`[ReferenceDataSetName <String>]`: Referens data uppsättningens namn.</span><span class="sxs-lookup"><span data-stu-id="7d09e-147">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="7d09e-148">`[ResourceGroupName <String>]`: Namnet på en Azure-resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="7d09e-148">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="7d09e-149">`[SubscriptionId <String>]`: ID för Azure-prenumeration.</span><span class="sxs-lookup"><span data-stu-id="7d09e-149">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="7d09e-150">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7d09e-150">RELATED LINKS</span></span>
